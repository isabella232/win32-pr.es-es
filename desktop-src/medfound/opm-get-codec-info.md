---
description: Obtiene el valor de meritorio de un códec de hardware.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf310ae3dafee7823119b2d5d5bd2c6b61fe822
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574841"
---
# <a name="opm_get_codec_info"></a>OPM \_ GET \_ CODEC \_ INFO

Obtiene el valor de meritorio de un códec de hardware.



| Requisito | Value |
|--------------|-------------------------------------------------------------------------------------------|
| GUID de solicitud | **OPM \_ GET \_ CODEC \_ INFO**                                                                 |
| Datos de entrada   | Estructura [**OPM \_ GET CODEC INFO \_ \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)   |
| Devolver datos  | Estructura [**OPM \_ GET CODEC INFO \_ \_ \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) |



 

## <a name="remarks"></a>Observaciones

Aunque este comando usa la [interfaz del](output-protection-manager.md) Administrador de protección de salida (OPM), solo se aplica a codificadores y descodificadores de hardware. No se aplica a los dispositivos de salida de vídeo.

Por lo general, no debe usar este comando directamente. Para obtener el valor de meritorio de un códec de hardware, llame a la [**función MFGetMFTMerit.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) Esta función realiza todas las llamadas de OPM necesarias para enviar el comando **OPM \_ GET CODEC \_ \_ INFO.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 \[ aplicaciones de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




