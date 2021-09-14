---
title: WINBIO_BIOMETRIC_TYPE constantes (Winbio \_ types.h)
description: Tipos biométricos estándar definidos por el National Institute of Standards and Technology Information (NISTIR) 6529-A, también conocido como Common Biometric Exchange Formats Framework (CBEFF) Formato A.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071166"
---
# <a name="winbio_biometric_type-constants"></a>Constantes DE \_ TIPO BIOMETRIC DE WINBIO \_

Las siguientes constantes representan los tipos biométricos estándar definidos por el National Institute of Standards and Technology Information (NISTIR) 6529-A, también conocido como Common Biometric Exchange Formats Framework (CBEFF) Formato A. Actualmente **solo se admite \_ WINBIO TYPE \_ FINGERPRINT.**



| Constante                                                                                                                                                                                                            | Descripción                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_STANDARD_TYPE_MASK"></span><span id="winbio_standard_type_mask"></span><dl> <dt>**MÁSCARA DE \_ TIPO ESTÁNDAR \_ DE WINBIO \_**</dt> </dl>                 | Máscara de bits que especifica el conjunto admitido de factores biométricos.<br/>                                                                |
| <span id="WINBIO_NO_TYPE_AVAILABLE"></span><span id="winbio_no_type_available"></span><dl> <dt>**WINBIO \_ NO \_ TYPE \_ AVAILABLE**</dt> </dl>                    | No hay ningún tipo biométrico disponible.<br/>                                                                                               |
| <span id="WINBIO_TYPE_MULTIPLE"></span><span id="winbio_type_multiple"></span><dl> <dt>**WINBIO \_ TYPE \_ MULTIPLE**</dt> </dl>                                 | Se especifican varios tipos.<br/>                                                                                                 |
| <span id="WINBIO_TYPE_FACIAL_FEATURES"></span><span id="winbio_type_facial_features"></span><dl> <dt>**CARACTERÍSTICAS \_ FACIALES DE TIPO \_ \_ WINBIO**</dt> </dl>           | Las características faciales se usan para determinar la identidad de un individuo.<br/>                                                          |
| <span id="WINBIO_TYPE_VOICE"></span><span id="winbio_type_voice"></span><dl> <dt>**VOZ DE TIPO WINBIO \_ \_**</dt> </dl>                                          | Los patrones de frecuencia y volumen en la voz de un individuo se usan para determinar la identidad de un individuo.<br/>              |
| <span id="WINBIO_TYPE_FINGERPRINT"></span><span id="winbio_type_fingerprint"></span><dl> <dt>**HUELLA DIGITAL DE TIPO WINBIO \_ \_**</dt> </dl>                        | Los patrones de huella digital se usan para determinar la identidad de un individuo.<br/>                                                     |
| <span id="WINBIO_TYPE_IRIS"></span><span id="winbio_type_iris"></span><dl> <dt>**WINBIO \_ TYPE \_ IRIS**</dt> </dl>                                             | Los patrones iris se usan para determinar la identidad de un individuo. Este valor se admite a partir de Windows 10.<br/>            |
| <span id="WINBIO_TYPE_RETINA"></span><span id="winbio_type_retina"></span><dl> <dt>**WINBIO \_ TYPE \_ RETINA**</dt> </dl>                                       | Para determinar la identidad de un individuo, se usan patrones de síntomas en la retina.<br/>                                              |
| <span id="WINBIO_TYPE_HAND_GEOMETRY"></span><span id="winbio_type_hand_geometry"></span><dl> <dt>**GEOMETRÍA DE MANO DE TIPO WINBIO \_ \_ \_**</dt> </dl>                 | La forma de una mano de un individuo se usa para determinar la identidad de un individuo.<br/>                                      |
| <span id="WINBIO_TYPE_SIGNATURE_DYNAMICS"></span><span id="winbio_type_signature_dynamics"></span><dl> <dt>**DINÁMICA DE FIRMA DE TIPO WINBIO \_ \_ \_**</dt> </dl>  | Los patrones de fuerza que usa el individuo cuando firman su nombre se usan para determinar la identidad de un individuo.<br/> |
| <span id="WINBIO_TYPE_KEYSTROKE_DYNAMICS"></span><span id="winbio_type_keystroke_dynamics"></span><dl> <dt>**WINBIO \_ TYPE \_ KEYSTROKE \_ DYNAMICS**</dt> </dl>  | Los patrones de velocidad y error al escribir por un individuo se usan para determinar la identidad de un individuo.<br/>                  |
| <span id="WINBIO_TYPE_LIP_MOVEMENT"></span><span id="winbio_type_lip_movement"></span><dl> <dt>**MOVIMIENTO \_ DE LIP \_ \_ WINBIO**</dt> </dl>                    | Los cambios en los ojos de un individuo que se producen cuando hablan se usan para determinar la identidad de un individuo.<br/>      |
| <span id="WINBIO_TYPE_THERMAL_FACE_IMAGE"></span><span id="winbio_type_thermal_face_image"></span><dl> <dt>**IMAGEN DE CARA TÉRMICO DE TIPO WINBIO \_ \_ \_ \_**</dt> </dl> | Los patrones de temperatura en la cara de un individuo se usan para determinar la identidad de un individuo.<br/>                    |
| <span id="WINBIO_TYPE_THERMAL_HAND_IMAGE"></span><span id="winbio_type_thermal_hand_image"></span><dl> <dt>**IMAGEN DE MANO TÉRMICO DE TIPO WINBIO \_ \_ \_ \_**</dt> </dl> | Los patrones de temperatura en la mano de un individuo se usan para determinar la identidad de un individuo.<br/>                    |
| <span id="WINBIO_TYPE_GAIT"></span><span id="winbio_type_gait"></span><dl> <dt>**WINBIO \_ TYPE \_ GAIT**</dt> </dl>                                             | Patrones de movimiento que se producen cuando se usan los paseos individuales para determinar la identidad de un individuo.<br/>            |
| <span id="WINBIO_TYPE_SCENT"></span><span id="winbio_type_scent"></span><dl> <dt>**WINBIO \_ TYPE \_ ESTADESTE**</dt> </dl>                                          | La esencia de un individuo se usa para determinar la identidad de un individuo.<br/>                                                |
| <span id="WINBIO_TYPE_DNA"></span><span id="winbio_type_dna"></span><dl> <dt>**DNA DE \_ TIPO \_ WINBIO**</dt> </dl>                                                | Las secuencias de acido desoxyribonucleic acid (DNA) se usan para determinar la identidad de un individuo.<br/>                                    |
| <span id="WINBIO_TYPE_EAR_SHAPE"></span><span id="winbio_type_ear_shape"></span><dl> <dt>**FORMA DE \_ OREJÓN DE TIPO \_ \_ WINBIO**</dt> </dl>                             | La forma de un oído del individuo se usa para determinar la identidad de un individuo.<br/>                                     |
| <span id="WINBIO_TYPE_FINGER_GEOMETRY"></span><span id="winbio_type_finger_geometry"></span><dl> <dt>**GEOMETRÍA DE \_ \_ DEDO DE TIPO WINBIO \_**</dt> </dl>           | Las formas de los dedos de un individuo se usan para determinar la identidad de un individuo.<br/>                               |
| <span id="WINBIO_TYPE_PALM_PRINT"></span><span id="winbio_type_palm_print"></span><dl> <dt>**IMPRESIÓN DE \_ HOJAS DE \_ TIPO WINBIO \_**</dt> </dl>                          | La forma de la mano se usa para determinar la identidad de un individuo.<br/>                                                     |
| <span id="WINBIO_TYPE_VEIN_PATTERN"></span><span id="winbio_type_vein_pattern"></span><dl> <dt>**PATRÓN DE \_ PATRÓN DE \_ PATRÓN DE \_**</dt> </dl>                    | Para determinar la identidad de un individuo, se usan patrones en los colores situados debajo de la máscara de la mano de un individuo.<br/>   |
| <span id="WINBIO_TYPE_FOOT_PRINT"></span><span id="winbio_type_foot_print"></span><dl> <dt>**IMPRESIÓN DE \_ PIE DE \_ TIPO \_ WINBIO**</dt> </dl>                          | La forma del pie se usa para determinar la identidad de un individuo.<br/>                                                     |
| <span id="WINBIO_TYPE_OTHER"></span><span id="winbio_type_other"></span><dl> <dt>**WINBIO \_ TYPE \_ OTHER**</dt> </dl>                                          | Las constantes actuales no definen los datos biométricos admitidos.<br/>                                                         |
| <span id="WINBIO_TYPE_PASSWORD"></span><span id="winbio_type_password"></span><dl> <dt>**CONTRASEÑA DE \_ TIPO \_ WINBIO**</dt> </dl>                                 | Los datos de contraseña se usan para determinar la identidad de un individuo.<br/>                                                             |
| <span id="WINBIO_TYPE_ANY"></span><span id="winbio_type_any"></span><dl> <dt>**WINBIO \_ TYPE \_ ANY**</dt> </dl>                                                | Cualquier tipo de datos se usa para determinar la identidad de un individuo.<br/>                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                                                                                  |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluya Winbio.h para aplicaciones cliente o Adaptadores \_ de Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





