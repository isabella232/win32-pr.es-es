---
description: El gráfico almacena en búfer los datos o ha detenido el almacenamiento en búfer de los datos.
ms.assetid: 39e8b151-0323-42b3-99f0-3dcd230925c8
title: EC_BUFFERING_DATA (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc937973db8435657d131ff4adea83892bf87681bb3db9b7d016565f5c38670
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965975"
---
# <a name="ec_buffering_data"></a>DATOS \_ DE ALMACENAMIENTO EN BÚFER DE \_ EC

El gráfico almacena en búfer los datos o ha detenido el almacenamiento en búfer de los datos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**BOOL**) **TRUE** si el gráfico está empezando a almacenar en búfer o **FALSE** si el gráfico ha detenido el almacenamiento en búfer.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Comentarios

Un filtro puede enviar este evento si necesita almacenar en búfer los datos de un origen externo. (Por ejemplo, podría estar cargando datos desde una red). La aplicación puede usar este evento para ajustar su interfaz de usuario.

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

 

 




