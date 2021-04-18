---
title: Propiedad BySymbolicLink de la interfaz IMsRdpCameraRedirConfigCollection
description: Devuelve un objeto IMsRdpCameraRedirConfig de la colección que corresponde al vínculo simbólico especificado de la interfaz **KSCATEGORY_VIDEO_CAMERA** de la cámara.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad BySymbolicLink
- Propiedad BySymbolicLink Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfigCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfigCollection, propiedad BySymbolicLink
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
ms.openlocfilehash: d4888c7e468e0522240d8ef922563ab28eb33e77
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "105720242"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a>IMsRdpCameraRedirConfigCollection::. Propiedad BySymbolicLink

Devuelve un objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección que corresponde al vínculo simbólico especificado de la interfaz **KSCATEGORY_VIDEO_CAMERA** de la cámara.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_BySymbolicLink(
    [in]          BSTR symbolicLink,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Valor de propiedad

El objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) que corresponde al vínculo simbólico especificado.

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