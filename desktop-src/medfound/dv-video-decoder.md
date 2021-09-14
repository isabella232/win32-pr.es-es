---
description: El Media Foundation de vídeo DV es un Media Foundation Transform que descodifica vídeo DV.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: Descodificador de vídeo DV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248547"
---
# <a name="dv-video-decoder"></a>Descodificador de vídeo DV

El Media Foundation de vídeo DV es [un Media Foundation Transform que](media-foundation-transforms.md) descodifica vídeo DV.

El descodificador de vídeo DV admite los siguientes tipos de entrada:



| Subtype                 | Descripción                  |
|-------------------------|------------------------------|
| **MFVideoFormat \_ DVC**  | Vídeo DVC/DV                 |
| **MFVideoFormat \_ DVHD** | HD-DVCR (1125-60 o 1250-50) |
| **MFVideoFormat \_ DVSD** | SDL-DVCR (525-60 o 625-50)  |
| **MFVideoFormat \_ DVSL** | SD-DVCR (525-60 o 625-50)   |



 

Admite un único tipo de salida:



| Subtype             | Descripción |
|---------------------|-------------|
| MFVideoFormat \_ YUY2 | Vídeo de YUY2  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Archivo DLL<br/>                      | <dl> <dt>Mfdvdec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> </dl>

 

 




