---
description: Proporciona eventos para los servicios HTTP de Microsoft Windows (WinHTTP).
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: Interfaz IWinHttpRequestEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequestEvents
api_type:
- COM
api_location:
- HttpRequest.idl
ms.openlocfilehash: 3cdd0bf10c0d4bd75351ddaab6e88ce7182850fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678293"
---
# <a name="iwinhttprequestevents-interface"></a>Interfaz IWinHttpRequestEvents

La interfaz **IWinHttpRequestEvents** proporciona eventos para los [servicios http de Microsoft Windows (WinHTTP)](about-winhttp.md). Solo usa métodos de evento.

## <a name="members"></a>Miembros

La interfaz **IWinHttpRequestEvents** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWinHttpRequestEvents** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWinHttpRequestEvents** tiene estos métodos.



| Método                                                                           | Descripción                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Se produce cuando hay un error de tiempo de ejecución en la aplicación.<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | Se produce cuando los datos están disponibles en la respuesta.<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | Se produce cuando se completan los datos de la respuesta.<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | Se produce cuando se inicia la recepción de los datos de respuesta.<br/>      |



 

## <a name="remarks"></a>Observaciones

En el procedimiento siguiente se describe cómo registrarse para recibir notificaciones.

1.  Obtenga una interfaz [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) llamando a **QueryInterface** en un objeto [**IWinHttpRequest**](iwinhttprequest-interface.md) .
2.  Llame a [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) en la interfaz devuelta y pase **IID \_ IWinHttpRequestEvents** a *riid*.
3.  Llame a [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) en el punto de conexión devuelto y pase un puntero a una interfaz **IUnknown** en un objeto que implemente **IWinHttpRequestEvents** en *pUnk*.

Las notificaciones se pueden finalizar llamando a [unvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) en el punto de conexión devuelto en el paso 2.

Para ver algún código que se registra para las notificaciones COM, consulte la sección Client del artículo [puntos de conexión com](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) .

> [!Note]  
> En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

