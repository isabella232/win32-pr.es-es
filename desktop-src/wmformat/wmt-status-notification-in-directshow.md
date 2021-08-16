---
title: WMT_STATUS notificación de eventos en DirectShow
description: Notificación de \_ eventos WMT STATUS en DirectShow
ms.assetid: 6b777c7e-2777-445b-88de-a9a28be6da9c
keywords:
- Windows SDK de formato multimedia, WMT_STATUS notificaciones de eventos en DirectShow
- Windows SDK de formato multimedia, notificaciones de eventos
- Windows SDK de formato multimedia, DirectShow
- Formato de sistemas avanzados (ASF), WMT_STATUS notificaciones de eventos en DirectShow
- ASF (formato de sistemas avanzados), WMT_STATUS notificaciones de eventos en DirectShow
- Formato de sistemas avanzados (ASF), notificaciones de eventos
- ASF (formato de sistemas avanzados), notificaciones de eventos
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- DirectShow,notificaciones de eventos
- DirectShow,WMT_STATUS notificaciones de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4bbe430f16872baf94a0d47417381bc8bcd23d5c9fbbdb69ff2496cd873908
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089635"
---
# <a name="wmt_status-event-notification-in-directshow"></a>Notificación de \_ eventos WMT STATUS en DirectShow

Tanto el lector de ASF como el escritor de ASF reenvía [**eventos WMT \_ STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) a las aplicaciones. El sistema de escritura reenvía todos estos eventos y el lector reenvía solo los que pertenecen a la adquisición de licencias DRM. Para recibir estas notificaciones de eventos en la aplicación, agregue un caso para **EC \_ WMT \_ EVENT** en la función de control de eventos. El *parámetro lParam1* asociado al evento contiene el código DE ESTADO DE WMT (que puede ser **\_ WMT ERROR**) y lParam2 contiene un AM [**\_ WMT \_ EVENT \_ DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) que incluye **HRESULT**. **\_**

 

 