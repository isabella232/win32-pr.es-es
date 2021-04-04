---
title: Constantes de WINBIO_REJECT_DETAIL (Winbio \_ Types. h)
description: Especifique el motivo por el que un procedimiento de identificación o captura de huellas digitales biométricos no se realizó correctamente.
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
ms.openlocfilehash: 4d9d23dcf568e5ed25fb5081283a421b1c0dbb07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804046"
---
# <a name="winbio_reject_detail-constants"></a>WINBIO \_ constantes de detalles de rechazo \_

Se pueden usar las siguientes constantes para especificar la razón por la que una captura de huella digital biométrica o un procedimiento de identificación no se han realizado correctamente.



| Constante                                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FP_TOO_HIGH"></span><span id="winbio_fp_too_high"></span><dl> <dt>**WINBIO \_ FP \_ demasiado \_ alto**</dt> </dl>                                                                  | El recorrido del dedo empezó a ser demasiado alto en el dedo.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_LOW"></span><span id="winbio_fp_too_low"></span><dl> <dt>**WINBIO \_ FP \_ demasiado \_ bajo**</dt> </dl>                                                                     | El recorrido del dedo comenzó demasiado bajo el dedo.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_LEFT"></span><span id="winbio_fp_too_left"></span><dl> <dt>**WINBIO \_ FP \_ demasiado a la \_ izquierda**</dt> </dl>                                                                  | El dedo estaba demasiado lejos durante el examen.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_RIGHT"></span><span id="winbio_fp_too_right"></span><dl> <dt>**WINBIO \_ FP \_ demasiado a la \_ derecha**</dt> </dl>                                                               | El dedo era demasiado adecuado durante el examen.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_FAST"></span><span id="winbio_fp_too_fast"></span><dl> <dt>**WINBIO \_ FP \_ demasiado \_ rápido**</dt> </dl>                                                                  | El dedo se deslice demasiado rápidamente en el sensor.<br/>                                                                                                                                                                                                                                       |
| <span id="WINBIO_FP_TOO_SLOW"></span><span id="winbio_fp_too_slow"></span><dl> <dt>**WINBIO \_ FP \_ demasiado \_ lento**</dt> </dl>                                                                  | El dedo se deslice demasiado lentamente en el sensor.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_FP_POOR_QUALITY"></span><span id="winbio_fp_poor_quality"></span><dl> <dt>**WINBIO \_ FP \_ de \_ calidad deficiente**</dt> </dl>                                                      | La calidad del examen era insuficiente.<br/>                                                                                                                                                                                                                                                         |
| <span id="WINBIO_FP_TOO_SKEWED"></span><span id="winbio_fp_too_skewed"></span><dl> <dt>**WINBIO \_ FP \_ demasiado \_ sesgado**</dt> </dl>                                                            | El dedo no pasó directamente por el sensor.<br/>                                                                                                                                                                                                                                    |
| <span id="WINBIO_FP_TOO_SHORT"></span><span id="winbio_fp_too_short"></span><dl> <dt>**WINBIO \_ FP \_ demasiado \_ corto**</dt> </dl>                                                               | No se examinó el dedo.<br/>                                                                                                                                                                                                                                                  |
| <span id="WINBIO_FP_MERGE_FAILURE"></span><span id="winbio_fp_merge_failure"></span><dl> <dt>**\_error de \_ combinación de FP de WINBIO \_**</dt> </dl>                                                   | No se pudieron combinar las capturas de huellas digitales.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK____"></span><span id="winbio_reject_detail_anti_spoof_mask____"></span><dl> <dt>**WINBIO \_ \_máscara de \_ \_ dessimulación \_ de detalles de rechazo**</dt> </dl> | Esta máscara cubre los 8 bits superiores del valor de detalle de rechazo en el que se encuentran los comportamientos de prueba de vida. Este valor se admite a partir de Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_POSITION_MASK______"></span><span id="winbio_reject_detail_position_mask______"></span><dl> <dt>**WINBIO \_ \_máscara de \_ posición \_ de detalles de rechazo**</dt> </dl>    | Esta máscara cubre el intervalo de bits dedicado a errores de posición. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                                         |
| <span id="WINBIO_REJECT_DETAIL_REASON_MASK"></span><span id="winbio_reject_detail_reason_mask"></span><dl> <dt>**WINBIO \_ \_ máscara de \_ motivo de detalle de rechazo \_**</dt> </dl>                       | Esta máscara cubre los 16 bits inferiores en los que se encuentra la razón enumerada para el rechazo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                           |
| <span id="WINBIO_IRIS_POOR_QUALITY"></span><span id="winbio_iris_poor_quality"></span><dl> <dt>**\_ \_ calidad deficiente de iris de WINBIO \_**</dt> </dl>                                                | Las condiciones hicieron que la cámara Capture una imagen deficiente. Indique al usuario que limpie el sensor y vuelva a examinarlo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_IRIS_TOO_BRIGHT"></span><span id="winbio_iris_too_bright"></span><dl> <dt>**WINBIO \_ iris \_ demasiado \_ brillante**</dt> </dl>                                                      | La imagen incluye demasiada luz ambiente para obtener una buena coincidencia. Indique al usuario que se asegure de que no se enfrenta a otro origen de luz brillante. Este valor se admite a partir de Windows 10.<br/>                                                                                        |
| <span id="WINBIO_IRIS_TOO_DARK"></span><span id="winbio_iris_too_dark"></span><dl> <dt>**WINBIO \_ iris \_ demasiado \_ oscuro**</dt> </dl>                                                            | La imagen es demasiado oscura para obtener una buena coincidencia. Indique al usuario que asegúrese de que su iris no esté oculto por elementos como un velo, gafas oscuras o contactos en color. Este valor se admite a partir de Windows 10.<br/>                                                                     |
| <span id="WINBIO_IRIS_SPOOF_DETECTED"></span><span id="winbio_iris_spoof_detected"></span><dl> <dt>**WINBIO \_ iris \_ falseado \_ detectado**</dt> </dl>                                          | El componente de reconocimiento considera que el iris no está activo, pero procede de una fuente de vídeo reproducida, una fotografía o una Sculpture en 3D. Este valor se admite a partir de Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_IRIS_TOO_SKEWED"></span><span id="winbio_iris_too_skewed"></span><dl> <dt>**WINBIO \_ iris \_ demasiado \_ sesgado**</dt> </dl>                                                      | El usuario no está mirando directamente a la cámara. Indique al usuario que mire directamente en la cámara y vuelva a examinarlo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                       |
| <span id="WINBIO_IRIS_TOO_CLOSED"></span><span id="winbio_iris_too_closed"></span><dl> <dt>**WINBIO \_ iris \_ demasiado \_ cerrado**</dt> </dl>                                                      | Los eyelids del usuario están ocultando el iris. Indique al usuario que abra sus ojos un poco más y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                          |
| <span id="WINBIO_IRIS_GLARE"></span><span id="winbio_iris_glare"></span><dl> <dt>**\_brillo de iris de WINBIO \_**</dt> </dl>                                                                      | La imagen incluye brillo de la lente. Indique al usuario que quite sus gafas y escanee de nuevo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                               |
| <span id="WINBIO_IRIS_DIRTY_LENS"></span><span id="winbio_iris_dirty_lens"></span><dl> <dt>**lente de WINBIO \_ iris \_ sucio \_**</dt> </dl>                                                      | La lente de la cámara ha cambiado. Indique al usuario que limpie la lente y digitalice de nuevo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                         |
| <span id="WINBIO_IRIS_POOR_FOCUS"></span><span id="winbio_iris_poor_focus"></span><dl> <dt>**\_Focus WINBIO iris \_ pobre \_**</dt> </dl>                                                      | Este iris está fuera del foco. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                                                                             |
| <span id="WINBIO_IRIS_WRONG_ORIENTATION"></span><span id="winbio_iris_wrong_orientation"></span><dl> <dt>**WINBIO \_ \_ orientación incorrecta del iris \_**</dt> </dl>                                 | La orientación de la cámara no coincide con la orientación obligatoria que especifica la estructura [**WINBIO \_ Extended \_ sensor \_ info**](winbio-extended-sensor-info.md) . Indique al usuario que cambie la orientación de la cámara y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/> |
| <span id="WINBIO_IRIS_TOO_HIGH"></span><span id="winbio_iris_too_high"></span><dl> <dt>**WINBIO \_ iris \_ demasiado \_ alto**</dt> </dl>                                                            | El iris está orientado hacia arriba. Indique al usuario que busque un poco y vuelva a examinarlo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LOW"></span><span id="winbio_iris_too_low"></span><dl> <dt>**WINBIO \_ iris \_ demasiado \_ bajo**</dt> </dl>                                                               | El iris está orientado hacia abajo. Indique al usuario que busque un poco y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LEFT"></span><span id="winbio_iris_too_left"></span><dl> <dt>**WINBIO \_ iris \_ demasiado a la \_ izquierda**</dt> </dl>                                                            | El iris está demasiado lejos a la izquierda. Indique al usuario que busque un poco más a la derecha y vuelva a examinarlo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_RIGHT"></span><span id="winbio_iris_too_right"></span><dl> <dt>**WINBIO \_ iris \_ demasiado a la \_ derecha**</dt> </dl>                                                         | El iris está demasiado lejos a la derecha. Indique al usuario que busque un poco más a la izquierda y vuelva a examinarlo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_NEAR"></span><span id="winbio_iris_too_near"></span><dl> <dt>**WINBIO \_ iris \_ demasiado \_ cerca**</dt> </dl>                                                            | El iris está demasiado cerca de la cámara. Indique al usuario que mueva un poco más lejos y vuelva a examinarlo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_IRIS_TOO_FAR"></span><span id="winbio_iris_too_far"></span><dl> <dt>**WINBIO \_ iris \_ demasiado \_ lejos**</dt> </dl>                                                               | El iris está demasiado lejos de la cámara. Indique al usuario que mueva un poco más cerca y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                         |
| <span id="WINBIO_FACE_POOR_QUALITY"></span><span id="winbio_face_poor_quality"></span><dl> <dt>**WINBIO a la \_ \_ mala \_ calidad**</dt> </dl>                                                | Las condiciones hicieron que la cámara Capture una imagen deficiente. Indique al usuario que limpie el sensor y vuelva a examinarlo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_FACE_TOO_BRIGHT"></span><span id="winbio_face_too_bright"></span><dl> <dt>**WINBIO con una \_ superficie \_ demasiado \_ brillante**</dt> </dl>                                                      | La imagen incluye demasiada luz ambiente para obtener una buena coincidencia. Indique al usuario que se asegure de que no se enfrenta a otro origen de luz brillante. Este valor se admite a partir de Windows 10.<br/>                                                                                        |
| <span id="WINBIO_FACE_TOO_DARK"></span><span id="winbio_face_too_dark"></span><dl> <dt>**WINBIO \_ sonriente \_ demasiado \_ oscuro**</dt> </dl>                                                            | La imagen es demasiado oscura para obtener una buena coincidencia. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                                                             |
| <span id="WINBIO_FACE_SPOOF_DETECTED"></span><span id="winbio_face_spoof_detected"></span><dl> <dt>**se \_ \_ ha detectado una simulación de WINBIO facial \_**</dt> </dl>                                          | El componente de reconocimiento considera que la cara no está activa, pero proviene de una fuente de vídeo reproducida, una fotografía o una Sculpture 3D. Este valor se admite a partir de Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_FACE_AMBIGUOUS_TARGET"></span><span id="winbio_face_ambiguous_target"></span><dl> <dt>**\_ \_ destino AMBIGUO de WINBIO facial \_**</dt> </dl>                                    | Dos o más caras se superponen en el fotograma de la cámara. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                                                     |
| <span id="WINBIO_FACE_EYES_OCCLUDED"></span><span id="winbio_face_eyes_occluded"></span><dl> <dt>**WINBIO \_ facial \_ Eyes \_ ocluidos**</dt> </dl>                                             | Los ojos del usuario son ocluidos. Indique al usuario que se asegure de que sus ojos no se oculten por elementos como un velo, gafas oscuras o contactos en color. Este valor se admite a partir de Windows 10.<br/>                                                                                 |
| <span id="WINBIO_FACE_WRONG_ORIENTATION"></span><span id="winbio_face_wrong_orientation"></span><dl> <dt>**WINBIO \_ \_ orientación incorrecta de la esfera \_**</dt> </dl>                                 | La orientación de la cámara no coincide con la orientación obligatoria que especifica la estructura [**WINBIO \_ Extended \_ sensor \_ info**](winbio-extended-sensor-info.md) . Indique al usuario que cambie la orientación de la cámara y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/> |
| <span id="WINBIO_FACE_TOO_HIGH"></span><span id="winbio_face_too_high"></span><dl> <dt>**WINBIO con una \_ superficie \_ demasiado \_ alta**</dt> </dl>                                                            | La cara está orientada. Indique al usuario que busque un poco y vuelva a examinarlo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LOW"></span><span id="winbio_face_too_low"></span><dl> <dt>**WINBIO con una \_ superficie \_ demasiado \_ baja**</dt> </dl>                                                               | La cara está orientada hacia abajo. Indique al usuario que busque un poco y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LEFT"></span><span id="winbio_face_too_left"></span><dl> <dt>**WINBIO \_ sonriente \_ demasiado a la \_ izquierda**</dt> </dl>                                                            | La superficie está demasiado lejos a la izquierda. Indique al usuario que mueva un poco más hacia la derecha y vuelva a examinarlo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_RIGHT"></span><span id="winbio_face_too_right"></span><dl> <dt>**WINBIO \_ sonriente \_ demasiado a la \_ derecha**</dt> </dl>                                                         | La superficie está demasiado lejos a la derecha. Indique al usuario que mueva un poco más hacia la izquierda y vuelva a examinarlo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_NEAR"></span><span id="winbio_face_too_near"></span><dl> <dt>**WINBIO con una \_ superficie \_ demasiado \_ cercana**</dt> </dl>                                                            | La superficie está demasiado cerca de la cámara. Indique al usuario que mueva un poco más lejos y vuelva a examinarlo. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_FACE_TOO_FAR"></span><span id="winbio_face_too_far"></span><dl> <dt>**WINBIO con una \_ superficie \_ demasiado \_ lejana**</dt> </dl>                                                               | La superficie está demasiado lejos de la cámara. Indique al usuario que mueva un poco más cerca y vuelva a examinar. Este valor se admite a partir de Windows 10.<br/>                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                                                                                  |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





