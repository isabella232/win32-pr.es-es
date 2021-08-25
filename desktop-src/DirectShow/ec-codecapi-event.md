---
description: Un codificador \_ envía el evento EC CODECAPI EVENT para indicar un evento de \_ codificación. El cliente se registra para el evento del codificador mediante una llamada al método ICodecAPI::RegisterForEvent.
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5765c2a1156653e66c5d3685cacfdd551cd22032eea34463f5450dc6d4fbea3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965945"
---
# <a name="ec_codecapi_event"></a>EVENTO \_ CODECAPI \_ DE EC

Un codificador \_ envía el evento EC CODECAPI EVENT para indicar un evento de \_ codificación. El cliente se registra para el evento del codificador mediante una llamada [**al método ICodecAPI::RegisterForEvent.**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent)

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Datos de usuario. El valor de este parámetro es el puntero que el autor de la llamada especificó en el parámetro *userData* del [**método RegisterForEvent.**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent)

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Puntero a los datos del evento. El codificador asigna estos datos y la aplicación debe liberar estos datos mediante la **función CoTaskMemFree.** El bloque de datos comienza con una [**estructura CodecAPIEventData;**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) convierte el *parámetro lParam2* en un puntero a esta estructura.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

No hay ninguna acción predeterminada.

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

 

 




