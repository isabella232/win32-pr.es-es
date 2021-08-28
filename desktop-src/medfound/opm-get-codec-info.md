---
description: Obtiene el valor de la propiedad de un códec de hardware.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988ffa9a962d9ed04b6a978da1534a6da4fa506e873d89d238bcbb2aa00fd865
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847985"
---
# <a name="opm_get_codec_info"></a>OPM \_ GET \_ CODEC \_ INFO

Obtiene el valor de la propiedad de un códec de hardware.



| Requisito | Value |
|--------------|-------------------------------------------------------------------------------------------|
| GUID de solicitud | **OPM \_ GET \_ CODEC \_ INFO**                                                                 |
| Datos de entrada   | Una [**estructura OPM \_ GET CODEC \_ INFO \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)   |
| Devolver datos  | Estructura [**OPM \_ GET CODEC INFO \_ \_ \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) |



 

## <a name="remarks"></a>Comentarios

Aunque este comando usa la [interfaz del](output-protection-manager.md) Administrador de protección de salida (OPM), solo se aplica a los codificadores y descodificadores de hardware. No se aplica a los dispositivos de salida de vídeo.

Por lo general, no debe usar este comando directamente. Para obtener el valor de los valores de un códec de hardware, llame a la [**función MFGetMFTMerit.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) Esta función realiza todas las llamadas de OPM necesarias para enviar el **comando \_ OPM GET \_ CODEC \_ INFO.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                             |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




