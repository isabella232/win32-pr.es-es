---
title: WINBIO_IRIS constantes (Winbio \_ types.h)
description: Especifique los tipos para el reconocimiento de iris.
ms.assetid: B1A594E3-6DEA-4071-B40F-569B8094E801
topic_type:
- apiref
api_name:
- WINBIO_IRIS_TYPE_UNKNOWN
- WINBIO_IRIS_LEFT_EYE
- WINBIO_IRIS_RIGHT_EYE
- WINBIO_IRIS_UNSPECIFIED_POS_01
- WINBIO_IRIS_UNSPECIFIED_POS_02
- WINBIO_IRIS_BOTH_EYES
- WINBIO_IRIS_EITHER_EYE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61e65505b8ef55b0fdc2dc9d8f5312e24856602
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476526"
---
# <a name="winbio_iris-constants"></a>Constantes DE IRIS DE WINBIO \_

Las siguientes constantes son valores **\_ DE \_ SUBTYPE BIOMETRIC** de WINBIO que se pueden usar para especificar los tipos para el reconocimiento de iris más allá de ANSI INCITS 379-2004: "Formato de intercambio de imágenes iris", que no define ningún valor de ojo izquierdo o derecho:



| Constante o valor                                                                                                                                                                                                                                                                   | Descripción                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <dt> **WINBIO \_ IRIS \_ TYPE \_ UNKNOWN**</dt> <dt>0</dt> </dl>                       | El tipo de iris es desconocido. <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <dt> **WINBIO \_ IRIS \_ LEFT \_ EYE**</dt> <dt>0xF5</dt> </dl>                               | El tipo de iris es el ojo izquierdo. <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <dt> **WINBIO \_ IRIS \_ RIGHT \_ EYE**</dt> <dt>0xF6</dt> </dl>                            | El tipo de iris es el ojo derecho. <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <dt>**WINBIO \_ IRIS \_ UNSPECIFIED \_ POS \_ 01**</dt> <dt>0xF7</dt> </dl>    | Subtipo asociado a la primera plantilla de un usuario cuando solo un ojo es el marco de la cámara y no se puede determinar si es el ojo izquierdo o derecho del usuario.<br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <dt> **WINBIO \_ IRIS \_ UNSPECIFIED \_ POS \_ 02**</dt> <dt>0xF8</dt> </dl> | Subtipo asociado a la segunda plantilla de un usuario cuando solo un ojo es el marco de la cámara y no se puede determinar si es el ojo izquierdo o derecho del usuario.<br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <dt> **WINBIO \_ IRIS \_ BOTH \_ EYES**</dt> <dt>0xF9</dt> </dl>                             | El tipo de iris son ambos ojos. <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <dt> **WINBIO \_ IRIS \_ EITHER \_ EYE**</dt> <dt>0xFA</dt> </dl>                          | El tipo de iris es cualquier ojo. <br/>                                                                                                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



 

 





