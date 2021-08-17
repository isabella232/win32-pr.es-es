---
title: Propiedad InstanceId de la interfaz IMsRdpCameraRedirConfig
description: Obtiene el identificador de instancia de la cámara.
ms.tgt_platform: multiple
keywords:
- Propiedad InstanceId Servicios de Escritorio remoto
- Propiedad InstanceId Servicios de Escritorio remoto , interfaz IMsRdpCameraRedirConfig
- Interfaz IMsRdpCameraRedirConfig Servicios de Escritorio remoto , propiedad InstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.InstanceId
- IMsRdpCameraRedirConfig.get_InstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 621c865f9727cf484430d00609dcfcfac2431a514cf2bade714fdd4d81b0408c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401005"
---
# <a name="imsrdpcameraredirconfiginstanceid-property"></a>Propiedad IMsRdpCameraRedirConfig::InstanceId

Obtiene el identificador de instancia de la cámara.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_InstanceId(
    [out, retval] BSTR* pInstanceId
);
```

## <a name="property-value"></a>Valor de propiedad

Identificador de instancia de la cámara.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfig se define como 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
</dt> </dl>