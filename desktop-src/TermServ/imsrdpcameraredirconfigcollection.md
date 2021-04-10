---
title: Interfaz IMsRdpCameraRedirConfigCollection
description: Representa la colección de cámaras (y las configuraciones asociadas) que están disponibles para la redirección.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfigCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfigCollection, descrito
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 3d97249a7485ec024ee3611809c87c5b6ed41143
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104151923"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a>Interfaz IMsRdpCameraRedirConfigCollection

 Representa la colección de cámaras (y las configuraciones asociadas) que están disponibles para la redirección.

## <a name="members"></a>Miembros

La interfaz **IMsRdpCameraRedirConfigCollection** hereda de **IUnknown**. **IMsRdpCameraRedirConfigCollection** también tiene estos tipos de miembros:

- [Métodos](#methods)
- [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IMsRdpCameraRedirConfigCollection** tiene estos métodos.

| Método            | Descripción              |
|:------------------|:-------------------------|
| [**AddConfig**](imsrdpcameraredirconfigcollection-addconfig.md)       |  Agrega un objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) a la colección (no es necesario que la cámara correspondiente esté conectada).                   |
| [**Volver a examinar**](imsrdpcameraredirconfigcollection-rescan.md)       |  Enumera los dispositivos de cámara conectados.                   |

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpCameraRedirConfigCollection** tiene estas propiedades.

| Propiedad         | Tipo de acceso           | Descripción            |
|:-----------------|:----------------------|:-----------------------|
| [**ByIndex**](imsrdpcameraredirconfigcollection-byindex.md)      | Solo lectura |  Devuelve un objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) por su índice en la colección.   |
| [**ByInstanceId**](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | Solo lectura |    Devuelve un objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección que corresponde al identificador de instancia especificado.    |
| [**BySymbolicLink**](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | Solo lectura |  Devuelve un objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección que corresponde al vínculo simbólico especificado de la interfaz **KSCATEGORY_VIDEO_CAMERA** de la cámara.  |
| [**Contabiliza**](imsrdpcameraredirconfigcollection-count.md)                       | Solo lectura |    Devuelve el número de objetos [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección.   |
| [**EncodeVideo**](imsrdpcameraredirconfigcollection-encodevideo.md)      | Lectura/Escritura |  Especifica si la secuencia de vídeo es H. 264 codificada.  |
| [**EncodingQuality**](imsrdpcameraredirconfigcollection-encodingquality.md)                       | Lectura/Escritura |    Especifica la calidad de codificación (velocidad de bits).   |
| [**RedirectByDefault**](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | Lectura/Escritura |   Especifica si cualquier cámara nueva se redirige de forma predeterminada.    |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection se define como AE45252B-AAAB-4504-B681-649D6073A37A            |

## <a name="see-also"></a>Vea también

- [**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
- [**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
