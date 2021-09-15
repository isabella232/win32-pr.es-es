---
description: Se produce cuando hay un error en tiempo de ejecución en la aplicación.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: Evento IWinHttpRequestEvents::OnError
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8582deec90eb6bfc2985460f3127d5c7ee9c01b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474525"
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

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHTTP.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




