---
title: Propiedad InstanceId de la interfaz IMsRdpCameraRedirConfig
description: Obtiene el identificador de instancia de la cámara.
ms.tgt_platform: multiple
keywords:
- Propiedad InstanceId Servicios de Escritorio remoto
- Propiedad InstanceId Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfig
- IMsRdpCameraRedirConfig interface Servicios de Escritorio remoto, InstanceId (propiedad)
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
ms.openlocfilehash: 42654e84f64b25a051a78963339ca95d4ebf760f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104274603"
---
# <a name="imsrdpcameraredirconfiginstanceid-property"></a>IMsRdpCameraRedirConfig:: InstanceId (propiedad)

Obtiene el identificador de instancia de la cámara.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_InstanceId(
    [out, retval] BSTR* pInstanceId
);
```

## <a name="property-value"></a>Valor de propiedad

El identificador de instancia de la cámara.

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