---
description: El conjunto de herramientas de configuración de seguridad de Microsoft es un conjunto de herramientas Microsoft Management Console (MMC) que simplifican la configuración y el análisis de la seguridad del sistema.
ms.assetid: c6558789-84eb-4998-a2c1-725d8a64d255
title: Datos adjuntos de seguridad del servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47cdd0ca3799615125900a3ae6b0b78c26f4abc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259423"
---
# <a name="service-security-attachments"></a>Datos adjuntos de seguridad del servicio

El conjunto de herramientas de configuración de seguridad de Microsoft es un conjunto de herramientas Microsoft Management Console (MMC) que simplifican la configuración y el análisis de la seguridad del sistema. Sin embargo, algunos servicios tienen necesidades de configuración especializadas que van más allá de la configuración de seguridad proporcionada por el conjunto de herramientas estándar. Para controlar esas necesidades, puede ampliar la funcionalidad del conjunto de herramientas escribiendo un archivo adjunto que controle las tareas de seguridad específicas del servicio.

Por ejemplo, Spooler es un servicio Windows NT que define objetos privados, que deben protegerse, por ejemplo, impresoras. El conjunto de herramientas estándar no controla esta funcionalidad y, por tanto, requiere datos adjuntos para controlar la configuración y el análisis de objetos de impresora. La configuración de parámetros de seguridad generales, como la directiva de invocación de servicio, todavía se controla mediante el conjunto de herramientas configuración de seguridad.

Los datos adjuntos del servicio de seguridad amplían la funcionalidad del conjunto de herramientas de configuración de seguridad para admitir configuraciones específicas del servicio.

Los datos adjuntos tienen dos componentes:

-   Extensión de complemento MMC que implementa la interfaz de usuario de datos adjuntos.
-   Motor de datos adjuntos que procesa tareas de análisis y configuración de seguridad específicas del servicio.

Los complementos de configuración de seguridad hospedan la extensión de complemento de datos adjuntos. Se trata de complementos MMC que proporcionan al usuario interfaces para configurar y analizar la configuración de seguridad general de un servicio. Los valores específicos del servicio se configuran mediante la extensión de complemento de datos adjuntos.

Cuando el usuario cambia una configuración, los complementos configuración de seguridad almacenan la nueva información y, a continuación, pasan la solicitud al motor de configuración de seguridad. El motor procesa la solicitud y establece el servicio en la nueva configuración. Si la solicitud afecta a una configuración de seguridad estándar, la controla el motor. Si la solicitud es específica del servicio, el motor llama al motor de datos adjuntos adecuado para controlar la solicitud.

En la ilustración siguiente se muestra cómo funcionan el motor de datos adjuntos y la extensión de complemento en el marco del conjunto de herramientas de configuración de seguridad.

![motor de datos adjuntos y complementos](images/model1a.png)

Para obtener más información sobre el uso del conjunto de herramientas de configuración de seguridad de Microsoft, busque Configuración de seguridad mediante el motor de búsqueda preferido.

 

 



