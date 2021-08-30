---
description: Siga estas directrices al crear un módulo de combinación de 64 bits.
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: Uso de módulos de mezcla de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ffc26c9a169eb4d340bcb406790ebef2677bfdf247f399c87e8eed1468cb1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809105"
---
# <a name="using-64-bit-merge-modules"></a>Uso de módulos de mezcla de 64 bits

Un módulo de combinación de 64 bits tiene cualquiera de las características identificadas en este tema.

-   El módulo merge contiene al menos un componente que se ha compilado para sistemas operativos de 64 bits.
-   El módulo merge no contiene componentes de 64 bits, pero está diseñado para usarse solo con paquetes de [64 bits Windows Installer.](64-bit-windows-installer-packages.md)

Los módulos de combinación se pueden usar de la siguiente manera:

-   Un módulo de combinación de 64 bits se puede combinar en un paquete de [64 bits Windows Installer.](64-bit-windows-installer-packages.md) Las [**propiedades Resumen de**](template-summary.md) plantilla del módulo de combinación y del paquete Windows Installer deben establecerse en el mismo tipo de procesador de 64 bits. Un módulo de combinación x64 solo se puede combinar en paquetes x64 y un módulo de combinación Intel64 solo se puede combinar en paquetes Intel64.
-   Un módulo de combinación de 32 bits se puede combinar en paquetes de 32 o [64 bits Windows Installer.](64-bit-windows-installer-packages.md)
-   Un módulo de combinación de 64 bits se puede combinar en un paquete de 64 bits en un sistema operativo de 32 bits.

Cumpla lo siguiente al crear un módulo de combinación de 64 bits:

-   Use el mismo procedimiento general que al crear módulos de combinación de 32 bits. Para obtener información, vea [Acerca de los módulos de mezcla](about-merge-modules.md) y Creación de [módulos de mezcla.](authoring-merge-modules.md)
-   Debe establecer la [**propiedad Resumen de**](template-summary.md) plantilla con el valor Intel64 si ejecuta un sistema Intel64. Debe establecer la **propiedad Resumen de** plantilla con el valor x64 si ejecuta un sistema x64. Para obtener información, vea Referencia de flujo de información [de resumen del módulo de mezcla](merge-module-summary-information-stream-reference.md).
-   Cuando existen módulos de combinación de 32 y 64 bits para el mismo componente, se recomienda que los módulos tengan firmas diferentes. Esto permitirá que un paquete contenga ambas versiones del componente.

Para obtener más información, [vea Windows Installer en sistemas operativos de 64 bits.](windows-installer-on-64-bit-operating-systems.md)

 

 



