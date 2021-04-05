---
title: Constantes de WINBIO_PRESENCE_CHANGE (Winbio \_ Types. h)
description: Describe los tipos de cambios que se pueden producir cuando el Plataforma de biometría de Windows supervisa la presencia de individuos.
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
ms.openlocfilehash: c2c864c82ddca6faec134716778dc2e795675371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078972"
---
# <a name="winbio_presence_change-constants"></a>WINBIO \_ constantes de cambio de presencia \_

Describe los tipos de cambios que se pueden producir cuando el Plataforma de biometría de Windows supervisa la presencia de individuos.



| Constante o valor                                                                                                                                                                                                                                                                                      | Descripción                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <dt>**WINBIO \_ Tipo de cambio de presencia \_ \_ \_ desconocido**</dt> <dt>0</dt> </dl>           | Se desconoce el tipo de evento. Este valor se usa para la estructura sin inicializar.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <dt>**WINBIO \_ Tipo de cambio de presencia \_ \_ \_ actualizar \_ todo**</dt> <dt>1</dt> </dl> | Proporciona información sobre todas las caras actuales en el fotograma de la cámara.<br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <dt>**WINBIO \_ \_Llegada del \_ tipo \_ de cambio de presencia**</dt> <dt>2</dt> </dl>              | Una nueva esfera entró en el marco de la cámara.<br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <dt>**WINBIO \_ Tipo de cambio de presencia \_ \_ \_ Recognize**</dt> <dt>3</dt> </dl>     | Una esfera coincidía con un usuario inscrito.<br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <dt>**WINBIO \_ Tipo de cambio de presencia en la \_ \_ \_ parte**</dt> <dt>4</dt> </dl>              | Una de las caras detectadas con anterioridad está fuera del marco de la cámara durante un período de tiempo.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <dt>**WINBIO \_ \_Seguimiento de \_ tipo \_ de cambio de presencia**</dt> <dt>5</dt> </dl>                 | Proporciona información sobre las actualizaciones del cuadro de límite y los valores de rechazo de un subconjunto de las caras que están actualmente en el marco de la cámara.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt> </dl> |



 

 





