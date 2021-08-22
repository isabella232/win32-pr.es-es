---
Description: En este tema se proporciona información sobre el uso del objeto COM WinHttpRequest winHTTP con lenguajes de scripting.
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
ms.openlocfilehash: 92fdcb9c6eff502dc5f19cb62d92af5d4db60e15890667c894f96cfb55a9e5ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132918"
---
# <a name="winhttprequest-object"></a>Objeto WinHttpRequest

En este tema se proporciona información sobre el uso del objeto COM **WinHttpRequest winHTTP** con lenguajes de scripting. Para obtener más información, incluida la API de C++ (WinHTTP), consulte [Acerca de WinHTTP.](about-winhttp.md) Consulte [Elección de una interfaz WinHTTP](choosing-a-winhttp-interface.md) para ver una comparación de estas interfaces.

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

Ejemplos de código tomados [de la propiedad IWinHttpRequest::Status](iwinhttprequest-status.md).



## <a name="members"></a>Miembros

El **objeto WinHttpRequest** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Eventos

El **objeto WinHttpRequest** tiene estos eventos.



| Evento                                                                            | Descripción                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Se produce cuando se produce un error en tiempo de ejecución en la aplicación.<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | Se produce cuando los datos están disponibles en la respuesta.<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | Se produce cuando se completan los datos de respuesta.<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | Se produce cuando los datos de respuesta comienzan a recibirse.<br/>      |



 

### <a name="methods"></a>Métodos

El **objeto WinHttpRequest** tiene estos métodos.



| Método                                                                 | Descripción                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aborta**](iwinhttprequest-abort.md)                                 | Anula un [método WinHTTP](about-winhttp.md) [**Send.**](iwinhttprequest-send.md)<br/>                                                              |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | Recupera todos los encabezados de respuesta HTTP.<br/>                                                                                                            |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | Recupera los encabezados de respuesta HTTP.<br/>                                                                                                            |
| [**Abierto**](iwinhttprequest-open.md)                                   | Abre una conexión HTTP a un recurso HTTP.<br/>                                                                                                   |
| [**Enviar**](iwinhttprequest-send.md)                                   | Envía una solicitud HTTP a un servidor HTTP.<br/>                                                                                                        |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | Establece la directiva de [inicio de sesión automático actual.](authentication-in-winhttp.md)<br/>                                                |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | Selecciona un certificado de cliente que se enviará a un servidor https (Protocolo seguro de transferencia de hipertexto).<br/>                                                    |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | Establece las credenciales que se usarán con un servidor HTTP, ya sea un servidor de origen o un servidor proxy.<br/>                                                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Establece la información del servidor proxy.<br/>                                                                                                                  |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | Agrega, cambia o elimina un encabezado de solicitud HTTP.<br/>                                                                                               |
| [**SetTimeouts**](iwinhttprequest-settimeouts.md)                     | Especifica, en milisegundos, los componentes de tiempo de espera individuales de una operación de envío y recepción.<br/>                                                     |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Especifica el tiempo de espera, en segundos, para que se complete un [**método Send**](iwinhttprequest-send.md) asincrónico, con un valor de tiempo de espera opcional.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto WinHttpRequest** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [**Opción**](iwinhttprequest-option.md)<br/>                 | Lectura/escritura<br/> | Establece o recupera un valor de opción WinHTTP.<br/>                            |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Solo lectura<br/>  | Recupera el cuerpo de la entidad de respuesta como una matriz de bytes sin signo.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Solo lectura<br/>  | Recupera el cuerpo de la entidad de respuesta como [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).<br/> |
| [**ResponseText**](iwinhttprequest-responsetext.md)<br/>     | Solo lectura<br/>  | Recupera el cuerpo de la entidad de respuesta como texto.<br/>                          |
| [**Estado**](iwinhttprequest-status.md)<br/>                 | Solo lectura<br/>  | Recupera el código de estado HTTP de la última respuesta.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Solo lectura<br/>  | Recupera el texto de estado HTTP.<br/>                                          |



 

## <a name="remarks"></a>Comentarios

El **objeto WinHttpRequest** usa la [**interfaz IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) para proporcionar datos de error. Se puede obtener una descripción y un valor de error numérico con el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) en Microsoft Visual Basic Scripting Edition (VBScript) y el objeto [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) en Microsoft JScript. Los 16 bits inferiores de un número de error corresponden a los valores encontrados en [**Mensajes de error**](error-messages.md).

> [!Note]  
> Para Windows XP y Windows 2000, vea [Requisitos en tiempo de ejecución](winhttp-start-page.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio SP3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Versiones winHTTP](winhttp-versions.md)
</dt> </dl>

 

