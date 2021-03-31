---
description: Valor que especifica el tamaño, en bytes, del tipo de objeto de metadatos de audio espacial que el descodificador generará.
ms.assetid: C133693D-A8D5-4520-B561-57BF11074257
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_LENGTH atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2cd0b3cab788dbc724ab896d2cbfeb0d42f633f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277077"
---
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a>\_Atributo de \_ \_ longitud de \_ metadatos de objetos de audio espacial \_ MF MT \_

Valor que especifica el tamaño, en bytes, del tipo de objeto de metadatos de audio espacial que el descodificador generará.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El BLOB de metadatos con el formato especificado se escribe mediante la interfaz [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) y se lee mediante la interfaz [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) . El BLOB de metadatos es opaco para la canalización Media Foundation y los componentes. El atributo se aplica al tipo de medio de audio espacial.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
