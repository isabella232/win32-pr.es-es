---
description: El gráfico de filtros ha cambiado de estado.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2b476c923f0b812196a5697444433ea0be65b8d3f46bd0388261b2a67a66881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905735"
---
# <a name="ec_state_change"></a>CAMBIO \_ DE ESTADO DE \_ EC

El gráfico de filtros ha cambiado de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Miembro del tipo [**enumerado FILTER \_ STATE,**](/windows/win32/api/strmif/ne-strmif-filter_state) que indica el nuevo estado del gráfico.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

No hay ninguna acción predeterminada. El evento no se envía a la aplicación.

> [!Note]  
> Este evento puede producirse cuando se cierra el gráfico. Si invalida la acción predeterminada y escucha este evento, debe tener especial cuidado de no procesar los eventos después de liberar el Administrador de filtros Graph Manager. De lo contrario, la aplicación podría hacer referencia a un puntero [**iMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) y un bloqueo no válidos. Para obtener más información, [vea Responder a eventos](responding-to-events.md).

 

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

 

 




