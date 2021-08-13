---
title: Propiedad EncodeVideo de la interfaz IMsRdpCameraRedirConfigCollection
description: Especifica si la secuencia de vídeo está codificada en H.264 o no.
ms.tgt_platform: multiple
keywords:
- Codificación de la propiedad EncodeVideo Servicios de Escritorio remoto
- Propiedad EncodeVideo Servicios de Escritorio remoto , interfaz IMsRdpCameraRedirConfigCollection
- Interfaz IMsRdpCameraRedirConfigCollection Servicios de Escritorio remoto , propiedad EncodeVideo
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodeVideo
- IMsRdpCameraRedirConfigCollection.put_EncodeVideo
- IMsRdpCameraRedirConfigCollection.get_EncodeVideo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 9eda6fd63953425001906595b0cd8b594496e0f83974ba9d359ed43a639a4164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475965"
---
# <a name="imsrdpcameraredirconfigcollectionencodevideo-property"></a>IMsRdpCameraRedirConfigCollection::EncodeVideo, propiedad

Especifica si la secuencia de vídeo está codificada en H.264 o no.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT put_EncodeVideo(
    [in] VARIANT_BOOL fEncode
);

HRESULT get_EncodeVideo(
    [out, retval] VARIANT_BOOL* pfEncode
);
```

## <a name="property-value"></a>Valor de propiedad

Valor que indica si la secuencia de vídeo está codificada o no en H.264.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection se define como AE45252B-AAAB-4504-B681-649D6073A37A          |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>