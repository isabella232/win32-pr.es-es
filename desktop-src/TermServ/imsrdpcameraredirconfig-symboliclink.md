---
title: Propiedad SymbolicLink de la interfaz IMsRdpCameraRedirConfig
description: Obtiene el vínculo simbólico de la **KSCATEGORY_VIDEO_CAMERA** interfaz de la cámara.
ms.tgt_platform: multiple
keywords:
- Propiedad SymbolicLink Servicios de Escritorio remoto
- Propiedad SymbolicLink Servicios de Escritorio remoto , interfaz IMsRdpCameraRedirConfig
- Interfaz IMsRdpCameraRedirConfig Servicios de Escritorio remoto , propiedad SymbolicLink
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
ms.openlocfilehash: 718dbade2997d41b6ad177a7fb9fe4f60c29b7149c499565f9c5de372caa8ba3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737395"
---
# <a name="imsrdpcameraredirconfigsymboliclink-property"></a>Propiedad IMsRdpCameraRedirConfig::SymbolicLink

Obtiene el vínculo simbólico de la **KSCATEGORY_VIDEO_CAMERA** interfaz de la cámara.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_SymbolicLink(
    [out, retval] BSTR* pSymbolicLink
);
```

## <a name="property-value"></a>Valor de propiedad

Vínculo simbólico de la **interfaz KSCATEGORY_VIDEO_CAMERA** para la cámara.

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