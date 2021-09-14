---
description: Las constantes XXX \_ de AUDIO ESPACIAL definen valores relacionados con las características de sonido \_ espacial.
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: SPATIAL_AUDIO_XXX constantes (SpatialAudioMetadata.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2c92b970f69cf84e0744f21a41932a8851efed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164814"
---
# <a name="spatial_audio_xxx-constants"></a>Constantes \_ \_ XXX de AUDIO ESPACIAL

Las constantes XXX \_ de AUDIO ESPACIAL definen valores relacionados con las características de sonido \_ espacial.



| Constante o valor                                                                                                                                                                                                                                                                                       | Descripción                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <dt>**SPATIAL \_ AUDIO \_ POSITION**</dt> <dt>200</dt> </dl>                                                   | Un comando estándar de metadatos de audio espacial definido por Microsoft que representa la posición del agente de escucha en el modelo estándar utilizado por [**ISpatialAudioClient,**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) donde la cabeza del agente de escucha se coloca en coordenadas (0,0,0), definidas en metros.<br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <dt>**SPATIAL \_ AUDIO \_ POSITION \_ BYTE \_ COUNT**</dt> <dt>sizeof(float) \* 3</dt> </dl> | Especifica el tamaño del valor **SPATIAL \_ AUDIO \_ POSITION.**<br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <dt>**SPATIAL \_ COMANDOS ESTÁNDAR DE AUDIO \_ \_ \_ START**</dt> <dt>200</dt> </dl>    | Especifica el inicio del intervalo de comandos de metadatos de audio espacial reservados por Microsoft. Los comandos de metadatos personalizados están restringidos a los IDs de comando 0 a 199. Los comandos 200 a 255 están reservados para uso de Microsoft.<br/>                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>SpatialAudioMetadata.h</dt> </dl> |



 

 




