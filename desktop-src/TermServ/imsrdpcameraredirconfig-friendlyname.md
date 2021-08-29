---
title: Propiedad FriendlyName de la interfaz IMsRdpCameraRedirConfig
description: Obtiene el nombre descriptivo de la cámara.
ms.tgt_platform: multiple
keywords:
- Propiedad FriendlyName Servicios de Escritorio remoto
- Propiedad FriendlyName Servicios de Escritorio remoto interfaz , IMsRdpCameraRedirConfig
- Interfaz IMsRdpCameraRedirConfig Servicios de Escritorio remoto propiedad , FriendlyName
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.FriendlyName
- IMsRdpCameraRedirConfig.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 31d6d775310d23cfe8a9cf8ab95ea56e9e2b2d0e418fc9d1a55d3cf26fcce26e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737415"
---
# <a name="imsrdpcameraredirconfigfriendlyname-property"></a>IMsRdpCameraRedirConfig::FriendlyName, propiedad

Obtiene el nombre descriptivo de la cámara.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT get_FriendlyName(
    [out, retval] BSTR* pFriendlyName
);
```

## <a name="property-value"></a>Valor de propiedad

Nombre descriptivo de la cámara.

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