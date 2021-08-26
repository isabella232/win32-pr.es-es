---
description: Se está activando o desactivando una ventana de vídeo.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14d9b0ad192045f179d9f0f366eed6a32efb0e6cc6f61b47255f118b7f55258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966065"
---
# <a name="ec_activate"></a>EC \_ ACTIVATE

Se está activando o desactivando una ventana de vídeo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**BOOL**) **TRUE** si la ventana está activada o **FALSE** si la ventana está desactivada.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del representador.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

El administrador de gráficos de filtros establece el foco a través de [**la interfaz IResourceManager.**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) No envía la notificación de eventos a la aplicación.

## <a name="remarks"></a>Comentarios

Un representador de vídeo envía este evento cada vez que se activa o desactiva su ventana (es decir, cuando recibe un mensaje \_ DE WM ACTIVATEAPP). La activación o desactivación de ventanas puede producirse porque la ventana ha adquirido o perdido el foco, o porque el representador ha cambiado entre el modo de pantalla completa y el modo de ventana.

Este evento permite al administrador de gráficos de filtros asignar recursos que dependen del foco de la ventana, como los dispositivos de audio.

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

 

 




