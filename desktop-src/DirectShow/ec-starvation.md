---
description: Un filtro no recibe suficientes datos.
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: EC_STARVATION (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988d550b93ecb9a3c2f78f2d07f50a3965be945d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653356"
---
# <a name="ec_starvation"></a>colapso de EC \_

Un filtro no recibe suficientes datos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Cero.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

El evento no se envía a la aplicación. Si el gráfico de filtros se está ejecutando, el administrador de gráficos de filtro pausa el gráfico y espera a que se complete la pausa. A continuación, vuelve a ejecutar el gráfico. El filtro que envía el evento no debe completar su transición a pausado hasta que tenga suficientes datos para reanudar. Si el gráfico de filtros no se está ejecutando, el administrador de gráficos de filtro omite este evento.

## <a name="remarks"></a>Observaciones

Un analizador o filtro de origen puede enviar este evento si llegan demasiado pocos datos.

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

 

 




