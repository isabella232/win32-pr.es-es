---
description: Los recursos de idioma constan de separadores de palabras y lematizadores que amplían las capacidades de creación y consulta de índices a nuevos idiomas y configuraciones regionales.
ms.assetid: 7963805e-e279-42cf-ba95-f81a7de8e68e
title: Descripción de los componentes de recursos de lenguaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8feb10d14edbf4aba59b912ae1945d5e87ec32ef684f0b1f5530f1770ba70053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462387"
---
# <a name="understanding-language-resource-components"></a>Descripción de los componentes de recursos de lenguaje

Los recursos de idioma constan de separadores de palabras y lematizadores que amplían las capacidades de creación y consulta de índices a nuevos idiomas y configuraciones regionales. Los separadores de palabras se usan durante la creación de índices y las consultas. Los lematizadores solo se usan para realizar consultas. Windows La búsqueda usa archivos DLL de recursos de lenguaje para enlazar con implementaciones [**de IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) e [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) para una configuración regional de idioma específica.

Este tema se organiza de la siguiente manera:

-   [Acerca de los recursos de lenguaje](#about-language-resources)
-   [Separación de palabras](#word-breaking)
-   [Raíz](#stemming)
-   [Normalización](#normalization)
-   [Palabras ruidosas](#noise-words)
-   [Temas relacionados](#related-topics)

## <a name="about-language-resources"></a>Acerca de los recursos de lenguaje

Windows La búsqueda usa un filtro (una implementación de la [**interfaz IFilter)**](/windows/win32/api/filter/nn-filter-ifilter) e [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) para acceder a un documento en su formato nativo. El [**componente IFilter**](/windows/win32/api/filter/nn-filter-ifilter) extrae contenido de texto, propiedades y formato del documento. El [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) identifica la configuración regional del documento que está filtrando. El componente de indexación invoca el separador de palabras adecuado para esa configuración regional. Si no hay ninguna disponible, el componente de indexación invoca el separador de palabras neutro. El separador de palabras recibe, de [**un IFilter,**](/windows/win32/api/filter/nn-filter-ifilter)un flujo de entrada de caracteres Unicode que el separador de palabras analiza para generar palabras y frases individuales. El separador de palabras también normaliza los formatos de fecha y hora. El indexador normaliza las palabras producidas por el separador de palabras mediante la conversión de las palabras a todas las letras mayúsculas. El indexador guarda las palabras mayúsculas en el índice de texto completo, a excepción de las palabras ruido identificadas para esa configuración regional.

En la tabla siguiente se enumeran las acciones y los resultados correspondientes de la frase "Figura 1 muestra el rol de los recursos de lenguaje para Windows Search durante el proceso de creación del índice".



| Acción                  | Texto resultante                                                                                                               |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Texto original           | En la figura 1 se muestra el rol de los recursos de lenguaje para Windows Search durante el proceso de creación del índice.                    |
| Filtrado               | En la figura 1 se muestra el rol de los recursos de lenguaje para Windows Search durante el proceso de creación del índice.                    |
| División de palabras           | Figura, 1, ilustra, el, rol, de, lenguaje, recursos, para, Windows, Búsqueda, durante, el, índice, creación, proceso, EOS |
| Normalización           | ILUSTRACIÓN, 1, ILUSTRA, THE, ROLE, OF, LANGUAGE, RESOURCES, WINDOWS, SEARCH, DURING, THE, INDEX, CREATION, PROCESS           |
| Eliminación de palabras ruido      | FIGURE, ILLUSTRATES, ROLE, LANGUAGE, RESOURCES, WINDOWS, SEARCH, DURING, INDEX, CREATION, PROCESS                            |
| Guardar en el índice de texto completo | FIGURE, ILLUSTRATES, ROLE, LANGUAGE, RESOURCES, WINDOWS, SEARCH, DURING, INDEX, CREATION, PROCESS                            |



 

Los separadores de palabras y lematizadores se usan para expandir las [consultas FREETEXT](-search-sql-freetext.md) en el momento de la consulta. La configuración regional de la consulta es la configuración regional predeterminada, a menos que se pase un identificador de código de idioma (LCID) como parámetro de consulta. El componente de consulta invoca el separador de palabras adecuado en los términos de consulta enumerados en la [cláusula WHERE](-search-sql-where.md) de la consulta. Por ejemplo, si la cláusula WHERE de la consulta contiene "FREETEXT (manzanas, naranjas y peras)", el separador de palabras recibe el texto "apples, oranges, and oranges". Si la cláusula WHERE de consulta usa el predicado [CONTAINS](-search-sql-contains.md) de texto completo, se normaliza la salida de texto del separador de palabras. De lo contrario, el componente de consulta pasa cada palabra identificada por el separador de palabras al lematizador adecuado para ese idioma y configuración regional. El lematizador genera una lista de formas alternativas, o inflectadas, para esa palabra. El componente de consulta normaliza la lista expandida de términos de consulta y quita las palabras ruido.

En la tabla siguiente se enumeran las acciones y los resultados correspondientes para la consulta "manzanas, naranjas y manzanas".



| Acción                       | Texto resultante                                            |
|------------------------------|-----------------------------------------------------------|
| Texto original                | manzanas, naranjas y naranjas                                |
| División de palabras                | manzanas, naranjas y, peras, EOS                          |
| Raíz                     | apple, apples, orange, orangey, oranges, and, oranges, albóndes |
| Normalización                | APPLE, APPLES, ORANGE, ORANGEY, ORANGES, AND, LONJAS |
| Eliminación de palabras ruido           | APPLE, APPLES, ORANGE, ORANGEY, ORANGES, LONJAS, HADAS      |
| Lista ampliada de términos de consulta | APPLE, APPLES, ORANGE, ORANGEY, ORANGES, LONJAS, HADAS      |



 

Los términos de consulta expandido aumentan la probabilidad de que la consulta encuentre documentos que coincidan con la intención de la consulta original. El texto que el separador de palabras o lematizador genera en el momento de la consulta no se almacena en el disco.

## <a name="word-breaking"></a>Separación de palabras

La separación de palabras es la separación de texto en tokens de texto individuales o palabras. Muchos idiomas, especialmente los que tienen alfabetos latinos, tienen una matriz de separadores de palabras (como espacios en blanco) y signos de puntuación que se usan para distinguir palabras, frases y oraciones. Los separadores de palabras deben basarse en una heurística de lenguaje precisa para proporcionar resultados confiables y precisos. La separación de palabras es más compleja para los sistemas basados en caracteres de escritura o alfabetos basados en scripts, donde el significado de los caracteres individuales se determina a partir del contexto. Para obtener más información sobre las consideraciones lingüísticas que pueden afectar a la implementación del separador de palabras, vea [Linguistic and Unicode Considerations](linguistic-and-unicode-considerations.md).

## <a name="stemming"></a>Raíz

Windows La búsqueda aplica lematizadores exclusivamente en el momento de la consulta para generar formularios de palabras adicionales para los términos [de las consultas FREETEXT](-search-sql-freetext.md) y de propiedad. Los lematizadores realizan análisis morphológicos y aplican reglas gramaticales para generar una lista de formas alternativas, o inflectadas, para las palabras. Las formas alternativas suelen tener la misma forma de lemat o base. Al generar los formularios desfasados para una palabra, Indexing Service devuelve resultados de consulta que son estadísticamente más relevantes para una consulta. Por ejemplo, una consulta de texto completo para la "reunión de nada" coincide con documentos que contienen "nada, nada, nada, swam, swum" o "meet, meet,meets, meets', meeting, met" y combinaciones de estos términos.

Algunos lenguajes requieren que los términos con inflexión se generen tanto en el momento del índice como en el tiempo de consulta para las inflexiones estándar y variante. En este caso, la lematización se produce en el componente separador de palabras, con un trabajo mínimo de lematización en el lematizador real. Por ejemplo, el separador de palabras japonés realiza la lematización durante la creación de índices y las consultas para permitir que una consulta encuentre formas diferentes de los términos de búsqueda.

## <a name="normalization"></a>Normalización

Los documentos de todos los idiomas se almacenan en un único índice. Aunque las palabras y las reglas lingüísticas difieren considerablemente, hay algunas consideraciones, como números, fechas y horas, que se controlan de forma coherente en todos los separadores de palabras. Para obtener más información sobre las consideraciones de normalización que pueden afectar a la implementación del separador de palabras, vea [Normalización de formularios surface.](surface-form-normalization.md)

## <a name="noise-words"></a>Palabras ruidosas

Las palabras ruidosas, también conocidas como palabras de detención, son palabras que no son indicadores significativos del contenido. Indexing Service quita palabras ruidosas de los términos de consulta y del contenido que se incluye en el índice de texto completo. Un *desplazamiento* es la aparición de una palabra en un documento o en una lista de términos de consulta. El desplazamiento de las palabras ruido en un documento o consulta se registra como en blanco. La eliminación de palabras ruido mejora el rendimiento de las consultas al evitar el crecimiento innecesario de índices. También mejora la relevancia de los resultados de la consulta. Puede configurar Windows Search para usar listas de palabras ruido para idiomas específicos. Estas listas se usan cuando se invoca un separador de palabras para ese idioma. Por ejemplo, "the" en inglés se produce con tanta frecuencia que tiene poco valor como clave única. "The" está en la lista de palabras con ruido, no se escribe en el índice de contenido y, si se consulta, no devuelve ningún resultado.

Las palabras ruido actúan como marcadores de posición en las consultas de frases. Un documento que contiene el texto "el perro" se almacena en el índice con "perro" en la aparición 1 y "perro" en la aparición 3. La consulta de frases "dog" no coincide, pero la consulta de frase "hacer un perro" sí, porque la información de repetición coincide. La frase "purple dog" no coincide porque "purple" no se encuentra en el índice en la aparición 2. Sin embargo, una consulta para "el perro del perro" devuelve documentos que contienen "perro púrpura" porque no hay ninguna manera de determinar de forma eficaz si el documento tenía una palabra sin ruido entre "perro" y "perro".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Extensión de recursos de lenguaje](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Implementar un separador de palabras y un lematizador](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[Consideraciones lingüísticas y Unicode](linguistic-and-unicode-considerations.md)
</dt> <dt>

[Solución de problemas de recursos de lenguaje y procedimientos recomendados](troubleshooting-language-resources.md)
</dt> </dl>

 

 
