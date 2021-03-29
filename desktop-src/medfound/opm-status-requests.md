---
description: Solicitudes de estado de OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Solicitudes de estado de OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd994d7cb8d43db23fe59352dba830e741b74b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811587"
---
# <a name="opm-status-requests"></a>Solicitudes de estado de OPM

En esta sección se enumeran las solicitudes de estado disponibles para el [Administrador de protección de salida](output-protection-manager.md) (OPM). Para enviar una solicitud de estado de OPM, llame a [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation). Para cada solicitud, se muestra la siguiente información.



|              |                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de solicitud | Identifica la solicitud. Establezca el miembro **guidSetting** de la estructura de parámetros de [**\_ obtención de \_ información \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) igual a este valor. |
| Datos de entrada   | Especifica cómo interpretar la matriz **abParameters** en la estructura [**de \_ \_ \_ parámetros de obtención de información de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) .                      |
| Datos de salida  | Especifica cómo interpretar la matriz **abRequestedInformation** en la estructura [**de \_ \_ información solicitada de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) .         |



 

Se definen las siguientes solicitudes de estado:



| Solicitud de estado                                                                                      | Descripción                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**la \_ \_ \_ señalización de OPM y \_ CGMSA de \_ OPM**](opm-get-acp-and-cgmsa-signaling.md)                     | Devuelve la siguiente información sobre una salida de vídeo:                                                                                               |
| [**\_formato de \_ \_ salida real \_ de OPM**](opm-get-actual-output-format.md)                            | Devuelve una descripción de la señal de vídeo que se transmite a través del conector.                                                               |
| [**\_obtener \_ nivel de \_ protección \_ real de OPM**](opm-get-actual-protection-level.md)                      | Devuelve el nivel de protección global para un mecanismo de protección especificado.                                                                             |
| [**\_tipo de \_ bus de adaptador OPM Get \_ \_**](opm-get-adapter-bus-type.md)                                    | Devuelve el tipo de bus de e/s utilizado por la salida del vídeo.                                                                                                 |
| [**\_información del \_ códec de obtención de OPM \_**](opm-get-codec-info.md)                                                 | Obtiene el valor de mérito de un códec de hardware.                                                                                                             |
| [**\_información de \_ \_ dispositivo HDCP \_ conectado \_ a OPM**](opm-get-connected-hdcp-device-information.md) | Obtiene información acerca de un dispositivo High-Bandwidth Digital Content Protection (HDCP) conectado a la salida de vídeo. Se devuelve la siguiente información: |
| [**\_tipo de \_ conector de obtención de OPM \_**](opm-get-connector-type.md)                                         | Devuelve el tipo de conector físico de la salida de vídeo.                                                                                              |
| [**\_obtener la \_ versión actual de \_ HDCP de HDCP \_ \_**](opm-get-current-hdcp-srm-version.md)                   | Devuelve el número de versión del mensaje de renovación de sistema (SRM) que usa actualmente la salida de vídeo.                                               |
| [**características de la \_ obtención de \_ DVI de OPM \_**](opm-get-dvi-characteristics.md)                               | Consulta si un conector de la interfaz de vídeo digital (DVI) admite DVI versión 1,1 o posterior.                                                          |
| [**\_obtener \_ \_ ID. de salida de OPM**](opm-get-output-id.md)                                                   | Devuelve el identificador único del monitor asociado a esta salida de vídeo.                                                                       |
| [**\_tipos de \_ protección compatible con OPM \_ \_**](opm-get-supported-protection-types.md)                | Devuelve la lista de mecanismos de protección admitidos por el conector.                                                                        |
| [**\_nivel de \_ \_ protección virtual \_ de OPM**](opm-get-virtual-protection-level.md)                    | Devuelve el nivel de protección virtual para un mecanismo de protección especificado.                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de OPM](opm-programming-reference.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> </dl>

 

 



