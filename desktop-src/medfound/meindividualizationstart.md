---
description: Lo genera el motor de directivas cuando la individualización está a punto de comenzar. La individualización se realiza mediante la implementación de aplicaciones de la interfaz IMFContentProtectionManager.
ms.assetid: a3ba98ee-4d2e-466d-be9a-c7e3b5f920a7
title: Evento MEIndividualizationStart (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 297ed3dea2dbdfe45a8ea812b7a5c674e1ef1bfb1c136aa54cfd5cd463cf9b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957455"
---
# <a name="meindividualizationstart-event"></a>Evento MEIndividualizationStart

Lo genera el motor de directivas cuando la individualización está a punto de comenzar. La individualización se realiza mediante la implementación de la aplicación de la [**interfaz IMFContentProtectionManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)

Una aplicación individualizada es aquella que ha recibido una actualización a sus componentes de administración de derechos digitales (DRM) que la diferencia de todas las demás copias de la misma aplicación. Los propietarios de contenido pueden requerir que sus archivos protegidos se re reproducen solo en una aplicación que se ha individualizado.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Cuando se completa la adquisición de licencias, el motor de directivas genera el [evento MEIndividualizationCompleted.](meindividualizationcompleted.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




