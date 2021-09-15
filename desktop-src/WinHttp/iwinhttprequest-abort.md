---
description: El método Abort anula un método WinHTTP Send.
ms.assetid: 8326feef-8611-4441-b52d-74855e6acfff
title: IWinHttpRequest::Abort (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Abort
- WinHttpRequest.Abort
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56290dfc16f9986cb7d7596c098bb53c207efebe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258655"
---
# <a name="iwinhttprequestabort-method"></a>IWinHttpRequest::Abort (método)

El **método Abort** anula un método [WinHTTP](about-winhttp.md) [**Send.**](iwinhttprequest-send.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Abort();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **S \_ OK on** success o un valor de error de lo contrario.

## <a name="remarks"></a>Observaciones

Puede anular los métodos Send asincrónicos [**y sincrónicos.**](iwinhttprequest-send.md) Para anular un [**método Send**](iwinhttprequest-send.md) sincrónico, debe llamar a **Abort** desde un [**evento IWinHttpRequestEvents.**](iwinhttprequestevents-interface.md)

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHttp.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio SP3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versiones winHTTP](winhttp-versions.md)
</dt> </dl>

 

 




