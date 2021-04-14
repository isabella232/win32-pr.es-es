---
title: Propiedad CameraRedirConfigCollection de la interfaz IMsRdpClientNonScriptable7
description: Obtiene la colección de cámaras (y las configuraciones asociadas) que están disponibles para la redirección.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad CameraRedirConfigCollection
- Propiedad CameraRedirConfigCollection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable7, propiedad CameraRedirConfigCollection
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
ms.openlocfilehash: 817d3d73b4abbf8aa8b4126fd99ed7d11c3fff51
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104359878"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a>IMsRdpClientNonScriptable7:: CameraRedirConfigCollection (propiedad)

Obtiene la colección de cámaras (y las configuraciones asociadas) que están disponibles para la redirección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a>Valor de propiedad

Un [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) que representa la colección de cámaras (y las configuraciones asociadas) que están disponibles para la redirección.

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