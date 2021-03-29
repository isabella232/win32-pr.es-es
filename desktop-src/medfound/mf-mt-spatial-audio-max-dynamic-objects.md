---
description: Especifica el número máximo de objetos de audio dinámicos que se pueden representar mediante el punto de conexión de audio simulataneously.
ms.assetid: 6B6D73C1-C2E6-4C23-BBAD-7B51E8441C71
title: MF_MT_SPATIAL_AUDIO_MAX_DYNAMIC_OBJECTS atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358045079fb9cf52ad1fd0c8969f54723c7f02d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648418"
---
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a>\_Atributo de \_ \_ \_ \_ objetos dinámicos Max MT Spatial audio \_

Especifica el número máximo de objetos de audio dinámicos que se pueden representar mediante el punto de conexión de audio simulataneously.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Un [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) puede contener menos muestras que el número especificado por este atributo. Si un ejemplo contiene más objetos de audio de los especificados por este atributo, el comportamiento es indefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




