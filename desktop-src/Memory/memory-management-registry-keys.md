---
description: El espacio de direcciones virtuales del sistema (VA) en sistemas de 32 bits se puede agotar debido a la fragmentación. Se pueden usar varias claves del Registro para configurar límites de memoria en sistemas de 32 bits que experimentan este problema.
ms.assetid: ec2a8c6b-cd8e-4085-b337-02f78a210bb5
title: Claves del Registro de administración de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e8c53bd54f8caeb82aad58ceed61cc5644c112
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159839"
---
# <a name="memory-management-registry-keys"></a>Claves del Registro de administración de memoria

El espacio de direcciones virtuales del sistema (VA) en sistemas de 32 bits se puede agotar debido a la fragmentación. Se pueden usar varias claves del Registro para configurar límites de memoria en sistemas de 32 bits que experimentan este problema. El espacio va del sistema en sistemas de 64 bits no está sujeto a agotamiento por fragmentación; Por lo tanto, estas claves no tienen ningún efecto en los sistemas de 64 bits.

En el caso de los sistemas de 32 bits, estas claves del Registro de administración de memoria deben crearse explícitamente con la siguiente clave del Registro:

**HKEY \_ LOCAL \_ MACHINE SYSTEM** \\ **Current** Control \\ **Set** \\ **Control** \\ **Session Manager Memory** \\ **Management**

**Windows Server 2008 y Windows Vista:** Estas claves del Registro están disponibles en sistemas de 32 bits a partir de Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).

Para conocer los límites predeterminados de memoria y espacio de direcciones en sistemas de 32 y 64 bits, vea [Límites](memory-limits-for-windows-releases.md)de memoria para Windows versiones .

En la tabla siguiente se describen las claves del Registro de administración de memoria que se pueden usar para configurar límites de memoria en sistemas de 32 bits. Todas estas claves tienen un tipo REG DWORD y valores posibles que oscilan entre \_ 0 y 2048 MB. El valor predeterminado es 0, lo que significa que no se aplica ningún límite. Los valores se redondea automáticamente al siguiente límite de asignación de VA del [](physical-address-extension.md) sistema, que es de 2 MB en sistemas de 32 bits que tienen habilitada la extensión de dirección física (PAE) y de 4 MB en sistemas de 32 bits que no tienen PAE habilitado.



| Clave                   | Descripción                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NonPagedPoolLimit** | Especifica la cantidad máxima de espacio va del sistema que puede usar el grupo sin página. En determinadas condiciones, este límite puede superarse en una pequeña cantidad. |
| **PagedPoolLimit**    | Especifica la cantidad máxima de espacio va del sistema que puede usar el grupo paginado.                                                                            |
| **SessionSpaceLimit** | Especifica la cantidad máxima de espacio va del sistema que pueden usar las asignaciones de espacio de sesión.                                                                 |
| **SystemCacheLimit**  | Especifica la cantidad máxima de espacio va del sistema que puede usar la caché del sistema. En determinadas condiciones, este límite puede superarse en una pequeña cantidad.  |
| **SystemPtesLimit**   | Especifica la cantidad máxima de espacio va del sistema que pueden usar las asignaciones de E/S y otros recursos que consumen entradas de tabla de páginas del sistema (PTE).            |



 

La determinación de si se agota el espacio va del sistema requiere el uso de un depurador de kernel. Para obtener más información, vea [Herramientas de depuración de Windows](https://msdn.microsoft.com/library/cc267445.aspx).

 

 



