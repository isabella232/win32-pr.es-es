---
description: El método Abort anula un método Send de WinHTTP.
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
ms.openlocfilehash: ca70917139059e8b0d038797ad61b137a259d615f6098a52bc86466f8054c7b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071775"
---
# <a name="iwinhttprequestabort-method"></a>IWinHttpRequest::Abort (método)

El **método Abort** anula un método Send [**de**](iwinhttprequest-send.md) [WinHTTP.](about-winhttp.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Abort();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **S \_ OK on** success o un valor de error en caso contrario.

## <a name="remarks"></a>Comentarios

Puede anular los métodos send asincrónicos [**y sincrónicos.**](iwinhttprequest-send.md) Para anular un método [**Send sincrónico,**](iwinhttprequest-send.md) debe llamar a **Abort** desde un [**evento IWinHttpRequestEvents.**](iwinhttprequestevents-interface.md)

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHttp.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




