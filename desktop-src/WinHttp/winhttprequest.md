---
Description: En este tema se proporciona información sobre el uso del objeto COM WinHTTP WinHttpRequest con lenguajes de scripting.
ms.assetid: 0bbbf3dc-84b8-41d8-8627-e3d80ddcb783
title: Objeto WinHttpRequest
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 907e94a731b2ec150a331347480c461d0d0fa319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708874"
---
# <a name="winhttprequest-object"></a>Objeto WinHttpRequest

En este tema se proporciona información sobre el uso del objeto com WinHTTP **WinHttpRequest** con lenguajes de scripting. Para obtener más información, incluida la API de C++ (WinHTTP), consulte [acerca de WinHTTP](about-winhttp.md). Vea [elegir una interfaz WinHTTP](choosing-a-winhttp-interface.md) para obtener una comparación de estas interfaces.

## <a name="example"></a>Ejemplo

```javascript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```

```cpp
 IWinHttpRequest *  pIWinHttpRequest = NULL;
 \\..
    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
```

Ejemplos de código tomados de la [propiedad IWinHttpRequest:: status](iwinhttprequest-status.md).



## <a name="members"></a>Miembros

El objeto **WinHttpRequest** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Events

El objeto **WinHttpRequest** tiene estos eventos.



| Evento                                                                            | Descripción                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Se produce cuando hay un error de tiempo de ejecución en la aplicación.<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | Se produce cuando los datos están disponibles en la respuesta.<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | Se produce cuando se completan los datos de la respuesta.<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | Se produce cuando se inicia la recepción de los datos de respuesta.<br/>      |



 

### <a name="methods"></a>Métodos

El objeto **WinHttpRequest** tiene estos métodos.



| Método                                                                 | Descripción                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aborta**](iwinhttprequest-abort.md)                                 | Anula un método de [**envío**](iwinhttprequest-send.md) de [WinHTTP](about-winhttp.md) .<br/>                                                              |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | Recupera todos los encabezados de respuesta HTTP.<br/>                                                                                                            |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | Recupera los encabezados de respuesta HTTP.<br/>                                                                                                            |
| [**Ábra**](iwinhttprequest-open.md)                                   | Abre una conexión HTTP a un recurso HTTP.<br/>                                                                                                   |
| [**Enviar**](iwinhttprequest-send.md)                                   | Envía una solicitud HTTP a un servidor HTTP.<br/>                                                                                                        |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | Establece la [Directiva de inicio de sesión automático](authentication-in-winhttp.md)actual.<br/>                                                |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | Selecciona un certificado de cliente para enviar a un servidor de protocolo seguro de transferencia de hipertexto (HTTPS).<br/>                                                    |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | Establece las credenciales que se van a usar con un servidor HTTP como un origen o un servidor proxy.<br/>                                                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Establece la información del servidor proxy.<br/>                                                                                                                  |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | Agrega, cambia o elimina un encabezado de solicitud HTTP.<br/>                                                                                               |
| [**SetTimeouts**](iwinhttprequest-settimeouts.md)                     | Especifica, en milisegundos, los componentes de tiempo de espera individuales de una operación de envío o recepción.<br/>                                                     |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Especifica el tiempo de espera, en segundos, para que se complete un método de [**envío**](iwinhttprequest-send.md) asincrónico, con un valor de tiempo de espera opcional.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **WinHttpRequest** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [**Opción**](iwinhttprequest-option.md)<br/>                 | Lectura/escritura<br/> | Establece o recupera un valor de opción de WinHTTP.<br/>                            |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Solo lectura<br/>  | Recupera el cuerpo de la entidad de respuesta como una matriz de bytes sin signo.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Solo lectura<br/>  | Recupera el cuerpo de la entidad de respuesta como una [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).<br/> |
| [**ResponseText**](iwinhttprequest-responsetext.md)<br/>     | Solo lectura<br/>  | Recupera el cuerpo de la entidad de respuesta como texto.<br/>                          |
| [**Status**](iwinhttprequest-status.md)<br/>                 | Solo lectura<br/>  | Recupera el código de Estado HTTP de la última respuesta.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Solo lectura<br/>  | Recupera el texto de Estado HTTP.<br/>                                          |



 

## <a name="remarks"></a>Observaciones

El objeto **WinHttpRequest** usa la interfaz [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) para proporcionar datos de error. Se puede obtener una descripción y un valor de error numérico con el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) en Microsoft Visual Basic Scripting Edition (VBScript) y el objeto [error](https://msdn.microsoft.com/library/dww52sbt.aspx) en Microsoft JScript. Los 16 bits inferiores de un número de error corresponden a los valores que se encuentran en [**los mensajes de error**](error-messages.md).

> [!Note]  
> En Windows XP y Windows 2000, consulte [requisitos de tiempo de ejecución](winhttp-start-page.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp. lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

