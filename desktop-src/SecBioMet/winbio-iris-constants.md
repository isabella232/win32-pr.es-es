---
title: Constantes de WINBIO_IRIS (Winbio \_ Types. h)
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491381"
---
# <a name="winbio_iris-constants"></a>WINBIO ( \_ constantes de iris)

Las siguientes constantes son valores **de \_ \_ subtipo biométrico WINBIO** que se pueden usar para especificar los tipos para el reconocimiento de iris más allá de ANSI INCITS 379-2004: "formato de intercambio de imagen de iris", que no define ningún valor de ojo izquierdo/derecho:



| Constante o valor                                                                                                                                                                                                                                                                   | Descripción                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <dt> **Tipo de iris de WINBIO \_ \_ \_ desconocido**</dt> <dt>0</dt> </dl>                       | No se conoce el tipo de iris. <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <dt> **WINBIO \_ de \_ \_ ojo izquierdo de iris**</dt> <dt>0xF5</dt> </dl>                               | El tipo de iris es el ojo izquierdo. <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <dt> **WINBIO \_ iris \_ derecha \_**</dt> <dt>0xF6</dt> </dl>                            | El tipo de iris es el ojo adecuado. <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <dt>**WINBIO \_ No se \_ especificó el \_ PDV \_ 01**</dt> <dt>0xF7</dt> de iris </dl>    | El subtipo asociado a una primera plantilla de usuario cuando solo hay un ojo es el fotograma de la cámara y no se puede determinar si es el usuario que se encuentra a la izquierda o a la derecha.<br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <dt> **WINBIO de \_ iris no especificado de iris \_ \_ \_ 02**</dt> <dt>0xF8</dt> </dl> | Subtipo asociado a una segunda plantilla de usuario cuando solo un ojo es el fotograma de la cámara y no se puede determinar si es el usuario que se encuentra en la parte izquierda o derecha.<br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <dt> **WINBIO \_ iris \_ ambos \_ ojos**</dt> <dt>0xF9</dt> </dl>                             | El tipo de iris es ambos ojos. <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <dt> **WINBIO \_ iris \_ \_**</dt> <dt>0xFA</dt> </dl>                          | El tipo de iris está bien. <br/>                                                                                                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



 

 





