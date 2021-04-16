---
description: El formato de los datos recuperados por la función RegQueryValueEx comienza con una estructura de encabezado de longitud fija, un bloque de datos de rendimiento \_ \_ .
ms.assetid: a68fa617-834c-4ad9-b922-fac3a648ad75
title: Formato de datos de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88029634594843a50fd6010993eb6517dce831f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567740"
---
# <a name="performance-data-format"></a>Formato de datos de rendimiento

El formato de los datos recuperados por la función [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) comienza con una estructura de encabezado de longitud fija, un [**bloque de \_ datos \_ de rendimiento**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block). La estructura de **\_ \_ bloque de datos** de rendimiento describe el sistema y los datos de rendimiento. La estructura de **\_ \_ bloque de datos de rendimiento** va seguida de un número variable de elementos de datos de objeto de longitud variable. El encabezado de cada elemento de objeto contiene el desplazamiento del siguiente elemento de objeto de la lista. En el diagrama siguiente se muestra la estructura básica de datos de rendimiento.

![estructura de datos de rendimiento](images/perfdata.png)

Hay dos formatos para los elementos de datos de objeto: uno que admite varias instancias y otro que no admite varias instancias.

Cada bloque de elementos de datos de objeto contiene una estructura de [**\_ \_ tipo de objeto de rendimiento**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) , que describe los datos de rendimiento para el objeto. La estructura de **\_ \_ tipo de objeto Perf** va seguida de una lista de estructuras de [**\_ \_ definición de contadores de rendimiento**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) , una para cada contador definida para el objeto. Para un objeto con una sola instancia, la lista de estructuras de **\_ \_ definición de contadores de rendimiento** va seguida de una única estructura de [**\_ \_ bloques de contadores de rendimiento**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) , seguida de los datos del contador. Cada estructura de **\_ \_ definición de contador de rendimiento** contiene el desplazamiento desde el inicio de la estructura de **\_ \_ bloques de contadores de rendimiento** a los datos de contador correspondientes. En el diagrama siguiente se muestra la estructura de un objeto de rendimiento que no admite varias instancias.

![estructura del objeto de rendimiento que no admite varias instancias](images/perfnoinst.png)

Para un tipo de objeto que admite varias instancias, la lista de estructuras de [**\_ \_ definición de contadores de rendimiento**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) va seguida de una lista de bloques de información de instancia (uno para cada instancia). Cada bloque de información de instancia contiene una estructura de [**\_ \_ definición de instancia de rendimiento**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition) , el nombre de la instancia y una estructura de [**\_ \_ bloques de contadores de rendimiento**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) . En el diagrama siguiente se muestra la estructura de un objeto de rendimiento que admite dos instancias de.

![estructura de un objeto de rendimiento que admite dos instancias](images/perfinst.png)

Para obtener un ejemplo en el que se usan los desplazamientos, vea [Mostrar los nombres de objeto, instancia y contador](displaying-object-instance-and-counter-names.md).

 

 
