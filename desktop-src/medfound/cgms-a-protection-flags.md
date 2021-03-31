---
description: Especifique los niveles de protección para el sistema de administración de generación de copias&\# 8212; Analógico (CGMS-A).
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: Marcas de protección de CGMS-A (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329ae13741490f2783d548baeead65ba59bc5ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423575"
---
# <a name="cgms-a-protection-flags"></a>Marcas de protección de CGMS-A

En las constantes de la tabla siguiente se especifican los niveles de protección para el sistema de administración de la generación de copias analógica (CGMS-A).



| Constante o valor                                                                                                                                                                                                                                                                                                 | Descripción                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <dt>**OPM \_ CGMSA \_**</dt> de <dt>0x00</dt> </dl>                                                                                       | CGMS-A está deshabilitado. <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <dt>**OPM \_ Copia de CGMSA con la \_ \_ libertad**</dt> <dt>0x01</dt> </dl>                                                              | El nivel de protección se copia libremente.<br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <dt>**OPM \_ CGMSA \_ copiar \_ no \_ más**</dt> <dt>0x02</dt> </dl>                                                          | El nivel de protección es la copia no más. <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <dt>**OPM \_ CGMSA \_ copiar \_ una \_ generación**</dt> <dt>0x03</dt> </dl>                                     | El nivel de protección es copiar una generación. <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <dt>**OPM \_ CGMSA \_ Copy \_ nunca**</dt> <dt>0x04</dt> </dl>                                                                 | El nivel de protección es copiar nunca.<br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <dt>**OPM \_ Se \_ requiere el \_ control \_ de redistribución de CGMSA**</dt> <dt>0x08</dt> </dl> | Es necesario el control de redistribución (también denominado *marca de difusión*). Esta marca se puede combinar con las demás marcas.<br/> |



## <a name="remarks"></a>Observaciones

Estas marcas son equivalentes a las constantes de enumeración de **\_ nivel de \_ protección \_ de COPP CGMSA** usadas en el protocolo de protección de la salida certificada (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de Media Foundation](media-foundation-constants.md)
</dt> </dl>

 

 




