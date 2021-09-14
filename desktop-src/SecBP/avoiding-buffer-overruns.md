---
description: Proporciona una breve introducción a algunos tipos de situaciones de saturación de búfer y ofrece algunas ideas y recursos para ayudarle a evitar la creación de nuevos riesgos y mitigar los existentes.
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: Evitar saturaciones de búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8a3456384e799380fa0041172fb2b2ea09c0c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071192"
---
# <a name="avoiding-buffer-overruns"></a>Evitar saturaciones de búfer

Una saturación del búfer es uno de los orígenes más comunes de riesgo de seguridad. Una saturación del búfer se debe básicamente al tratamiento de la entrada externa no desactivada como datos de confianza. El acto de copiar estos datos, mediante operaciones como [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy** o **wcscpy,** puede crear resultados imprevistos, lo que permite daños en el sistema. En el mejor de los casos, la aplicación se anulará con un volcado de memoria, un error de segmentación o una infracción de acceso. En el peor de los casos, un atacante puede aprovechar la saturación del búfer mediante la introducción y ejecución de otro código malintencionado en el proceso. Copiar datos de entrada no desactivados en un búfer basado en la pila es la causa más común de errores que se pueden aprovechar.

Las saturaciones del búfer pueden producirse de varias maneras. En la lista siguiente se proporciona una breve introducción a algunos tipos de situaciones de saturación de búfer y se ofrecen algunas ideas y recursos que le ayudarán a evitar la creación de nuevos riesgos y a mitigar los existentes:

<dl> <dt>

<span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Saturaciones de búfer estático
</dt> <dd>

Una saturación del búfer estático se produce cuando se escribe un búfer, que se ha declarado en la pila, con más datos de los que se asignaron para contener. Las versiones menos evidentes de este error se producen cuando los datos de entrada del usuario noverificados se copian directamente en una variable estática, lo que provoca posibles daños en la pila.

</dd> <dt>

<span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Saturaciones del montón
</dt> <dd>

Las saturaciones del montón, como las saturaciones de búfer estático, pueden provocar daños en la memoria y la pila. Dado que las saturaciones del montón se producen en la memoria del montón en lugar de en la pila, algunas personas consideran que son menos capaces de causar problemas graves. No obstante, las saturaciones del montón requieren una atención de programación real y son igual de capaces de permitir riesgos del sistema como saturaciones de búfer estático.

</dd> <dt>

<span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Errores de indexación de matrices
</dt> <dd>

Los errores de indexación de matrices también son un origen de saturaciones de memoria. La comprobación cuidadosa de límites y la administración de índices ayudarán a evitar este tipo de saturación de memoria.

</dd> </dl>

La prevención de saturaciones del búfer se basa principalmente en escribir código correcto. Valide siempre todas las entradas y se producirá un error correctamente cuando sea necesario. Para más información sobre cómo escribir código seguro, consulte los siguientes recursos:

-   Maguire, Steve \[ 1993, \] Writing Solid *Code*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.
-   Howard, Michael y LePeri, David \[ 2003, \] *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.

> [!Note]  
> Es posible que estos recursos no estén disponibles en algunos idiomas y países.

 

Caja fuerte control de cadenas es un problema de larga duración que se sigue abordando siguiendo los procedimientos de programación recomendados y, a menudo, mediante el uso y la retroajuste de los sistemas existentes con funciones seguras y de control de cadenas. Un ejemplo de este conjunto de funciones para el shell de Windows se inicia con [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).

 

 
