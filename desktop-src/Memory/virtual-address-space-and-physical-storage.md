---
description: La cantidad máxima de memoria física admitida por Microsoft Windows oscila entre 2 GB y 2 TB, en función de la versión de Windows.
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: Espacio de direcciones virtuales y almacenamiento físico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d36445eb2639cbfc4db2a6e4abaf28b9af87cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545211"
---
# <a name="virtual-address-space-and-physical-storage"></a>Espacio de direcciones virtuales y almacenamiento físico

La cantidad máxima de memoria física admitida por Microsoft Windows oscila entre 2 GB y 24 TB, dependiendo de la versión de Windows. Para obtener más información, consulte [límites de memoria para las versiones de Windows](memory-limits-for-windows-releases.md). El espacio de direcciones virtuales de cada proceso puede ser menor o mayor que la memoria física total disponible en el equipo. El subconjunto del espacio de direcciones virtuales de un proceso que reside en la memoria física se conoce como espacio de *trabajo*. Si los subprocesos de un proceso intentan usar más memoria física de la que está disponible actualmente, el sistema pagina parte del contenido de la memoria en el disco. La cantidad total de espacio de direcciones virtuales disponible para un proceso está limitada por la memoria física y el espacio libre en disco disponible para el archivo de paginación.

El almacenamiento físico y el espacio de direcciones virtuales de cada proceso se organizan en *páginas*, unidades de memoria, cuyo tamaño depende del equipo host. Por ejemplo, en equipos x86, el tamaño de página del host es de 4 kilobytes.

Para maximizar la flexibilidad en la administración de la memoria, el sistema puede trasladar páginas de la memoria física hacia y desde un archivo de paginación en el disco. Cuando una página se mueve en la memoria física, el sistema actualiza los mapas de páginas de los procesos afectados. Cuando el sistema necesita espacio en la memoria física, mueve las páginas usadas menos recientemente de la memoria física al archivo de paginación. La manipulación de la memoria física por parte del sistema es completamente transparente para las aplicaciones, que solo funcionan en sus espacios de direcciones virtuales.

 

 



