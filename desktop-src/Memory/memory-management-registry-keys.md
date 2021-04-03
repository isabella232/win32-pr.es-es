---
description: El espacio de la dirección virtual del sistema (VA) en los sistemas de 32 bits se puede agotar debido a la fragmentación. Se pueden utilizar varias claves del registro para configurar los límites de memoria en los sistemas de 32 bits que experimentan este problema.
ms.assetid: ec2a8c6b-cd8e-4085-b337-02f78a210bb5
title: Claves del registro de administración de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e8c53bd54f8caeb82aad58ceed61cc5644c112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913682"
---
# <a name="memory-management-registry-keys"></a>Claves del registro de administración de memoria

El espacio de la dirección virtual del sistema (VA) en los sistemas de 32 bits se puede agotar debido a la fragmentación. Se pueden utilizar varias claves del registro para configurar los límites de memoria en los sistemas de 32 bits que experimentan este problema. El espacio del sistema VA en los sistemas de 64 bits no está sujeto a agotamiento por fragmentación; por lo tanto, estas claves no tienen ningún efecto en los sistemas de 64 bits.

En los sistemas de 32 bits, estas claves del registro de administración de memoria se deben crear explícitamente en la siguiente clave del registro:

**HKEY \_ \_** \\ Control actual **del sistema** de equipo local \\ **configuración** de \\ **control** \\  \\ **Administración** de la memoria de administrador de sesión

**Windows Server 2008 y Windows Vista:** Estas claves del registro están disponibles en sistemas de 32 bits a partir de Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).

Para conocer los límites de memoria y espacio de direcciones predeterminados en los sistemas de 32 y 64 bits, consulte [límites de memoria para las versiones de Windows](memory-limits-for-windows-releases.md).

En la tabla siguiente se describen las claves del registro de administración de memoria que se pueden usar para configurar los límites de memoria en los sistemas de 32 bits. Todas estas claves tienen un tipo de registro \_ DWORD y valores posibles que van de 0 a 2.048 MB. El valor predeterminado es 0, lo que significa que no se aplica ningún límite. Los valores se redondean al siguiente límite de asignación de redondeos del sistema, que es 2 MB en los sistemas de 32 bits con la [extensión de dirección física](physical-address-extension.md) (PAE) habilitada y 4 MB en sistemas de 32 bits que no tienen habilitado PAE.



| Clave                   | Descripción                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NonPagedPoolLimit** | Especifica la cantidad máxima de espacio de fin del sistema que puede usar el bloque no paginado. En determinadas condiciones, este límite se puede superar en una pequeña cantidad. |
| **PagedPoolLimit**    | Especifica la cantidad máxima de espacio de fin del sistema que puede usar el grupo paginado.                                                                            |
| **SessionSpaceLimit** | Especifica la cantidad máxima de espacio de fin del sistema que pueden usar las asignaciones de espacio de sesión.                                                                 |
| **SystemCacheLimit**  | Especifica la cantidad máxima de espacio de fin del sistema que puede usar la memoria caché del sistema. En determinadas condiciones, este límite se puede superar en una pequeña cantidad.  |
| **SystemPtesLimit**   | Especifica la cantidad máxima de espacio de fin del sistema que pueden usar las asignaciones de e/s y otros recursos que consumen las entradas de la tabla de páginas del sistema (PTE).            |



 

La determinación de si se está agotando el espacio del sistema VA requiere el uso de un depurador de kernel. Para obtener más información, vea [Herramientas de depuración de Windows](https://msdn.microsoft.com/library/cc267445.aspx).

 

 



