---
description: Siga estas instrucciones al crear un módulo de combinación de 64 bits.
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: Usar módulos de combinación de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bfeec3f77e497fac0686cd6aeb44b69e987655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815430"
---
# <a name="using-64-bit-merge-modules"></a>Usar módulos de combinación de 64 bits

Un módulo de combinación de 64 bits tiene cualquiera de las características que se identifican en este tema.

-   El módulo de combinación contiene al menos un componente que se ha compilado para los sistemas operativos de 64 bits.
-   El módulo de combinación no contiene componentes de 64 bits, pero está pensado para usarse solo con paquetes de [Windows Installer de 64 bits](64-bit-windows-installer-packages.md) .

Los módulos de combinación se pueden usar de la siguiente manera:

-   Un módulo de combinación de 64 bits se puede combinar en un paquete de [Windows Installer de 64 bits](64-bit-windows-installer-packages.md) . Las propiedades de Resumen de la [**plantilla**](template-summary.md) en el módulo de combinación y en el paquete de Windows Installer se deben establecer en el mismo tipo de procesador de 64 bits. Un módulo de fusión mediante combinación x64 solo se puede combinar en paquetes x64 y un módulo Intel64 Merge solo se puede combinar en paquetes de Intel64.
-   Un módulo de combinación de 32 bits se puede combinar en paquetes de Windows Installer de 32 bits o [de 64 bits](64-bit-windows-installer-packages.md) .
-   Un módulo de combinación de 64 bits se puede combinar en un paquete de 64 bits en un sistema operativo de 32 bits.

Al crear un módulo de combinación de 64 bits, siga estos pasos:

-   Utilice el mismo procedimiento general que al crear módulos de combinación de 32 bits. Para obtener más información, vea acerca de los [módulos de combinación](about-merge-modules.md) y de creación de [módulos de combinación](authoring-merge-modules.md).
-   Debe establecer la propiedad de Resumen de la [**plantilla**](template-summary.md) con el valor Intel64 si se ejecuta un sistema Intel64. Debe establecer la propiedad de Resumen de la **plantilla** con el valor x64 si ejecuta un sistema x64. Para obtener más información, vea [referencia de flujo de información de resumen del módulo de mezcla](merge-module-summary-information-stream-reference.md).
-   Cuando existen módulos de combinación de 32 y 64 bits para el mismo componente, se recomienda que los módulos tengan firmas diferentes. Esto permitirá que un paquete contenga ambas versiones del componente.

Para obtener más información, consulte [Windows Installer en sistemas operativos de 64 bits](windows-installer-on-64-bit-operating-systems.md).

 

 



