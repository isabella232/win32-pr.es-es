---
description: Una ventana de vídeo se está activando o desactivando.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e48adb3ae98af172664b807386c615d34b6b22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680266"
---
# <a name="ec_activate"></a>activación de EC \_

Una ventana de vídeo se está activando o desactivando.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**Bool**) **True** si la ventana está activada o **false** si la ventana está desactivada.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del representador.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

El administrador de gráficos de filtro establece el foco a través de la interfaz [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) . No envía la notificación de eventos a la aplicación.

## <a name="remarks"></a>Observaciones

Un representador de vídeo envía este evento cada vez que su ventana está activada o desactivada (es decir, cuando recibe un mensaje de ACTIVATEAPP de WM \_ ). La activación o desactivación de ventanas puede producirse porque la ventana ha ganado o perdido el foco, o porque el representador ha cambiado entre el modo de pantalla completa y el modo de ventana.

Este evento permite al administrador de gráficos de filtro asignar recursos que dependen del foco de la ventana, como dispositivos de audio.

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

 

 




