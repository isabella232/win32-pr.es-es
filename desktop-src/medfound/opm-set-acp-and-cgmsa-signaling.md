---
description: Especifica información sobre la señal de vídeo, aparte del nivel de protección.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02247c48b89e61d49afe7f8f6f3821da68ff050b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361126"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a>SEÑALIZACIÓN DE \_ OPM SET \_ ACP Y \_ \_ CGMSA \_

Especifica información sobre la señal de vídeo, aparte del nivel de protección.



| Requisito | Value |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| GUID del comando | SEÑALIZACIÓN DE \_ OPM SET \_ ACP Y \_ \_ CGMSA \_                                                                                |
| Datos de entrada   | Estructura [**OPM \_ SET ACP \_ Y \_ \_ CGMSA \_ SIGNALING \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) |



 

## <a name="remarks"></a>Observaciones

Este comando es equivalente al comando DXVA COPPSetSignaling que se usa en el Protocolo de protección de salida \_ certificado (COPP).

Para CGMS-A, ciertos estándares de protección requieren que la señal de televisión contenga información dentro de los mismos paquetes de onda de VBI que los bits de CGMS-A. Entre otras cosas, esta información incluye la relación de aspecto de la imagen. Las televisión pueden mostrarse mal si la información de relación de aspecto no es coherente con la secuencia de vídeo. La aplicación puede usar este comando para especificar la relación de aspecto para que el controlador de gráficos pueda generar los paquetes de VBI correctos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandos de OPM](opm-commands.md)
</dt> </dl>

 

 




