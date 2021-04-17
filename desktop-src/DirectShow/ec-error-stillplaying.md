---
description: Error de un comando asincrónico para ejecutar el gráfico.
ms.assetid: 0bfcf4b4-b35a-4593-9956-8e1e8c9139cb
title: EC_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1c99db8c6b332ad4531f04171d960c5cfa9824
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679055"
---
# <a name="ec_error_stillplaying"></a>\_STILLPLAYING de error de EC \_

Error de un comando asincrónico para ejecutar el gráfico.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Código de error de la operación en la que se produjo un error.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Observaciones

Si Filter Graph Manager emite un comando de ejecución asincrónico que produce un error, envía este evento a la aplicación. El gráfico permanece en estado de ejecución. El estado de los filtros subyacentes es indeterminado. Es posible que algunos filtros se estén ejecutando y otros no.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




