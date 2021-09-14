---
title: Propiedad ByInstanceId de la interfaz IMsRdpCameraRedirConfigCollection
description: Devuelve un objeto IMsRdpCameraRedirConfig de la colección que corresponde al identificador de instancia especificado.
ms.tgt_platform: multiple
keywords:
- ByInstanceId, propiedad Servicios de Escritorio remoto
- Propiedad ByInstanceId Servicios de Escritorio remoto , interfaz IMsRdpCameraRedirConfigCollection
- Interfaz IMsRdpCameraRedirConfigCollection Servicios de Escritorio remoto , propiedad ByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByInstanceId
- IMsRdpCameraRedirConfigCollection.get_ByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d90cb7d2f309a3df9e354ace04a840b667e5569b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965360"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a>IMsRdpCameraRedirConfigCollection::ByInstanceId, propiedad

Devuelve un [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección que corresponde al identificador de instancia especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Valor de propiedad

Objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) que corresponde al identificador de instancia especificado.

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