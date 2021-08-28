---
description: Error en un comando asincrónico para ejecutar el gráfico.
ms.assetid: 0bfcf4b4-b35a-4593-9956-8e1e8c9139cb
title: EC_ERROR_STILLPLAYING (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82383c541f2ba5294cf4d45844f096ff510f25444ce87a54b956d0a777a7fc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051785"
---
# <a name="ec_error_stillplaying"></a>\_ERROR DE EC \_ STILLPLAYING

Error en un comando asincrónico para ejecutar el gráfico.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Código de error de la operación que ha generado un error.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Comentarios

Si el administrador de gráficos de filtros emite un comando de ejecución asincrónica que produce un error, envía este evento a la aplicación. El gráfico permanece en estado de ejecución. El estado de los filtros subyacentes es indeterminado. Es posible que algunos filtros se ejecuten y otros no.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




