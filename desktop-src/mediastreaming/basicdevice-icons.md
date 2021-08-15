---
title: BasicDevice.Icons, propiedad
description: Obtiene un vector de interfaces IDeviceIcon.
ms.assetid: 54933FD0-27A6-48D8-A49A-200AD9214B9A
keywords:
- Propiedad Icons de Media Streaming API
- Propiedad icons Media Streaming API , BasicDispositivo
- Interfaz básicaDispositivo Media Streaming API, propiedad Iconos
topic_type:
- apiref
api_name:
- BasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9807c41680c042ee74b2ddc659ad1558dd13ff8b4000d08cfa0591768c301bb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554665"
---
# <a name="basicdeviceicons-property"></a>BasicDevice.Icons, propiedad

Obtiene un vector de [**interfaces IDeviceIcon.**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="property-value"></a>Valor de propiedad

Colección enumerable de punteros [**de interfaz IDeviceIcon.**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

 