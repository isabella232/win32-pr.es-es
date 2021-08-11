---
title: Propiedad DevicePair Renderer
description: Obtiene el representador del par de dispositivos básico activo.
ms.assetid: DB2ED5D3-CCDF-4704-A29A-F1A13F7B953A
keywords:
- Api de streaming multimedia de propiedad del representador
- Propiedad del representador Media Streaming API, interfaz DevicePair
- Interfaz DevicePair Media Streaming API, propiedad representador
topic_type:
- apiref
api_name:
- DevicePair.Renderer
- DevicePair.get_Renderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05707fd65e2ac8998fa2412ec15c12d3b003b88990641aad6510d87bd7692e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236088"
---
# <a name="devicepairrenderer-property"></a>DevicePair::Renderer, propiedad

Obtiene el representador del par de dispositivos básico activo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Renderer(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a>Valor de propiedad

Recibe un [**objeto ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) que representa el dispositivo representador.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

 