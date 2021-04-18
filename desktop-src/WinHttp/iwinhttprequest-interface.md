---
description: La interfaz IWinHttpRequest proporciona todos los métodos no pares para los servicios HTTP de Microsoft Windows (WinHTTP).
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277134"
---
# <a name="iwinhttprequest-interface"></a>Interfaz IWinHttpRequest

La interfaz **IWinHttpRequest** proporciona todos los métodos no pares para los [servicios http de Microsoft Windows (WinHTTP)](about-winhttp.md).

## <a name="members"></a>Miembros

La interfaz **IWinHttpRequest** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWinHttpRequest** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IWinHttpRequest** tiene estos métodos.



| Método                                                                 | Descripción                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Aborta**](iwinhttprequest-abort.md)                                 | Anula un método de [**envío**](iwinhttprequest-send.md) de [WinHTTP](about-winhttp.md) .<br/>                                           |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | Recupera todos los encabezados de respuesta HTTP.<br/>                                                                                         |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | Recupera los encabezados de respuesta HTTP.<br/>                                                                                         |
| [**Ábra**](iwinhttprequest-open.md)                                   | Abre una conexión HTTP a un recurso HTTP.<br/>                                                                                |
| [**Enviar**](iwinhttprequest-send.md)                                   | Envía una solicitud HTTP a un servidor HTTP.<br/>                                                                                     |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | Establece la [Directiva de inicio de sesión automático](authentication-in-winhttp.md)actual.<br/>                             |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | Selecciona un certificado de cliente para enviar a un servidor de protocolo seguro de transferencia de hipertexto (HTTPS).<br/>                                 |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | Establece las credenciales que se van a usar con un servidor HTTP, ya sea un servidor proxy o un servidor de origen.<br/>                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Establece la información del servidor proxy.<br/>                                                                                               |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | Agrega, cambia o elimina un encabezado de solicitud HTTP.<br/>                                                                            |
| [**SetTimeouts**](iwinhttprequest-settimeouts.md)                     | Especifica los componentes de tiempo de espera individuales de una operación de envío y recepción, en milisegundos.<br/>                                   |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Espera a que se complete un método de [**envío**](iwinhttprequest-send.md) asincrónico, en segundos, con un valor de tiempo de espera opcional.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IWinHttpRequest** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Opción**](iwinhttprequest-option.md)<br/>                 | Lectura/escritura<br/> | Un valor de la opción WinHTTP.<br/>                                    |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Solo lectura<br/>  | El cuerpo de la entidad de respuesta como una matriz de bytes sin signo.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Solo lectura<br/>  | El cuerpo de la entidad de respuesta como una [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).<br/> |
| [**ResponseText**](iwinhttprequest-responsetext.md)<br/>     | Solo lectura<br/>  | El cuerpo de la entidad de respuesta.<br/>                                  |
| [**Status**](iwinhttprequest-status.md)<br/>                 | Solo lectura<br/>  | Código de Estado HTTP de la última respuesta.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Solo lectura<br/>  | El texto de Estado HTTP.<br/>                                      |



 

## <a name="remarks"></a>Observaciones

La interfaz **IWinHttpRequest** definida en HttpRequest. idl está implementada por una clase con el **identificador \_ WinHttpRequest CLSID**. Una aplicación obtiene esta interfaz llamando a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con un ID. de clase de **CLSID \_ WinHttpRequest** y un ID. de interfaz de **IID \_ IWinHttpRequest**.

> [!Note]  
> En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.

 

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

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

