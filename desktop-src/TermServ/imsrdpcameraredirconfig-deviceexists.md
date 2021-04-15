---
title: Propiedad DeviceExists de la interfaz IMsRdpCameraRedirConfig
description: Especifica si el dispositivo de cámara existe actualmente (es decir, si la cámara está conectada).
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DeviceExists
- Propiedad DeviceExists Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfig
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfig, propiedad DeviceExists
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.DeviceExists
- IMsRdpCameraRedirConfig.get_DeviceExists
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 368b2d46e6dfc2c32c0bb294edceda31f8a58f4e
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494176"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a>IMsRdpCameraRedirConfig::D propiedad eviceExists

Especifica si el dispositivo de cámara existe actualmente (es decir, si la cámara está conectada).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a>Valor de propiedad

Valor que indica si el dispositivo de cámara existe actualmente (es decir, si la cámara está conectada).

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