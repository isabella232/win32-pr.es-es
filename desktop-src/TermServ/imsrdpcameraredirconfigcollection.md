---
title: Interfaz IMsRdpCameraRedirConfigCollection
description: Representa la colección de cámaras (y las configuraciones asociadas) que están disponibles para el redireccionamiento.
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpCameraRedirConfigCollection Servicios de Escritorio remoto
- Interfaz IMsRdpCameraRedirConfigCollection Servicios de Escritorio remoto , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965339"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a>Interfaz IMsRdpCameraRedirConfigCollection

 Representa la colección de cámaras (y las configuraciones asociadas) que están disponibles para el redireccionamiento.

## <a name="members"></a>Members

La **interfaz IMsRdpCameraRedirConfigCollection** hereda de **IUnknown.** **IMsRdpCameraRedirConfigCollection** también tiene estos tipos de miembros:

- [Métodos](#methods)
- [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IMsRdpCameraRedirConfigCollection** tiene estos métodos.

| Método            | Descripción              |
|:------------------|:-------------------------|
| [**AddConfig**](imsrdpcameraredirconfigcollection-addconfig.md)       |  Agrega un [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) a la colección (no es necesario conectar la cámara correspondiente).                   |
| [**Reescaneo**](imsrdpcameraredirconfigcollection-rescan.md)       |  Enumera los dispositivos de cámara conectados.                   |

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpCameraRedirConfigCollection** tiene estas propiedades.

| Propiedad         | Tipo de acceso           | Descripción            |
|:-----------------|:----------------------|:-----------------------|
| [**ByIndex**](imsrdpcameraredirconfigcollection-byindex.md)      | Solo lectura |  Devuelve un [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) por su índice en la colección.   |
| [**ByInstanceId**](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | Solo lectura |    Devuelve un [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección que corresponde al identificador de instancia especificado.    |
| [**BySymbolicLink**](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | Solo lectura |  Devuelve un [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección que corresponde al vínculo simbólico dado de la **interfaz** KSCATEGORY_VIDEO_CAMERA para la cámara.  |
| [**Count**](imsrdpcameraredirconfigcollection-count.md)                       | Solo lectura |    Devuelve el número de [objetos IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección.   |
| [**CodificaciónVideo**](imsrdpcameraredirconfigcollection-encodevideo.md)      | Lectura/Escritura |  Especifica si la secuencia de vídeo está codificada en H.264 o no.  |
| [**EncodingQuality**](imsrdpcameraredirconfigcollection-encodingquality.md)                       | Lectura/Escritura |    Especifica la calidad de codificación (velocidad de bits).   |
| [**RedirectByDefault**](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | Lectura/Escritura |   Especifica si cualquier cámara nueva se redirige de forma predeterminada.    |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------|
| Cliente mínimo compatible| Windows 10, versión 1803 (compilación 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| Archivo DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection se define como AE45252B-AAAB-4504-B681-649D6073A37A            |

## <a name="see-also"></a>Consulte también

- [**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
- [**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
