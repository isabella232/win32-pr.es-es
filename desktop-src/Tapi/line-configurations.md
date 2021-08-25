---
description: Un dispositivo de línea puede representar un grupo de recursos homogéneos (canales) que se usan para establecer llamadas. En un equipo cliente, un TSP normalmente proporciona acceso a uno o varios dispositivos de línea.
ms.assetid: cb599a4d-80dd-40fe-b448-f9ea58f01124
title: Configuraciones de línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d3705854a5bd485dba01452a3885e52c3c2d0baf0d495a65a2db24d75894eeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126255"
---
# <a name="line-configurations"></a>Configuraciones de línea

Un dispositivo de línea puede representar un grupo de recursos homogéneos (canales) que se usan para establecer llamadas. En un equipo cliente, un TSP normalmente proporciona acceso a uno o varios dispositivos de línea.

Estos son algunos ejemplos de cómo un proveedor de servicios puede modelar varias configuraciones:

**Ejemplo 1:** Una sola línea de POTS en los modelos de conexión centrados en el equipo o en el teléfono. El modelo más sencillo es un dispositivo de una sola línea con un canal.

**Ejemplo 2:** Una sola línea BRI-ISDN en los modelos de conexión centrados en el equipo o en el teléfono. El proveedor de servicios tiene una serie de opciones sobre cómo puede querer modelar esto, por ejemplo:

-   Modele la línea BRI como un dispositivo de una sola línea con un grupo de dos canales B que permite combinar ambos canales para establecer llamadas de 128 kbps.
-   Modele cada canal B como un dispositivo de línea independiente y no permitir que ambos canales se combinen en un único canal de 128 kbps.
-   Modele la conexión BRI como dos dispositivos de línea independientes, cada uno de los que se dibujan hasta dos canales de un grupo compartido de dos canales B.
-   Modele como tres dispositivos de línea, uno para cada canal B y otro para la combinación. Claramente, en los dos últimos modelos, los recursos se pueden asignar a distintos dispositivos de línea en momentos diferentes.

**Ejemplo 3:** En los sistemas cliente/servidor, un grupo de puertos telefónicos conectados a un servidor se puede compartir entre varios equipos cliente a través de una red de área local. El grupo se puede administrar para asignar un número máximo de dispositivos de línea (cuota) a cada estación de trabajo cliente. No es inusual que la suma de todas las cuotas supere el número total de líneas. Además, un cliente determinado con una cuota igual a 2 puede satisfacerse mediante los puertos 1 y 2 a la vez y los puertos 7 y 11 más adelante. El proveedor de servicios del grupo puede modelar esta disposición al dar a cada estación de trabajo cliente acceso a dos dispositivos de línea.

Supongamos que la configuración de los proveedores de servicios para un equipo determinado es tal que este proveedor de servicios en particular obtiene un **DeviceIDBase** de 3. Esto implica que los identificadores de dispositivo (fijos) para este cliente son 3 y 4. Si más adelante la aplicación llama a la línea de función TAPI [**2GetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) para el dispositivo 3 y de nuevo para el dispositivo 4, debería ser capaz de asumir que las funcionalidades del dispositivo para cada uno de estos dispositivos son constantes, porque ese es el modelo de dispositivo. Siempre que la configuración del proveedor de servicios del equipo determinado siga siendo constante, los identificadores de dispositivo que aparecen en el nivel de TSPI permanecen constantes, incluso si el servidor cambia las asignaciones de puertos. En el caso de los dispositivos basados en servidor que se agrupan como se describe en el ejemplo 3, solo se admite para los dispositivos de línea que tienen funcionalidades de dispositivo idénticas. Por supuesto, si se cambia la configuración del proveedor de servicios del equipo dado, de modo que este proveedor de servicios obtiene un **DeviceIDBase** diferente, los identificadores de dispositivo cambian en consecuencia.

**Ejemplo 4:** Vínculo de cambio a host:

-   Para proporcionar telefonía personal a cada escritorio, el proveedor de servicios podría modelar la línea DE LAN emparejada con el equipo como un dispositivo de una sola línea con un canal. Cada equipo cliente tendría un dispositivo de línea disponible.
-   Cada estación de terceros se podría modelar como un dispositivo de línea independiente. Esto permite que la aplicación controle las llamadas en otras estaciones. Esta solución requiere que la aplicación abra cada línea que quiera manipular o supervisar, lo que puede ser bueno si solo un número pequeño de líneas es de interés, pero puede generar una gran sobrecarga si hay un gran número de líneas implicadas.
-   El conjunto de todas las estaciones de terceros se podría modelar como un dispositivo de una sola línea con una dirección (número de teléfono) asignada por estación. Solo se abrirá un único dispositivo, lo que proporciona supervisión y control de todas las direcciones de la línea (todas las estaciones). Para originar una llamada en cualquiera de estas estaciones, la aplicación solo necesita especificar la dirección de la estación a la operación que realiza la llamada. No se requiere ninguna operación de apertura adicional. Este modelado implica que todas las estaciones tienen las mismas funcionalidades de dispositivo de línea, aunque sus capacidades de dirección podrían ser diferentes.

> [!Note]  
> Todos estos ejemplos son simplemente diferentes maneras en que un proveedor de servicios puede optar por implementar la asignación del comportamiento del dispositivo de línea en alguna realización física.

 

 

 
