---
description: Se produce cuando los datos están disponibles en la respuesta.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: Evento IWinHttpRequestEvents::OnResponseDataAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b55f87584164a47b47920caf961f02f0bd9cc6596c4c90f76f381027af545e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114249"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a>Evento IWinHttpRequestEvents::OnResponseDataAvailable

El **evento OnResponseDataAvailable** tiene lugar cuando los datos están disponibles en la respuesta.

## <a name="syntax"></a>Sintaxis


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Datos* \[ En\]
</dt> <dd>

Matriz de bytes de base cero que recibe los datos de respuesta recibidos por Microsoft Windows Http Services (WinHTTP) hasta el punto en que se produce este evento. Se trata de una **VARIANTE de** tipo VT ARRAY \_ VT \| \_ UI1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Dado que los datos están en bytes, se deben convertir en caracteres anchos cuando se colocan en una cadena de caracteres anchos (Unicode).

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHTTP.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




