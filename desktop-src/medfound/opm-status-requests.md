---
description: Solicitudes de estado de OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Solicitudes de estado de OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c78f3725132110e8a97356f2e7e3377f10cddc4c2c1346e9256c55663d818f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058665"
---
# <a name="opm-status-requests"></a>Solicitudes de estado de OPM

En esta sección se enumeran las solicitudes de estado disponibles para [Output Protection Manager](output-protection-manager.md) (OPM). Para enviar una solicitud de estado de OPM, llame a [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation). Para cada solicitud, se muestra la siguiente información.



| Valor             | Descripción                                                                                                                                                           |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de solicitud | Identifica la solicitud. Establezca el **miembro guidSetting** de la estructura [**OPM \_ GET INFO \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) igual a este valor. |
| Datos de entrada   | Especifica cómo interpretar la matriz **abParameters** en la [**estructura OPM \_ GET INFO \_ \_ PARAMETERS.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)                      |
| Datos de salida  | Especifica cómo interpretar la matriz **abRequestedInformation** en la [**estructura OPM \_ REQUESTED \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)         |



 

Se definen las siguientes solicitudes de estado:



| Solicitud de estado                                                                                      | Descripción                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OPM \_ GET \_ ACP \_ AND \_ CGMSA \_ SIGNALING**](opm-get-acp-and-cgmsa-signaling.md)                     | Devuelve la siguiente información sobre una salida de vídeo:                                                                                               |
| [**OPM \_ GET REAL OUTPUT \_ \_ \_ FORMAT**](opm-get-actual-output-format.md)                            | Devuelve una descripción de la señal de vídeo que se transmite a través del conector.                                                               |
| [**OPM \_ GET REAL PROTECTION \_ \_ \_ LEVEL**](opm-get-actual-protection-level.md)                      | Devuelve el nivel de protección global para un mecanismo de protección especificado.                                                                             |
| [**OPM \_ GET \_ ADAPTER \_ BUS \_ TYPE**](opm-get-adapter-bus-type.md)                                    | Devuelve el tipo de bus de E/S usado por la salida de vídeo.                                                                                                 |
| [**OPM \_ GET \_ CODEC \_ INFO**](opm-get-codec-info.md)                                                 | Obtiene el valor de meritorio de un códec de hardware.                                                                                                             |
| [**OPM \_ GET \_ CONNECTED \_ HDCP \_ DEVICE \_ INFORMATION**](opm-get-connected-hdcp-device-information.md) | Obtiene información sobre un High-Bandwidth de Content Protection digital (HDCP) conectado a la salida de vídeo. Se devuelve la siguiente información: |
| [**OPM \_ GET \_ CONNECTOR \_ TYPE**](opm-get-connector-type.md)                                         | Devuelve el tipo de conector físico de la salida de vídeo.                                                                                              |
| [**OPM \_ GET \_ CURRENT \_ HDCP \_ SRM \_ VERSION**](opm-get-current-hdcp-srm-version.md)                   | Devuelve el número de versión del mensaje de renovación del sistema (SRM) utilizado actualmente por la salida de vídeo.                                               |
| [**CARACTERÍSTICAS DE OPM \_ GET \_ \_ DVI**](opm-get-dvi-characteristics.md)                               | Consulta si un conector de interfaz de vídeo digital (DVI) admite DVI versión 1.1 o posterior.                                                          |
| [**OPM \_ GET \_ OUTPUT \_ ID**](opm-get-output-id.md)                                                   | Devuelve el identificador único del monitor asociado a esta salida de vídeo.                                                                       |
| [**OPM \_ GET \_ SUPPORTED \_ PROTECTION \_ TYPES**](opm-get-supported-protection-types.md)                | Devuelve la lista de mecanismos de protección admitidos por el conector.                                                                        |
| [**OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL**](opm-get-virtual-protection-level.md)                    | Devuelve el nivel de protección virtual para un mecanismo de protección especificado.                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de OPM](opm-programming-reference.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> </dl>

 

 



