---
description: Microsoft proporciona separadores de palabras y lematizadores para varios idiomas. En este tema se describe cómo implementar y usar separadores de palabras y lematizadores personalizados para idiomas y configuraciones regionales más allá de los proporcionados por Microsoft.
ms.assetid: 47768691-7071-440e-bfbf-975713880c00
title: Implementar un separador de palabras y un lematizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fcabd4074f9a61587492e70841e98a9ba29a60b81fd07fbeff2498754245085
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863064"
---
# <a name="implementing-a-word-breaker-and-stemmer"></a>Implementar un separador de palabras y un lematizador

Microsoft proporciona separadores de palabras y lematizadores para varios idiomas. En este tema se describe cómo implementar y usar separadores de palabras y lematizadores personalizados para idiomas y configuraciones regionales más allá de los proporcionados por Microsoft.

> [!Note]
> A partir de julio de 2018 se realizó un cambio de seguridad en Windows Server 2019 que impide que SearchIndexer.exe cargue archivos DLL sin una firma de Microsoft. Como resultado, Windows Server 2019 ya no admite separadores de palabras personalizados firmados por Microsoft. 

Este tema se organiza de la siguiente manera:

-   [Registro de un archivo DLL de recursos de lenguaje](#registering-a-language-resource-dll)
-   [Registro de un idioma](#registering-a-language-resource-dll)
-   [Implementación de un beaker de Word](#implementing-a-word-beaker)
    -   [WordSink y PhraseSink](#wordsink-and-phrasesink)
    -   [Saltos](#breaks)
    -   [Escalabilidad, rendimiento y seguridad](#scalability-performancy-and-security)
-   [Implementación de un lematizador](#implementing-a-stemmer)
    -   [Escalabilidad, rendimiento y seguridad](#scalability-performancy-and-security)
-   [Temas relacionados](#related-topics)

## <a name="registering-a-language-resource-dll"></a>Registro de un archivo DLL de recursos de lenguaje

Cada archivo DLL de recursos de lenguaje debe implementar y exportar los siguientes puntos de entrada. El archivo DLL se puede registrar para que esté en cualquier carpeta.

-   DllMain es el punto de entrada estándar a DLL.
-   DllRegisterServer registra el archivo DLL en el registro, por ejemplo, `regsvr32.exe %SystemRoot%\MyFolder\wordbreaker.dll`
-   DllCanUnloadNow permite a los clientes llamar a este punto de entrada a través del Modelo de objetos componentes (COM) para determinar si es posible descargar el archivo DLL de recursos de lenguaje.
-   DllUnRegisterServer quita el archivo DLL del Registro.

## <a name="registering-a-language"></a>Registro de un idioma

El Registro contiene entradas específicas del idioma para el idioma que se está indexando y estas entradas controlan las partes de los procesos de indexación y consulta específicos del lenguaje. Estas entradas del Registro se pueden encontrar en la siguiente clave del Registro.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         ContentIndex
            Control
               Language
                  
```

## <a name="implementing-a-word-beaker"></a>Implementación de un beaker de Word

Los separadores de palabras [**implementan IWordBreaker.**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) El [**método IWordBreaker::BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) realiza todo el procesamiento y análisis de texto. Para implementar un componente de separador de palabras, debe tener heurística de idioma para el idioma. Esto incluye información sobre la sintaxis y la morfología. También puede que necesite una lista de palabras para excluir o incluir. El archivo de palabras ruido para la configuración regional del idioma se compila a partir de la lista de palabras excluidas. Para obtener más información sobre las consideraciones lingüísticas y cómo afectan estas consideraciones a las implementaciones de separador de palabras, vea [Consideraciones lingüísticas y Unicode.](linguistic-and-unicode-considerations.md)

El propósito principal de [**IWordBreaker::BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) es procesar texto continuamente desde [**TEXT \_ SOURCE**](/windows/win32/api/indexsrv/ns-indexsrv-text_source) hasta que se procese todo el texto o hasta que el separador de palabras encuentre un error. En este bucle de procesamiento de datos, **IWordBreaker::BreakText** llama a métodos de análisis y de utilidad que realizan tareas específicas para ese proceso. Por ejemplo, el separador de palabras alemán puede controlar palabras compuestas, mientras que el separador de palabras francés puede procesar [signos diacríticos](surface-form-normalization.md) [o clitics](surface-form-normalization.md). Las funciones específicas que realiza el separador de palabras y la estrategia que usa para realizar estas tareas dependen completamente de los requisitos de ese lenguaje.

Al dividir el texto, los separadores de palabras identifican formas "alternativas" para las palabras que pueden tener varias representaciones. No hay ninguna relación semántica implícita entre las palabras generadas. De hecho, es posible que la palabra original no se incluya en la lista de alternativas. Los formularios alternativos se guardan en la misma posición del índice que la palabra original para indicar que son idénticos.

Cuando se incluye un documento en el índice, a cada palabra se le asigna un valor entero que representa el desplazamiento o la distancia de la palabra desde el principio de un documento. La distancia relativa entre las palabras de una consulta se compara con los desplazamientos almacenados en el índice de texto completo. La consulta "Where is Ctrl's document" coincide con cualquier documento con "Where" en el desplazamiento n, "is" en n+1, "Va" en n+2 y "document" en n+3. "¿Dónde se ha presentado el documento de Asíns en la base de datos?" se representa como:



|       |     |                        |          |       |     |     |                               |
|-------|-----|------------------------|----------|-------|-----|-----|-------------------------------|
| Where | is  | De Asínes<br/> | documento | Presentado | in  | el | base de datos de base de datos<br/> |



 

En este ejemplo, el separador de palabras almacena formularios alternativos para "Asín" y "base de datos" en el índice. El separador de palabras genera y almacena palabras alternativas durante el proceso de creación del índice en las condiciones siguientes:

-   Si es probable que una palabra alternativa aparezca como una sola palabra en una consulta
-   Si no es probable que un lematizador derive la palabra original de la alternativa

La generación de formularios de palabras alternativos aumenta el número de formas que las consultas representan y coinciden con una oración, como se muestra en las variaciones siguientes:

1.  ¿Dónde se ha presentado el documento de Asíns en la base de datos?
2.  ¿Dónde se ha presentado el documento de Asíns en la base de datos?
3.  ¿Dónde se ha presentado el documento de Asíns en la base de datos?
4.  ¿Dónde se ha presentado el documento de Asíns en la base de datos?

### <a name="wordsink-and-phrasesink"></a>WordSink y PhraseSink

Los separadores de palabras usan los objetos [**IWordSink**](iwordsink.md) e [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) para recopilar y almacenar todas las palabras y frases que extraen del texto. Un separador de palabras almacena las palabras en un formulario lo más cercano posible al formulario de palabra original del documento. **IPhraseSink** almacena frases en tiempo de consulta. Las frases mejoran la relevancia de los resultados de la consulta porque las secuencias de palabras más largas son más poco frecuentes y proporcionan una mayor distinción que las frases más pequeñas. Cuando el indexador coloca una frase en **IPhraseSink** en el momento de la consulta, crea una instancia del separador de palabras para dividir la frase en palabras. A continuación, el indexador evalúa la frase comprobando si las palabras de la frase se producen adyacentes entre sí en el índice. Por ejemplo, si se produce "ABCD" en el índice en las posiciones *x*, *x*+1, *x*+2 y *x*+3, se producirá la coincidencia de frases si se envía alguna subcadena adyacente de "ABCD" en una consulta. Esta estrategia es eficaz para los separadores de palabras basados en caracteres que dividen frases y palabras largas durante la creación del índice y que generan frases durante el tiempo de consulta.

### <a name="breaks"></a>Saltos

Los saltos son los espacios entre palabras. Los espacios en blanco, los signos de puntuación, el formato o simplemente la naturaleza del propio lenguaje pueden provocar interrupciones. Hay cuatro tipos diferentes de saltos que usa el indexador: final de palabra (EOW), fin de oración (EOS), fin de párrafo (EOP) y final del capítulo (EOC). La interrupción EOW es la predeterminada. Después de cada token, cada interrupción indica una distancia semántica diferente entre las palabras de cada lado. Las palabras separadas por EOW tienen el vínculo semántico más estricto, seguido de EOS, EOP y EOC. Varias llamadas a [**IWordSink::P utBreak**](iwordsink-putbreak.md) son acumulativas y son análogas a la inserción de palabras o oraciones nulas.

### <a name="scalability-performancy-and-security"></a>Escalabilidad, rendimiento y seguridad

La forma en que el separador de palabras responde a llamadas simultáneas viene determinada en gran medida por la elección del modelo de subprocesamiento. El indexador es una aplicación de un solo subproceso. Para que los separadores de palabras funcionen en un entorno de un solo subproceso, los separadores de palabras deben escribirse con un modelo de subprocesos "libre" o "ambos". Los separadores de palabras no deben registrarse con COM mediante el modelo de subprocesos "apartment".

Se recomienda que los separadores de palabras eviten los estados globales y almacenen datos en la instancia del separador de palabras. El único contenido que se debe almacenar en la implementación del separador de palabras es para los parámetros *fQuery* y *ulMaxTokenSize.* Los separadores de palabras no deben ser más de dos veces más lentos que el banco de pruebas establecido por el separador de palabras inglés. El rendimiento del separador de palabras también debe mejorar con una mayor funcionalidad de hardware.

Los separadores de palabras para el indexador se ejecutan en el contexto de seguridad del sistema local. Se deben escribir para administrar búferes y para apilar correctamente. Todas las copias de cadena deben tener comprobaciones explícitas para protegerse contra saturaciones de búfer. Siempre debe comprobar el tamaño asignado del búfer y probar el tamaño de los datos con el tamaño del búfer. Los separadores de palabras no pueden suponer que el texto pasado al método [**IWordBreaker::BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) tiene el formato correcto. Para obtener más información sobre la solución de problemas de separadores de palabras, vea Solución de problemas [de recursos de lenguaje y procedimientos recomendados.](troubleshooting-language-resources.md)

## <a name="implementing-a-stemmer"></a>Implementación de un lematizador

Los lematizadores implementan la [**interfaz IStemmer.**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) El [**método IStemmer::GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) genera una lista de formularios de palabras desenfasados para una palabra de entrada determinada. Para implementar un componente de lematizador, debe tener heurística del lenguaje para su idioma. Esto incluye información sobre la morfología. También puede que necesite una lista de palabras para excluir o incluir. Para obtener más información sobre las consideraciones lingüísticas y cómo afectan estas consideraciones a las implementaciones de lematizador, vea [Consideraciones lingüísticas y Unicode.](linguistic-and-unicode-considerations.md)

Se recomienda que los lematizadores no generen mayúsculas de minúsculas ni posesivas para las palabras. Por ejemplo, "David" no se genera como una forma alternativa para "David". El separador de palabras genera "David" y "David" cuando analiza "David".

El lematizador usa el [objeto IWordFormSink](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) para recopilar la lista de palabras alternativas. [**IWordFormSink::P utWord**](iwordformsink-putword.md) genera la palabra final del lematizador. En todos los casos, esta palabra final es la misma que la palabra de entrada de [**IStemmer::GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms). Por ejemplo, dada la palabra "nado", el lematizador genera las siguientes formas de palabra: "nadando", "nadando", "nadando" y "swum", a través de llamadas a [**IWordFormSink::P utAltWord**](iwordformsink-putphrase.md). El lematizador genera "nada" a través **de IWordFormSink::P utWord**.

### <a name="scalability-performancy-and-security"></a>Escalabilidad, rendimiento y seguridad

Los lematizadores, al igual que los separadores de palabras, deben usar un modelo de subprocesamiento "libre" y registrarse en COM con su modelo de subprocesos establecido en "gratis" o "ambos". Windows La búsqueda llama a instancias independientes del lematizador desde subprocesos diferentes al mismo tiempo. Por lo tanto, los lematizadores deben tener datos de instancia mínimos.

La precisión del lematizador tiene un impacto significativo en la relevancia de las consultas. Si el lematizador lematizador le da el texto incorrectamente, las consultas pueden devolver resultados imprevisibles e inexactos. Los lematizadores deben controlar cientos de consultas por segundo sin afectar negativamente al rendimiento de las consultas. El rendimiento del lematizador debe mejorar con una mayor funcionalidad de hardware. Para obtener información sobre la solución de problemas de lematizadores, consulte Solución de problemas [de recursos de lenguaje y procedimientos recomendados.](troubleshooting-language-resources.md)

Los lematizadores Windows search se ejecutan en el contexto de seguridad local. Se deben escribir para administrar búferes y para apilar correctamente. Todas las copias de cadena deben tener comprobaciones explícitas para protegerse contra saturaciones de búfer. Siempre debe comprobar el tamaño asignado del búfer y probar el tamaño de los datos con el tamaño del búfer.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Extensión de recursos de lenguaje](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Descripción de los componentes de recursos de lenguaje](understanding-language-resource-components.md)
</dt> <dt>

[Consideraciones lingüísticas y Unicode](linguistic-and-unicode-considerations.md)
</dt> <dt>

[Solución de problemas de recursos de lenguaje y procedimientos recomendados](troubleshooting-language-resources.md)
</dt> </dl>

 

 
