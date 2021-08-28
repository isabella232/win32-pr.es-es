---
title: Propiedad ParentInstanceId de la interfaz IMsRdpCameraRedirConfig
description: Obtiene el identificador de instancia del dispositivo primario de la cámara.
ms.tgt_platform: multiple
keywords:
- Propiedad ParentInstanceId Servicios de Escritorio remoto
- Propiedad ParentInstanceId Servicios de Escritorio remoto , interfaz IMsRdpCameraRedirConfig
- Interfaz IMsRdpCameraRedirConfig Servicios de Escritorio remoto , propiedad ParentInstanceId
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
ms.openlocfilehash: 149e4f536996376193596db6c4fd4cf659637c05bb92e3afcdb7ee78c480b893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574565"
---
# <a name="imsrdpcameraredirconfigparentinstanceid-property"></a>IMsRdpCameraRedirConfig::P arentInstanceId

Obtiene el identificador de instancia del dispositivo primario de la cámara.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_ParentInstanceId(
    [out, retval] BSTR* pParentInstanceId
);
```

## <a name="property-value"></a>Valor de propiedad

Identificador de instancia del dispositivo primario de la cámara.

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