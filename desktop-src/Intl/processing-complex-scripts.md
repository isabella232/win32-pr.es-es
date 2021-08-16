---
description: Para proporcionar una justificación de texto, una aplicación puede usar uno de estos dos métodos.
ms.assetid: 1190baed-5959-4f7a-8946-ac3b3da85821
title: Procesamiento de scripts complejos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987c58cd1d6e8979573b47bbf3e2e7ff248617b12907f81ef70761c08403a067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390429"
---
# <a name="processing-complex-scripts"></a>Procesamiento de scripts complejos

Para proporcionar una justificación de texto, una aplicación puede usar uno de estos dos métodos. Para una implementación sencilla de justificación multilingüe, la aplicación debe llamar a [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify). Genera la matriz delta dx teniendo en cuenta kashida, después el espaciado entre palabras y, a continuación, el espaciado entre caracteres. Para una justificación más sofisticada, la aplicación puede generar una matriz delta dx actualizada mediante su propio conocimiento de lenguaje y la información recuperada por [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) en la matriz [**SCRIPT \_ VISATTR.**](/windows/win32/api/usp10/ns-usp10-script_visattr)

El espacio de justificación o kashida se debe insertar donde lo identifique **el miembro uJustification** de [**SCRIPT \_ VISATTR.**](/windows/win32/api/usp10/ns-usp10-script_visattr) Al realizar la justificación entre caracteres, la aplicación debe insertar espacio adicional solo después de glifos marcados con SCRIPT \_ JUSTIFY \_ CHARACTER.

La aplicación realiza la selección de inserción y las pruebas de posicionamiento [**mediante ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) [**y ScriptCPtoX.**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) Para obtener más información, vea [Managing Caret Placement and Hit Testing](managing-caret-placement-and-hit-testing.md).

Para obtener anchos de forma independiente de la fuente, la aplicación llama a [**ScriptGetLogicalWidths.**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths) Al pasar los anchos lógicos a [**ScriptApplyLogicalWidth,**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)se puede volver a mostrar un bloque de texto en los mismos límites con una pérdida aceptable de calidad incluso cuando la fuente original no está disponible. Genera una matriz de anchos de glifo [(anchos de avance) adecuados](uniscribe-glossary.md)para pasar a [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout). Este tipo de grabación y aplicación de información de ancho de avance de forma independiente de la fuente puede ser útil en situaciones como el metafiling en un formato definido por la aplicación.

> [!Note]  
> Los metarchivos no admiten índices de glifo. Para escribir en un metarchivo mejorado, la aplicación debe usar [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) y escribir los caracteres lógicos directamente. Con este mecanismo, la generación y la colocación del glifo no se producen hasta que se reproduce el texto.

 

Para recuperar los glifos específicos que se usan para el valor predeterminado, blanks, kashida, etc., para la fuente actual, la aplicación debe llamar a [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties). Para determinar qué caracteres de una ejecución son compatibles con la fuente seleccionada, la aplicación llama a [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap). Los caracteres que no están disponibles tienen el glifo predeterminado en el búfer del glifo. Tenga en cuenta que este método produce un error si una fuente representa un carácter mediante una combinación de glifos en lugar de un único glifo. Por ejemplo, 00C9; LATIN CAPITAL LETTER E WITH GLYPH se puede representar mediante un glifo E de mayúscula y un glifo desasistido. Para determinar la compatibilidad de fuente para una cadena que contiene estos tipos de puntos de código, la aplicación puede llamar a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape). Para obtener más información, [vea Using Shaping Engines](using-shaping-engines.md).

La [**función ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight) devuelve el alto de la fuente de la caché de fuentes. [**ScriptGetProperties proporciona**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) información sobre el procesamiento especial necesario para todos los scripts, indexados por script. Por ejemplo, incluye el lenguaje principal asociado al script, datos que indican si el script es numérico y datos que indican si el script es un script complejo.

[**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth) devuelve el ancho [ABC](uniscribe-glossary.md) de un glifo determinado, lo que podría ser útil para dibujar gráficos de glifos. Sin embargo, no debe usarse para el formato de texto de script complejo normal.

## <a name="related-topics"></a>Temas relacionados

[Uso de Uniscribe](using-uniscribe.md)


 

 
