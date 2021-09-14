---
description: Se produce cuando los datos de respuesta comienzan a recibirse.
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: Evento IWinHttpRequestEvents::OnResponseStart
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a299c535dd854bff07f2c24989096f7b9e49fc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068326"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a>Evento IWinHttpRequestEvents::OnResponseStart

El **evento OnResponseStart** tiene lugar cuando los datos de respuesta comienzan a recibirse.

## <a name="syntax"></a>Sintaxis


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Estado* \[ En\]
</dt> <dd>

Recibe el código de estado estándar devuelto con los datos de respuesta. Los códigos de estado se definen [en RFC 2616.](https://www.ietf.org/rfc/rfc2616.txt)

</dd> <dt>

*ContentType* \[ En\]
</dt> <dd>

Especifica el tipo de contenido recibido, como "text/html" o "image/gif".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para que se produzca este evento, use [**Abrir**](iwinhttprequest-open.md) para enviar una conexión HTTP en modo asincrónico y use [**Enviar**](iwinhttprequest-send.md) para enviar una solicitud de datos a un servidor de Internet.

Este es el primer evento WinHTTP que se produce después de [**enviar**](iwinhttprequest-send.md).

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHTTP.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio SP3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versiones winHTTP](winhttp-versions.md)
</dt> </dl>

 

 




