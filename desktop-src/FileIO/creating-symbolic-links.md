---
description: Cree vínculos simbólicos que usen una ruta de acceso absoluta o relativa mediante la función CreateSymbolicLink.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Crear vínculos simbólicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c978532ffc11e44615d4de0ea902152438ecc7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361165"
---
# <a name="creating-symbolic-links"></a>Crear vínculos simbólicos

La función [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) permite crear vínculos simbólicos mediante una ruta de acceso absoluta o relativa.

Los vínculos simbólicos pueden ser vínculos absolutos o relativos. Los vínculos absolutos son vínculos que especifican cada parte del nombre de ruta de acceso; los vínculos relativos se determinan en relación con los especificadores de vínculo relativo, en una ruta de acceso especificada. Los vínculos relativos se especifican mediante las convenciones siguientes:

-   Punto (. y..) convenciones, por ejemplo, ".. \\ " resuelve la ruta de acceso relativa al directorio principal.
-   Los nombres sin barras diagonales ( \) por ejemplo, "tmp" resuelven la ruta de acceso relativa al directorio actual.
-   Relativa a la raíz: por ejemplo, " \\ Windows \\ system32" se resuelve como la "*unidad actual*: \\ Windows \\ system32". directory
-   Directorio de trabajo actual-relativo: por ejemplo, si el directorio de trabajo actual es "C: \\ Windows \\ system32", "C:File.txt" se resuelve como "c: \\ Windows \\ system32 \\File.txt".

    **Nota:**  Si especifica un vínculo relativo al directorio de trabajo actual, se crea como un vínculo absoluto, debido a la manera en que se procesa el directorio de trabajo actual en función del usuario y el subproceso.

Un vínculo simbólico también puede contener tanto puntos de Unión como carpetas montadas como parte del nombre de la ruta de acceso.

Los vínculos simbólicos pueden apuntar directamente a un archivo o directorio remoto mediante la ruta de acceso UNC.

Los vínculos simbólicos relativos están restringidos a un solo volumen.

## <a name="example-of-an-absolute-symbolic-link"></a>Ejemplo de un vínculo simbólico absoluto

En este ejemplo, la ruta de acceso original contiene un componente, '*x*', que es un vínculo simbólico absoluto. Cuando se encuentra '*x*', el fragmento de la ruta de acceso original hasta e incluye '*x*' se reemplaza completamente por la ruta de acceso a la que apunta '*x*'. El resto de la ruta de acceso después de "*x*" se anexa a esta nueva ruta de acceso. Ahora se convierte en la ruta de acceso modificada.

X: "C: \\ alpha \\ beta \\ absLink \\ \\ archivo gamma"

Link: "absLink" se asigna a " \\ \\ machineB \\ share"

Ruta de acceso modificada: " \\ \\ machineB \\ share \\ gamma \\ file"

## <a name="example-of-a-relative-symbolic-links"></a>Ejemplo de vínculos simbólicos relativos

En este ejemplo, la ruta de acceso original contiene un componente '*x*', que es un vínculo simbólico relativo. Cuando se encuentra '*x*', '*x*' se reemplaza completamente por el nuevo fragmento al que apunta '*x*'. El resto de la ruta de acceso después de '*x*' se anexa a la nueva ruta de acceso. Los puntos (..) de esta nueva ruta de acceso reemplazan a los componentes que aparecen delante de los puntos (..). Cada conjunto de puntos reemplaza al componente anterior. Si el número de puntos (..) supera el número de componentes, se devuelve un error. De lo contrario, cuando haya finalizado todo el reemplazo de componentes, permanecerá la ruta de acceso modificada final.

Archivo gamma X: C: \\ alpha \\ beta \\ Link \\ \\

Link: "link" se asigna a ".. \\ .. \\ Zeta

Ruta de acceso modificada: "C: \\ alpha \\ beta \\ ... \\ . \\ \\archivo gamma Theta \\ "

Ruta final: "C: \\ Theta \\ gamma \\ file"

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vínculos simbólicos](symbolic-links.md)
</dt> <dt>

[Vínculos físicos y uniones](hard-links-and-junctions.md)
</dt> <dt>

[Nomenclatura de archivos, rutas de acceso y espacios de nombres](naming-a-file.md)
</dt> </dl>

 

 



