---
title: BasicDevice. Icons (propiedad)
description: Obtiene un vector de interfaces IDeviceIcon.
ms.assetid: 54933FD0-27A6-48D8-A49A-200AD9214B9A
keywords:
- Propiedad Icons media streaming API
- Propiedad Icons media streaming API, BasicDevice (interfaz)
- Interfaz BasicDevice API de streaming de multimedia, propiedad Icons
topic_type:
- apiref
api_name:
- BasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdd0235a2b07ea86cbace87defb92f44d6b42315
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420685"
---
# <a name="basicdeviceicons-property"></a>BasicDevice. Icons (propiedad)

Obtiene un vector de interfaces [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="property-value"></a>Valor de propiedad

Colección enumerable de punteros de interfaz [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

 