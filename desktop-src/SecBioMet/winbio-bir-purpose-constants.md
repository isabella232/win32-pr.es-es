---
title: WINBIO_BIR_PURPOSE constantes (Winbio \_ types.h)
description: Especifique el propósito para el que está pensado el registro de información biométrica (BIR) o para el que es adecuado.
ms.assetid: AAFD3203-4D3D-43B5-A833-1258E1E281D3
topic_type:
- apiref
api_name:
- WINBIO_NO_PURPOSE_AVAILABLE
- WINBIO_PURPOSE_VERIFY
- WINBIO_PURPOSE_IDENTIFY
- WINBIO_PURPOSE_ENROLL
- WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION
- WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION
- WINBIO_PURPOSE_AUDIT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19cffe266cf30155be3c299b0d1b5e6a3d45f9991aa83fd66e62e705ddc4850f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080795"
---
# <a name="winbio_bir_purpose-constants"></a>Constantes WINBIO \_ BIR \_ PURPOSE

El miembro Purpose de  la estructura [**WINBIO \_ BIR \_ HEADER**](winbio-bir-header.md) usa las marcas siguientes para especificar el propósito para el que está pensado el registro de información biométrica (BIR) o para el que es adecuado.



| Constante                                                                                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <dt>**WINBIO \_ NO \_ PURPOSE \_ AVAILABLE**</dt> </dl>                                         | No se especifica ningún propósito.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <dt>**COMPROBACIÓN DEL \_ PROPÓSITO DE \_ WINBIO**</dt> </dl>                                                            | Compruebe la identidad de un usuario.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <dt>**IDENTIFICACIÓN DE \_ PROPÓSITO DE \_ WINBIO**</dt> </dl>                                                      | Identificar a un usuario.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <dt>**INSCRIPCIÓN DE PROPÓSITO DE WINBIO \_ \_**</dt> </dl>                                                            | Inscribir un usuario.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <dt>**INSCRIPCIÓN DE PROPÓSITO DE WINBIO \_ \_ PARA LA \_ \_ COMPROBACIÓN**</dt> </dl>       | Capture una muestra biométrica y determine si la muestra corresponde a la identidad de usuario especificada.<br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <dt>**INSCRIPCIÓN DE PROPÓSITO DE WINBIO \_ \_ PARA \_ IDENTIFICACIÓN \_**</dt> </dl> | Capture una muestra biométrica y determine si coincide con una plantilla biométrica existente.<br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <dt>**AUDITORÍA DE \_ PROPÓSITO DE \_ WINBIO**</dt> </dl>                                                               | Información adicional que se puede usar para el registro o para la presentación. Todas las funciones omiten este valor en la entrada. En la salida, solo estará disponible si es compatible con la unidad biométrica y se especifica **WINBIO \_ DATA FLAG \_ \_ RAW** en el parámetro *Flags* de la [**función WinBioCaptureSample.**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample)<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> <dt>

[**ENCABEZADO WINBIO \_ BIR \_**](winbio-bir-header.md)
</dt> </dl>

 

 





