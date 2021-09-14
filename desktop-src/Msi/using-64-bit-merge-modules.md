---
description: Siga estas instrucciones al crear un módulo de combinación de 64 bits.
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: Uso de módulos de combinación de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bfeec3f77e497fac0686cd6aeb44b69e987655
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069597"
---
# <a name="using-64-bit-merge-modules"></a>Uso de módulos de combinación de 64 bits

Un módulo de combinación de 64 bits tiene cualquiera de las características identificadas en este tema.

-   El módulo merge contiene al menos un componente que se ha compilado para sistemas operativos de 64 bits.
-   El módulo merge no contiene componentes de 64 bits, pero está diseñado para usarse solo con paquetes de [64 Windows Installer.](64-bit-windows-installer-packages.md)

Los módulos de combinación se pueden usar de la siguiente manera:

-   Un módulo de combinación de 64 bits se puede combinar en un paquete de [Windows instalador de 64](64-bit-windows-installer-packages.md) bits. Las [**propiedades Resumen de**](template-summary.md) plantilla del módulo de combinación y del paquete Windows Installer deben establecerse en el mismo tipo de procesador de 64 bits. Un módulo de combinación x64 solo se puede combinar en paquetes x64 y un módulo de combinación Intel64 solo se puede combinar en paquetes Intel64.
-   Un módulo merge de 32 bits se puede combinar en paquetes de 32 o [64 bits Windows Installer.](64-bit-windows-installer-packages.md)
-   Un módulo de combinación de 64 bits se puede combinar en un paquete de 64 bits en un sistema operativo de 32 bits.

Al crear un módulo de combinación de 64 bits, siga estos pasos:

-   Use el mismo procedimiento general que al crear módulos de combinación de 32 bits. Para obtener información, vea [Acerca de los módulos de combinación](about-merge-modules.md) y Creación de [módulos de mezcla.](authoring-merge-modules.md)
-   Debe establecer la propiedad [**Resumen de plantilla**](template-summary.md) con el valor Intel64 si ejecuta un sistema Intel64. Debe establecer la propiedad **Resumen de plantilla** con el valor x64 si ejecuta un sistema x64. Para obtener información, [vea Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md).
-   Cuando existen módulos de combinación de 32 y 64 bits para el mismo componente, se recomienda que los módulos tengan firmas diferentes. Esto permitirá que un paquete contenga ambas versiones del componente.

Para obtener más información, vea Windows Installer en sistemas operativos [de 64 bits.](windows-installer-on-64-bit-operating-systems.md)

 

 



