---
description: GUID definido por el descodificador que identifica el formato de metadatos de audio espacial, y notifica a los componentes de nivel inferior del tipo de objeto de metadatos que el descodificador generará.
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed16188a24b4c61facf1e325867d093b9b5cc869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277078"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a>\_Atributo de \_ \_ identificador de \_ \_ formato de metadatos del objeto de audio \_ espacial \_ MF MT

GUID definido por el descodificador que identifica el formato de metadatos de audio espacial, y notifica a los componentes de nivel inferior del tipo de objeto de metadatos que el descodificador generará.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Observaciones

El BLOB de metadatos con el formato especificado se escribe mediante la interfaz [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) y se lee mediante la interfaz [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) . El BLOB de metadatos es opaco para la canalización Media Foundation y los componentes. El atributo se aplica al tipo de medio de audio espacial. Si un componente de nivel inferior no admite el formato de metadatos especificado por el GUID, el componente debe rechazar el tipo de medio de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
