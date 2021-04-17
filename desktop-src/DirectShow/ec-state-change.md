---
description: El gráfico de filtro ha cambiado de estado.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64cc62ba15f77370e52821c3335f9a22f573d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690323"
---
# <a name="ec_state_change"></a>\_cambio de estado de EC \_

El gráfico de filtro ha cambiado de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Miembro del tipo enumerado de [**\_ Estado de filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , que indica el nuevo estado del gráfico.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguna acción predeterminada. El evento no se envía a la aplicación.

> [!Note]  
> Este evento puede producirse cuando se cierra el gráfico. Si invalida la acción predeterminada y escucha este evento, debe tener especial cuidado de no procesar eventos después de liberar el administrador de gráficos de filtros. De lo contrario, la aplicación podría hacer referencia a un puntero [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) no válido y bloquearse. Para obtener más información, consulte [responder a eventos](responding-to-events.md).

 

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

 

 




