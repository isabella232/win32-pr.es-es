---
description: Especifica información sobre la señal de vídeo, que no sea el nivel de protección.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 265d2986c624e30d342a4b3bc5e957e04c56bd01d51e146536de5731db42ace8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343515"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a>SEÑALIZACIÓN DE \_ OPM SET \_ ACP Y \_ \_ CGMSA \_

Especifica información sobre la señal de vídeo, que no sea el nivel de protección.



| Requisito | Value |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| GUID de comando | SEÑALIZACIÓN DE \_ OPM SET \_ ACP Y \_ \_ CGMSA \_                                                                                |
| Datos de entrada   | Una [**estructura OPM \_ SET ACP \_ Y \_ \_ CGMSA \_ SIGNALING \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) |



 

## <a name="remarks"></a>Comentarios

Este comando es equivalente al comando COPPSetSignaling de DXVA que se usa en el Protocolo de protección de salida \_ certificado (COPP).

Para CGMS-A, ciertos estándares de protección requieren que la señal de televisión contenga información dentro de los mismos paquetes de onda de VBI que los bits DE CGMS-A. Entre otras cosas, esta información incluye la relación de aspecto de la imagen. Los televisores pueden mostrarse mal si la información de relación de aspecto no es coherente con la secuencia de vídeo. La aplicación puede usar este comando para especificar la relación de aspecto para que el controlador de gráficos pueda generar los paquetes VBI correctos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandos de OPM](opm-commands.md)
</dt> </dl>

 

 




