---
title: Propiedad EncodingQuality de la interfaz IMsRdpCameraRedirConfigCollection
description: Especifica la calidad de codificación (velocidad de bits).
ms.tgt_platform: multiple
keywords:
- Propiedad EncodingQuality Servicios de Escritorio remoto
- Propiedad EncodingQuality Servicios de Escritorio remoto , interfaz IMsRdpCameraRedirConfigCollection
- Interfaz IMsRdpCameraRedirConfigCollection Servicios de Escritorio remoto , propiedad EncodingQuality
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodingQuality
- IMsRdpCameraRedirConfigCollection.put_EncodingQuality
- IMsRdpCameraRedirConfigCollection.get_EncodingQuality
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d8044c2fb70233243a3a74d8dc5faac96873cb48
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965335"
---
# <a name="imsrdpcameraredirconfigcollectionencodingquality-property"></a>Propiedad IMsRdpCameraRedirConfigCollection::EncodingQuality

Especifica la calidad de codificación (velocidad de bits).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT put_EncodingQuality(
    [in] CameraRedirEncodingQuality encodingQuality
);

HRESULT get_EncodingQuality(
    [out, retval] CameraRedirEncodingQuality* pEncodingQuality
);
```

## <a name="property-value"></a>Valor de propiedad

Uno de los siguientes **valores de enumeración CameraRedirEncodingQuality** que especifica la calidad de codificación (velocidad de bits).

| Nombre del miembro de enumeración | Value |
|-----------------|--------|
| encodingQualityLow | 0x0000 |
| encodingQualityMedium | 0x0001 |
| encodingQualityHigh | 0x0002 |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection se define como AE45252B-AAAB-4504-B681-649D6073A37A          |

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>