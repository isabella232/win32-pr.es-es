---
title: Propiedad ParentInstanceId de la interfaz IMsRdpCameraRedirConfig
description: Obtiene el identificador de instancia del dispositivo primario de la cámara.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ParentInstanceId
- Propiedad ParentInstanceId Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfig
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfig, propiedad ParentInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.ParentInstanceId
- IMsRdpCameraRedirConfig.get_ParentInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e4a399659c33000207930bfe7d17818a2ad8438f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "105720246"
---
# <a name="imsrdpcameraredirconfigparentinstanceid-property"></a>IMsRdpCameraRedirConfig::P propiedad arentInstanceId

Obtiene el identificador de instancia del dispositivo primario de la cámara.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_ParentInstanceId(
    [out, retval] BSTR* pParentInstanceId
);
```

## <a name="property-value"></a>Valor de propiedad

IDENTIFICADOR de instancia del dispositivo primario de la cámara.

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