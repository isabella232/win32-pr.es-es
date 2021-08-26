---
title: Método AddConfig de la interfaz IMsRdpCameraRedirConfigCollection
description: Agrega un objeto IMsRdpCameraRedirConfig a la colección (no es necesario conectar la cámara correspondiente).
ms.tgt_platform: multiple
keywords:
- Método AddConfig Servicios de Escritorio remoto
- Método AddConfig Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfigCollection
- Interfaz IMsRdpCameraRedirConfigCollection Servicios de Escritorio remoto, método AddConfig
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.AddConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 88d4f7952497ca0afd970a979441f98864b2855ed3f36f3e556dc4241ed52769
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033655"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a>IMsRdpCameraRedirConfigCollection::AddConfig (método)

Agrega un [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) a la colección (no es necesario conectar la cámara correspondiente).

## <a name="syntax"></a>Sintaxis

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a>Parámetros

*symbolicLink* \[ En\]

Vínculo simbólico para el nuevo [objeto IMsRdpCameraRedirConfig.](imsrdpcameraredirconfig.md)

*fRedirected* \[ En\]

Especifica si la nueva cámara se redirige de forma predeterminada.

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** se realiza correctamente.

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