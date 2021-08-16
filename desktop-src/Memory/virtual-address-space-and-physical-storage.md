---
description: La cantidad máxima de memoria física compatible con Microsoft Windows oscila entre 2 GB y 2 TB, dependiendo de la versión de Windows.
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: Espacio de direcciones virtuales y Storage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 774e0af302fbd965f16b09a88d6dabb7c95948855c8d939d3c856ebe098337d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386160"
---
# <a name="virtual-address-space-and-physical-storage"></a>Espacio de direcciones virtuales y Storage

La cantidad máxima de memoria física admitida por Microsoft Windows oscila entre 2 GB y 24 TB, dependiendo de la versión de Windows. Para obtener más información, vea [Límites de memoria para Windows versiones](memory-limits-for-windows-releases.md). El espacio de direcciones virtuales de cada proceso puede ser menor o mayor que la memoria física total disponible en el equipo. El subconjunto del espacio de direcciones virtuales de un proceso que reside en la memoria física se conoce como el *espacio de trabajo*. Si los subprocesos de un proceso intentan usar más memoria física de la que está disponible actualmente, el sistema pagina parte del contenido de la memoria en el disco. La cantidad total de espacio de direcciones virtuales disponible para un proceso está limitada por la memoria física y el espacio disponible en el disco para el archivo de paginación.

El almacenamiento físico y el espacio de direcciones virtuales de cada proceso se organizan en páginas *,* unidades de memoria, cuyo tamaño depende del equipo host. Por ejemplo, en equipos x86, el tamaño de página del host es de 4 kilobytes.

Para maximizar su flexibilidad en la administración de memoria, el sistema puede mover páginas de memoria física hacia y desde un archivo de paginación en disco. Cuando una página se mueve a la memoria física, el sistema actualiza los mapas de página de los procesos afectados. Cuando el sistema necesita espacio en la memoria física, mueve las páginas de memoria física usadas menos recientemente al archivo de paginación. La manipulación de la memoria física por parte del sistema es completamente transparente para las aplicaciones, que solo funcionan en sus espacios de direcciones virtuales.

 

 



