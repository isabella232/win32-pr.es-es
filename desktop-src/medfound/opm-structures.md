---
description: Las siguientes estructuras se usan con el administrador de protección de salida (OPM).
ms.assetid: 676a60ca-393e-4b5d-89d3-50cf4b771492
title: Estructuras OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62bc7cbc13b987a2cfdda5d210cddd2fd05b8fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687172"
---
# <a name="opm-structures"></a>Estructuras OPM

Las siguientes estructuras se usan con el [Administrador de protección de salida](output-protection-manager.md) (OPM).



| Estructura                                                                                              | Descripción                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_encabezado GRL**](grl-header.md)                                                                      | Contiene el encabezado de la lista de revocación global (GRL).                                                                                                          |
| [**\_firma MF**](mf-signature.md)                                                                  | Contiene una firma de lista de revocación global (GRL).                                                                                                         |
| [**\_ \_ \_ señalización de CGMSA y ACP de OPM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)                                 | Contiene el resultado de una consulta de [**\_ \_ \_ \_ \_ señalización de CGMSA de OPM ACP y de marcado**](opm-get-acp-and-cgmsa-signaling.md) .                                         |
| [**\_formato de \_ salida \_ real de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)                                        | Contiene el resultado de una consulta de [**formato de salida de OPM \_ \_ \_ \_ real**](opm-get-actual-output-format.md) en el administrador de protección de salida (OPM).               |
| [**\_parámetros de configuración de OPM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)                                         | Contiene un comando OPM o el administrador de protección de la salida (COPP) certificado.                                                                                     |
| [**\_información del \_ \_ dispositivo HDCP conectado a \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)             | Contiene el resultado de una consulta de [**\_ \_ \_ \_ \_ información del dispositivo HDCP Get Connected de OPM**](opm-get-connected-hdcp-device-information.md) .                     |
| [**\_parámetros de \_ obtención \_ de \_ información compatible de \_ COPP de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_copp_compatible_get_info_parameters)        | Contiene parámetros para el método [**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) . |
| [**\_parámetros de \_ inicialización cifrados de OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters)          | Contiene los parámetros de inicialización de una sesión de OPM.                                                                                                     |
| [**\_información de obtención de \_ \_ información de códec \_ de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)                           | Contiene el resultado de una consulta de [**\_ \_ \_ información de códec OPM**](opm-get-codec-info.md) .                                                                     |
| [**\_parámetros de obtención de \_ información de códec de \_ OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)                             | Contiene información para el comando [**OPM \_ Get \_ codec \_ info**](opm-get-codec-info.md) .                                                                  |
| [**\_parámetros de obtención de \_ información de OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)                                          | Contiene parámetros para el método [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) .                             |
| [**\_Vector de \_ selección de clave de HDCP de OPM \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_hdcp_key_selection_vector)                             | Contiene el vector de selección de clave (KSV) para un receptor de High-Bandwidth Digital Content Protection (HDCP).                                                   |
| [**\_OMAC OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_omac)                                                                          | Contiene un código de autentificación de mensajes (MAC) (MAC) para un mensaje OPM.                                                                                           |
| [**\_datos de \_ ID. de salida OPM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)                                                    | Contiene el resultado de una solicitud de estado de obtención de ID. de [**\_ \_ salida \_ OPM**](opm-get-output-id.md) .                                                              |
| [**\_número aleatorio de OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number)                                                       | Contiene un número aleatorio de 128 bits para su uso con OPM.                                                                                                         |
| [**\_información solicitada de OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)                                       | Contiene el resultado de una solicitud de estado de OPM.                                                                                                              |
| [**\_ \_ \_ \_ \_ parámetros de señalización de configuración de CGMSA de OPM e ACP \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) | Contiene información para el comando de [**\_ \_ \_ \_ \_ señalización de CGMSA de OPM y set ACP**](opm-set-acp-and-cgmsa-signaling.md) en OPM.                               |
| [**\_parámetros de configuración de HDCP de set \_ HDCP \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)                                 | Contiene parámetros para el comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .                                                                       |
| [**\_parámetros de \_ nivel de protección de conjunto OPM \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)                 | Contiene datos para el comando de [ \_ \_ \_ nivel de protección de OPM](opm-set-protection-level.md) en OPM.                                                          |
| [**\_información estándar de OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                         | Contiene el resultado de una solicitud de estado de OPM.                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de OPM](opm-programming-reference.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> </dl>

 

 



