---
description: El gráfico almacena en búfer los datos o ha dejado de almacenar en búfer los datos.
ms.assetid: 39e8b151-0323-42b3-99f0-3dcd230925c8
title: EC_BUFFERING_DATA (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1395a10458abd7a29fdb65e7ab55fba62328d6d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061203"
---
# <a name="ec_buffering_data"></a>DATOS \_ DE ALMACENAMIENTO EN BÚFER DE \_ EC

El gráfico almacena en búfer los datos o ha dejado de almacenar en búfer los datos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**BOOL**) **TRUE** si el gráfico está empezando a almacenar en búfer, **o FALSE** si el gráfico ha detenido el almacenamiento en búfer.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Observaciones

Un filtro puede enviar este evento si necesita almacenar en búfer los datos de un origen externo. (Por ejemplo, podría estar cargando datos desde una red). La aplicación puede usar este evento para ajustar su interfaz de usuario.

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

 

 




