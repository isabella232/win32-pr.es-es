---
title: Propiedad CameraRedirConfigCollection de la interfaz IMsRdpClientNonScriptable7
description: Obtiene la colección de cámaras (y las configuraciones asociadas) que están disponibles para el redireccionamiento.
ms.tgt_platform: multiple
keywords:
- Propiedad CameraRedirConfigCollection Servicios de Escritorio remoto
- Propiedad CameraRedirConfigCollection Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable7
- Interfaz IMsRdpClientNonScriptable7 Servicios de Escritorio remoto , propiedad CameraRedirConfigCollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.CameraRedirConfigCollection
- IMsRdpClientNonScriptable7.get_CameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: ea90c06403c1ba44e129867f2d739990a37ee178ebe5d0b8f4afd684b17eb09e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033175"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a>Propiedad IMsRdpClientNonScriptable7::CameraRedirConfigCollection

Obtiene la colección de cámaras (y las configuraciones asociadas) que están disponibles para el redireccionamiento.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a>Valor de propiedad

[IMsRdpCameraRedirConfigCollection que](imsrdpcameraredirconfigcollection.md) representa la colección de cámaras (y las configuraciones asociadas) que están disponibles para el redireccionamiento.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable7 se define como 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC          |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>