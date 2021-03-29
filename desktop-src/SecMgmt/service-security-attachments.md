---
description: El conjunto de herramientas de configuración de seguridad de Microsoft es un conjunto de herramientas de Microsoft Management Console (MMC) que simplifican la configuración y el análisis de la seguridad del sistema.
ms.assetid: c6558789-84eb-4998-a2c1-725d8a64d255
title: Datos adjuntos de seguridad del servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47cdd0ca3799615125900a3ae6b0b78c26f4abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360217"
---
# <a name="service-security-attachments"></a>Datos adjuntos de seguridad del servicio

El conjunto de herramientas de configuración de seguridad de Microsoft es un conjunto de herramientas de Microsoft Management Console (MMC) que simplifican la configuración y el análisis de la seguridad del sistema. Sin embargo, algunos servicios tienen necesidades de configuración especializadas que van más allá de la configuración de seguridad proporcionada por el conjunto de herramientas estándar. Para controlar esas necesidades, puede extender la funcionalidad del conjunto de herramientas escribiendo datos adjuntos que controlan las tareas de seguridad específicas del servicio.

Por ejemplo, el administrador de trabajos de impresión es un servicio de Windows NT que define objetos privados, que deben protegerse, por ejemplo, impresoras. Esta funcionalidad no está controlada por el conjunto de herramientas estándar y, por tanto, requiere un dato adjunto para controlar la configuración y el análisis de los objetos de impresora. La configuración de los parámetros de seguridad generales, como la Directiva de invocación de servicio, todavía se controla mediante el conjunto de herramientas de configuración de seguridad.

Los datos adjuntos del servicio de seguridad amplían la funcionalidad del conjunto de herramientas de configuración de seguridad para admitir configuraciones específicas del servicio.

Los datos adjuntos tienen dos componentes:

-   Extensión del complemento MMC que implementa la interfaz de usuario de datos adjuntos.
-   Motor de datos adjuntos que procesa tareas de análisis y configuración de seguridad específicas del servicio.

Los complementos de configuración de seguridad hospedan la extensión del complemento de datos adjuntos. Se trata de complementos de MMC que proporcionan al usuario interfaces para configurar y analizar la configuración de seguridad general de un servicio. La configuración específica del servicio se configura mediante la extensión del complemento de datos adjuntos.

Cuando el usuario cambia una opción de configuración, los complementos de configuración de seguridad almacenan la nueva información y, a continuación, pasan la solicitud al motor de configuración de seguridad. El motor procesa la solicitud y establece el servicio en la nueva configuración. Si la solicitud afecta a una configuración de seguridad estándar, la administra el motor. Si la solicitud es específica del servicio, el motor llama al motor de datos adjuntos adecuado para administrar la solicitud.

En la ilustración siguiente se muestra cómo funcionan el motor de datos adjuntos y la extensión del complemento en el marco del conjunto de herramientas de configuración de seguridad.

![complemento y motor de datos adjuntos](images/model1a.png)

Para obtener más información sobre el uso del conjunto de herramientas de configuración de seguridad de Microsoft, busque configuración de seguridad con el motor de búsqueda preferido.

 

 



