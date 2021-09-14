---
description: El espacio de direcciones virtuales para un proceso es el conjunto de direcciones de memoria virtual que puede usar. El espacio de direcciones de cada proceso es privado y otros procesos no pueden acceder a él a menos que se comparta.
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: Espacio de direcciones virtuales (administración de memoria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6584d0404799e6b0e5ab343c7d8b39d7f8d741a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159792"
---
# <a name="virtual-address-space-memory-management"></a>Espacio de direcciones virtuales (administración de memoria)

El espacio de direcciones virtuales para un proceso es el conjunto de direcciones de memoria virtual que puede usar. El espacio de direcciones de cada proceso es privado y otros procesos no pueden acceder a él a menos que se comparta.

Una dirección virtual no representa la ubicación física real de un objeto en memoria; en su lugar, el sistema mantiene una tabla *de* páginas para cada proceso, que es una estructura de datos interna que se usa para traducir direcciones virtuales en sus direcciones físicas correspondientes. Cada vez que un subproceso hace referencia a una dirección, el sistema convierte la dirección virtual en una dirección física.

El espacio de direcciones virtuales para el Windows de 32 bits tiene un tamaño de 4 gigabytes (GB) y se divide en dos particiones: una para su uso por el proceso y la otra reservada para su uso por el sistema. Para obtener más información sobre el espacio de direcciones virtuales en Windows de 64 bits, vea Espacio de direcciones virtuales en Windows de [64 Windows](../winprog64/virtual-address-space.md).

Para obtener más información sobre la memoria virtual, vea los temas siguientes:

-   [Espacio de direcciones virtuales y espacio de direcciones Storage](virtual-address-space-and-physical-storage.md)
-   [Espacio de trabajo](working-set.md)
-   [Estado de la página](page-state.md)
-   [Ámbito de la memoria asignada](scope-of-allocated-memory.md)
-   [Prevención de ejecución de datos](data-execution-prevention.md)
-   [Protección de la memoria](memory-protection.md)
-   [Límites de memoria para Windows versiones anteriores](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a>Espacio de direcciones virtuales predeterminado para máquinas virtuales de 32 Windows

En la tabla siguiente se muestra el intervalo de memoria predeterminado para cada partición.



| Intervalo de memoria                             | Uso                |
|------------------------------------------|----------------------|
| Bajo de 2 GB (0x00000000 a 0x7FFFFFFF)  | Usado por el proceso. |
| Alto de 2 GB (0x80000000 a 0xFFFFFFFF) | Usado por el sistema.  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a>Espacio de direcciones virtuales para máquinas virtuales de 32 Windows con 4GT

Si [la optimización de 4 gigabytes](4-gigabyte-tuning.md) (4GT) está habilitada, el intervalo de memoria para cada partición es el siguiente.



| Intervalo de memoria                             | Uso                |
|------------------------------------------|----------------------|
| Bajo de 3 GB (0x00000000 a 0xBFFFFFFF)  | Usado por el proceso. |
| Alto de 1 GB (0xC0000000 a 0xFFFFFFFF) | Usado por el sistema.  |



 

Después de habilitar 4GT, un proceso que tenga la marca [**IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) establecida en su encabezado de imagen tendrá acceso a los 1 GB de memoria adicionales por encima de los 2 GB bajos.

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a>Ajustar el espacio de direcciones virtuales para las máquinas virtuales de 32 Windows

Puede usar el siguiente comando para establecer una opción de entrada de arranque que configure el tamaño de la partición que está disponible para su uso por el proceso en un valor entre 2048 (2 GB) y 3072 (3 GB):

[BCDEdit /set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *Megabytes*

Una vez establecida la opción de entrada de arranque, el intervalo de memoria de cada partición es el siguiente.



| Intervalo de memoria                            | Uso                |
|-----------------------------------------|----------------------|
| Bajo (0x00000000 a *megabytes*)    | Usado por el proceso. |
| Alto *(megabytes*+1 a 0xFFFFFFFF) | Usado por el sistema.  |



 

**Windows Server 2003:** Establezca el **modificador /USERVA** boot.ini un valor entre 2048 y 3072.

 

 
