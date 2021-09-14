---
description: Especifica el número máximo de objetos de audio dinámicos que el punto de conexión de audio puede representar de forma simulada.
ms.assetid: 6B6D73C1-C2E6-4C23-BBAD-7B51E8441C71
title: MF_MT_SPATIAL_AUDIO_MAX_DYNAMIC_OBJECTS atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358045079fb9cf52ad1fd0c8969f54723c7f02d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363954"
---
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a>Atributo MF \_ MT SPATIAL AUDIO MAX DYNAMIC \_ \_ \_ \_ \_ OBJECTS

Especifica el número máximo de objetos de audio dinámicos que el punto de conexión de audio puede representar de forma simulada.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

UN VALOR DE LA CLASE [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) puede contener menos muestras que el número especificado por este atributo. Si un ejemplo contiene más objetos de audio de los especificados por este atributo, el comportamiento es indefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1703 \[ solo para aplicaciones de escritorio\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




