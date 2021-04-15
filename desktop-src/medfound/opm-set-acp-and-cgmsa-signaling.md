---
description: Especifica información sobre la señal de vídeo, excepto el nivel de protección.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02247c48b89e61d49afe7f8f6f3821da68ff050b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543859"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a>\_configuración \_ de la \_ \_ señalización de CGMSA de OPM y ACP \_

Especifica información sobre la señal de vídeo, excepto el nivel de protección.



| Requisito | Value |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| GUID de comando | \_configuración \_ de la \_ \_ señalización de CGMSA de OPM y ACP \_                                                                                |
| Datos de entrada   | Una [**estructura \_ \_ \_ de \_ \_ \_ parámetros de señalización de CGMSA de OPM y set ACP**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) |



 

## <a name="remarks"></a>Observaciones

Este comando es equivalente al comando DXVA \_ COPPSetSignaling usado en el protocolo de protección de la salida certificada (COPP).

En el caso de CGMS-A, determinados estándares de protección requieren que la señal de televisión contenga información dentro de los mismos paquetes de forma de onda de VBI que los bits de CGMS-A. Entre otras cosas, esta información incluye la relación de aspecto de la imagen. Los televisores pueden mostrarse mal si la información de la relación de aspecto no es coherente con el flujo de vídeo. La aplicación puede usar este comando para especificar la relación de aspecto de modo que el controlador de gráficos pueda generar los paquetes VBI correctos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IOPMVideoOutput:: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandos OPM](opm-commands.md)
</dt> </dl>

 

 




