---
title: Interfaz IMsRdpCameraRedirConfig
description: Representa las configuraciones de una cámara que está disponible para la redirección.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfig
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfig, descrito
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: fbb0f3344e0653ea4a87c876bb8ca7b8a67e7d21
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104536382"
---
# <a name="imsrdpcameraredirconfig-interface"></a>Interfaz IMsRdpCameraRedirConfig

Representa las configuraciones de una cámara que está disponible para la redirección.

## <a name="members"></a>Miembros

La interfaz **IMsRdpCameraRedirConfig** hereda de **IUnknown**. **IMsRdpCameraRedirConfig** también tiene estos tipos de miembros:

- [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpCameraRedirConfig** tiene estas propiedades.

| Propiedad         | Tipo de acceso           | Descripción            |
|:-----------------|:----------------------|:-----------------------|
| [**DeviceExists**](imsrdpcameraredirconfig-deviceexists.md)      | Solo lectura | Especifica si el dispositivo de cámara existe actualmente (es decir, si la cámara está conectada).   |
| [**FriendlyName**](imsrdpcameraredirconfig-friendlyname.md)                       | Solo lectura |    Obtiene el nombre descriptivo de la cámara.    |
| [**ID**](imsrdpcameraredirconfig-instanceid.md)      | Solo lectura |  Obtiene el identificador de instancia de la cámara.  |
| [**ParentInstanceId**](imsrdpcameraredirconfig-parentinstanceid.md)                       | Solo lectura |    Obtiene el identificador de instancia del dispositivo primario de la cámara.   |
| [**Redirected**](imsrdpcameraredirconfig-redirected.md)      | Lectura/Escritura |  Especifica si se redirige la cámara.  |
| [**SymbolicLink**](imsrdpcameraredirconfig-symboliclink.md)                       | Solo lectura |   Obtiene el vínculo simbólico de la interfaz **KSCATEGORY_VIDEO_CAMERA** de la cámara.   |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfig se define como 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>Vea también

- [**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
- [**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)