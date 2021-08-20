---
description: Cree vínculos simbólicos que usen una ruta de acceso absoluta o relativa mediante la función CreateSymbolicLink.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Crear vínculos simbólicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0340dc362ff550ab2d74e533ac66e74622c965266440103d6f6ec155bfa80f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150861"
---
# <a name="creating-symbolic-links"></a>Crear vínculos simbólicos

La función [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) permite crear vínculos simbólicos mediante una ruta de acceso absoluta o relativa.

Los vínculos simbólicos pueden ser vínculos absolutos o relativos. Los vínculos absolutos son vínculos que especifican cada parte del nombre de ruta de acceso; los vínculos relativos se determinan en relación con dónde se encuentran los especificadores de vínculo relativo en una ruta de acceso especificada. Los vínculos relativos se especifican mediante las convenciones siguientes:

-   Punto (. y ). convenciones, por ejemplo, ".. \\ " resuelve la ruta de acceso relativa al directorio primario.
-   Nombres sin barras diagonales ( ): por ejemplo, "tmp" resuelve la ruta de acceso \\ relativa al directorio actual.
-   Relación raíz: por ejemplo, "Windows System32" se resuelve en la unidad actual \\ \\ : Windows \\ \\ System32". directory
-   Actual relativa al directorio de trabajo: por ejemplo, si el directorio de trabajo actual es "C: \\ Windows \\ System32", "C:File.txt" se resuelve en "C: \\ Windows \\ System32 \\File.txt".

    **Nota**  Si especifica un vínculo relativo al directorio de trabajo actual, se crea como un vínculo absoluto, debido a la forma en que se procesa el directorio de trabajo actual en función del usuario y el subproceso.

Un vínculo simbólico también puede contener puntos de unión y carpetas montadas como parte del nombre de ruta de acceso.

Los vínculos simbólicos pueden apuntar directamente a un archivo o directorio remoto mediante la ruta de acceso UNC.

Los vínculos simbólicos relativos están restringidos a un solo volumen.

## <a name="example-of-an-absolute-symbolic-link"></a>Ejemplo de un vínculo simbólico absoluto

En este ejemplo, la ruta de acceso original contiene un componente,*'x',* que es un vínculo simbólico absoluto. Cuando se *encuentra ' x*', el fragmento de la ruta de acceso original hasta y incluyendo '*x*' se reemplaza completamente por la ruta de acceso a la que apunta '*x*'. El resto de la ruta de acceso después *de 'x'* se anexa a esta nueva ruta de acceso. Ahora se convierte en la ruta de acceso modificada.

X: "C: \\ alpha \\ beta \\ absLink gamma \\ \\ file"

Vínculo: "absLink" se asigna a \\ \\ "machineB \\ share"

Ruta de acceso modificada: \\ \\ "archivo \\ gamma de recurso compartido de \\ \\ machineB"

## <a name="example-of-a-relative-symbolic-links"></a>Ejemplo de vínculos simbólicos relativos

En este ejemplo, la ruta de acceso original contiene un componente *' x*', que es un vínculo simbólico relativo. Cuando se *encuentra ' x*', '*x*' se reemplaza completamente por el nuevo fragmento al que apunta '*x*'. El resto de la ruta de acceso después de *'x',* se anexa a la nueva ruta de acceso. Los puntos (..) de esta nueva ruta de acceso reemplazan los componentes que aparecen antes de los puntos (..). Cada conjunto de puntos reemplaza al componente anterior. Si el número de puntos (..) supera el número de componentes, se devuelve un error. De lo contrario, cuando haya finalizado el reemplazo de todos los componentes, permanece la ruta de acceso final modificada.

X: C: \\ alfa beta link gamma \\ \\ \\ \\ file

Vínculo: "link" se asigna a ".. \\ .. \\ theta"

Ruta de acceso modificada: "C: \\ \\ alfa beta \\ .. \\ .. \\ theta \\ gamma \\ file"

Ruta de acceso final: "C: \\ theta \\ gamma \\ file"

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vínculos simbólicos](symbolic-links.md)
</dt> <dt>

[Vínculos duros y uniones](hard-links-and-junctions.md)
</dt> <dt>

[Asignar nombres a archivos, rutas de acceso y espacios de nombres](naming-a-file.md)
</dt> </dl>

 

 



