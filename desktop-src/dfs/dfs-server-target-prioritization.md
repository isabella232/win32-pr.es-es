---
title: Asignación de prioridades de destino de servidor DFS
description: La priorización de destino de servidor DFS es una característica disponible en Microsoft Windows Server 2003 con Service Pack 1 (SP1) y sistemas operativos posteriores.
ms.assetid: 0aacebf7-49cc-4287-a5c4-0d25a416d227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e784a540a67f624ca5b8075009cd862c6063427
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275084"
---
# <a name="dfs-server-target-prioritization"></a>Asignación de prioridades de destino de servidor DFS

La priorización de destino de servidor DFS es una característica disponible en Microsoft Windows Server 2003 con Service Pack 1 (SP1) y sistemas operativos posteriores. Esta característica permite que los servidores DFS aprovechen la información disponible sobre el Active Directory de los costos del sitio para priorizar los destinos en las referencias de cliente.

Antes de Windows Server 2003 con SP1, los destinos se agrupaban en dos conjuntos: uno para contener todos los destinos en el mismo sitio que el cliente. y otro grupo para todos los demás destinos. Los destinos que comparten el mismo sitio que el cliente se denominan "en el sitio" y, si el costo del sitio está habilitado, se les asigna un valor de costo específico en relación con el sitio global, con menores costos de sitio preferidos en los más altos.

Con la disponibilidad de este sitio: los datos de costo, los destinos de servidor se pueden priorizar para las estrategias de conmutación por error de servidores DFS más eficaces. En el pasado, este nivel de detalle granular no estaba disponible y los administradores tenían que recurrir a medias artificiales (como sitios ficticios en AD) para admitir incluso requisitos simples como la designación de servidores específicos como un servidor de "copia de seguridad" o "secundario" en el caso de que se produzca un error en el servidor DFS principal. Ahora, con los detalles adicionales proporcionados por los costos del sitio, se pueden realizar estrategias de conmutación por error de varios niveles.

En el siguiente debate se supone que el costo del sitio está habilitado.

## <a name="target-prioritization"></a>Priorización de destino

La prioridad de destino es un orden específico desde una perspectiva administrativa, clasificación y clasificación de servidores en el sitio en términos de preferencias explícitas según el costo del sitio de un cliente DFS. La prioridad global es independiente del costo del sitio. Tenga en cuenta que las clases de prioridad global no indican necesariamente los destinos más óptimos de la perspectiva de un cliente DFS, sino que reflejan la importancia o falta de importancia de los objetivos específicos de la perspectiva de un administrador del sitio.

La prioridad de destino de servidor se divide en dos categorías de valor: clase de prioridad y rango de prioridad. Las clases de prioridad se dividen en dos niveles: local y global. Dentro de estas clases, existe una ordenación aproximada de los destinos según el costo del sitio, agrupados como altos, normales y de baja prioridad. El resultado son cinco clases de prioridad, en orden de mayor a menor prioridad como se indica a continuación:

- Prioridad alta global
- Sitio-costo de alta prioridad
- Prioridad de costo normal del sitio
- Sitio-costo de baja prioridad
- Prioridad baja global

Las clases de costo del sitio se pueden considerar subdivisiones de "prioridad normal global". El rango de prioridad es una clasificación de entero simple basada en valores ordinales: 0, 1, 2 y posteriores, siendo 0 el valor más alto y todos los valores subsiguientes que indican la disminución del rango.

Las prioridades globales alta y baja no tienen en cuenta los valores de costo del sitio. Los destinos con una preferencia de recepción de prioridad alta global sobre todos los demás destinos y los destinos con una prioridad baja global reciben la menor preferencia.

En el orden de una referencia, el proceso completo consta de los siguientes pasos:

1. Se identifican los conjuntos de destinos globales alto y bajo, junto con los destinos "normales globales" restantes.
2. Si se establece la opción "INSITE", se quitan todos los destinos fuera del sitio del cliente. La opción "INSITE" no se aplica a los conjuntos globales de prioridad alta y baja.
3. Dentro de cada uno de estos tres conjuntos, los destinos se ordenan mediante el mecanismo de costo del sitio de AD, mediante el costo de sitio local o completo. El resultado es un conjunto de destinos de igual costo del sitio.
4. Dentro de los conjuntos de objetivos de "normal general" de igual costo del sitio, a los destinos se les asigna una clase de prioridad de las clasificaciones de prioridad alta, normal y baja prioridad.
5. Dentro de los conjuntos de destinos de la misma clase de prioridad y costo del sitio, los destinos se ordenan ahora por rango de prioridad, siendo 0 el rango más alto.
6. Dentro de los conjuntos de destinos de igual costo del sitio, clase de prioridad y rango de prioridad, los destinos se ordenan aleatoriamente para el equilibrio de carga.

Gráficamente, un conjunto de destinos se ordena como se muestra a continuación:

- destinos de clase de alta prioridad global 
- objetivos de clase de prioridad alta de nivel de sitio con costo de sitio = 0
- normal con costo del sitio = 0
- bajo con costo de sitio = 0
- objetivos de clase de prioridad alta de nivel de sitio con costo de sitio = 1
- normal con costo del sitio = 1
- bajo con costo de sitio = 1
- Etcétera.
- destinos de clase de baja prioridad global

Dentro de cada uno de estos conjuntos, los destinos se ordenan según la clasificación de prioridad. El rango más alto es cero, con cada valor entero subsiguiente (1, 2, etc.) que indica un rango cada vez más bajo.

La prioridad de destino se establece en un destino específico de un vínculo (o raíz) en un espacio de nombres DFS. La prioridad de un destino para un vínculo no influye en el orden de otros vínculos si se usa varias veces esa misma ruta de acceso de destino. Por ejemplo, si dos vínculos tienen \\ \\ \\ el servidor share1 como destino, la prioridad de \\ \\ servidor \\ share1 se establece por separado para ambos vínculos.

La prioridad predeterminada para todos los vínculos es la prioridad normal del sitio con un rango de 0. La prioridad de destino no afecta al orden de las referencias a menos que se use, y todos los vínculos existentes se ordenan a medida que se reciben.

La respuesta de referencia de un servidor DFS se compone de conjuntos de destino ordenados tal y como se indicó anteriormente, con cada conjunto de destino no global que contiene destinos del mismo costo de sitio, clase de prioridad y rango de prioridad. Los destinos dentro de cada conjunto se ordenan aleatoriamente. Los clientes DFS que reciben la referencia se inician con el primer destino del primer conjunto y continúan a través de la lista hasta que se encuentra un destino disponible para un vínculo o una raíz DFS determinados.

Para la implementación de API específica de esta característica, consulte los temas de referencia siguientes:

[**DFS_INFO_6**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6) 
 [**DFS_INFO_104**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104) 
 [**DFS_INFO_106**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106) 
 [**DFS_TARGET_PRIORITY**](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority) 
 [**DFS_TARGET_PRIORITY_CLASS**](/windows/win32/api/lmdfs/ne-lmdfs-dfs_target_priority_class~r1)
