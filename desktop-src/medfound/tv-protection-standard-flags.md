---
description: Las constantes de la tabla siguiente especifican los estándares y formatos de televisión de Output Protection Manager (OPM).
ms.assetid: 8f26aa92-ed40-483e-ac78-c071619f0e12
title: Marcas estándar de protección de TV (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28fc4db73bb68fd1aeb0749134d8d6cf998cec40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082431"
---
# <a name="tv-protection-standard-flags"></a>Marcas estándar de protección de TV

Las constantes de la tabla siguiente especifican los estándares y formatos de televisión de Output Protection Manager (OPM).



| Constante o valor                                                                                                                                                                                                                                                                                                              | Descripción                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="OPM_PROTECTION_STANDARD_OTHER"></span><span id="opm_protection_standard_other"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ estándar, \_ otros**</dt> <dt>0x80000000</dt> </dl>                                             | Se desconoce el estándar de protección.<br/>                 |
| <span id="OPM_PROTECTION_STANDARD_NONE"></span><span id="opm_protection_standard_none"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ estándar \_ ninguno**</dt> <dt>0x00000000</dt> </dl>                                                | No hay ningún estándar de protección vigente.<br/>                 |
| <span id="OPM_PROTECTION_STANDARD_IEC61880_525I"></span><span id="opm_protection_standard_iec61880_525i"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ estándar \_ IEC61880 \_ 525I**</dt> <dt>0x00000001</dt> </dl>                    | El estándar de protección es IEC 61880, 525i.<br/>         |
| <span id="OPM_PROTECTION_STANDARD_IEC61880_2_525I"></span><span id="opm_protection_standard_iec61880_2_525i"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ estándar \_ IEC61880 \_ 2 \_ 525I**</dt> <dt>0x00000002</dt> </dl>             | El estándar de protección es IEC 61880-2, 525i.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_IEC62375_625P"></span><span id="opm_protection_standard_iec62375_625p"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ estándar \_ IEC62375 \_ 625P**</dt> <dt>0x00000004</dt> </dl>                    | El estándar de protección es IEC 62375, 625p.<br/>         |
| <span id="OPM_PROTECTION_STANDARD_EIA608B_525"></span><span id="opm_protection_standard_eia608b_525"></span><dl> <dt>**OPM \_ Estándar de protección \_ \_ EIA608B \_ 525**</dt> <dt>0x00000008</dt> </dl>                          | El estándar de protección es EIA/CEA-no525i.<br/>     |
| <span id="OPM_PROTECTION_STANDARD_EN300294_625I"></span><span id="opm_protection_standard_en300294_625i"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ estándar \_ EN300294 \_ 625I**</dt> <dt>0x00000010</dt> </dl>                    | El estándar de protección es ETSI EN 300 294, 625i.<br/>   |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_525P"></span><span id="opm_protection_standard_cea805a_typea_525p"></span><dl> <dt>**OPM \_ Estándar de protección \_ \_ CEA805A \_ TypeA \_ 525p**</dt> <dt>0x00000020</dt> </dl>    | El estándar de protección es CEA-805-un tipo A, 525p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_750P"></span><span id="opm_protection_standard_cea805a_typea_750p"></span><dl> <dt>**OPM \_ \_CEA805A estándar de protección \_ \_ Escriba \_ 750P**</dt> <dt>0x00000040</dt> </dl>    | El estándar de protección es CEA-805-un tipo A, 750P.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_1125I"></span><span id="opm_protection_standard_cea805a_typea_1125i"></span><dl> <dt>**OPM \_ Estándar de protección \_ \_ CEA805A \_ TypeA \_ 1125I**</dt> <dt>0x00000080</dt> </dl> | El estándar de protección es CEA-805-un tipo A, 1125i.<br/> |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_525P"></span><span id="opm_protection_standard_cea805a_typeb_525p"></span><dl> <dt>**OPM \_ Estándar de protección \_ \_ CEA805A \_ TYPEB \_ 525p**</dt> <dt>0x00000100</dt> </dl>    | El estándar de protección es CEA-805-A tipo B, 525p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_750P"></span><span id="opm_protection_standard_cea805a_typeb_750p"></span><dl> <dt>**OPM \_ PROTECCIÓN \_ estándar \_ CEA805A \_ TYPEB \_ 750P**</dt> <dt>0x00000200</dt> </dl>    | El estándar de protección es CEA-805-A tipo B, 750P.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_1125I"></span><span id="opm_protection_standard_cea805a_typeb_1125i"></span><dl> <dt>**OPM \_ Estándar de protección \_ \_ CEA805A \_ TYPEB \_ 1125I**</dt> <dt>0x00000400</dt> </dl> | El estándar de protección es CEA-805-A tipo B, 1125i.<br/> |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_525I"></span><span id="opm_protection_standard_aribtrb15_525i"></span><dl> <dt>**OPM \_ Estándar de protección \_ \_ ARIBTRB15 \_ 525I**</dt> <dt>0x00000800</dt> </dl>                 | El estándar de protección es ARIB TR-B15, 525i.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_525P"></span><span id="opm_protection_standard_aribtrb15_525p"></span><dl> <dt>**OPM \_ Estándar de protección \_ \_ ARIBTRB15 \_ 525p**</dt> <dt>0x00001000</dt> </dl>                 | El estándar de protección es ARIB TR-B15, 525p.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_750P"></span><span id="opm_protection_standard_aribtrb15_750p"></span><dl> <dt>**OPM \_ Estándar de protección \_ \_ ARIBTRB15 \_ 750P**</dt> <dt>0x00002000</dt> </dl>                 | El estándar de protección es ARIB TR-B15, 750P.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_1125I"></span><span id="opm_protection_standard_aribtrb15_1125i"></span><dl> <dt>**OPM \_ Estándar de protección \_ \_ ARIBTRB15 \_ 1125I**</dt> <dt>0x00004000</dt> </dl>              | El estándar de protección es ARIB TR-B15, 1125i.<br/>      |



## <a name="remarks"></a>Observaciones

Estas marcas son numéricamente equivalentes a la enumeración **COPP \_ TVProtectionStandard** usada en el protocolo de protección de la salida certificada (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de Media Foundation](media-foundation-constants.md)
</dt> <dt>

[**\_configuración \_ de la \_ \_ señalización de CGMSA de OPM y ACP \_**](opm-set-acp-and-cgmsa-signaling.md)
</dt> <dt>

[la \_ \_ \_ señalización de OPM y \_ CGMSA de \_ OPM](opm-get-acp-and-cgmsa-signaling.md)
</dt> </dl>

 

 




