---
description: El bloqueo de un recurso implica conceder acceso de CPU a su almacenamiento.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Bloquear recursos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d66a7a420a33cb908d0974f9d942597019aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705231"
---
# <a name="locking-resources-direct3d-9"></a>Bloquear recursos (Direct3D 9)

El bloqueo de un recurso implica conceder acceso de CPU a su almacenamiento. Las siguientes opciones de bloqueo se definen para los recursos:

-   \_Descartar D3DLOCK
-   D3DLOCK \_ ReadOnly
-   D3DLOCK \_ NOOVERWRITE
-   D3DLOCK \_ NOSYSLOCK
-   \_No se \_ pudo \_ Actualizar D3DLOCK

Para obtener más información sobre las marcas de bloqueo y cómo se relacionan con recursos específicos, vea las páginas de referencia en los métodos de bloqueo de recursos individuales. Los desarrolladores de aplicaciones deben tener en cuenta que las \_ marcas D3DLOCK discard, D3DLOCK \_ ReadOnly y D3DLOCK \_ NOOVERWRITE solo son sugerencias. El tiempo de ejecución no comprueba que las aplicaciones estén siguiendo la funcionalidad especificada por estas marcas. Una aplicación que especifica D3DLOCK \_ ReadOnly pero después escribe en el recurso debe esperar resultados indefinidos. En general, no se garantiza que el trabajo con marcas de bloqueo, incluidas las marcas de uso de bloqueo, funcione en versiones posteriores y puede suponer una penalización significativa en el rendimiento.

Una operación de bloqueo va seguida de una operación de desbloqueo. Por ejemplo, después de bloquear una textura, la aplicación abandona posteriormente el acceso directo a las texturas bloqueadas mediante su desbloqueo. Además de conceder acceso al procesador, cualquier otra operación que implique ese recurso se serializa mientras dure un bloqueo. Solo se permite un bloqueo único para un recurso, incluso para las regiones que no se superponen, y no se pueden realizar operaciones de acelerador en una superficie mientras una operación de bloqueo esté pendiente en esa superficie.

Cada interfaz de recursos tiene métodos para bloquear los búferes contenidos. Cada recurso de textura también puede bloquear una subparte de ese recurso. los recursos 2D (superficies) permiten el bloqueo de los subrectángulos y los recursos de volumen permiten el bloqueo de los subvolumens o cuadros. Cada método de bloqueo devuelve una estructura que contiene un puntero al almacenamiento que respalda el recurso y los valores que representan las distancias entre las filas o los planos de datos, dependiendo del tipo de recurso. Para obtener más información, consulte las listas de métodos de las interfaces de recursos. El puntero devuelto siempre apunta al byte superior izquierdo de las subregiones bloqueadas.

Al trabajar con búferes de índice y vértices, puede realizar varias llamadas de bloqueo; sin embargo, debe asegurarse de que el número de llamadas de bloqueo coincide con el número de llamadas de desbloqueo.

DXTn almacena píxeles en bloques 4x4 codificados y solo se puede bloquear en límites 4x4.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de Direct3D](direct3d-resources.md)
</dt> </dl>

 

 



