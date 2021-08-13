---
title: WINBIO_ANSI_385_FACE constantes (Winbio \_ types.h)
description: Especifique los tipos de imagen de cara frontal para el reconocimiento facial.
ms.assetid: 16D21E40-C158-4674-80D0-AE9494124B96
topic_type:
- apiref
api_name:
- WINBIO_ANSI_385_FACE_TYPE_UNKNOWN
- WINBIO_ANSI_385_FACE_FRONTAL_FULL
- WINBIO_ANSI_385_FACE_FRONTAL_TOKEN
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6bd8ddc173915e2bbd912a6a668c63b4be733f32357189fe6ff3365a20bacfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410315"
---
# <a name="winbio_ansi_385_face-constants"></a>Constantes FACE de WINBIO \_ ANSI \_ 385 \_

Las siguientes constantes son valores **\_ DE \_ SUBTYPE BIOMETRIC** DE WINBIO que se pueden usar para especificar los dos tipos de imágenes de caras frontales definidas por ANSI INCITS 385-2004: "Face Recognition Format for Data Interchange": resolución completa y resolución baja. En la práctica, el marco biométrico usará solo imágenes de resolución completa para el reconocimiento facial.



| Constante o valor                                                                                                                                                                                                                                                                          | Descripción                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WINBIO_ANSI_385_FACE_TYPE_UNKNOWN"></span><span id="winbio_ansi_385_face_type_unknown"></span><dl> <dt>**WINBIO \_ ANSI \_ 385 \_ FACE TYPE \_ \_ UNKNOWN**</dt> <dt>0</dt> </dl>    | Se desconoce el tipo de imagen frontal de la cara.<br/>         |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_FULL"></span><span id="winbio_ansi_385_face_frontal_full"></span><dl> <dt>**WINBIO \_ ANSI \_ 385 \_ FACE FRONTAL \_ \_ FULL**</dt> <dt>1</dt> </dl>    | El tipo de imagen frontal de la cara es de resolución completa.<br/> |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_TOKEN"></span><span id="winbio_ansi_385_face_frontal_token"></span><dl> <dt>**WINBIO \_ ANSI \_ 385 \_ FACE FRONTAL \_ \_ TOKEN**</dt> <dt>2</dt> </dl> | El tipo de imagen frontal de la cara es de baja resolución.<br/>  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



 

 





