---
title: Priorización de destinos del servidor DFS
description: La priorización de destino del servidor DFS es una característica disponible en Microsoft Windows Server 2003 con Service Pack 1 (SP1) y sistemas operativos posteriores.
ms.assetid: 0aacebf7-49cc-4287-a5c4-0d25a416d227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23140a1e35d1980427012a0728f5acbc62f3ac0ef5dc288183e50f1ce29255a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895675"
---
# <a name="dfs-server-target-prioritization"></a>Priorización de destinos del servidor DFS

La priorización de destino del servidor DFS es una característica disponible en Microsoft Windows Server 2003 con Service Pack 1 (SP1) y sistemas operativos posteriores. Esta característica permite a los servidores DFS aprovechar las ventajas de la información Active Directory costo del sitio para priorizar los destinos en las referencias de cliente.

Antes Windows Server 2003 con SP1, los destinos se agrupaban en dos conjuntos: un grupo para contener todos los destinos en el mismo sitio que el cliente; y otro grupo para todos los demás destinos. Esos destinos que comparten el mismo sitio que el cliente se denominan "in-site" y, si el costo del sitio está habilitado, se les asigna un valor de costo específico en relación con el sitio en general, con costos de sitio más bajos preferidos sobre los más altos.

Con la disponibilidad de estos datos de costos de sitio, se puede priorizar los destinos de servidor para estrategias de conmutación por error de servidor DFS más eficaces. En el pasado, este nivel granular de detalle no estaba disponible y los administradores tenían que recurrir a medios artificiales (como sitios ficticios en AD) para admitir incluso requisitos sencillos, como la designación de servidores específicos como un servidor de "copia de seguridad" o "secundario" en caso de que se produce un error en un servidor DFS "principal". Ahora, con los detalles adicionales proporcionados por el costo del sitio, son posibles estrategias de conmutación por error de varios niveles.

En la siguiente explicación se da por supuesto que está habilitado el costo del sitio.

## <a name="target-prioritization"></a>Priorización de destino

La prioridad de destino es una ordenación específica desde una perspectiva administrativa, la clasificación y clasificación de servidores en el sitio en términos de preferencia explícita en función de su costo de sitio de un cliente DFS. La prioridad global es independiente del costo del sitio. Tenga en cuenta que las clases de prioridad global no indican necesariamente los destinos más óptimos desde la perspectiva de un cliente DFS, sino que reflejan la importancia, o falta de importancia, de destinos específicos desde la perspectiva del administrador del sitio.

La prioridad de destino del servidor se divide en dos categorías de valor: clase de prioridad y rango de prioridad. Las clases de prioridad se dividen en dos niveles: local y global. Dentro de estas clases hay una ordenación aproximada de los destinos en función del costo del sitio, agrupados como prioridad alta, normal y baja. El resultado son cinco clases de prioridad, en orden de prioridad más alta a menor como se muestra a continuación:

- Prioridad alta global
- Prioridad alta del costo del sitio
- Prioridad normal del costo del sitio
- Prioridad baja de costo de sitio
- Prioridad baja global

Las clases de costo de sitio se pueden considerar como subdivisiones de "prioridad normal global". Rango de prioridad es una clasificación de entero simple basada en valores ordinales: 0, 1, 2 y versiones posteriores, siendo 0 el valor más alto y todos los valores posteriores que indican una clasificación decreciente.

Las prioridades globales altas y bajas no tienen en cuenta los valores de costo del sitio. Los destinos con una prioridad alta global reciben preferencias sobre todos los demás destinos y los destinos con una prioridad baja global reciben la menor preferencia.

Para ordenar una referencia, el proceso completo tiene los pasos siguientes:

1. Se identifican los conjuntos de destinos globales altos y bajos, junto con los destinos "normales globales" restantes.
2. Si se establece la opción "INSITE", se quitan todos los destinos fuera del sitio del cliente. La opción "INSITE" no se aplica a los conjuntos globales de prioridad alta y baja.
3. Dentro de cada uno de estos tres conjuntos, los destinos se ordenan mediante el mecanismo de costo del sitio de AD, mediante el costo del sitio local o completo. El resultado son conjuntos de destinos de igual costo de sitio.
4. Dentro de los conjuntos de destinos "normales globales" del mismo costo de sitio, a los destinos se les asigna una clase de prioridad de las clasificaciones de prioridad alta, normal y de bajo costo del sitio.
5. Dentro de los conjuntos de destinos de la misma clase de prioridad y costo de sitio, los destinos ahora se ordenan por rango de prioridad, siendo 0 la clasificación más alta.
6. Dentro de los conjuntos de destinos con el mismo costo de sitio, clase de prioridad y rango de prioridad, los destinos se ordenan aleatoriamente para el equilibrio de carga.

Gráficamente, un conjunto de destinos se ordenan como se muestra a continuación:

- objetivos de clase de prioridad alta global 
- destinos de clase de alta prioridad de costo de sitio con costo de sitio = 0
- normal con costo de sitio = 0
- bajo con costo de sitio = 0
- destinos de clase de alta prioridad de costo de sitio con costo de sitio = 1
- normal con costo de sitio = 1
- bajo con costo de sitio = 1
- Etcétera.
- objetivos de clase global de prioridad baja

Dentro de cada uno de estos conjuntos, los destinos se ordenan según el rango de prioridad. La clasificación más alta es cero, con cada valor entero subsiguiente (1, 2, y así sucesivamente) que indica una clasificación cada vez más baja.

La prioridad de destino se establece en un destino específico de un vínculo (o raíz) en un espacio de nombres DFS. La prioridad de un destino para un vínculo no influye en el orden de otros vínculos si esa misma ruta de acceso de destino se usa varias veces. Por ejemplo, si dos vínculos tienen server share1 como destino, la prioridad de server share1 se establece \\ \\ por separado para \\ ambos \\ \\ \\ vínculos.

La prioridad predeterminada para todos los vínculos es la prioridad normal del costo del sitio con un rango de 0. La prioridad de destino no afecta al orden de las referencias a menos que se utilice y todos los vínculos existentes se ordenan a medida que se reciben.

La respuesta de referencia de un servidor DFS consta de conjuntos de destino ordenados como se indicó anteriormente, y cada conjunto de destinos no global contiene destinos del mismo costo de sitio, clase de prioridad y rango de prioridad. Los destinos dentro de cada conjunto se ordenan aleatoriamente. Los clientes DFS que reciben la referencia comienzan con el primer destino del primer conjunto y continúan por la lista hasta que se encuentra un destino disponible para una raíz o vínculo DFS determinado.

Para la implementación de API específica de esta característica, consulte los siguientes temas de referencia:

[**DFS_INFO_6**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6) 
 [**DFS_INFO_104**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104) 
 [**DFS_INFO_106**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106) 
 [**DFS_TARGET_PRIORITY**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority) 
 [**DFS_TARGET_PRIORITY_CLASS**](/windows/win32/api/lmdfs/ne-lmdfs-dfs_target_priority_class~r1)
