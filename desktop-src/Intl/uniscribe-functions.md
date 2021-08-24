---
description: En esta sección se describen las funciones para la tipografía y para el procesamiento de scripts complejos.
ms.assetid: 876e36f5-a91c-490b-87bd-b7cb4993f8c4
title: Funciones de unidiscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547bdd2179e734120fe07c2ae774c8a066d9fd5d9db2be1262e67b505cbb04ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582195"
---
# <a name="uniscribe-functions"></a>Funciones de unidiscribe

En esta sección se describen las funciones para la tipografía y para el procesamiento de scripts complejos.



| Función                                                               | Descripción                                                                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution)   | Aplica la configuración de sustitución de dígitos especificada a las estructuras de estado de script y control de script especificadas.                                                                    |
| [**ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)             | Toma una matriz de anchos de avance para una ejecución y genera una matriz de anchos de glifos de avance ajustados.                                                                               |
| [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)                                     | Recupera información para determinar los saltos de línea.                                                                                                                                |
| [**ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight)                   | Recupera el alto de la fuente almacenada actualmente en caché.                                                                                                                                |
| [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)                                     | Genera el desplazamiento x desde el extremo izquierdo o el borde inicial de una ejecución hasta el borde inicial o final de un clúster de caracteres lógicos.                                          |
| [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache)                             | Libera una caché de scripts.                                                                                                                                                             |
| [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap)                                 | Recupera los índices de glifo de los caracteres Unicode de una cadena según la tabla cmap TrueType o la tabla cmap estándar implementada para las fuentes de estilo antiguo.         |
| [**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)   | Recupera una lista de glifos alternativos para un carácter especificado al que se puede acceder a través de una característica OpenType especificada.                                                         |
| [**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)           | Recupera una lista de características tipográficos para el sistema de escritura definido para el procesamiento de OpenType.                                                                                  |
| [**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)         | Recupera una lista de etiquetas de idioma que están disponibles para el elemento especificado y que son compatibles con una etiqueta de script especificada para el procesamiento de OpenType.                                  |
| [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)             | Recupera información de la caché de fuentes en los glifos especiales utilizados por una fuente.                                                                                                   |
| [**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)             | Recupera una lista de scripts disponibles en la fuente para el procesamiento de OpenType.                                                                                                        |
| [**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth)               | Recupera el ancho ABC de un glifo determinado.                                                                                                                                         |
| [**ScriptGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths)               | Convierte los anchos de avance del glifo de una fuente específica en anchos lógicos.                                                                                                        |
| [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties)                     | Recupera información sobre los scripts actuales.                                                                                                                                  |
| [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex)                             | Determina si una cadena Unicode requiere un procesamiento de script complejo.                                                                                                           |
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)                                 | Divide una cadena Unicode en elementos con forma individual.                                                                                                                        |
| [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)                 | Divide una cadena Unicode en elementos con forma individual y proporciona una matriz de etiquetas de características para cada elemento con forma para el procesamiento openType.                                  |
| [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify)                                 | Crea una tabla de anchos avanzados para permitir la justificación de texto cuando se pasa a la [**función ScriptTextOut.**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)                                                   |
| [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout)                                   | Convierte una matriz de niveles de inserción de ejecución en un mapa de posición visual a lógica o de lógica a visual.                                                               |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)                                     | Genera información de desplazamiento bidimensional y ancho de avance de glifo a partir de la salida de [**ScriptShape.**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)                                                       |
| [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)                     | Genera glifos y atributos visuales para una ejecución Unicode con información de OpenType a partir de la [**salida de ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).                         |
| [**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)         | Coloca un glifo único con un único ajuste mediante una característica especificada proporcionada en la fuente para el procesamiento de OpenType.                                                         |
| [**ScriptRecordDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) | Lee la configuración de sustitución de dígitos y dígitos nativos de National Language Support (NLS) y los registra en una [**estructura \_ SCRIPT DIGITSUBSTITUTE.**](/windows/win32/api/usp10/ns-usp10-script_digitsubstitute) |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)                                     | Genera glifos y atributos visuales para una ejecución Unicode.                                                                                                                         |
| [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)                     | Genera glifos y atributos visuales para una ejecución Unicode con información de OpenType.                                                                                               |
| [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)                     | Analiza una cadena de texto sin formato.                                                                                                                                                     |
| [**ScriptStringCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox)                         | Recupera la coordenada x para el borde inicial o final de una posición de carácter.                                                                                              |
| [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)                           | Libera una estructura [**SCRIPT \_ STRING \_ ANALYSIS.**](script-string-analysis.md)                                                                                                     |
| [**ScriptStringGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths)   | Convierte los anchos visuales en anchos lógicos.                                                                                                                                       |
| [**ScriptStringGetOrder**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder)                   | Crea una matriz que asigna una posición de carácter original a una posición de glifo.                                                                                                    |
| [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)                             | Muestra una cadena generada por una llamada anterior a [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) y, opcionalmente, agrega resaltado.                                               |
| [**ScriptString \_ pcOutChars**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars)            | Devuelve un puntero a la longitud de una cadena después del recorte.                                                                                                                       |
| [**ScriptString \_ pLogAttr**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr)                | Devuelve un puntero a un búfer de atributos lógicos para una cadena analizada.                                                                                                          |
| [**ScriptString \_ pSize**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize)                      | Devuelve un puntero a una [**estructura SIZE**](/previous-versions//dd145106(v=vs.85)) para una cadena analizada.                                                                                                     |
| [**ScriptStringValidate**](/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate)                   | Comprueba si hay secuencias no válidas en una estructura [**SCRIPT \_ STRING \_ ANALYSIS.**](script-string-analysis.md)                                                                              |
| [**ScriptStringXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp)                         | Convierte una coordenada x en una posición de carácter.                                                                                                                                 |
| [**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)     | Habilita la sustitución de un único glifo con una forma alternativa del mismo glifo para el procesamiento de OpenType.                                                                         |
| [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)                                 | Muestra texto para la forma de script y la información de posición especificadas.                                                                                                               |
| [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)                                     | Genera el borde inicial o final de un clúster de caracteres lógicos a partir del desplazamiento x de una ejecución.                                                                                 |



 

 

 
