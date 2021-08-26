---
description: GUID definido por descodificador que identifica el formato de metadatos de audio espacial, notificando a los componentes de nivel inferior del tipo de objeto de metadatos que el descodificador va a generar.
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b43751655f2a583d50c8de3fe108babcaa08d11d78df552b6ddf1f10e413be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955505"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a>Atributo MF \_ MT SPATIAL AUDIO OBJECT METADATA FORMAT \_ \_ \_ \_ \_ \_ ID

GUID definido por descodificador que identifica el formato de metadatos de audio espacial, notificando a los componentes de nivel inferior del tipo de objeto de metadatos que el descodificador va a generar.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Comentarios

El blob de metadatos con el formato especificado se escribe mediante la interfaz [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) y se lee mediante la [**interfaz ISpatialAudioMetadataReader.**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) El blob de metadatos es opaco para la Media Foundation y los componentes. El atributo se aplica al tipo de medio de audio espacial. Si un componente de nivel inferior no admite el formato de metadatos especificado por el GUID, el componente debe rechazar el tipo de medio de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
