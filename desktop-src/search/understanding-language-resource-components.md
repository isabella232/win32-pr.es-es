---
description: Los recursos de idioma se componen de separadores de palabras y lematizadores que amplían las capacidades de creación y consulta de índices a nuevos idiomas y configuraciones regionales.
ms.assetid: 7963805e-e279-42cf-ba95-f81a7de8e68e
title: Descripción de los componentes de recursos de lenguaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e03c9294eaf6e50de024b866372093a0359fc79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540614"
---
# <a name="understanding-language-resource-components"></a>Descripción de los componentes de recursos de lenguaje

Los recursos de idioma se componen de separadores de palabras y lematizadores que amplían las capacidades de creación y consulta de índices a nuevos idiomas y configuraciones regionales. Los separadores de palabras se usan durante la creación de índices y las consultas. Lematizadores solo se usan para realizar consultas. Windows Search usa archivos dll de recursos de idioma para enlazar con las implementaciones de [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) y [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) para una configuración regional de idioma específico.

Este tema se organiza de la siguiente manera:

-   [Acerca de los recursos de idioma](#about-language-resources)
-   [Separación de palabras](#word-breaking)
-   [Raíz](#stemming)
-   [Normalización](#normalization)
-   [Palabras irrelevantes](#noise-words)
-   [Temas relacionados](#related-topics)

## <a name="about-language-resources"></a>Acerca de los recursos de idioma

Windows Search usa un filtro (una implementación de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) y [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) para tener acceso a un documento en su formato nativo. El componente [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) extrae el contenido de texto, las propiedades y el formato del documento. El [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) identifica la configuración regional del documento que está filtrando. El componente de indización invoca el separador de palabras adecuado para esa configuración regional. Si no hay ninguno disponible, el componente de indización invoca el separador de palabras neutro. El separador de palabras recibe, de un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), un flujo de entrada de caracteres Unicode que el separador de palabras analiza para generar palabras y frases individuales. El separador de palabras también normaliza los formatos de fecha y hora. El indexador normaliza las palabras generadas por el separador de palabras convirtiendo las palabras en mayúsculas. El indexador guarda las palabras en mayúsculas en el índice de texto completo, con la excepción de las palabras irrelevantes identificadas para esa configuración regional.

En la tabla siguiente se enumeran las acciones y los resultados correspondientes de la frase "figura 1 muestra el rol de los recursos de idioma para Windows Search durante el proceso de creación del índice".



| Acción                  | Texto resultante                                                                                                               |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Texto original           | La figura 1 muestra la función de los recursos de idioma para la búsqueda de Windows durante el proceso de creación de índices.                    |
| Filtrado               | La figura 1 muestra la función de los recursos de idioma para la búsqueda de Windows durante el proceso de creación de índices.                    |
| División de palabras           | Ilustración, 1, ilustra,, role, of, Language, Resources, for, Windows, Search, During,, index, Creation, Process, EOS |
| Normalización           | ILUSTRACIÓN, 1, ILUSTRA, EL ROL,, DE, IDIOMA, RECURSOS, VENTANAS, BUSCAR, DURANTE, EL ÍNDICE, LA CREACIÓN, EL PROCESO           |
| Eliminación de palabras irrelevantes      | ILUSTRACIÓN, ILUSTRA EL ROL, EL IDIOMA, LOS RECURSOS, LAS VENTANAS, LA BÚSQUEDA, DURANTE, EL ÍNDICE, LA CREACIÓN, EL PROCESO                            |
| Guardar en Índice de texto completo | ILUSTRACIÓN, ILUSTRA EL ROL, EL IDIOMA, LOS RECURSOS, LAS VENTANAS, LA BÚSQUEDA, DURANTE, EL ÍNDICE, LA CREACIÓN, EL PROCESO                            |



 

Los separadores de palabras y lematizadores se utilizan para expandir las consultas [FREETEXT](-search-sql-freetext.md) en el momento de la consulta. La configuración regional de la consulta es la configuración regional predeterminada a menos que se pase un identificador de código de idioma (LCID) como parámetro de consulta. El componente de consulta invoca el separador de palabras adecuado en los términos de consulta enumerados en la cláusula [Where](-search-sql-where.md) de la consulta. Por ejemplo, si la cláusula WHERE de la consulta contiene "FREETEXT (manzanas, naranjas y peras)", el separador de palabras recibe el texto "manzanas, naranjas y peras". Si la cláusula WHERE de la consulta usa el predicado [Contains](-search-sql-contains.md) Text, se normaliza el resultado del texto del separador de palabras. De lo contrario, el componente de consulta pasa cada palabra identificada por el separador de palabras al analizador lingüístico adecuado para ese idioma y configuración regional. El analizador lingüístico genera una lista de formularios alternativos o que se derivan de esa palabra. El componente de consulta normaliza la lista expandida de términos de consulta y quita las palabras irrelevantes.

En la tabla siguiente se enumeran las acciones y los resultados correspondientes para la consulta "manzanas, naranjas y peras".



| Acción                       | Texto resultante                                            |
|------------------------------|-----------------------------------------------------------|
| Texto original                | manzanas, naranjas y peras                                |
| División de palabras                | manzanas, naranjas y, peras, EOS                          |
| Raíz                     | Apple, manzanas, naranja, naranja, naranja y, pera, peras |
| Normalización                | APPLE, MANZANAS, NARANJA, NARANJA, NARANJA Y, PERA, PERAS |
| Eliminación de palabras irrelevantes           | APPLE, MANZANAS, NARANJA, NARANJA, NARANJA, PERALES, PERAS      |
| Lista expandida de términos de consulta | APPLE, MANZANAS, NARANJA, NARANJA, NARANJA, PERALES, PERAS      |



 

Los términos de consulta expandidos aumentan la probabilidad de que la consulta busque documentos que coincidan con la intención de la consulta original. El texto que genera el separador de palabras o el analizador lingüístico en el momento de la consulta no se almacena en el disco.

## <a name="word-breaking"></a>Separación de palabras

La separación de palabras es la separación del texto en tokens de texto individuales o palabras. Muchos idiomas, especialmente los que tienen alfabetos romanos, tienen una matriz de separadores de palabras (como un espacio en blanco) y signos de puntuación que se usan para discernir palabras, frases y oraciones. Los separadores de palabras deben basarse en la heurística de lenguaje precisa para proporcionar resultados confiables y precisos. La separación de palabras es más compleja para sistemas basados en caracteres de escritura o de alfabetos basados en script, donde el significado de los caracteres individuales se determina a partir del contexto. Para obtener más información sobre las consideraciones lingüísticas que pueden afectar a la implementación de separadores de palabras, consulte [consideraciones lingüísticas y Unicode](linguistic-and-unicode-considerations.md).

## <a name="stemming"></a>Raíz

Windows Search se aplica lematizadores exclusivamente en el momento de la consulta para generar formularios de Word adicionales para términos en las consultas [FREETEXT](-search-sql-freetext.md) y de propiedades. Lematizadores realizar análisis morfológicos y aplicar reglas gramaticales para generar una lista de formas alternativas o derivadas para las palabras. Los formularios alternativos suelen tener el mismo tallo o el mismo formulario base. Al generar las formas derivadas para una palabra, el servicio de Index Server devuelve los resultados de la consulta que son estadísticamente más relevantes para una consulta. Por ejemplo, una consulta de texto completo para "nadar Meet" coincide con los documentos que contienen "nadar, nadar, nadar, nadar", natación, Swam, swum "o" Meet, Meets, meetd, meetd ", Meeting, mét" y combinaciones de estos términos.

Algunos lenguajes requieren que los términos supuestos se generen en el tiempo de índice y en el tiempo de consulta para las inflexiones estándar y variantes. En este caso, la lematización se produce en el componente separador de palabras, con una lematización mínima en el analizador real. Por ejemplo, el separador de palabras en japonés realiza la lematización durante la creación de índices y las consultas para permitir que una consulta busque diferentes formas de los términos de búsqueda.

## <a name="normalization"></a>Normalización

Los documentos de todos los lenguajes se almacenan en un solo índice. Aunque las reglas lingüísticas y de palabras se diferencian drásticamente, hay algunas consideraciones, como números, fechas y horas, que se tratan de forma coherente en todos los separadores de palabras. Para obtener más información sobre las consideraciones de normalización que pueden afectar a la implementación de separadores de palabras, vea [normalización de formularios de superficie](surface-form-normalization.md).

## <a name="noise-words"></a>Palabras irrelevantes

Las palabras irrelevantes, también conocidas como palabras vacías, son palabras que no son indicadores significativos para el contenido. El servicio de Index Server quita las palabras irrelevantes de los términos de la consulta y del contenido que se incluye en el índice de texto completo. Un *desplazamiento* es la aparición de una palabra en un documento o en una lista de términos de consulta. El desplazamiento de las palabras irrelevantes en un documento o una consulta se registra en blanco. La eliminación de palabras irrelevantes mejora el rendimiento de las consultas evitando el crecimiento innecesario del índice. También mejora la relevancia de los resultados de la consulta. Puede configurar Windows Search para que use listas de palabras irrelevantes para idiomas específicos. Estas listas se usan cuando se invoca un separador de palabras para ese idioma. Por ejemplo, "la" en el idioma inglés se produce con tanta frecuencia que tiene poco valor como clave única. "El" está en la lista de palabras irrelevantes, no se escribe en el índice de contenido y, si se consulta para, no devuelve ningún resultado.

Las palabras irrelevantes actúan como marcadores de posición en las consultas de frases. Un documento que contiene el texto "WAG the Dog" se almacena en el índice con "WAG" en la ocurrencia 1 y "Dog" en la ocurrencia 3. La consulta de frase "WAG Dog" no coincide, pero la frase "WAG a Dog" sí lo hace, ya que la información de las repeticiones coincide. La frase "WAG Purple Dog" no coincide porque "Purple" no se encuentra en el índice en la ocurrencia 2. No obstante, una consulta para "WAG the Dog" devuelve documentos que contienen "WAG Purple Dog" porque no hay ninguna manera de determinar de forma eficaz si el documento tenía una palabra no irrelevante entre "WAG" y "Dog".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Extensión de recursos de idioma](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Implementar un separador de palabras y un analizador lingüístico](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[Consideraciones lingüísticas y Unicode](linguistic-and-unicode-considerations.md)
</dt> <dt>

[Solución de problemas de recursos de lenguaje y procedimientos recomendados](troubleshooting-language-resources.md)
</dt> </dl>

 

 
