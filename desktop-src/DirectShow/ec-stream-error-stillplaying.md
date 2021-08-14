---
description: Se produjo un error en una secuencia, pero la secuencia todavía se está reproduciendo.
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: EC_STREAM_ERROR_STILLPLAYING (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf78f1fba25316155e36eef1ed469a32bba1ce7c194a6dffb200f1fce5ede3ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820002"
---
# <a name="ec_stream_error_stillplaying"></a>ERROR \_ DE EC STREAM \_ \_ STILLPLAYING

Se produjo un error en una secuencia, pero la secuencia todavía se está reproduciendo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Código de error de la operación que ha generado un error.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Código de error menor. Este valor suele ser cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno. La aplicación debe decidir si se debe detener el gráfico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




