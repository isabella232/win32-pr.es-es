---
title: WINBIO_REJECT_DETAIL constantes (Winbio \_ types.h)
description: Especifique el motivo por el que un procedimiento de identificación o captura biométrica de huellas digitales no se ha hecho correctamente.
ms.assetid: b1ae4e65-9e53-42dd-99ba-1910b72688dd
topic_type:
- apiref
api_name:
- WINBIO_FP_TOO_HIGH
- WINBIO_FP_TOO_LOW
- WINBIO_FP_TOO_LEFT
- WINBIO_FP_TOO_RIGHT
- WINBIO_FP_TOO_FAST
- WINBIO_FP_TOO_SLOW
- WINBIO_FP_POOR_QUALITY
- WINBIO_FP_TOO_SKEWED
- WINBIO_FP_TOO_SHORT
- WINBIO_FP_MERGE_FAILURE
- WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK
- WINBIO_REJECT_DETAIL_POSITION_MASK
- WINBIO_REJECT_DETAIL_REASON_MASK
- WINBIO_IRIS_POOR_QUALITY
- WINBIO_IRIS_TOO_BRIGHT
- WINBIO_IRIS_TOO_DARK
- WINBIO_IRIS_SPOOF_DETECTED
- WINBIO_IRIS_TOO_SKEWED
- WINBIO_IRIS_TOO_CLOSED
- WINBIO_IRIS_GLARE
- WINBIO_IRIS_DIRTY_LENS
- WINBIO_IRIS_POOR_FOCUS
- WINBIO_IRIS_WRONG_ORIENTATION
- WINBIO_IRIS_TOO_HIGH
- WINBIO_IRIS_TOO_LOW
- WINBIO_IRIS_TOO_LEFT
- WINBIO_IRIS_TOO_RIGHT
- WINBIO_IRIS_TOO_NEAR
- WINBIO_IRIS_TOO_FAR
- WINBIO_FACE_POOR_QUALITY
- WINBIO_FACE_TOO_BRIGHT
- WINBIO_FACE_TOO_DARK
- WINBIO_FACE_SPOOF_DETECTED
- WINBIO_FACE_AMBIGUOUS_TARGET
- WINBIO_FACE_EYES_OCCLUDED
- WINBIO_FACE_WRONG_ORIENTATION
- WINBIO_FACE_TOO_HIGH
- WINBIO_FACE_TOO_LOW
- WINBIO_FACE_TOO_LEFT
- WINBIO_FACE_TOO_RIGHT
- WINBIO_FACE_TOO_NEAR
- WINBIO_FACE_TOO_FAR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad5ac7a2f96555aa8ccfb305c66061ba4e0ffd468f18a1a93be215c367f034be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909353"
---
# <a name="winbio_reject_detail-constants"></a>Constantes DE \_ DETALLES DE WINBIO REJECT \_

Las siguientes constantes se pueden usar para especificar el motivo por el que un procedimiento biométrico de identificación o captura de huellas digitales no se ha hecho correctamente.



| Constante                                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FP_TOO_HIGH"></span><span id="winbio_fp_too_high"></span><dl> <dt>**WINBIO \_ FP \_ TOO \_ HIGH**</dt> </dl>                                                                  | El examen del dedo comenzó demasiado alto en el dedo.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_LOW"></span><span id="winbio_fp_too_low"></span><dl> <dt>**WINBIO \_ FP \_ TOO \_ LOW**</dt> </dl>                                                                     | El examen del dedo comenzó demasiado bajo en el dedo.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_LEFT"></span><span id="winbio_fp_too_left"></span><dl> <dt>**WINBIO \_ FP \_ TOO \_ LEFT**</dt> </dl>                                                                  | El dedo estaba demasiado lejos a la izquierda durante el examen.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_RIGHT"></span><span id="winbio_fp_too_right"></span><dl> <dt>**WINBIO \_ FP \_ TOO \_ RIGHT**</dt> </dl>                                                               | El dedo estaba demasiado a la derecha durante el examen.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_FAST"></span><span id="winbio_fp_too_fast"></span><dl> <dt>**WINBIO \_ FP \_ TOO \_ FAST**</dt> </dl>                                                                  | El dedo se ha deslizado demasiado rápidamente en el sensor.<br/>                                                                                                                                                                                                                                       |
| <span id="WINBIO_FP_TOO_SLOW"></span><span id="winbio_fp_too_slow"></span><dl> <dt>**WINBIO \_ FP \_ DEMASIADO \_ LENTO**</dt> </dl>                                                                  | El dedo se deslizaba demasiado lentamente en el sensor.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_FP_POOR_QUALITY"></span><span id="winbio_fp_poor_quality"></span><dl> <dt>**WINBIO \_ FP DE BAJA \_ \_ CALIDAD**</dt> </dl>                                                      | La calidad del examen era demasiado baja.<br/>                                                                                                                                                                                                                                                         |
| <span id="WINBIO_FP_TOO_SKEWED"></span><span id="winbio_fp_too_skewed"></span><dl> <dt>**WINBIO \_ FP \_ DEMASIADO \_ SESGADO**</dt> </dl>                                                            | El dedo no pasó directamente por el sensor.<br/>                                                                                                                                                                                                                                    |
| <span id="WINBIO_FP_TOO_SHORT"></span><span id="winbio_fp_too_short"></span><dl> <dt>**WINBIO \_ FP \_ TOO \_ SHORT**</dt> </dl>                                                               | No se ha examinado suficiente parte del dedo.<br/>                                                                                                                                                                                                                                                  |
| <span id="WINBIO_FP_MERGE_FAILURE"></span><span id="winbio_fp_merge_failure"></span><dl> <dt>**ERROR DE COMBINACIÓN \_ DE FP \_ DE \_ WINBIO**</dt> </dl>                                                   | No se pudieron combinar las capturas de huellas digitales.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK____"></span><span id="winbio_reject_detail_anti_spoof_mask____"></span><dl> <dt>**WINBIO \_ RECHAZAR \_ MÁSCARA \_ ANTI \_ SUPLANTACIÓN DE \_ DETALLES**</dt> </dl> | Esta máscara cubre los 8 bits superiores del valor de detalle de rechazo donde se encuentran los comportamientos de prueba de vida. Este valor se admite a partir de Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_POSITION_MASK______"></span><span id="winbio_reject_detail_position_mask______"></span><dl> <dt>**WINBIO \_ RECHAZAR MÁSCARA \_ DE \_ POSICIÓN DE \_ DETALLE**</dt> </dl>    | Esta máscara cubre el intervalo de bits dedicados a los errores de posición. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                                         |
| <span id="WINBIO_REJECT_DETAIL_REASON_MASK"></span><span id="winbio_reject_detail_reason_mask"></span><dl> <dt>**MÁSCARA DE MOTIVO DE DETALLE DE RECHAZO DE WINBIO \_ \_ \_ \_**</dt> </dl>                       | Esta máscara cubre los 16 bits inferiores donde se encuentra el motivo enumerado del rechazo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                           |
| <span id="WINBIO_IRIS_POOR_QUALITY"></span><span id="winbio_iris_poor_quality"></span><dl> <dt>**WINBIO \_ IRIS DE BAJA \_ \_ CALIDAD**</dt> </dl>                                                | Las condiciones provocaron que la cámara capturara una imagen deficiente. Indique al usuario que limpie el sensor y vuelva a examinarlo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_IRIS_TOO_BRIGHT"></span><span id="winbio_iris_too_bright"></span><dl> <dt>**WINBIO \_ IRIS \_ TOO \_ BRIGHT**</dt> </dl>                                                      | La imagen incluye demasiada luz ambiental para obtener una buena coincidencia. Indique al usuario que se asegure de que no tiene otra fuente de luz brillante. Este valor se admite a partir de Windows 10.<br/>                                                                                        |
| <span id="WINBIO_IRIS_TOO_DARK"></span><span id="winbio_iris_too_dark"></span><dl> <dt>**WINBIO \_ IRIS \_ TOO \_ DARK**</dt> </dl>                                                            | La imagen es demasiado oscura para obtener una buena coincidencia. Indique al usuario que asegúrese de que los elementos como un veil, gafas oscuras o contactos coloreados no ocultan su iris. Este valor se admite a partir de Windows 10.<br/>                                                                     |
| <span id="WINBIO_IRIS_SPOOF_DETECTED"></span><span id="winbio_iris_spoof_detected"></span><dl> <dt>**SE \_ DETECTÓ \_ UNA SUPLANTACIÓN DE IRIS DE \_ WINBIO**</dt> </dl>                                          | El componente de reconocimiento cree que el iris no está activo, pero que viene de una fuente de vídeo reproducida, una foto o un 3D. Este valor se admite a partir de Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_IRIS_TOO_SKEWED"></span><span id="winbio_iris_too_skewed"></span><dl> <dt>**WINBIO \_ IRIS \_ DEMASIADO \_ SESGADO**</dt> </dl>                                                      | El usuario no está mirando directamente a la cámara. Indique al usuario que mire directamente a la cámara y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                       |
| <span id="WINBIO_IRIS_TOO_CLOSED"></span><span id="winbio_iris_too_closed"></span><dl> <dt>**WINBIO \_ IRIS \_ TOO \_ CLOSED**</dt> </dl>                                                      | Los gestos del usuario ocultan el iris. Indique al usuario que abra los ojos un poco más y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                          |
| <span id="WINBIO_IRIS_GLARE"></span><span id="winbio_iris_glare"></span><dl> <dt>**WINBIO \_ IRIS \_ GLARE**</dt> </dl>                                                                      | La imagen incluye el reflejo de la lente. Indique al usuario que quite las gafas y vuelva a examinarla. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                               |
| <span id="WINBIO_IRIS_DIRTY_LENS"></span><span id="winbio_iris_dirty_lens"></span><dl> <dt>**WINBIO \_ IRIS \_ DIRTY \_ LENS**</dt> </dl>                                                      | La lente de la cámara estaba desnuciado. Indique al usuario que limpie la lente y vuelva a examinarla. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                         |
| <span id="WINBIO_IRIS_POOR_FOCUS"></span><span id="winbio_iris_poor_focus"></span><dl> <dt>**ENFOQUE DEFICIENTE DE WINBIO \_ IRIS \_ \_**</dt> </dl>                                                      | Este iris está fuera de foco. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                                                                             |
| <span id="WINBIO_IRIS_WRONG_ORIENTATION"></span><span id="winbio_iris_wrong_orientation"></span><dl> <dt>**ORIENTACIÓN INCORRECTA \_ DE WINBIO IRIS \_ \_**</dt> </dl>                                 | La orientación de la cámara no coincide con la orientación obligatoria que especifica la [**estructura WINBIO \_ EXTENDED SENSOR \_ \_ INFO.**](winbio-extended-sensor-info.md) Indique al usuario que cambie la orientación de la cámara y vuelva a examinarla. Este valor se admite a partir de Windows 10.<br/> |
| <span id="WINBIO_IRIS_TOO_HIGH"></span><span id="winbio_iris_too_high"></span><dl> <dt>**WINBIO \_ IRIS \_ TOO \_ HIGH**</dt> </dl>                                                            | El iris está orientado hacia arriba. Indique al usuario que mire un poco hacia abajo y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LOW"></span><span id="winbio_iris_too_low"></span><dl> <dt>**WINBIO \_ IRIS \_ TOO \_ LOW**</dt> </dl>                                                               | El iris está orientado hacia abajo. Indique al usuario que busque un poco y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LEFT"></span><span id="winbio_iris_too_left"></span><dl> <dt>**WINBIO \_ IRIS \_ TOO \_ LEFT**</dt> </dl>                                                            | El iris está demasiado lejos a la izquierda. Indique al usuario que mire un poco más a la derecha y que vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_RIGHT"></span><span id="winbio_iris_too_right"></span><dl> <dt>**WINBIO \_ IRIS \_ TOO \_ RIGHT**</dt> </dl>                                                         | El iris está demasiado lejos a la derecha. Indique al usuario que mire un poco más a la izquierda y que vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_NEAR"></span><span id="winbio_iris_too_near"></span><dl> <dt>**WINBIO \_ IRIS \_ TOO \_ NEAR**</dt> </dl>                                                            | El iris está demasiado cerca de la cámara. Indique al usuario que se mueva un poco más lejos y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_IRIS_TOO_FAR"></span><span id="winbio_iris_too_far"></span><dl> <dt>**WINBIO \_ IRIS \_ TOO \_ FAR**</dt> </dl>                                                               | El iris está demasiado lejos de la cámara. Indique al usuario que se acerque un poco y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                         |
| <span id="WINBIO_FACE_POOR_QUALITY"></span><span id="winbio_face_poor_quality"></span><dl> <dt>**WINBIO \_ FACE \_ POOR \_ QUALITY**</dt> </dl>                                                | Las condiciones provocaron que la cámara capturara una imagen deficiente. Indique al usuario que limpie el sensor y vuelva a examinarlo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_FACE_TOO_BRIGHT"></span><span id="winbio_face_too_bright"></span><dl> <dt>**WINBIO \_ FACE \_ TOO \_ BRIGHT**</dt> </dl>                                                      | La imagen incluye demasiada luz ambiente para obtener una buena coincidencia. Indique al usuario que se asegure de que no tiene otra fuente de luz brillante. Este valor se admite a partir de Windows 10.<br/>                                                                                        |
| <span id="WINBIO_FACE_TOO_DARK"></span><span id="winbio_face_too_dark"></span><dl> <dt>**WINBIO \_ FACE \_ TOO \_ DARK**</dt> </dl>                                                            | La imagen es demasiado oscura para obtener una buena coincidencia. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                                                             |
| <span id="WINBIO_FACE_SPOOF_DETECTED"></span><span id="winbio_face_spoof_detected"></span><dl> <dt>**SE \_ DETECTÓ \_ UNA SUPLANTACIÓN DE CARA DE WINBIO \_**</dt> </dl>                                          | El componente de reconocimiento cree que la cara no está en directo, pero que viene de una fuente de vídeo reproducida, una foto o una fotografía 3D. Este valor se admite a partir de Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_FACE_AMBIGUOUS_TARGET"></span><span id="winbio_face_ambiguous_target"></span><dl> <dt>**OBJETIVO \_ AMBIGUO DE WINBIO \_ \_**</dt> </dl>                                    | Dos o más caras se superponen en el marco de la cámara. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                                                     |
| <span id="WINBIO_FACE_EYES_OCCLUDED"></span><span id="winbio_face_eyes_occluded"></span><dl> <dt>**OJOS FACIALES DE WINBIO \_ \_ \_ OCCLUDED**</dt> </dl>                                             | Los ojos del usuario se ocultan. Indique al usuario que asegúrese de que los ojos no estén ocultas por elementos como un veil, gafas oscuras o contactos coloreados. Este valor se admite a partir de Windows 10.<br/>                                                                                 |
| <span id="WINBIO_FACE_WRONG_ORIENTATION"></span><span id="winbio_face_wrong_orientation"></span><dl> <dt>**ORIENTACIÓN INCORRECTA DE WINBIO \_ \_ \_**</dt> </dl>                                 | La orientación de la cámara no coincide con la orientación obligatoria que especifica la estructura [**DE INFORMACIÓN DEL SENSOR EXTENDIDO \_ \_ \_ DE WINBIO.**](winbio-extended-sensor-info.md) Indique al usuario que cambie la orientación de la cámara y vuelva a examinarla. Este valor se admite a partir de Windows 10.<br/> |
| <span id="WINBIO_FACE_TOO_HIGH"></span><span id="winbio_face_too_high"></span><dl> <dt>**WINBIO \_ FACE \_ TOO \_ HIGH**</dt> </dl>                                                            | La cara está orientada hacia arriba. Indique al usuario que mire un poco hacia abajo y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LOW"></span><span id="winbio_face_too_low"></span><dl> <dt>**WINBIO \_ FACE \_ TOO \_ LOW**</dt> </dl>                                                               | La cara está orientada hacia abajo. Indique al usuario que busque un poco y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LEFT"></span><span id="winbio_face_too_left"></span><dl> <dt>**WINBIO \_ FACE \_ TOO \_ LEFT**</dt> </dl>                                                            | La cara está demasiado lejos a la izquierda. Indique al usuario que mueva un poco más a la derecha y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_RIGHT"></span><span id="winbio_face_too_right"></span><dl> <dt>**WINBIO \_ FACE \_ TOO \_ RIGHT**</dt> </dl>                                                         | La cara está demasiado lejos a la derecha. Indique al usuario que mueva un poco más a la izquierda y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_NEAR"></span><span id="winbio_face_too_near"></span><dl> <dt>**WINBIO \_ FACE \_ TOO \_ NEAR**</dt> </dl>                                                            | La cara está demasiado cerca de la cámara. Indique al usuario que se mueva un poco más lejos y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_FACE_TOO_FAR"></span><span id="winbio_face_too_far"></span><dl> <dt>**WINBIO \_ FACE \_ TOO \_ FAR**</dt> </dl>                                                               | La cara está demasiado lejos de la cámara. Indique al usuario que se acerque un poco y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                                                                                  |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluya Winbio.h para aplicaciones cliente o Adaptadores \_ de Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





