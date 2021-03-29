---
description: El descodificador de vídeo DV Media Foundation es una transformación Media Foundation que descodifica vídeo DV.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: Descodificador de vídeo DV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808095"
---
# <a name="dv-video-decoder"></a>Descodificador de vídeo DV

El descodificador de vídeo DV Media Foundation es una [transformación Media Foundation](media-foundation-transforms.md) que DESCODIFICA vídeo DV.

El descodificador de vídeo DV admite los siguientes tipos de entrada:



| Subtype                 | Descripción                  |
|-------------------------|------------------------------|
| **MFVideoFormat \_ DVC**  | Vídeo de DVC/DV                 |
| **MFVideoFormat \_ DVHD** | HD-DVCR (1125-60 o 1250-50) |
| **MFVideoFormat \_ DVSD** | SDL-DVCR (525-60 o 625-50)  |
| **MFVideoFormat \_ DVSL** | SD-DVCR (525-60 o 625-50)   |



 

Admite un solo tipo de salida:



| Subtype             | Descripción |
|---------------------|-------------|
| MFVideoFormat \_ YUY2 | Vídeo de YUY2  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                |
| Archivo DLL<br/>                      | <dl> <dt>Mfdvdec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> </dl>

 

 




