# JsBridgeWeb
Modified version of Js Bridge for use mainly with Py Bridge Web

# Example
'__web_route_ws__' refers to the websocket server url handling the connection
'{0}' is to be replaced with the connection id

```html
  <script src="/js_bridge_web.js"></script>
  <script>
      let client = new JSBridge.JSBridgeClient({
          host: location.hostname,
          port: location.port || 80,
          path: "/__web_route_ws__/{0}",
          conn_id: "{0}",
          reconnect: true
      });
      client.set_mode("python")
      client.start();
  </script>
```
