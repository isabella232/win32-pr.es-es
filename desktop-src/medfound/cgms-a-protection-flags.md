---
description: Especifique los niveles de protección para Copy Generation Management System&\# 8212; Análogo (CGMS-A).
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: Marcas de protección de CGMS-A (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329ae13741490f2783d548baeead65ba59bc5ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241166"
---
# <a name="cgms-a-protection-flags"></a>Marcas de protección CGMS-A

Las constantes de la tabla siguiente especifican los niveles de protección para el análogo del sistema de administración de generación de copias (CGMS-A).



| Constante o valor                                                                                                                                                                                                                                                                                                 | Descripción                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <dt>**OPM \_ CGMSA \_ OFF**</dt> <dt>0x00</dt> </dl>                                                                                       | CGMS-A está deshabilitado. <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <dt>**OPM \_ COPIA GRATUITA \_ \_ DE CGMSA**</dt> <dt>0x01</dt> </dl>                                                              | El nivel de protección es Copiar libremente.<br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <dt>**OPM \_ NO COPIAR \_ MÁS \_ ARCHIVOS \_ DE CGMSA**</dt> <dt>0x02</dt> </dl>                                                          | El nivel de protección es Copiar no más. <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <dt>**OPM \_ CGMSA \_ COPY \_ ONE \_ GENERATION**</dt> <dt>0x03</dt> </dl>                                     | El nivel de protección es Copiar una generación. <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <dt>**OPM \_ NUNCA COPIA \_ DE \_ CGMSA**</dt> <dt>0x04</dt> </dl>                                                                 | El nivel de protección es Copiar nunca.<br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <dt>**OPM \_ SE REQUIERE \_ CONTROL DE \_ REDISTRIBUCIÓN \_ DE CGMSA**</dt> <dt>0x08</dt> </dl> | Se requiere el control de redistribución (también denominado *marca de* difusión). Esta marca se puede combinar con las demás marcas.<br/> |



## <a name="remarks"></a>Observaciones

Estas marcas son equivalentes a las constantes de enumeración de nivel de protección **\_ CGMSA \_ \_** de COPP que se usan en el Protocolo de protección de salida certificado (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation constantes](media-foundation-constants.md)
</dt> </dl>

 

 




