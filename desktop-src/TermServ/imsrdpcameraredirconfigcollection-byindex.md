---
title: Propiedad ByIndex de la interfaz IMsRdpCameraRedirConfigCollection
description: Devuelve un objeto IMsRdpCameraRedirConfig por su índice en la colección.
ms.tgt_platform: multiple
keywords:
- Propiedad ByIndex Servicios de Escritorio remoto
- Propiedad ByIndex Servicios de Escritorio remoto , interfaz IMsRdpCameraRedirConfigCollection
- Interfaz IMsRdpCameraRedirConfigCollection Servicios de Escritorio remoto , propiedad ByIndex
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByIndex
- IMsRdpCameraRedirConfigCollection.get_ByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 68c179023e93295ee846da22357d5f8efb75b15c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968456"
---
# <a name="imsrdpcameraredirconfigcollectionbyindex-property"></a>IMsRdpCameraRedirConfigCollection::ByIndex, propiedad

Devuelve un [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) por su índice en la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_ByIndex(
    [in]            ULONG index,
    [out, retval]   IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Valor de propiedad

Objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) que corresponde al índice especificado.

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