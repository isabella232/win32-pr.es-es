---
description: Devuelve la lista de mecanismos de protección admitidos por el conector.
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: OPM_GET_SUPPORTED_PROTECTION_TYPES (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eddc6f4006f9692ec6152875cda412191b87d247e907d33b615aa6d4fb89748e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012545"
---
# <a name="opm_get_supported_protection_types"></a>OPM \_ OBTIENE TIPOS DE PROTECCIÓN \_ \_ \_ ADMITIDOS

Devuelve la lista de mecanismos de protección admitidos por el conector.



| Requisito | Value |
|--------------|-----------------------------------------------------------------------------|
| GUID de solicitud | OPM \_ OBTIENE TIPOS DE PROTECCIÓN \_ \_ \_ ADMITIDOS                                      |
| Datos de entrada   | Ninguno                                                                        |
| Devolver datos  | Una [**estructura OPM \_ STANDARD \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Comentarios

Los mecanismos de protección se devuelven en el **miembro ulInformation** de la [**estructura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) El valor es un OR bit a bit **de** marcas de tipo de protección [de OPM](opm-protection-type-flags.md).

Esta consulta es equivalente a la consulta COPPQueryProtectionType de DXVA que se usa en el Protocolo de protección de salida \_ certificado (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Solicitudes de estado de OPM](opm-status-requests.md)
</dt> </dl>

 

 




