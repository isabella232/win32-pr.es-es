---
description: Comandos OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Comandos OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa14026123656b26e978bc179d65c3b61913c62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705895"
---
# <a name="opm-commands"></a>Comandos OPM

En esta sección se enumeran los comandos disponibles para el [Administrador de protección de salida](output-protection-manager.md) (OPM).

Para enviar un comando OPM, llame a [**IOPMVideoOutput:: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure). Para cada comando, se muestra la siguiente información.



|              |                                                                                                                                                             |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de comando | Identifica el comando. Establezca el miembro **guidSetting** de la estructura de [**\_ \_ parámetros de configuración de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) igual a este valor. |
| Datos de entrada   | Especifica cómo interpretar la matriz **abParameters** en la estructura [**de \_ \_ parámetros de configuración de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) .                      |



 

Se definen los siguientes comandos:



| Get-Help                                                                                                       | Descripción                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**\_configuración \_ de la \_ \_ señalización de CGMSA de OPM y ACP \_**](opm-set-acp-and-cgmsa-signaling.md)                               | Especifica información sobre la señal de vídeo, excepto el nivel de protección.                      |
| [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md)                                                               | Actualiza el mensaje de renovación de sistema (SRM) para High-Bandwidth Digital Content Protection (HDCP). |
| [**\_nivel de \_ protección de conjunto de OPM \_**](opm-set-protection-level.md)                                               | Establece el nivel de protección de un mecanismo de protección de la salida.                                       |
| [**\_configuración \_ \_ \_ de nivel de protección de OPM según el \_ \_ DVD de CSS \_**](opm-set-protection-level-according-to-css-dvd.md) | Establece el nivel de protección de HDCP para la reproducción de DVD, siguiendo las reglas del sistema de cifrado de contenido (CSS) de DVD. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de OPM](opm-programming-reference.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> </dl>

 

 



