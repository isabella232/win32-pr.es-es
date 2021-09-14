---
description: La interfaz IWinHttpRequest proporciona todos los métodos sin eventos para Microsoft Windows HTTP Services (WinHTTP).
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: Interfaz IWinHttpRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 77ebc8947ad36d2dc9efba121cdd6da2d6de359b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068345"
---
# <a name="iwinhttprequest-interface"></a>Interfaz IWinHttpRequest

La **interfaz IWinHttpRequest proporciona** todos los métodos sin eventos para Microsoft Windows HTTP Services [(WinHTTP).](about-winhttp.md)

## <a name="members"></a>Members

La **interfaz IWinHttpRequest** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWinHttpRequest** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IWinHttpRequest** tiene estos métodos.



| Método                                                                 | Descripción                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Aborta**](iwinhttprequest-abort.md)                                 | Anula un [método Send de WinHTTP.](about-winhttp.md) [](iwinhttprequest-send.md)<br/>                                           |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | Recupera todos los encabezados de respuesta HTTP.<br/>                                                                                         |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | Recupera los encabezados de respuesta HTTP.<br/>                                                                                         |
| [**Abrir**](iwinhttprequest-open.md)                                   | Abre una conexión HTTP a un recurso HTTP.<br/>                                                                                |
| [**Envío**](iwinhttprequest-send.md)                                   | Envía una solicitud HTTP a un servidor HTTP.<br/>                                                                                     |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | Establece la directiva de [inicio de sesión automático actual.](authentication-in-winhttp.md)<br/>                             |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | Selecciona un certificado de cliente que se enviará a un servidor https (Protocolo seguro de transferencia de hipertexto).<br/>                                 |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | Establece las credenciales que se usarán con un servidor HTTP, ya sea un servidor proxy o un servidor de origen.<br/>                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Establece la información del servidor proxy.<br/>                                                                                               |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | Agrega, cambia o elimina un encabezado de solicitud HTTP.<br/>                                                                            |
| [**SetTimeouts**](iwinhttprequest-settimeouts.md)                     | Especifica los componentes de tiempo de espera individuales de una operación de envío/recepción, en milisegundos.<br/>                                   |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Espera a que se complete [**un método Send**](iwinhttprequest-send.md) asincrónico, con un valor de tiempo de espera opcional, en segundos.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IWinHttpRequest** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Opción**](iwinhttprequest-option.md)<br/>                 | Lectura y escritura<br/> | Valor de la opción WinHTTP.<br/>                                    |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Solo lectura<br/>  | Cuerpo de la entidad de respuesta como una matriz de bytes sin signo.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Solo lectura<br/>  | Cuerpo de la entidad de respuesta como [**IStream.**](/windows/desktop/api/objidl/nn-objidl-istream)<br/> |
| [**ResponseText**](iwinhttprequest-responsetext.md)<br/>     | Solo lectura<br/>  | Cuerpo de la entidad de respuesta.<br/>                                  |
| [**Estado**](iwinhttprequest-status.md)<br/>                 | Solo lectura<br/>  | Código de estado HTTP de la última respuesta.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Solo lectura<br/>  | Texto de estado HTTP.<br/>                                      |



 

## <a name="remarks"></a>Observaciones

La **interfaz IWinHttpRequest** definida en httprequest.idl se implementa mediante una clase con el identificador **de CLSID \_ WinHttpRequest**. Una aplicación obtiene esta interfaz llamando a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con un identificador de clase de **CLSID \_ WinHttpRequest** y un identificador de interfaz **de \_ IID IWinHttpRequest**.

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHttp.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

