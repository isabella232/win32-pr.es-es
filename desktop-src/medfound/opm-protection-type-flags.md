---
description: En las marcas de la tabla siguiente se especifican los mecanismos de protección de salida para el administrador de protección de salida (OPM).
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: Marcas de tipo de protección OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc8b30a18f5c7bf68fb01775751aa56e1e619f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715522"
---
# <a name="opm-protection-type-flags"></a>Marcas de tipo de protección OPM

En las marcas de la tabla siguiente se especifican los mecanismos de protección de salida para el administrador de protección de salida (OPM).



| Constante o valor                                                                                                                                                                                                                                                                                                     | Descripción                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <dt>**OPM \_ Tipo de protección \_ \_ otro**</dt> <dt>0x80000000</dt> </dl>                                                | Mecanismo de protección desconocido.<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <dt>**OPM \_ Tipo de protección \_ \_ ninguno**</dt> <dt>0x00000000</dt> </dl>                                                   | Sin mecanismos de protección.<br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <dt>**OPM \_ Tipo de protección de \_ \_ \_ \_ HDCP compatible con COPP**</dt> <dt>0x00000001</dt> </dl> | High-Bandwidth Digital Content Protection (HDCP). Esta marca se usa al emular el protocolo de protección de la salida (COPP). Para obtener más información, vea la sección Comentarios. Esta marca no se admite para la semántica de OPM.<br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <dt>**OPM \_ Tipo de protección \_ \_ ACP**</dt> <dt>0x00000002</dt> </dl>                                                      | Protección de copia analógica (ACP).<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <dt>**OPM \_ Tipo de protección \_ \_ CGMSA**</dt> <dt>0x00000004</dt> </dl>                                                | Sistema de administración de generación de copias: analógico (CGMS-A).<br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <dt>**OPM \_ Tipo de protección \_ \_ HDCP**</dt> <dt>0x00000008</dt> </dl>                                                   | HDCP. Esta marca se usa cuando el objeto OPM tiene semántica de OPM. No se admite para la semántica de COPP.<br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <dt>**OPM \_ Tipo de protección \_ \_ DPCP**</dt> <dt>0x00000010</dt> </dl>                                                   | Content Protection de DisplayPort (DPCP).<br/>                                                                                                                                                                           |



## <a name="remarks"></a>Observaciones

Estas marcas se usan en los siguientes comandos de OPM y solicitudes de estado.

-   [\_nivel de \_ protección de conjunto de OPM \_](opm-set-protection-level.md)
-   [\_nivel de \_ \_ protección virtual \_ de OPM](opm-get-virtual-protection-level.md)
-   [\_obtener \_ nivel de \_ protección \_ real de OPM](opm-get-actual-protection-level.md)

### <a name="hdcp"></a>HDCP

Las dos marcas siguientes están definidas para HDCP.



| Value                                         | Descripción                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_tipo de protección OPM \_ \_ HDCP                   | Use esta marca si se ha creado el puntero [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) con semántica de OPM.                                                                        |
| tipo de protección OPM, \_ \_ \_ \_ HDCP compatible con COPP \_ | Use esta marca si el puntero [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) se creó con la semántica de COPP. Esta marca corresponde a la \_ marca de \_ HDCP PROTECTIONTYPE de COPP en COPP. |



 

Ambos modos (semántica de OPM y semántica de COPP) admiten las siguientes operaciones para HDCP:

-   Habilite o deshabilite HDCP mediante el comando de [nivel de protección de set de OPM \_ \_ \_ ](opm-set-protection-level.md) .
-   Consulte si se ha habilitado HDCP mediante la solicitud de estado de nivel de [ \_ \_ \_ protección \_ virtual de OPM](opm-get-virtual-protection-level.md) o [OPM obtener estado de \_ \_ \_ protección \_ real](opm-get-actual-protection-level.md) .

La semántica de OPM también admite lo siguiente:

-   Repetidores de HDCP. Un *repetidor de HDCP* es un dispositivo HDCP que puede recibir contenido de HDCP y también volver a cifrar y transmitir el mismo contenido.
-   Revocación de HDCP. Si un dispositivo HDCP revocado está conectado a la salida de vídeo OPM, la salida de vídeo no transmitirá el vídeo. La aplicación no necesita analizar los mensajes de renovación del sistema HDCP (SRMs) o determinar si se ha revocado el dispositivo de salida. Para obtener más información, consulte el comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .

Cuando se usan semánticas de COPP, la interfaz [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) no admite repetidores de HDCP. Además, no controla la revocación de HDCP. En su lugar, la aplicación debe analizar el SRM para determinar si se ha revocado un dispositivo HDCP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de OPM](opm-enumerations.md)
</dt> </dl>

 

 




