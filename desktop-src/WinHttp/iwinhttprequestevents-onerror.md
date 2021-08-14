---
description: Se produce cuando hay un error en tiempo de ejecución en la aplicación.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: Evento IWinHttpRequestEvents::OnError
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31127dcc3155b804bbda1c3ab94ee8a410c73f5a96c3ecfc6f787479ccd51539
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744343"
---
# <a name="iwinhttprequesteventsonerror-event"></a>Evento IWinHttpRequestEvents::OnError

El **evento OnError** se produce cuando hay un error en tiempo de ejecución en la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ErrorNumber* \[ En\]
</dt> <dd>

Recibe el valor numérico del error. Los 16 bits inferiores de este número de error corresponden a uno de los errores enumerados en [**Mensajes de error**](error-messages.md).

</dd> <dt>

*ErrorDescription* \[ En\]
</dt> <dd>

Especifica una breve descripción del error que se produjo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHTTP.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




