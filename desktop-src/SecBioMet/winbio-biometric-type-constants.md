---
title: Constantes de WINBIO_BIOMETRIC_TYPE (Winbio \_ Types. h)
description: Tipos biométricos estándar definidos por el National Institute of Standards and Technology Information (NISTIR) 6529-A, que se conoce como el formato de la plataforma de formatos biométricos (CBEFF) del marco de trabajo.
ms.assetid: DCBDB5F9-FF81-44C1-B439-2B8C02483212
topic_type:
- apiref
api_name:
- WINBIO_STANDARD_TYPE_MASK
- WINBIO_NO_TYPE_AVAILABLE
- WINBIO_TYPE_MULTIPLE
- WINBIO_TYPE_FACIAL_FEATURES
- WINBIO_TYPE_VOICE
- WINBIO_TYPE_FINGERPRINT
- WINBIO_TYPE_IRIS
- WINBIO_TYPE_RETINA
- WINBIO_TYPE_HAND_GEOMETRY
- WINBIO_TYPE_SIGNATURE_DYNAMICS
- WINBIO_TYPE_KEYSTROKE_DYNAMICS
- WINBIO_TYPE_LIP_MOVEMENT
- WINBIO_TYPE_THERMAL_FACE_IMAGE
- WINBIO_TYPE_THERMAL_HAND_IMAGE
- WINBIO_TYPE_GAIT
- WINBIO_TYPE_SCENT
- WINBIO_TYPE_DNA
- WINBIO_TYPE_EAR_SHAPE
- WINBIO_TYPE_FINGER_GEOMETRY
- WINBIO_TYPE_PALM_PRINT
- WINBIO_TYPE_VEIN_PATTERN
- WINBIO_TYPE_FOOT_PRINT
- WINBIO_TYPE_OTHER
- WINBIO_TYPE_PASSWORD
- WINBIO_TYPE_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d2ab5c41a3c2af26312c97a67d1179b50fd759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685984"
---
# <a name="winbio_biometric_type-constants"></a>WINBIO \_ constantes de \_ tipo biométrico

Las siguientes constantes representan los tipos de biométricos estándar definidos por el National Institute of Standards and Technology Information (NISTIR) 6529-A, que se conoce como el formato de la plataforma de formatos biométricos (CBEFF) de los que tiene el formato A. Actualmente solo se admite la **\_ \_ huella digital de tipo WINBIO** .



| Constante                                                                                                                                                                                                            | Descripción                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_STANDARD_TYPE_MASK"></span><span id="winbio_standard_type_mask"></span><dl> <dt>**\_máscara de \_ tipo \_ estándar de WINBIO**</dt> </dl>                 | Máscara de máscara que especifica el conjunto admitido de factores biométricos.<br/>                                                                |
| <span id="WINBIO_NO_TYPE_AVAILABLE"></span><span id="winbio_no_type_available"></span><dl> <dt>**WINBIO \_ no hay ningún \_ tipo \_ disponible**</dt> </dl>                    | No hay ningún tipo biométrico disponible.<br/>                                                                                               |
| <span id="WINBIO_TYPE_MULTIPLE"></span><span id="winbio_type_multiple"></span><dl> <dt>**WINBIO \_ tipo \_ múltiple**</dt> </dl>                                 | Se especifican varios tipos.<br/>                                                                                                 |
| <span id="WINBIO_TYPE_FACIAL_FEATURES"></span><span id="winbio_type_facial_features"></span><dl> <dt>**\_ \_ características faciales de tipo WINBIO \_**</dt> </dl>           | Las características faciales se usan para determinar la identidad de un individuo.<br/>                                                          |
| <span id="WINBIO_TYPE_VOICE"></span><span id="winbio_type_voice"></span><dl> <dt>**WINBIO \_ tipo de \_ voz**</dt> </dl>                                          | Los patrones de frecuencia y volumen de la voz de una persona se usan para determinar la identidad de un individuo.<br/>              |
| <span id="WINBIO_TYPE_FINGERPRINT"></span><span id="winbio_type_fingerprint"></span><dl> <dt>**\_huella digital de tipo WINBIO \_**</dt> </dl>                        | Los patrones de huellas digitales se usan para determinar la identidad de un individuo.<br/>                                                     |
| <span id="WINBIO_TYPE_IRIS"></span><span id="winbio_type_iris"></span><dl> <dt>**WINBIO \_ tipo \_ iris**</dt> </dl>                                             | Los patrones de iris se usan para determinar la identidad de un individuo. Este valor se admite a partir de Windows 10.<br/>            |
| <span id="WINBIO_TYPE_RETINA"></span><span id="winbio_type_retina"></span><dl> <dt>**WINBIO \_ tipo \_ retina**</dt> </dl>                                       | Los patrones de la retina se usan para determinar la identidad de un individuo.<br/>                                              |
| <span id="WINBIO_TYPE_HAND_GEOMETRY"></span><span id="winbio_type_hand_geometry"></span><dl> <dt>**geometría de la \_ mano del tipo WINBIO \_ \_**</dt> </dl>                 | La forma de una mano de un individuo se usa para determinar la identidad de un individuo.<br/>                                      |
| <span id="WINBIO_TYPE_SIGNATURE_DYNAMICS"></span><span id="winbio_type_signature_dynamics"></span><dl> <dt>**WINBIO \_ tipo de \_ firma \_ Dynamics**</dt> </dl>  | Los patrones de fuerza que usa el individuo cuando firman su nombre se usan para determinar la identidad de un individuo.<br/> |
| <span id="WINBIO_TYPE_KEYSTROKE_DYNAMICS"></span><span id="winbio_type_keystroke_dynamics"></span><dl> <dt>**WINBIO \_ de \_ pulsación de tecla tipo \_ Dynamics**</dt> </dl>  | La velocidad y los patrones de error que se escriben en una persona se usan para determinar la identidad de un individuo.<br/>                  |
| <span id="WINBIO_TYPE_LIP_MOVEMENT"></span><span id="winbio_type_lip_movement"></span><dl> <dt>**\_movimiento del \_ Lip del tipo WINBIO \_**</dt> </dl>                    | Los cambios en los Lip de un individuo que se producen cuando hablan se usan para determinar la identidad de un individuo.<br/>      |
| <span id="WINBIO_TYPE_THERMAL_FACE_IMAGE"></span><span id="winbio_type_thermal_face_image"></span><dl> <dt>**\_imagen de \_ la \_ esfera \_ térmica del tipo WINBIO**</dt> </dl> | Los patrones de temperatura en la superficie de una persona se usan para determinar la identidad de un individuo.<br/>                    |
| <span id="WINBIO_TYPE_THERMAL_HAND_IMAGE"></span><span id="winbio_type_thermal_hand_image"></span><dl> <dt>**\_imagen de \_ la \_ mano \_ térmica del tipo WINBIO**</dt> </dl> | Los patrones de temperatura a mano de una persona se usan para determinar la identidad de un individuo.<br/>                    |
| <span id="WINBIO_TYPE_GAIT"></span><span id="winbio_type_gait"></span><dl> <dt>**WINBIO \_ Type \_ el**</dt> </dl>                                             | Los patrones de movimiento que se producen cuando se usan los recorridos individuales para determinar la identidad de un individuo.<br/>            |
| <span id="WINBIO_TYPE_SCENT"></span><span id="winbio_type_scent"></span><dl> <dt>**WINBIO \_ Type \_ scent**</dt> </dl>                                          | El scent de una persona se usa para determinar la identidad de un individuo.<br/>                                                |
| <span id="WINBIO_TYPE_DNA"></span><span id="winbio_type_dna"></span><dl> <dt>**WINBIO \_ tipo \_ DNA**</dt> </dl>                                                | Las secuencias de ácido deoxyribonucleic (DNA) se usan para determinar la identidad de un individuo.<br/>                                    |
| <span id="WINBIO_TYPE_EAR_SHAPE"></span><span id="winbio_type_ear_shape"></span><dl> <dt>**WINBIO \_ tipo \_ EAR \_**</dt> </dl>                             | La forma de una lengüeta del individuo se usa para determinar la identidad de un individuo.<br/>                                     |
| <span id="WINBIO_TYPE_FINGER_GEOMETRY"></span><span id="winbio_type_finger_geometry"></span><dl> <dt>**\_geometría de \_ dedo de tipo WINBIO \_**</dt> </dl>           | Las formas de los dedos de una persona se usan para determinar la identidad de un individuo.<br/>                               |
| <span id="WINBIO_TYPE_PALM_PRINT"></span><span id="winbio_type_palm_print"></span><dl> <dt>**WINBIO \_ tipo \_ Palm \_ Print**</dt> </dl>                          | La forma de la palma se usa para determinar la identidad de un individuo.<br/>                                                     |
| <span id="WINBIO_TYPE_VEIN_PATTERN"></span><span id="winbio_type_vein_pattern"></span><dl> <dt>**\_patrón de texto de tipo WINBIO \_ \_**</dt> </dl>                    | Los patrones del Veins debajo de la máscara de la mano de una persona se usan para determinar la identidad de un individuo.<br/>   |
| <span id="WINBIO_TYPE_FOOT_PRINT"></span><span id="winbio_type_foot_print"></span><dl> <dt>**WINBIO \_ escribir \_ pie de página \_**</dt> </dl>                          | La forma del pie se usa para determinar la identidad de un individuo.<br/>                                                     |
| <span id="WINBIO_TYPE_OTHER"></span><span id="winbio_type_other"></span><dl> <dt>**tipo de WINBIO \_ \_**</dt> </dl>                                          | Los datos biométricos admitidos no están definidos por las constantes actuales.<br/>                                                         |
| <span id="WINBIO_TYPE_PASSWORD"></span><span id="winbio_type_password"></span><dl> <dt>**\_contraseña del tipo WINBIO \_**</dt> </dl>                                 | Los datos de contraseña se usan para determinar la identidad de un individuo.<br/>                                                             |
| <span id="WINBIO_TYPE_ANY"></span><span id="winbio_type_any"></span><dl> <dt>**WINBIO \_ tipo \_ any**</dt> </dl>                                                | Cualquier tipo de datos se utiliza para determinar la identidad de un individuo.<br/>                                                          |



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

 

 





