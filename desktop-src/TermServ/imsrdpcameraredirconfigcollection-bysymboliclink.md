---
title: Propiedad BySymbolicLink de la interfaz IMsRdpCameraRedirConfigCollection
description: Devuelve un objeto IMsRdpCameraRedirConfig de la colección que corresponde al vínculo simbólico dado de la **interfaz** KSCATEGORY_VIDEO_CAMERA para la cámara.
ms.tgt_platform: multiple
keywords:
- BySymbolicLink, propiedad Servicios de Escritorio remoto
- Propiedad BySymbolicLink Servicios de Escritorio remoto , interfaz IMsRdpCameraRedirConfigCollection
- Interfaz IMsRdpCameraRedirConfigCollection Servicios de Escritorio remoto , propiedad BySymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.BySymbolicLink
- IMsRdpCameraRedirConfigCollection.get_BySymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: a46cd3daf8cc4270473433bb0c4c20dee0616dba3619b056d33136e0d4dd8f5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033635"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a>IMsRdpCameraRedirConfigCollection::. BySymbolicLink, propiedad

Devuelve un [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección que corresponde al vínculo simbólico dado de la **interfaz** KSCATEGORY_VIDEO_CAMERA para la cámara.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_BySymbolicLink(
    [in]          BSTR symbolicLink,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Valor de propiedad

Objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) que corresponde al vínculo simbólico especificado.

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