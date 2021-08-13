---
title: WINBIO_PRESENCE_CHANGE constantes (Winbio \_ types.h)
description: Describe los tipos de cambios que pueden producirse cuando el Windows Biometric Framework supervisa la presencia de individuos.
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08cce9cc74bafdba6cf8d1aa11abccdaf7315370223ff6edf47eaba167af84f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909730"
---
# <a name="winbio_presence_change-constants"></a>Constantes \_ DE CAMBIO DE PRESENCIA DE WINBIO \_

Describe los tipos de cambios que pueden producirse cuando el Windows Biometric Framework supervisa la presencia de individuos.



| Constante o valor                                                                                                                                                                                                                                                                                      | Descripción                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <dt>**WINBIO \_ PRESENCE \_ CHANGE \_ TYPE \_ UNKNOWN**</dt> <dt>0</dt> </dl>           | El tipo de evento es desconocido. Este valor se usa para la estructura sin inicializar.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <dt>**WINBIO \_ PRESENCE \_ CHANGE TYPE UPDATE \_ \_ \_ ALL**</dt> <dt>1</dt> </dl> | Proporciona información sobre todas las caras actuales en el marco de la cámara.<br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <dt>**WINBIO \_ TIPO \_ DE CAMBIO DE PRESENCIA \_ \_ ARRIVE**</dt> <dt>2</dt> </dl>              | Una nueva cara entró en el marco de la cámara.<br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <dt>**WINBIO \_ RECONOCIMIENTO \_ DE TIPO DE CAMBIO DE \_ \_ PRESENCIA**</dt> <dt>3</dt> </dl>     | Una cara coincidía con un usuario inscrito.<br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <dt>**WINBIO \_ PRESENCE \_ CHANGE \_ TYPE \_ DEPART**</dt> <dt>4</dt> </dl>              | Una cara detectada previamente ha estado fuera del marco de la cámara durante un período de tiempo.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <dt>**WINBIO \_ PRESENCE \_ CHANGE \_ TYPE \_ TRACK**</dt> <dt>5</dt> </dl>                 | Proporciona información de actualizaciones sobre el cuadro de límite y rechaza los valores de detalle de un subconjunto de las caras que se encuentran actualmente en el marco de la cámara.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluye Winbio.h para aplicaciones cliente o Adaptadores de \_ Winbio.h para adaptadores)</dt> </dl> |



 

 





