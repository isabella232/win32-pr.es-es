---
title: Método AddConfig de la interfaz IMsRdpCameraRedirConfigCollection
description: Agrega un objeto IMsRdpCameraRedirConfig a la colección (no es necesario que la cámara correspondiente esté conectada).
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
ms.openlocfilehash: e8c954b710c3f35bca9685d461e478104dac9039
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104536381"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a>IMsRdpCameraRedirConfigCollection:: AddConfig (método)

Agrega un objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) a la colección (no es necesario que la cámara correspondiente esté conectada).

## <a name="syntax"></a>Sintaxis

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a>Parámetros

*symbolicLink* \[ de\]

Vínculo simbólico para el nuevo objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) .

*fRedirected* \[ de\]

Especifica si la nueva cámara se redirige de forma predeterminada o no.

## <a name="return-value"></a>Valor devuelto

Vuelva **a \_ Aceptar si es** correcto.

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