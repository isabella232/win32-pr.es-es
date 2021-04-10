---
description: Microsoft proporciona separadores de palabras y lematizadores para varios idiomas. En este tema se describe cómo implementar y usar separadores de palabras y lematizadores personalizados para idiomas y configuraciones regionales más allá de las proporcionadas por Microsoft.
ms.assetid: 47768691-7071-440e-bfbf-975713880c00
title: Implementar un separador de palabras y un analizador lingüístico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd4f4e3210e7f4e17bb035115fd694656cc6e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082016"
---
# <a name="implementing-a-word-breaker-and-stemmer"></a>Implementar un separador de palabras y un analizador lingüístico

Microsoft proporciona separadores de palabras y lematizadores para varios idiomas. En este tema se describe cómo implementar y usar separadores de palabras y lematizadores personalizados para idiomas y configuraciones regionales más allá de las proporcionadas por Microsoft.

> [!Note]
> A partir del 2018 de julio, se realizó un cambio de seguridad en Windows Server 2019 que impide que los archivos DLL que no tengan una firma de Microsoft se carguen mediante SearchIndexer.exe. Como resultado, Windows Server 2019 ya no es compatible con los separadores de palabras personalizados firmados que no sean de Microsoft. 

Este tema se organiza de la siguiente manera:

-   [Registro de un archivo DLL de recursos de idioma](#registering-a-language-resource-dll)
-   [Registrar un idioma](#registering-a-language-resource-dll)
-   [Implementación de un vaso de palabras](#implementing-a-word-beaker)
    -   [WordSink y PhraseSink](#wordsink-and-phrasesink)
    -   [Saltos](#breaks)
    -   [Escalabilidad, performancy y seguridad](#scalability-performancy-and-security)
-   [Implementación de un analizador lingüístico](#implementing-a-stemmer)
    -   [Escalabilidad, performancy y seguridad](#scalability-performancy-and-security)
-   [Temas relacionados](#related-topics)

## <a name="registering-a-language-resource-dll"></a>Registro de un archivo DLL de recursos de idioma

Cada archivo DLL de recursos de idioma debe implementar y exportar los siguientes puntos de entrada. El archivo DLL se puede registrar para que esté en cualquier carpeta.

-   DllMain es el punto de entrada estándar a DLL.
-   DllRegisterServer registra el archivo DLL en el registro, como `regsvr32.exe %SystemRoot%\MyFolder\wordbreaker.dll`
-   DllCanUnloadNow permite que los clientes llamen a este punto de entrada a través del modelo de objetos componentes (COM) para determinar si es posible descargar el archivo DLL de recursos de idioma.
-   DllUnRegisterServer quita el archivo DLL del registro.

## <a name="registering-a-language"></a>Registrar un idioma

El registro contiene entradas específicas del idioma para el idioma que se está indizando y estas entradas controlan las partes de los procesos de indexación y consulta que son específicos del idioma. Estas entradas del registro pueden encontrarse en la siguiente clave del registro.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         ContentIndex
            Control
               Language
                  
```

## <a name="implementing-a-word-beaker"></a>Implementación de un vaso de palabras

Los separadores de palabras implementan [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker). El método [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) realiza todo el procesamiento y el análisis de texto. Para implementar un componente de separador de palabras, debe tener la heurística de idioma para su idioma. Esto incluye información sobre la sintaxis y la morfología. También puede necesitar una lista de palabras para excluir o incluir. Cree el archivo de palabras irrelevantes para su configuración regional de idioma en la lista de palabras excluidas. Para obtener más información sobre las consideraciones lingüísticas y el modo en que estas consideraciones afectan a las implementaciones de separadores de palabras, consulte [consideraciones lingüísticas y Unicode](linguistic-and-unicode-considerations.md).

El propósito principal de [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) es procesar el texto continuamente desde el [**\_ origen del texto**](/windows/win32/api/indexsrv/ns-indexsrv-text_source) hasta que se procese todo el texto, o hasta que el separador de palabras encuentre un error. En este bucle de procesamiento de datos, **IWordBreaker:: BreakText** llama a métodos de análisis y de utilidad que realizan tareas específicas para ese proceso. Por ejemplo, el separador de palabras en alemán puede controlar palabras compuestas, mientras que el separador de palabras en francés puede procesar [signos diacríticos](surface-form-normalization.md) o [clitics](surface-form-normalization.md). Las funciones específicas que realiza el separador de palabras y la estrategia que utiliza para realizar estas tareas dependen por completo de los requisitos de ese idioma.

Al romper texto, los separadores de palabras identifican los formularios "alternativos" para las palabras que pueden tener varias representaciones. No se implica ninguna relación semántica entre las palabras generadas. De hecho, es posible que la palabra original no esté incluida entre la lista de alternativas. Los formularios alternativos se guardan en la misma posición en el índice que la palabra original para indicar que son idénticos.

Cuando se incluye un documento en el índice, se asigna a cada palabra un valor entero que representa el desplazamiento, o la distancia de la palabra desde el principio de un documento. La distancia relativa entre las palabras de una consulta se compara con los desplazamientos almacenados en el índice de texto completo. La consulta "Where is Kyle Document" coincide con cualquier documento con "where" en el desplazamiento n, "is" en n + 1, "Kyle" en n + 2 y "Document" en n + 3. "¿Dónde se archivó el documento de Kyle en la base de datos?" se representa como:



|       |     |                        |          |       |     |     |                               |
|-------|-----|------------------------|----------|-------|-----|-----|-------------------------------|
| Where | is  | Kyle Kyle<br/> | documento | registrado | in  | el | base de datos Database<br/> |



 

En este ejemplo, el separador de palabras almacena formularios alternativos para "Kyle" ("Kyle") y "Database" ("base de datos") en el índice. El separador de palabras genera y almacena palabras alternativas durante el proceso de creación de índices en las siguientes condiciones:

-   Si es probable que una palabra alternativa aparezca como una sola palabra en una consulta
-   Si no es probable que un analizador lingüístico derive la palabra original de la alternativa

La generación de formularios de Word alternativos aumenta el número de formas en que las consultas representan y coinciden con una oración, tal y como se muestra en las siguientes variaciones:

1.  Donde es el documento Kyle almacenado en la base de datos
2.  Donde es el documento de Kyle en la base de datos
3.  Donde es el documento Kyle almacenado en la base de datos
4.  Donde es el documento de Kyle en la base de datos

### <a name="wordsink-and-phrasesink"></a>WordSink y PhraseSink

Los separadores de palabras usan los objetos [**IWordSink**](iwordsink.md) y [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) para recopilar y almacenar todas las palabras y frases que extraen del texto. Un separador de palabras almacena las palabras en un formato lo más cerca posible del formulario de Word original en el documento. **IPhraseSink** almacena frases en el momento de la consulta. Las frases mejoran la relevancia de los resultados de la consulta, ya que las secuencias de palabras más largas son menos frecuentes y ofrecen una distinción mayor que las frases más pequeñas. Cuando el indexador coloca una frase en el **IPhraseSink** en el momento de la consulta, crea una instancia del separador de palabras para dividir la frase en palabras. A continuación, el indexador evalúa la frase comprobando si las palabras de la frase aparecen adyacentes entre sí en el índice. Por ejemplo, si "ABCD" aparece en el índice en las posiciones *x*, *x*+ 1, *x*+ 2 y *x*+ 3, la frase se producirá si se envía cualquier subcadena adyacente de "ABCD" en una consulta. Esta estrategia es eficaz para los separadores de palabras basados en caracteres que dividen frases y largas palabras durante la creación del índice y que generan frases durante el tiempo de consulta.

### <a name="breaks"></a>Saltos

Los saltos son los espacios entre las palabras. Los espacios en blanco, los signos de puntuación, los formatos o simplemente la naturaleza del propio idioma pueden provocar interrupciones. Hay cuatro tipos diferentes de interrupciones que usa el indexador: final de palabra (EOW), final de frase (EOS), final de párrafo (EOP) y final del capítulo (EOC). La interrupción EOW es la interrupción predeterminada. Después de cada token, cada interrupción indica una distancia semántica diferente entre las palabras de ambos lados. Las palabras separadas por EOW tienen el vínculo semántico más estrecho, seguido de EOS, EOP y EOC. Varias llamadas a [**IWordSink::P utbreak**](iwordsink-putbreak.md) son acumulativas y son análogas a la inserción de palabras o oraciones nulas.

### <a name="scalability-performancy-and-security"></a>Escalabilidad, performancy y seguridad

La forma en que el separador de palabras responde a las llamadas simultáneas viene determinada en gran medida por el modelo de subprocesos elegido. El indexador es una aplicación de un solo subproceso. Para que los separadores de palabras funcionen en un entorno de un solo subproceso, los separadores de palabras se deben escribir con un modelo de subprocesos "Free" o "both". Los separadores de palabras no deben registrarse con COM mediante el modelo de subprocesos "Apartamento".

Se recomienda que los separadores de palabras eviten los Estados globales y almacenen los datos en la instancia del separador de palabras. El único contenido que debe almacenarse en la implementación del separador de palabras son para los parámetros *fQuery* y *ulMaxTokenSize*. Los separadores de palabras no deben ser más de dos veces más lentos que la prueba comparativa establecida por el separador de palabras en inglés. El rendimiento del separador de palabras también debe mejorar con mayor capacidad de hardware.

Los separadores de palabras del indexador se ejecutan en el contexto de seguridad del sistema local. Se deben escribir para administrar los búferes y para apilarlos correctamente. Todas las copias de cadena deben tener comprobaciones explícitas para evitar las saturaciones del búfer. Siempre debe comprobar el tamaño asignado del búfer y probar el tamaño de los datos con respecto al tamaño del búfer. Los separadores de palabras no pueden suponer que el texto que se pasa al método [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) tiene el formato correcto. Para obtener más información acerca de cómo solucionar problemas de los separadores de palabras, consulte [solución de problemas de recursos de lenguaje y procedimientos recomendados](troubleshooting-language-resources.md).

## <a name="implementing-a-stemmer"></a>Implementación de un analizador lingüístico

Lematizadores implementa la interfaz [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) . El método [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) genera una lista de formas de palabras derivadas para una palabra de entrada determinada. Para implementar un componente lingüístico, debe tener la heurística de idioma para su idioma. Esto incluye información sobre la morfología. También puede necesitar una lista de palabras para excluir o incluir. Para obtener más información acerca de las consideraciones lingüísticas y el modo en que estas consideraciones afectan a las implementaciones de lingüísticos, consulte [consideraciones lingüísticas y Unicode](linguistic-and-unicode-considerations.md).

Se recomienda que lematizadores no genere el caso genitivo, o Possessive, para las palabras. Por ejemplo, "David" no se genera como una forma alternativa para "David". El separador de palabras genera "David" y "David" cuando analiza "David".

El analizador lingüístico usa el objeto [IWordFormSink](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) para recopilar la lista de palabras alternativas. [**IWordFormSink::P utword**](iwordformsink-putword.md) genera la palabra final a partir del analizador lingüístico. En todos los casos, esta palabra final es igual que la palabra de entrada de [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms). Por ejemplo, dada la palabra "nadar", el analizador lingüístico genera los siguientes formatos de palabra: "natación", "Swimmer", "nadar", "Swam" y "swum", a través de las llamadas a [**IWordFormSink::P utaltword**](iwordformsink-putphrase.md). El analizador lingüístico genera "nadar" a través de **IWordFormSink::P utword**.

### <a name="scalability-performancy-and-security"></a>Escalabilidad, performancy y seguridad

Lematizadores, al igual que los separadores de palabras, deben usar un modelo de subprocesos "gratuito" y registrarse con COM con el modelo de subprocesos establecido en "Free" o "both". Windows Search llama a instancias independientes del analizador lingüístico desde distintos subprocesos al mismo tiempo. Por lo tanto, lematizadores debe tener datos de instancia mínimos.

La precisión de los lingüísticos tiene un impacto significativo en la relevancia de la consulta. Si el analizador lingüístico no tiene el texto correctamente, las consultas pueden devolver resultados imprevisibles e imprecisos. Lematizadores debe controlar cientos de consultas por segundo sin afectar negativamente al rendimiento de las consultas. El rendimiento del analizador lingüístico debería mejorar con mayor capacidad de hardware. Para obtener información sobre la solución de problemas de lematizadores, consulte [solución de problemas de recursos de lenguaje y procedimientos recomendados](troubleshooting-language-resources.md).

Lematizadores para Windows Search se ejecuta en el contexto de seguridad local. Se deben escribir para administrar los búferes y para apilarlos correctamente. Todas las copias de cadena deben tener comprobaciones explícitas para evitar las saturaciones del búfer. Siempre debe comprobar el tamaño asignado del búfer y probar el tamaño de los datos con respecto al tamaño del búfer.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Extensión de recursos de idioma](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Descripción de los componentes de recursos de lenguaje](understanding-language-resource-components.md)
</dt> <dt>

[Consideraciones lingüísticas y Unicode](linguistic-and-unicode-considerations.md)
</dt> <dt>

[Solución de problemas de recursos de lenguaje y procedimientos recomendados](troubleshooting-language-resources.md)
</dt> </dl>

 

 
