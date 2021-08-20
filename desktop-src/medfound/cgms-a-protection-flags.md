---
description: Especifique los niveles de protección para Copy Generation Management System&\# 8212; Análogo (CGMS-A).
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: Marcas de protección de CGMS-A (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfe52f6b6f8c282e9dacebd6528373fc8ba7b7717a8e721d7d414117585bb188
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065144"
---
# <a name="cgms-a-protection-flags"></a>Marcas de protección de CGMS-A

Las constantes de la tabla siguiente especifican los niveles de protección para Copy Generation Management System Analog (CGMS-A).



| Constante o valor                                                                                                                                                                                                                                                                                                 | Descripción                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <dt>**OPM \_ CGMSA \_ OFF**</dt> <dt>0x00</dt> </dl>                                                                                       | CGMS-A está deshabilitado. <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <dt>**OPM \_ COPIA GRATUITA \_ \_ DE CGMSA**</dt> <dt>0x01</dt> </dl>                                                              | El nivel de protección es Copiar libremente.<br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <dt>**OPM \_ NO COPIAR \_ MÁS \_ ARCHIVOS \_ DE CGMSA**</dt> <dt>0x02</dt> </dl>                                                          | El nivel de protección es No copiar más. <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <dt>**OPM \_ COPIA DE \_ CGMSA \_ DE UNA \_ GENERACIÓN**</dt> <dt>0x03</dt> </dl>                                     | El nivel de protección es Copiar una generación. <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <dt>**OPM \_ COPIA DE CGMSA \_ \_ NUNCA**</dt> <dt>0X04</dt> </dl>                                                                 | El nivel de protección es Copiar nunca.<br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <dt>**OPM \_ CONTROL DE REDISTRIBUCIÓN DE CGMSA \_ \_ \_ 0X08**</dt> <dt></dt> </dl> | Se requiere el control de redistribución (también denominado *marca de* difusión). Esta marca se puede combinar con las otras marcas.<br/> |



## <a name="remarks"></a>Comentarios

Estas marcas son equivalentes a las constantes de enumeración de nivel de protección **\_ DE COPP \_ \_ CGMSA** que se usan en el Protocolo de protección de salida certificado (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation constantes](media-foundation-constants.md)
</dt> </dl>

 

 




