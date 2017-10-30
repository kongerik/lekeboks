// viewController.swift som hentet fra nettet hvordan laste eksterne sider


import UIKit
import WebKit

class ViewController: UIViewController {
    
    @IBOutlet var containerView : UIView! = nil
    var webView: WKWebView?
                            
    override func loadView() {
        super.loadView()
        
        self.webView = WKWebView()
        self.view = self.webView!
    }
    
    override func viewDidLoad() {
        super.viewDidLoad()
       
        var url = NSURL(string:"http://www.kinderas.com/")
        var req = NSURLRequest(URL:url)
        self.webView!.loadRequest(req)
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
    }
    
}
