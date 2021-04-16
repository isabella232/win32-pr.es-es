---
description: Las \_ constantes de audio espacial \_ XXX definen valores relacionados con las características de sonido espacial.
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: Constantes de SPATIAL_AUDIO_XXX (SpatialAudioMetadata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2c92b970f69cf84e0744f21a41932a8851efed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650021"
---
# <a name="spatial_audio_xxx-constants"></a>\_Constantes de audio espacial \_ XXX

Las \_ constantes de audio espacial \_ XXX definen valores relacionados con las características de sonido espacial.



| Constante o valor                                                                                                                                                                                                                                                                                       | Descripción                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <dt>**Espacial \_ \_Posición de AUDIO**</dt> <dt>200</dt> </dl>                                                   | Un comando estándar de metadatos de audio espacial definido por Microsoft que representa la posición del agente de escucha en el modelo estándar usado por [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) , donde el encabezado del agente de escucha se coloca en las coordenadas (0,0), definido en metros.<br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <dt>**Espacial \_ \_ \_ \_ Número de bytes de posición de audio**</dt> <dt>sizeof (float) \* 3</dt> </dl> | Especifica el tamaño del valor **de \_ \_ posición de audio espacial** .<br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <dt>**Espacial \_ \_Comandos estándar de audio \_ \_ Start**</dt> <dt>200</dt> </dl>    | Especifica el inicio del intervalo de comandos de metadatos de audio espaciales reservados de Microsoft. Los comandos de metadatos personalizados están restringidos a los identificadores de comando 0-199. Los comandos 200-255 están reservados para su uso por Microsoft.<br/>                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>SpatialAudioMetadata. h</dt> </dl> |



 

 




