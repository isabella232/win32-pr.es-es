---
description: Obtiene el valor de mérito de un códec de hardware.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf310ae3dafee7823119b2d5d5bd2c6b61fe822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275834"
---
# <a name="opm_get_codec_info"></a>\_información del \_ códec de obtención de OPM \_

Obtiene el valor de mérito de un códec de hardware.



| Requisito | Value |
|--------------|-------------------------------------------------------------------------------------------|
| GUID de solicitud | **\_información del \_ códec de obtención de OPM \_**                                                                 |
| Datos de entrada   | Una estructura de [**\_ parámetros de \_ \_ información \_ de códec de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)   |
| Devolver datos  | Una estructura de [**\_ información del códec de obtención de \_ \_ \_ información de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) |



 

## <a name="remarks"></a>Observaciones

Aunque este comando usa la interfaz del [Administrador de protección de salida](output-protection-manager.md) (OPM), solo se aplica a los codificadores y descodificadores de hardware. No se aplica a los dispositivos de salida de vídeo.

Por lo general, no debe usar este comando directamente. Para obtener el valor de mérito de un códec de hardware, llame a la función [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) . Esta función realiza todas las llamadas OPM necesarias para enviar el comando **OPM \_ Get \_ codec \_ info** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




