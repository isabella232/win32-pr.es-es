---
description: Un dispositivo de línea puede representar un grupo de recursos homogéneos (canales) que se utilizan para establecer llamadas. En un equipo cliente, un TSP normalmente proporciona acceso a uno o varios dispositivos de línea.
ms.assetid: cb599a4d-80dd-40fe-b448-f9ea58f01124
title: Configuraciones de línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722dab15763822f6535783ecc8bc18e681e13ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908211"
---
# <a name="line-configurations"></a>Configuraciones de línea

Un dispositivo de línea puede representar un grupo de recursos homogéneos (canales) que se utilizan para establecer llamadas. En un equipo cliente, un TSP normalmente proporciona acceso a uno o varios dispositivos de línea.

Estos son algunos ejemplos de cómo un proveedor de servicios puede modelar diversas configuraciones:

**Ejemplo 1:** Una sola línea de POTS en los modelos de conexión centrados en el equipo o en el teléfono. El modelo más sencillo es un dispositivo de una sola línea con un canal.

**Ejemplo 2:** Una sola línea BRI-ISDN en los modelos de conexión centrados en el equipo o en el teléfono. El proveedor de servicios tiene varias opciones para que pueda modelar este, por ejemplo:

-   Modelar la línea BRI como un dispositivo de una sola línea con un grupo de dos canales B que permite combinar ambos canales para establecer llamadas de 128 kbps.
-   Modelar cada canal B como un dispositivo de línea independiente y no permitir que ambos canales se combinen en un solo canal de 128 kbps.
-   Modelar la conexión BRI como dos dispositivos de línea independientes, cada uno de los cuales dibuja hasta dos canales desde un grupo compartido de dos canales B.
-   Modelo como tres dispositivos de línea, uno para cada canal B y otro para la combinación. Claramente en los dos últimos modelos, los recursos pueden asignarse a diferentes dispositivos de línea en momentos diferentes.

**Ejemplo 3:** En los sistemas cliente/servidor, un grupo de puertos de teléfono conectados a un servidor puede compartirse entre varios equipos cliente a través de una red de área local. El grupo se puede administrar para asignar un número máximo de dispositivos de línea (cuota) a cada estación de trabajo cliente. No es raro que la suma de todas las cuotas supere el número total de líneas. Además, un cliente determinado cuya cuota sea igual a 2 se puede satisfacer mediante los puertos 1 y 2 a la vez y los puertos 7 y 11 en un momento posterior. El proveedor de servicios del grupo puede modelar esta disposición proporcionando a cada estación de trabajo del cliente acceso a dos dispositivos de línea.

Supongamos que la configuración de proveedores de servicios para un equipo determinado es tal que este proveedor de servicios concreto obtiene un **DeviceIDBase** de 3. Esto implica que los identificadores de dispositivo (fijos) para este cliente son 3 y 4. Si posteriormente la aplicación llama a la función [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) de TAPI 2 para el dispositivo 3 y de nuevo para el dispositivo 4, debe ser capaz de asumir que las capacidades del dispositivo para cada uno de estos dispositivos son constantes, ya que ese es el modelo del dispositivo. Siempre y cuando la configuración del proveedor de servicios del equipo determinada permanezca constante, los identificadores de dispositivo que aparecen en el nivel TSPI permanecen constantes, incluso si el servidor cambia las asignaciones de puerto. En el caso de los dispositivos basados en servidor que se agrupan como se describe en el ejemplo 3, esto solo se aplica a los dispositivos de línea que tienen funcionalidades de dispositivo idénticas. Por supuesto, si se cambia la configuración del proveedor de servicios del equipo determinado, de modo que este proveedor de servicios obtenga un **DeviceIDBase** diferente, los identificadores de dispositivo cambiarán de forma correspondiente.

**Ejemplo 4:** Vínculo de cambio a host:

-   Para proporcionar telefonía personal a cada escritorio, el proveedor de servicios podría modelar la línea de PBX emparejada con el equipo como un dispositivo de una sola línea con un canal. Cada equipo cliente tendrá disponible un dispositivo de línea.
-   Cada estación de terceros podría modelarse como un dispositivo de línea independiente. Esto permite que la aplicación controle las llamadas en otras estaciones. Esta solución requiere que la aplicación abra cada línea que desee manipular o supervisar, lo que puede ser adecuado si solo un número pequeño de líneas es de interés, pero puede generar una gran sobrecarga si se implica un gran número de líneas.
-   El conjunto de todas las estaciones de terceros podría modelarse como un dispositivo de una sola línea con una dirección (número de teléfono) asignada por estación. Solo se abrirá un único dispositivo, lo que proporcionará supervisión y control de todas las direcciones de la línea (todas las estaciones). Para originar una llamada en cualquiera de estas estaciones, la aplicación solo tiene que especificar la dirección de la estación para la operación que realiza la llamada. No se requiere ninguna operación de apertura adicional. Este modelado implica que todas las estaciones tienen las mismas funcionalidades de dispositivo de línea, aunque sus capacidades de dirección podrían ser diferentes.

> [!Note]  
> Todos estos ejemplos son simplemente diferentes maneras en que un proveedor de servicios puede optar por implementar la asignación del comportamiento de los dispositivos de línea en alguna realización física.

 

 

 
