---
description: Un filtro no recibe suficientes datos.
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: EC_STARVATION (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3405bcf67db3e7dbfead0d841b542e155175bcabdd8283b5a5f76f4195cdd714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905785"
---
# <a name="ec_starvation"></a>EC \_ STARVATION

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

El evento no se envía a la aplicación. Si el gráfico de filtro se está ejecutando, el administrador de gráficos de filtro pausa el gráfico y espera a que se complete la pausa. A continuación, ejecuta el gráfico de nuevo. El filtro que envía el evento no debe completar su transición a en pausa hasta que tenga suficientes datos para reanudarse. Si el gráfico de filtros no se está ejecutando, el administrador de gráficos de filtro omite este evento.

## <a name="remarks"></a>Comentarios

Un analizador o filtro de origen puede enviar este evento si llegan demasiados datos.

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

 

 




