---
description: Se produce cuando se inicia la recepción de los datos de respuesta.
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: 'Evento IWinHttpRequestEvents:: OnResponseStart'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a299c535dd854bff07f2c24989096f7b9e49fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706607"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a>Evento IWinHttpRequestEvents:: OnResponseStart

El evento **OnResponseStart** se produce cuando se inicia la recepción de los datos de respuesta.

## <a name="syntax"></a>Sintaxis


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Estado* \[ de de\]
</dt> <dd>

Recibe el código de estado estándar devuelto con los datos de respuesta. Los códigos de estado se definen en [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

*ContentType* \[ de\]
</dt> <dd>

Especifica el tipo de contenido recibido, como "text/html" o "image/gif".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para que se produzca este evento, utilice [**Open**](iwinhttprequest-open.md) para enviar una conexión http en modo asincrónico y utilice [**send**](iwinhttprequest-send.md) para enviar una solicitud de datos a un servidor de Internet.

Este es el primer evento de WinHTTP que debe producirse después del [**envío**](iwinhttprequest-send.md).

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

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




