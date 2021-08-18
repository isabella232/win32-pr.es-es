---
description: Las marcas de la tabla siguiente especifican mecanismos de protección de salida para Output Protection Manager (OPM).
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: Marcas de tipo de protección de OPM (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ee61b17ee1708f8c2fc7e2f91b33d966b17f8fd2e198e2772c30ccccf837d04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101894"
---
# <a name="opm-protection-type-flags"></a>Marcas de tipo de protección de OPM

Las marcas de la tabla siguiente especifican mecanismos de protección de salida para Output Protection Manager (OPM).



| Constante o valor                                                                                                                                                                                                                                                                                                     | Descripción                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <dt>**OPM \_ TIPO \_ DE \_ PROTECCIÓN OTROS**</dt> <dt>0x80000000</dt> </dl>                                                | Mecanismo de protección desconocido.<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <dt>**OPM \_ TIPO \_ DE \_ PROTECCIÓN NONE**</dt> <dt>0x00000000</dt> </dl>                                                   | Sin mecanismos de protección.<br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <dt>**OPM \_ TIPO \_ DE PROTECCIÓN COMPATIBLE CON \_ \_ \_ HDCP DE COPP**</dt> <dt>0x00000001</dt> </dl> | High-Bandwidth Digital Content Protection (HDCP). Esta marca se usa al emular el Protocolo de protección de salida certificado (COPP). Para obtener más información, vea la sección Comentarios. Esta marca no se admite para la semántica de OPM.<br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <dt>**OPM \_ TIPO \_ DE \_ PROTECCIÓN ACP**</dt> <dt>0x00000002</dt> </dl>                                                      | Protección de copia análoga (ACP).<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <dt>**OPM \_ TIPO \_ DE \_ PROTECCIÓN CGMSA**</dt> <dt>0x00000004</dt> </dl>                                                | Sistema de administración de generación de copias: análogo (CGMS-A).<br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <dt>**OPM \_ TIPO \_ DE \_ PROTECCIÓN HDCP**</dt> <dt>0x00000008</dt> </dl>                                                   | Hdcp. Esta marca se usa cuando el objeto OPM tiene semántica de OPM. No se admite para la semántica de COPP.<br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <dt>**OPM \_ TIPO \_ DE \_ PROTECCIÓN DPCP**</dt> <dt>0x00000010</dt> </dl>                                                   | DisplayPort Content Protection (DPCP).<br/>                                                                                                                                                                           |



## <a name="remarks"></a>Comentarios

Estas marcas se usan en los siguientes comandos OPM y solicitudes de estado.

-   [OPM \_ SET \_ PROTECTION \_ LEVEL](opm-set-protection-level.md)
-   [OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL](opm-get-virtual-protection-level.md)
-   [OPM \_ GET REAL PROTECTION \_ \_ \_ LEVEL](opm-get-actual-protection-level.md)

### <a name="hdcp"></a>Hdcp

Las dos marcas siguientes se definen para HDCP.



| Valor                                         | Descripción                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| OPM \_ PROTECTION \_ TYPE \_ HDCP                   | Use esta marca si el [**puntero IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) se creó con semántica de OPM.                                                                        |
| HDCP \_ COMPATIBLE CON \_ OPM PROTECTION TYPE \_ COPP \_ COMPATIBLE \_ | Use esta marca si el [**puntero IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) se creó con semántica de COPP. Esta marca corresponde a la marca COPP \_ ProtectionType \_ HDCP en COPP. |



 

Ambos modos (semántica de OPM y semántica de COPP) admiten las siguientes operaciones para HDCP:

-   Habilite o deshabilite HDCP mediante el [comando OPM \_ SET PROTECTION \_ \_ LEVEL.](opm-set-protection-level.md)
-   Consulte si HDCP está habilitado mediante la solicitud [de estado OPM \_ GET VIRTUAL \_ PROTECTION \_ \_ LEVEL](opm-get-virtual-protection-level.md) u [OPM GET REAL PROTECTION \_ \_ \_ \_ LEVEL.](opm-get-actual-protection-level.md)

La semántica de OPM también admite lo siguiente:

-   Repetidores HDCP. Un *repetidor de HDCP* es un dispositivo HDCP que puede recibir contenido de HDCP y también volver a cifrar y transmitir el mismo contenido.
-   Revocación de HDCP. Si un dispositivo HDCP revocado está conectado a la salida de vídeo OPM, la salida de vídeo no transmitirá el vídeo. La aplicación no necesita analizar los mensajes de renovación del sistema (SRE) de HDCP ni determinar si se ha revocado el dispositivo de salida. Para más información, consulte el comando [**OPM \_ SET \_ HDCP \_ SRM.**](opm-set-hdcp-srm.md)

Cuando se usa la semántica de COPP, la interfaz [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) no admite repetidores HDCP. Además, no controla la revocación de HDCP. En su lugar, la aplicación debe analizar el SRM para determinar si se ha revocado un dispositivo HDCP.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones de OPM](opm-enumerations.md)
</dt> </dl>

 

 




