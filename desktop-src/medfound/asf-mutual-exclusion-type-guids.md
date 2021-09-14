---
description: Los siguientes GUID definen los tipos para el objeto de exclusión mutua para secuencias de formato de sistemas avanzados (ASF).
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: GUID de tipo de exclusión mutua de ASF (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a6fedc766e26c35bb967054a704b732ca03e8a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361189"
---
# <a name="asf-mutual-exclusion-type-guids"></a>GUID de tipo de exclusión mutua de ASF

Los siguientes GUID definen los tipos para el objeto de exclusión mutua para secuencias de formato de sistemas avanzados (ASF).



| Constante                                                                                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <dt>**Lenguaje MFASFMutexType \_**</dt> </dl>                 | Las secuencias se excluyen mutuamente por lenguaje. Este tipo de exclusión mutua es similar a las pistas de audio de un DVD.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <dt>**Velocidad de bits MFASFMutexType \_**</dt> </dl>                     | Las secuencias se excluyen mutuamente por velocidad de bits. Este tipo de exclusión mutua también se denomina exclusión de velocidad de bits múltiple (MBR).<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <dt>**Presentación de MFASFMutexType \_**</dt> </dl> | Las secuencias son mutuamente excluyentes por presentación. Este tipo se puede usar en muchos escenarios, pero solo se debe usar cuando el contenido es el mismo, pero tiene una forma diferente. Por ejemplo, dos secuencias que contienen el mismo vídeo, una con formato para rellenar la pantalla y la otra que mantiene la relación de aspecto de pantalla ancha original, se deben hacer mutuamente excluyentes mediante este tipo. Otro ejemplo son las secuencias que contienen vídeo de la misma escena que se toma desde distintos ángulos.<br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <dt>**MFASFMutexType \_ Unknown**</dt> </dl>                     | Las secuencias se excluyen mutuamente en función de criterios personalizados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMFASFMutualExclusion::GetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[**IMFASFMutualExclusion::SetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[Media Foundation constantes](media-foundation-constants.md)
</dt> </dl>

 

 




