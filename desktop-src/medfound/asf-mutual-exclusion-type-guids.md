---
description: Los siguientes GUID definen los tipos para el objeto de exclusión mutua de las secuencias de formato ASF (Advanced Systems Format).
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: GUID de tipo de exclusión mutua de ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a6fedc766e26c35bb967054a704b732ca03e8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275151"
---
# <a name="asf-mutual-exclusion-type-guids"></a>GUID de tipo de exclusión mutua de ASF

Los siguientes GUID definen los tipos para el objeto de exclusión mutua de las secuencias de formato ASF (Advanced Systems Format).



| Constante                                                                                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <dt>**\_Lenguaje MFASFMutexType**</dt> </dl>                 | Los flujos se excluyen mutuamente por lenguaje. Este tipo de exclusión mutua es similar a las pistas de audio en un DVD.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <dt>**\_Velocidad de bits MFASFMutexType**</dt> </dl>                     | Las secuencias se excluyen mutuamente a través de la velocidad de bits. Este tipo de exclusión mutua también se denomina exclusión de velocidad de bits múltiple (MBR).<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <dt>**Presentación de MFASFMutexType \_**</dt> </dl> | Los flujos se excluyen mutuamente mediante presentación. Este tipo se puede usar para muchos escenarios, pero solo se debe usar cuando el contenido es el mismo pero tiene un formato diferente. Por ejemplo, dos flujos que contienen el mismo vídeo, uno formateado para rellenar la pantalla y el otro que mantiene la relación de aspecto de pantalla panorámica original, se deben hacer mutuamente excluyentes mediante este tipo. Otro ejemplo son las secuencias que contienen vídeo de la misma escena capturados de distintos ángulos.<br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <dt>**MFASFMutexType \_ desconocido**</dt> </dl>                     | Las secuencias se excluyen mutuamente en función de criterios personalizados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFASFMutualExclusion:: GetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[**IMFASFMutualExclusion::SetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[Constantes de Media Foundation](media-foundation-constants.md)
</dt> </dl>

 

 




