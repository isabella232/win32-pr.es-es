---
description: Bloquear un recurso significa conceder acceso de CPU a su almacenamiento.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Bloqueo de recursos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6cdb7cde646bd5073bc0c5b574694be69f05f1bf15d8c5c08e00b7182cfe044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799498"
---
# <a name="locking-resources-direct3d-9"></a>Bloqueo de recursos (Direct3D 9)

Bloquear un recurso significa conceder acceso de CPU a su almacenamiento. Se definen las siguientes opciones de bloqueo para los recursos:

-   D3DLOCK \_ DISCARD
-   D3DLOCK \_ READONLY
-   D3DLOCK \_ NOOVERWRITE
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ NO \_ DIRTY \_ UPDATE

Para más información sobre las marcas de bloqueo y cómo se relacionan con recursos específicos, consulte las páginas de referencia de los métodos de bloqueo de recursos individuales. Los desarrolladores de aplicaciones deben tener en cuenta que las marcas D3DLOCK \_ DISCARD, D3DLOCK \_ READONLY y D3DLOCK NOOVERWRITE solo son \_ sugerencias. El tiempo de ejecución no comprueba que las aplicaciones estén siguiendo la funcionalidad especificada por estas marcas. Una aplicación que especifica D3DLOCK READONLY pero, a continuación, escribe en \_ el recurso debe esperar resultados no definidos. En general, no se garantiza que el trabajo con marcas de bloqueo, incluidas las marcas de uso de bloqueo, funcione en versiones posteriores y puede producir una reducción significativa del rendimiento.

Una operación de bloqueo va seguida de una operación de desbloqueo. Por ejemplo, después de bloquear una textura, la aplicación posteriormente cedía el acceso directo a las texturas bloqueadas desbloqueándolos. Además de conceder acceso al procesador, cualquier otra operación que implique ese recurso se serializa mientras dure un bloqueo. Solo se permite un bloqueo único para un recurso, incluso para regiones no superpuestas, y no se puede realizar ninguna operación de acelerador en una superficie mientras hay una operación de bloqueo pendiente en esa superficie.

Cada interfaz de recursos tiene métodos para bloquear los búferes contenidos. Cada recurso de textura también puede bloquear una subsección de ese recurso. Los recursos 2D (superficies) permiten el bloqueo de sub rectángulos y los recursos de volumen permiten el bloqueo de sub volúmenes o cuadros. Cada método de bloqueo devuelve una estructura que contiene un puntero al almacenamiento que hace una copia de seguridad del recurso y los valores que representan las distancias entre filas o planos de datos, según el tipo de recurso. Para más información, consulte las listas de métodos para las interfaces de recursos. El puntero devuelto siempre apunta al byte superior izquierdo en las subrecciones bloqueadas.

Al trabajar con búferes de índice y vértice, puede realizar varias llamadas de bloqueo; sin embargo, debe asegurarse de que el número de llamadas de bloqueo coincide con el número de llamadas de desbloqueo.

DXTn almacena píxeles en bloques 4x4 codificados y solo se puede bloquear en límites 4x4.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de Direct3D](direct3d-resources.md)
</dt> </dl>

 

 



