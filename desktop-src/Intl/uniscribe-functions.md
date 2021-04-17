---
description: En esta sección se describen las funciones de tipografía y para el procesamiento de scripts complejos.
ms.assetid: 876e36f5-a91c-490b-87bd-b7cb4993f8c4
title: Funciones de Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f623c8da04f985f88d091f8e9e2b4cb724c0801
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653091"
---
# <a name="uniscribe-functions"></a>Funciones de Uniscribe

En esta sección se describen las funciones de tipografía y para el procesamiento de scripts complejos.



| Función                                                               | Descripción                                                                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution)   | Aplica la configuración de sustitución de dígitos especificada a las estructuras de control de script y de estado de script especificadas.                                                                    |
| [**ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)             | Toma una matriz de anchos de avance para una ejecución y genera una matriz de anchos de glifos adelantados ajustados.                                                                               |
| [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)                                     | Recupera información para determinar los saltos de línea.                                                                                                                                |
| [**ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight)                   | Recupera el alto de la fuente almacenada actualmente en la memoria caché.                                                                                                                                |
| [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)                                     | Genera el desplazamiento x desde el extremo izquierdo o el borde inicial de una ejecución hasta el borde inicial o final de un clúster de caracteres lógicos.                                          |
| [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache)                             | Libera una memoria caché de scripts.                                                                                                                                                             |
| [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap)                                 | Recupera los índices de glifo de los caracteres Unicode de una cadena de acuerdo con la tabla de tipos de colores TrueType o la tabla CMAP estándar implementada para fuentes de estilo antiguo.         |
| [**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)   | Recupera una lista de glifos alternativos para un carácter especificado al que se puede tener acceso a través de una característica OpenType especificada.                                                         |
| [**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)           | Recupera una lista de características tipográficas para el sistema de escritura definido para el procesamiento de OpenType.                                                                                  |
| [**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)         | Recupera una lista de etiquetas de lenguaje que están disponibles para el elemento especificado y que son compatibles con una etiqueta de script especificada para el procesamiento de OpenType.                                  |
| [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)             | Recupera información de la memoria caché de fuentes en los glifos especiales utilizados por una fuente.                                                                                                   |
| [**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)             | Recupera una lista de scripts disponibles en la fuente para el procesamiento de OpenType.                                                                                                        |
| [**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth)               | Recupera el ancho ABC de un glifo determinado.                                                                                                                                         |
| [**ScriptGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths)               | Convierte los anchos de avance del glifo para una fuente concreta en el ancho lógico.                                                                                                        |
| [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties)                     | Recupera información sobre los scripts actuales.                                                                                                                                  |
| [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex)                             | Determina si una cadena Unicode requiere un procesamiento de scripts complejo.                                                                                                           |
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)                                 | Divide una cadena Unicode en elementos con forma individual.                                                                                                                        |
| [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)                 | Divide una cadena Unicode en elementos que se van a formar individualmente y proporciona una matriz de etiquetas de características para cada elemento que se va a formar para el procesamiento de OpenType.                                  |
| [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify)                                 | Crea una tabla de anchos de avance para permitir la justificación del texto cuando se pasa a la función [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) .                                                   |
| [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout)                                   | Convierte una matriz de niveles de incrustación de ejecución en una asignación de posición de visual a lógica y/o de lógica a visual.                                                               |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)                                     | Genera el ancho de avance del glifo y la información de desplazamiento bidimensional a partir de la salida de [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape).                                                       |
| [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)                     | Genera glifos y atributos visuales para una ejecución de Unicode con información OpenType de la salida de [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).                         |
| [**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)         | Coloca un solo glifo con un solo ajuste mediante una característica especificada proporcionada en la fuente para el procesamiento de OpenType.                                                         |
| [**ScriptRecordDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) | Lee la configuración de la sustitución de dígitos nativos del dígito y del dígito de National Language support (NLS) y los registra en una estructura de [**\_ DIGITSUBSTITUTE de script**](/windows/win32/api/usp10/ns-usp10-script_digitsubstitute) . |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)                                     | Genera glifos y atributos visuales para una ejecución de Unicode.                                                                                                                         |
| [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)                     | Genera glifos y atributos visuales para una ejecución de Unicode con información OpenType.                                                                                               |
| [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)                     | Analiza una cadena de texto sin formato.                                                                                                                                                     |
| [**ScriptStringCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox)                         | Recupera la coordenada x del borde inicial o final de una posición de carácter.                                                                                              |
| [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)                           | Libera una estructura [**de \_ \_ análisis de cadenas de script**](script-string-analysis.md) .                                                                                                     |
| [**ScriptStringGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths)   | Convierte los anchos visuales en anchos lógicos.                                                                                                                                       |
| [**ScriptStringGetOrder**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder)                   | Crea una matriz que asigna una posición de carácter original a una posición del glifo.                                                                                                    |
| [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)                             | Muestra una cadena generada por una llamada anterior a [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) y, opcionalmente, agrega resaltado.                                               |
| [**ScriptString \_ pcOutChars**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars)            | Devuelve un puntero a la longitud de una cadena después del recorte.                                                                                                                       |
| [**ScriptString \_ pLogAttr**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr)                | Devuelve un puntero a un búfer de atributos lógicos para una cadena analizada.                                                                                                          |
| [**ScriptString \_ pSize**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize)                      | Devuelve un puntero a una estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85)) para una cadena analizada.                                                                                                     |
| [**ScriptStringValidate**](/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate)                   | Comprueba si hay secuencias no válidas en una estructura de [**\_ \_ análisis de cadenas de script**](script-string-analysis.md) .                                                                              |
| [**ScriptStringXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp)                         | Convierte una coordenada x en una posición de carácter.                                                                                                                                 |
| [**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)     | Habilita la sustitución de un solo glifo con una forma alternativa del mismo glifo para el procesamiento de OpenType.                                                                         |
| [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)                                 | Muestra el texto de la forma de script especificada y la información de ubicación.                                                                                                               |
| [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)                                     | Genera el borde inicial o final de un clúster de caracteres lógicos a partir del desplazamiento x de una ejecución.                                                                                 |



 

 

 
