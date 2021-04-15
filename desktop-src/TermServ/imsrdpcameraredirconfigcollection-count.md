---
title: Propiedad Count de la interfaz IMsRdpCameraRedirConfigCollection
description: Devuelve el número de objetos IMsRdpCameraRedirConfig de la colección.
ms.tgt_platform: multiple
keywords:
- Propiedad Count Servicios de Escritorio remoto
- Propiedad Count Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfigCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfigCollection, propiedad Count
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.Count
- IMsRdpCameraRedirConfigCollection.get_Count
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 31927428b709136de87f436ad92cc6a78fa9795a
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494164"
---
# <a name="imsrdpcameraredirconfigcollectioncount-property"></a>IMsRdpCameraRedirConfigCollection:: Count (propiedad)

Devuelve el número de objetos [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_Count(
    [out, retval] ULONG *pCount
);
```

## <a name="property-value"></a>Valor de propiedad

Número de objetos [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección.

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