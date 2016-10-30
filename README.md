# ToUnderstandingAlamofireImage
# 我来尝试翻译一下Swift最流行的网络库给自己用XD
##发出请求
> import Alamofire<br>
> Alamofire.request("https://httpbin.org/get")
##相应处理
Alamofire在处理响应或者一个请求时，应该这么做：
"""swift
Alamofire.request("https://httpbin.org/get").responseJSON { response in
    print(response.request)  // original URL request
    print(response.response) // HTTP URL response
    print(response.data)     // server data
    print(response.result)   // result of response serialization

    if let JSON = response.result.value {
        print("JSON: \(JSON)")
    }
}
"""
