---
description: El espacio de direcciones virtuales para un proceso es el conjunto de direcciones de memoria virtual que puede usar. El espacio de direcciones de cada proceso es privado y no es accesible para otros procesos a menos que sea compartido.
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: Espacio de direcciones virtuales (administración de memoria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6584d0404799e6b0e5ab343c7d8b39d7f8d741a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001297"
---
# <a name="virtual-address-space-memory-management"></a>Espacio de direcciones virtuales (administración de memoria)

El espacio de direcciones virtuales para un proceso es el conjunto de direcciones de memoria virtual que puede usar. El espacio de direcciones de cada proceso es privado y no es accesible para otros procesos a menos que sea compartido.

Una dirección virtual no representa la ubicación física real de un objeto en la memoria; en su lugar, el sistema mantiene una *tabla de páginas* para cada proceso, que es una estructura de datos interna que se usa para traducir direcciones virtuales en sus direcciones físicas correspondientes. Cada vez que un subproceso hace referencia a una dirección, el sistema traduce la dirección virtual a una dirección física.

El espacio de direcciones virtuales para Windows de 32 bits tiene un tamaño de 4 gigabytes (GB) y se divide en dos particiones: una para su uso por parte del proceso y la otra reservada para su uso por parte del sistema. Para obtener más información sobre el espacio de direcciones virtuales en Windows de 64 bits, consulte [espacio de direcciones virtuales en Windows de 64 bits](../winprog64/virtual-address-space.md).

Para obtener más información acerca de la memoria virtual, vea los temas siguientes:

-   [Espacio de direcciones virtuales y almacenamiento físico](virtual-address-space-and-physical-storage.md)
-   [Espacio de trabajo](working-set.md)
-   [Estado de la página](page-state.md)
-   [Ámbito de la memoria asignada](scope-of-allocated-memory.md)
-   [Prevención de ejecución de datos](data-execution-prevention.md)
-   [Protección de la memoria](memory-protection.md)
-   [Límites de memoria para las versiones de Windows](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a>Espacio de direcciones virtual predeterminado para Windows de 32 bits

En la tabla siguiente se muestra el intervalo de memoria predeterminado para cada partición.



| Intervalo de memoria                             | Uso                |
|------------------------------------------|----------------------|
| 2 GB inferiores (de 0x00000000 a 0x7FFFFFFF)  | Utilizado por el proceso. |
| 2 GB superiores (0x80000000 a 0xFFFFFFFF) | Utilizado por el sistema.  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a>Espacio de direcciones virtuales para Windows de 32 bits con 4GT

Si está habilitada la [optimización de 4 gigabytes](4-gigabyte-tuning.md) (4GT), el intervalo de memoria para cada partición es el siguiente.



| Intervalo de memoria                             | Uso                |
|------------------------------------------|----------------------|
| 3 GB bajos (0x00000000 a 0xBFFFFFFF)  | Utilizado por el proceso. |
| 1 GB alto (de 0xC0000000 a 0xFFFFFFFF) | Utilizado por el sistema.  |



 

Una vez habilitada la opción 4GT, un proceso que tiene la marca [**\_ \_ \_ \_ reconocimiento de direcciones grandes del archivo de imagen**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) establecida en su encabezado de imagen tendrá acceso a los 1 GB de memoria adicionales por encima de 2 GB de nivel inferior.

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a>Ajuste del espacio de direcciones virtuales para Windows de 32 bits

Puede usar el siguiente comando para establecer una opción de entrada de arranque que configure el tamaño de la partición que está disponible para que la use el proceso en un valor entre 2048 (2 GB) y 3072 (3 GB):

[Bcdedit/Set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *megabytes*

Después de establecer la opción de entrada de arranque, el intervalo de memoria para cada partición es el siguiente.



| Intervalo de memoria                            | Uso                |
|-----------------------------------------|----------------------|
| Bajo (de 0x00000000 a *megabytes*)    | Utilizado por el proceso. |
| Alto (*megabytes*+ 1 hasta 0xFFFFFFFF) | Utilizado por el sistema.  |



 

**Windows Server 2003:** Establezca el modificador **/USERVA** en boot.ini en un valor entre 2048 y 3072.

 

 
