---
description: Las estructuras siguientes se usan con Output Protection Manager (OPM).
ms.assetid: 676a60ca-393e-4b5d-89d3-50cf4b771492
title: Estructuras de OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35d72c5a5301dbc07b990aa4076f14fc221a1fde6af9c81e1f4a37fb424e24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737652"
---
# <a name="opm-structures"></a>Estructuras de OPM

Las estructuras siguientes se usan con [Output Protection Manager](output-protection-manager.md) (OPM).



| Estructura                                                                                              | Descripción                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ENCABEZADO \_ GRL**](grl-header.md)                                                                      | Contiene el encabezado de lista de revocación global (GRL).                                                                                                          |
| [**MF \_ SIGNATURE**](mf-signature.md)                                                                  | Contiene una firma de lista de revocación global (GRL).                                                                                                         |
| [**SEÑALIZACIÓN \_ DE OPM ACP Y \_ \_ CGMSA \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)                                 | Contiene el resultado de una consulta [**OPM \_ GET ACP \_ Y \_ \_ CGMSA \_ SIGNALING.**](opm-get-acp-and-cgmsa-signaling.md)                                         |
| [**FORMATO DE SALIDA \_ REAL \_ DE \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)                                        | Contiene el resultado de una consulta [**GET ACTUAL OUTPUT FORMAT \_ \_ \_ \_ de OPM**](opm-get-actual-output-format.md) en Output Protection Manager (OPM).               |
| [**CONFIGURACIÓN DE PARÁMETROS DE OPM \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)                                         | Contiene un comando OPM o Certified Output Protection Manager (COPP).                                                                                     |
| [**INFORMACIÓN DEL DISPOSITIVO \_ \_ HDCP CONECTADO A \_ OPM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)             | Contiene el resultado de una consulta [**\_ OPM GET \_ CONNECTED \_ HDCP \_ DEVICE \_ INFORMATION.**](opm-get-connected-hdcp-device-information.md)                     |
| [**PARÁMETROS \_ GET \_ INFO COMPATIBLES CON OPM COPP \_ \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_copp_compatible_get_info_parameters)        | Contiene parámetros para [**el método IOPMVideoOutput::COPPCompatibleGetInformation.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) |
| [**PARÁMETROS DE \_ INICIALIZACIÓN CIFRADA \_ DE OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters)          | Contiene parámetros de inicialización para una sesión de OPM.                                                                                                     |
| [**OPM \_ GET \_ CODEC \_ INFO \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)                           | Contiene el resultado de una consulta [**OPM \_ GET CODEC \_ \_ INFO.**](opm-get-codec-info.md)                                                                     |
| [**OPM \_ GET \_ CODEC \_ INFO \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)                             | Contiene información para el comando [**\_ GET CODEC INFO \_ \_ de OPM.**](opm-get-codec-info.md)                                                                  |
| [**OPM \_ GET \_ INFO \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)                                          | Contiene parámetros para el [**método IOPMVideoOutput::GetInformation.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)                             |
| [**VECTOR DE SELECCIÓN \_ DE CLAVES DE HDCP \_ \_ DE \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_hdcp_key_selection_vector)                             | Contiene el vector de selección de claves (KSV) para un receptor High-Bandwidth digital Content Protection (HDCP).                                                   |
| [**OMAC de OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_omac)                                                                          | Contiene un código de autenticación de mensajes (MAC) para un mensaje OPM.                                                                                           |
| [**DATOS DE IDENTIFICADOR \_ DE \_ SALIDA DE \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)                                                    | Contiene el resultado de una solicitud [**de estado OPM \_ GET OUTPUT \_ \_ ID.**](opm-get-output-id.md)                                                              |
| [**NÚMERO ALEATORIO DE OPM \_ \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number)                                                       | Contiene un número aleatorio de 128 bits para su uso con OPM.                                                                                                         |
| [**INFORMACIÓN SOLICITADA DE OPM \_ \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)                                       | Contiene el resultado de una solicitud de estado de OPM.                                                                                                              |
| [**OPM \_ SET \_ ACP \_ AND \_ CGMSA \_ SIGNALING \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) | Contiene información para el comando [**OPM \_ SET ACP Y \_ \_ \_ CGMSA \_ SIGNALING**](opm-set-acp-and-cgmsa-signaling.md) en OPM.                               |
| [**OPM \_ SET \_ HDCP \_ SRM \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)                                 | Contiene parámetros para el [**comando OPM \_ SET \_ HDCP \_ SRM.**](opm-set-hdcp-srm.md)                                                                       |
| [**OPM \_ SET \_ PROTECTION \_ LEVEL \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)                 | Contiene datos para el [comando OPM \_ SET PROTECTION \_ \_ LEVEL](opm-set-protection-level.md) en OPM.                                                          |
| [**INFORMACIÓN ESTÁNDAR DE OPM \_ \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                         | Contiene el resultado de una solicitud de estado de OPM.                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de OPM](opm-programming-reference.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> </dl>

 

 



