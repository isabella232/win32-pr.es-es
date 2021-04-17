---
description: '\_ \_ Un codificador envía el evento de evento CODECAPI de EC para señalar un evento de codificación. El cliente se registra para el evento Encoder llamando al método ICodecAPI:: RegisterForEvent.'
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c24ece20a0c729b251c56b50b5b44fc9f7fa98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680258"
---
# <a name="ec_codecapi_event"></a>\_evento CODECAPI de EC \_

\_ \_ Un codificador envía el evento de evento CODECAPI de EC para señalar un evento de codificación. El cliente se registra para el evento Encoder llamando al método [**ICodecAPI:: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Datos de usuario. El valor de este parámetro es el puntero que el llamador especificó en el parámetro *UserData* del método [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Puntero a los datos de evento. El codificador asigna estos datos y la aplicación debe liberarlos mediante la función **CoTaskMemFree** . El bloque de datos se inicia con una estructura [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) . convierta el parámetro *lParam2* en un puntero a esta estructura.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguna acción predeterminada.

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

 

 




