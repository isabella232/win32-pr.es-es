---
title: Constantes de WINBIO_BIR_PURPOSE (Winbio \_ Types. h)
description: Especifique el propósito para el que está previsto el registro de información biométrica (BIR) o para el que es adecuado.
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
ms.openlocfilehash: f5a662a5ae045d3afc631f93cdf296508dabccf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996448"
---
# <a name="winbio_bir_purpose-constants"></a>\_Constantes WINBIO Bir \_ purpose

El miembro **purpose** de la estructura de [**\_ \_ encabezado WINBIO Bir**](winbio-bir-header.md) usa las marcas siguientes para especificar el propósito para el que está previsto el registro de información biométrico (BIR) o para el que es adecuado.



| Constante                                                                                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <dt>**WINBIO \_ no hay ningún \_ propósito \_ disponible**</dt> </dl>                                         | No se especifica ningún propósito.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <dt>**\_comprobación de propósito de WINBIO \_**</dt> </dl>                                                            | Comprobar la identidad de un usuario.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <dt>**\_identificación de propósito de WINBIO \_**</dt> </dl>                                                      | Identifique a un usuario.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <dt>**\_inscripción de propósito de WINBIO \_**</dt> </dl>                                                            | Inscribir a un usuario.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <dt>**WINBIO \_ propósito \_ inscribirse \_ para la \_ comprobación**</dt> </dl>       | Capture un ejemplo biométrico y determine si el ejemplo corresponde a la identidad de usuario especificada.<br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <dt>**WINBIO \_ propósito \_ inscribirse \_ para \_ identificación**</dt> </dl> | Capture un ejemplo biométrico y determine si coincide con una plantilla biométrica existente.<br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <dt>**\_Auditoría de propósito de WINBIO \_**</dt> </dl>                                                               | Información adicional que se puede usar para el registro o para la visualización. Todas las funciones omiten este valor en la entrada. En la salida, solo estará disponible si es compatible con la unidad biométrica y especifica **WINBIO \_ Data \_ Flag \_ raw** en el parámetro *Flags* de la función [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) .<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> <dt>

[**WINBIO \_ \_ encabezado Bir**](winbio-bir-header.md)
</dt> </dl>

 

 





