---
title: Propiedad SymbolicLink de la interfaz IMsRdpCameraRedirConfig
description: Obtiene el vínculo simbólico de la interfaz **KSCATEGORY_VIDEO_CAMERA** de la cámara.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad SymbolicLink
- Propiedad SymbolicLink Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfig
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfig, propiedad SymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.SymbolicLink
- IMsRdpCameraRedirConfig.SymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 439ead6fa0868887cc5965205b22236abb5aada6
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "103906287"
---
# <a name="imsrdpcameraredirconfigsymboliclink-property"></a>IMsRdpCameraRedirConfig:: SymbolicLink (propiedad)

Obtiene el vínculo simbólico de la interfaz **KSCATEGORY_VIDEO_CAMERA** de la cámara.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_SymbolicLink(
    [out, retval] BSTR* pSymbolicLink
);
```

## <a name="property-value"></a>Valor de propiedad

Vínculo simbólico de la interfaz **KSCATEGORY_VIDEO_CAMERA** de la cámara.

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