---
description: El sistema utiliza contadores para recopilar datos de rendimiento.
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: Specifying a Counter Path (Especificar una ruta de acceso de contador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3a92f94b4bf3d2252903d92785f43bb0cac110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667247"
---
# <a name="specifying-a-counter-path"></a>Specifying a Counter Path (Especificar una ruta de acceso de contador)

El sistema utiliza contadores para recopilar datos de rendimiento. Cada contador se identifica de forma única a través de su nombre y su ruta de acceso, o ubicación. La sintaxis de una ruta de contador es:

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

El elemento Computer especifica el nombre o la dirección IP del equipo desde el que desea consultar los datos de rendimiento. El nombre del equipo es opcional si el contador se encuentra en el equipo local.

El elemento PerfObject especifica el objeto de rendimiento que se va a consultar. Un objeto de rendimiento puede ser un componente físico, como procesadores, discos y memoria, o un objeto del sistema, como procesos y subprocesos. Cada objeto del sistema está relacionado con un elemento funcional del equipo y tiene un conjunto de contadores estándar asignados. Cada equipo puede tener un conjunto diferente de objetos y contadores de rendimiento instalados en él, ya que las aplicaciones pueden instalar sus propios objetos y contadores de rendimiento. Para obtener una lista de los objetos y contadores de rendimiento instalados en el equipo, vea el cuadro de diálogo **Agregar contadores** en la herramienta rendimiento del equipo. Estos objetos también se muestran en el cuadro de diálogo examinar de PDH (vea [contadores de exploración](browsing-counters.md)). Para obtener una lista de los objetos y contadores de rendimiento del sistema, vea [contadores por objeto](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).

ParentInstance, ObjectInstance y InstanceIndex se incluyen en la ruta de acceso si pueden existir varias instancias del objeto. Por ejemplo, los procesos y subprocesos son varios objetos de instancia porque se puede ejecutar más de un proceso o subproceso al mismo tiempo. Si un objeto puede tener más de una instancia, la ruta de acceso del contador debe especificar una instancia de objeto.

El formato de los elementos relacionados con la instancia depende del tipo de objeto. Si el objeto tiene instancias simples, el formato es solo el nombre de la instancia entre paréntesis. Por ejemplo:

``` syntax
(Explorer)
```

Si la instancia de este objeto también requiere un nombre de instancia primaria, el nombre de la instancia primaria debe ir delante de la instancia del objeto y estar separado por un carácter de barra diagonal. Por ejemplo, los subprocesos pertenecen a procesos. Si consulta un objeto de subproceso, también debe especificar el proceso al que pertenece, tal como se muestra en el ejemplo siguiente:

``` syntax
(Explorer/0)
```

Si el objeto tiene varias instancias que tienen la misma cadena de nombre, se pueden indexar secuencialmente especificando el índice de instancia precedido por un signo de almohadilla. Los índices de instancia se basan en 0. Si desea consultar la primera instancia, no incluya \# 0, simplemente especifique el nombre de la instancia. Para especificar la segunda instancia, use \# 1; para especificar la tercera instancia, use \# 2; y así sucesivamente. Por ejemplo:

``` syntax
(Explorer/0#1)
```

El elemento Counter especifica el contador de rendimiento que desea consultar para el objeto de rendimiento dado.

PDH usa los siguientes caracteres especiales en una ruta de acceso de contador. Los proveedores no deben usar estos caracteres en sus nombres. Si un proveedor usa estos caracteres especiales, PDH no puede analizar la ruta de acceso completa del contador para obtener los nombres del contador y de las instancias.



| Carácter | Descripción                                                |
|-----------|------------------------------------------------------------|
| \\        | Separador genérico para el equipo, el objeto y el contador.       |
| (         | Inicio del nombre de instancia.                                |
| )         | Final del nombre de instancia.                                   |
| /         | Separa la instancia y la instancia primaria.                    |
| \#n       | Identifica una aparición específica de una instancia con el mismo nombre. |
| \*        | Carácter comodín.                                        |



 

En los ejemplos siguientes se muestran los posibles formatos de las rutas de acceso de contador:

-   \\\\contador de objeto de equipo \\ (índice de instancia/principal \# ) \\
-   \\\\\\contador objeto de equipo (principal/instancia) \\
-   \\\\contador de objeto de equipo \\ (índice de instancia \# ) \\
-   \\\\contador de objeto de equipo \\ (instancia) \\
-   \\\\\\contador de objetos de equipo \\
-   \\contador de objeto (índice de instancia/principal \# ) \\
-   \\contador de objeto (primario/instancia) \\
-   \\contador de objeto (índice de instancia \# ) \\
-   \\contador de objeto (instancia) \\
-   \\contador de objetos \\

## <a name="using-wildcard-characters"></a>Usar caracteres comodín

Las rutas de acceso de contador solo pueden contener un carácter comodín para el nombre de instancia, tal y como se muestra en el ejemplo siguiente.

``` syntax
\Process(*)\% Processor Time
```

Para expandir el carácter comodín en una lista de rutas de acceso de contador que contengan instancias encontradas en el equipo o en el archivo de registro, llame a [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).

 

 
