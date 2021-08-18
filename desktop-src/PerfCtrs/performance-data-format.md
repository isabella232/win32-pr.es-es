---
description: El formato de los datos recuperados por la función RegQueryValueEx comienza con una estructura de encabezado de longitud fija, PERF \_ DATA \_ BLOCK.
ms.assetid: a68fa617-834c-4ad9-b922-fac3a648ad75
title: Formato de datos de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea20d0cc0be6174fdd945c4bf956d7df60a067cd9f20b3d08d9762d75b8b97a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143924"
---
# <a name="performance-data-format"></a>Formato de datos de rendimiento

El formato de los datos recuperados por la [**función RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) comienza con una estructura de encabezado de longitud fija, [**PERF \_ DATA \_ BLOCK**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block). La **estructura PERF \_ DATA \_ BLOCK** describe el sistema y los datos de rendimiento. La **estructura PERF \_ DATA \_ BLOCK** va seguida de un número variable de elementos de datos de objeto de longitud variable. El encabezado de cada elemento de objeto contiene el desplazamiento del siguiente elemento de objeto de la lista. En el diagrama siguiente se muestra la estructura de datos de rendimiento básica.

![estructura de datos de rendimiento](images/perfdata.png)

Hay dos formatos para los elementos de datos de objeto: uno que admite varias instancias y el otro que no admite varias instancias.

Cada bloque de elementos de datos de objeto contiene [**una estructura \_ PERF OBJECT \_ TYPE,**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) que describe los datos de rendimiento del objeto. La **estructura PERF \_ OBJECT \_ TYPE** va seguida de una lista de estructuras [**PERF COUNTER \_ \_ DEFINITION,**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) una para cada contador definido para el objeto. Para un objeto con una sola instancia, la lista de estructuras **\_ PERF COUNTER \_ DEFINITION** va seguida de una única estructura [**PERF \_ COUNTER \_ BLOCK,**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) seguida de los datos del contador. Cada **estructura PERF \_ COUNTER \_ DEFINITION** contiene el desplazamiento desde el principio de la estructura **COUNTER BLOCK \_ \_ de PERF** a los datos de contador correspondientes. En el diagrama siguiente se muestra la estructura de un objeto de rendimiento que no admite varias instancias.

![Estructura del objeto de rendimiento que no admite varias instancias](images/perfnoinst.png)

Para un tipo de objeto que admite varias instancias, la lista de estructuras [**\_ PERF COUNTER \_ DEFINITION**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) va seguida de una lista de bloques de información de instancia (uno para cada instancia). Cada bloque de información de instancia contiene una [**estructura PERF \_ INSTANCE \_ DEFINITION,**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition) el nombre de la instancia y una [**estructura \_ PERF COUNTER \_ BLOCK.**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) En el diagrama siguiente se muestra la estructura de un objeto de rendimiento que admite dos instancias.

![Estructura de un objeto de rendimiento que admite dos instancias](images/perfinst.png)

Para obtener un ejemplo en el que se usan los desplazamientos, vea [Mostrar nombres de objeto, instancia y contador.](displaying-object-instance-and-counter-names.md)

 

 
