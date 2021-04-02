---
description: Para proporcionar una justificación del texto, una aplicación puede usar uno de dos métodos.
ms.assetid: 1190baed-5959-4f7a-8946-ac3b3da85821
title: Procesamiento de scripts complejos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bea5b75e87afc4177b03c03f4263ba2592a0e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082081"
---
# <a name="processing-complex-scripts"></a>Procesamiento de scripts complejos

Para proporcionar una justificación del texto, una aplicación puede usar uno de dos métodos. Para una implementación simple de la justificación multilingüe, la aplicación debe llamar a [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify). Genera la matriz DX Delta mediante la consideración de kashida, el espaciado entre palabras y, a continuación, el espaciado entre caracteres. Para obtener una justificación más sofisticada, la aplicación puede generar una matriz DX Delta actualizada con su propio conocimiento de lenguaje y la información recuperada por [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) en la matriz [**\_ VISATTR de script**](/windows/win32/api/usp10/ns-usp10-script_visattr) .

Se debe insertar el espacio de justificación o kashida, donde se identifique por el miembro **uJustification** de la [**secuencia de comandos \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr). Al realizar la justificación entre caracteres, la aplicación debe insertar espacio adicional solo después de los glifos marcados con el carácter de alineación de SCRIPT \_ \_ .

La aplicación realiza la colocación del símbolo de intercalación y la prueba de posicionamiento mediante [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) y [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox). Para obtener más información, vea [administrar la colocación del símbolo de intercalación y la prueba de posicionamiento](managing-caret-placement-and-hit-testing.md).

Para obtener los anchos de una manera independiente de la fuente, la aplicación llama a [**ScriptGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths). Al pasar los anchos lógicos a [**ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth), se puede volver a mostrar un bloque de texto en los mismos límites con una pérdida aceptable de calidad incluso cuando la fuente original no esté disponible. Genera una matriz de anchos de glifo ([anchos de avance](uniscribe-glossary.md)) adecuado para pasar a [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout). Esta grabación y reaplicación de la información de ancho avanzado de una manera independiente de la fuente puede ser útil en situaciones como la generación de metadatos en un formato definido por la aplicación.

> [!Note]  
> Los metaarchivos no admiten índices de glifo. Para escribir en un metarchivo mejorado, la aplicación debe utilizar [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) y escribir los caracteres lógicos directamente. Con este mecanismo, la generación y colocación del glifo no se produce hasta que el texto se reproduce.

 

Para recuperar los glifos específicos que se usan para el valor predeterminado, los valores en blanco, kashida, etc., para la fuente actual, la aplicación debe llamar a [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties). Para determinar qué caracteres de una ejecución son compatibles con la fuente seleccionada, la aplicación llama a [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap). Los caracteres que no están disponibles tienen el glifo predeterminado en el búfer del glifo. Tenga en cuenta que este método produce un error si una fuente representa un carácter utilizando una combinación de glifos en lugar de un único glifo. Por ejemplo, 00C9; La letra mayúscula latina E con acento agudo se puede representar con un glifo E de mayúsculas y un glifo de agudos. Para determinar la compatibilidad de fuentes para una cadena que contiene estos tipos de puntos de código, la aplicación puede llamar a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape). Para obtener más información, consulte [uso de motores de modelado](using-shaping-engines.md).

La función [**ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight) devuelve el alto de la fuente de la memoria caché de fuentes. [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) proporciona información sobre el procesamiento especial que se requiere para todos los scripts, indizados por script. Por ejemplo, incluye el lenguaje principal asociado con el script, datos que indican si el script es numérico y datos que indican si el script es un script complejo.

[**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth) devuelve el [ancho ABC](uniscribe-glossary.md) de un glifo determinado, que puede ser útil para dibujar gráficos de glifos. Sin embargo, no debe usarse para el formato de texto de script complejo normal.

## <a name="related-topics"></a>Temas relacionados

[Usar Uniscribe](using-uniscribe.md)


 

 
