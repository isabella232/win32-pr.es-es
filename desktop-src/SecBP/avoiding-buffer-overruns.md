---
description: Proporciona una breve introducción a algunos tipos de situaciones de saturación del búfer y ofrece algunas ideas y recursos para ayudarle a evitar la creación de nuevos riesgos y a mitigar los existentes.
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: Evitar saturaciones del búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8a3456384e799380fa0041172fb2b2ea09c0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668045"
---
# <a name="avoiding-buffer-overruns"></a>Evitar saturaciones del búfer

Una saturación del búfer es uno de los orígenes más comunes de riesgos para la seguridad. Una saturación del búfer se produce esencialmente al tratar la entrada externa no comprobada como datos de confianza. La acción de copiar estos datos, mediante operaciones como [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy** o **wcscpy**, puede crear resultados inesperados, lo que permite daños en el sistema. En el mejor de los casos, la aplicación se anulará con un volcado de memoria principal, un error de segmentación o una infracción de acceso. En el peor de los casos, un atacante puede aprovechar la saturación del búfer introduciendo y ejecutando otro código malintencionado en el proceso. La copia de los datos no comprobados en un búfer basado en la pila es la causa más común de los errores explotables.

Las saturaciones del búfer pueden producirse de varias maneras. En la lista siguiente se proporciona una breve introducción a algunos tipos de situaciones de saturación del búfer y se ofrecen algunas ideas y recursos para ayudarle a evitar la creación de nuevos riesgos y a mitigar los existentes:

<dl> <dt>

<span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Saturaciones estáticas del búfer
</dt> <dd>

Una saturación del búfer estático se produce cuando un búfer, que se ha declarado en la pila, se escribe en con más datos de los que se asignaron para contener. Las versiones menos aparente de este error se producen cuando los datos de entrada del usuario no comprobados se copian directamente en una variable estática, lo que produce daños en la pila.

</dd> <dt>

<span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Saturaciones del montón
</dt> <dd>

Las saturaciones del montón, como las saturaciones del búfer estático, pueden provocar daños en la memoria y la pila. Dado que las saturaciones del montón se producen en la memoria del montón en lugar de en la pila, algunas personas consideran que son menos capaces de provocar problemas graves. No obstante, las saturaciones del montón requieren un cuidado de programación real y son como capaces de permitir riesgos del sistema como saturaciones del búfer estático.

</dd> <dt>

<span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Errores de indización de matriz
</dt> <dd>

Los errores de indización de matriz también son un origen de saturaciones de memoria. La comprobación de los límites cuidadosos y la administración de índices ayudarán a evitar este tipo de saturación de la memoria.

</dd> </dl>

Evitar las saturaciones del búfer consiste principalmente en escribir código correcto. Valide siempre todas las entradas y genere un error correctamente cuando sea necesario. Para obtener más información sobre cómo escribir código seguro, vea los siguientes recursos:

-   Maguire, Steve \[ 1993 \] , *escritura de código sólido*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.
-   Howard, Michael y LeBlanc, David \[ 2003 \] , *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.

> [!Note]  
> Es posible que estos recursos no estén disponibles en algunos idiomas y países.

 

El control de cadenas seguras es un problema de larga duración que se sigue solucionando siguiendo los buenos procedimientos de programación y con frecuencia mediante el uso de y el reajuste de sistemas existentes con funciones seguras de control de cadenas. Un ejemplo de este conjunto de funciones para el shell de Windows se inicia con [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).

 

 
