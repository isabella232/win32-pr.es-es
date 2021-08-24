---
title: Interfaz IMsRdpCameraRedirConfig
description: Representa las configuraciones de una cámara que está disponible para el redireccionamiento.
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpCameraRedirConfig Servicios de Escritorio remoto
- Interfaz IMsRdpCameraRedirConfig Servicios de Escritorio remoto , descrito
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
ms.openlocfilehash: aa030d462a16eacd521709c5be534f3d90e14f446da519490ee62f0260766084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574545"
---
# <a name="imsrdpcameraredirconfig-interface"></a>Interfaz IMsRdpCameraRedirConfig

Representa las configuraciones de una cámara que está disponible para el redireccionamiento.

## <a name="members"></a>Miembros

La **interfaz IMsRdpCameraRedirConfig** hereda de **IUnknown.** **IMsRdpCameraRedirConfig** también tiene estos tipos de miembros:

- [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpCameraRedirConfig** tiene estas propiedades.

| Propiedad         | Tipo de acceso           | Descripción            |
|:-----------------|:----------------------|:-----------------------|
| [**DeviceExists**](imsrdpcameraredirconfig-deviceexists.md)      | Solo lectura | Especifica si el dispositivo de cámara existe actualmente (es decir, la cámara está conectada).   |
| [**FriendlyName**](imsrdpcameraredirconfig-friendlyname.md)                       | Solo lectura |    Obtiene el nombre descriptivo de la cámara.    |
| [**InstanceId**](imsrdpcameraredirconfig-instanceid.md)      | Solo lectura |  Obtiene el identificador de instancia de la cámara.  |
| [**ParentInstanceId**](imsrdpcameraredirconfig-parentinstanceid.md)                       | Solo lectura |    Obtiene el identificador de instancia del dispositivo primario de la cámara.   |
| [**Redirected**](imsrdpcameraredirconfig-redirected.md)      | Lectura/Escritura |  Especifica si se redirige o no la cámara.  |
| [**SymbolicLink**](imsrdpcameraredirconfig-symboliclink.md)                       | Solo lectura |   Obtiene el vínculo simbólico de la **KSCATEGORY_VIDEO_CAMERA** interfaz de la cámara.   |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfig se define como 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>Vea también

- [**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
- [**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)