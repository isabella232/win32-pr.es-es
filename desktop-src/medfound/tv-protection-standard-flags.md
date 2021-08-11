---
description: Las constantes de la tabla siguiente especifican los estándares y formatos de televisión para Output Protection Manager (OPM).
ms.assetid: 8f26aa92-ed40-483e-ac78-c071619f0e12
title: Marcas estándar de protección de TV (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf739e9ec2fc93f427891e2e841d7dc77049eb5d878028372b2c7757f536169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237584"
---
# <a name="tv-protection-standard-flags"></a>Marcas estándar de protección de TV

Las constantes de la tabla siguiente especifican los estándares y formatos de televisión para Output Protection Manager (OPM).



| Constante o valor                                                                                                                                                                                                                                                                                                              | Descripción                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="OPM_PROTECTION_STANDARD_OTHER"></span><span id="opm_protection_standard_other"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ OTRAS**</dt> <dt>0x80000000</dt> </dl>                                             | Se desconoce el estándar de protección.<br/>                 |
| <span id="OPM_PROTECTION_STANDARD_NONE"></span><span id="opm_protection_standard_none"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ NONE**</dt> <dt>0x00000000</dt> </dl>                                                | No hay ningún estándar de protección en su lugar.<br/>                 |
| <span id="OPM_PROTECTION_STANDARD_IEC61880_525I"></span><span id="opm_protection_standard_iec61880_525i"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ IEC61880 \_ 525I**</dt> <dt>0x00000001</dt> </dl>                    | El estándar de protección es IEC 61880, 525i.<br/>         |
| <span id="OPM_PROTECTION_STANDARD_IEC61880_2_525I"></span><span id="opm_protection_standard_iec61880_2_525i"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ IEC61880 \_ 2 \_ 525I**</dt> <dt>0x00000002</dt> </dl>             | El estándar de protección es IEC 61880-2, 525i.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_IEC62375_625P"></span><span id="opm_protection_standard_iec62375_625p"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ IEC62375 \_ 625P**</dt> <dt>0x00000004</dt> </dl>                    | El estándar de protección es IEC 62375, 625p.<br/>         |
| <span id="OPM_PROTECTION_STANDARD_EIA608B_525"></span><span id="opm_protection_standard_eia608b_525"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ EIA608B \_ 525**</dt> <dt>0x00000008</dt> </dl>                          | El estándar de protección es EIA/CEA-608-B, 525i.<br/>     |
| <span id="OPM_PROTECTION_STANDARD_EN300294_625I"></span><span id="opm_protection_standard_en300294_625i"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ EN300294 \_ 625I**</dt> <dt>0x00000010</dt> </dl>                    | El estándar de protección es ETSI EN 300 294, 625i.<br/>   |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_525P"></span><span id="opm_protection_standard_cea805a_typea_525p"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ CEA805A \_ TYPEA \_ 525P**</dt> <dt>0x00000020</dt> </dl>    | El estándar de protección es CEA-805-A de tipo A, 525p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_750P"></span><span id="opm_protection_standard_cea805a_typea_750p"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ CEA805A \_ TYPEA \_ 750P**</dt> <dt>0x00000040</dt> </dl>    | El estándar de protección es CEA-805-A de tipo A, 750p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_1125I"></span><span id="opm_protection_standard_cea805a_typea_1125i"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ CEA805A \_ TYPEA \_ 1125I**</dt> <dt>0x00000080</dt> </dl> | El estándar de protección es CEA-805-A de tipo A, 1125i.<br/> |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_525P"></span><span id="opm_protection_standard_cea805a_typeb_525p"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ CEA805A \_ TYPEB \_ 525P**</dt> <dt>0x00000100</dt> </dl>    | El estándar de protección es CEA-805-A de tipo B, 525p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_750P"></span><span id="opm_protection_standard_cea805a_typeb_750p"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ CEA805A \_ TYPEB \_ 750P**</dt> <dt>0x00000200</dt> </dl>    | El estándar de protección es CEA-805-A de tipo B, 750p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_1125I"></span><span id="opm_protection_standard_cea805a_typeb_1125i"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ CEA805A \_ TYPEB \_ 1125I**</dt> <dt>0x00000400</dt> </dl> | El estándar de protección es CEA-805-A de tipo B, 1125i.<br/> |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_525I"></span><span id="opm_protection_standard_aribtrb15_525i"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ ARIBTRB15 \_ 525I**</dt> <dt>0x00000800</dt> </dl>                 | El estándar de protección es ARIB TR-B15, 525i.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_525P"></span><span id="opm_protection_standard_aribtrb15_525p"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ ARIBTRB15 \_ 525P**</dt> <dt>0x00001000</dt> </dl>                 | El estándar de protección es ARIB TR-B15, 525p.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_750P"></span><span id="opm_protection_standard_aribtrb15_750p"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ ARIBTRB15 \_ 750P**</dt> <dt>0x00002000</dt> </dl>                 | El estándar de protección es ARIB TR-B15, 750p.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_1125I"></span><span id="opm_protection_standard_aribtrb15_1125i"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ ESTÁNDAR \_ ARIBTRB15 \_ 1125I**</dt> <dt>0x00004000</dt> </dl>              | El estándar de protección es ARIB TR-B15, 1125i.<br/>      |



## <a name="remarks"></a>Comentarios

Estas marcas son numéricamente equivalentes a la enumeración **\_ COPP TVProtectionStandard** que se usa en el Protocolo de protección de salida certificado (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation constantes](media-foundation-constants.md)
</dt> <dt>

[**SEÑALIZACIÓN DE \_ OPM SET \_ ACP Y \_ \_ CGMSA \_**](opm-set-acp-and-cgmsa-signaling.md)
</dt> <dt>

[OPM \_ GET \_ ACP \_ AND \_ CGMSA \_ SIGNALING](opm-get-acp-and-cgmsa-signaling.md)
</dt> </dl>

 

 




