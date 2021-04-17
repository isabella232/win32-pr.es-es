---
description: 'A continuación se muestran opciones para la presentación y el procesamiento de texto relacionado para admitir efectos tipográficos finos o scripts complejos: Text functionsEdit controlsRich Edit controlsUniscribe'
ms.assetid: 337bc798-e75d-4389-8fea-577eb82a0ed5
title: Procesamiento complejo de scripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e4be6295bff949c8e29036ef3af496c673575e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687623"
---
# <a name="complex-script-processing"></a>Procesamiento complejo de scripts

A continuación se muestran opciones para la presentación y el procesamiento de texto relacionado para admitir efectos tipográficos finos o scripts complejos:

-   Funciones de texto
-   Controles de edición
-   Controles Rich Edit
-   Uniscribe

Las opciones que elija dependen de los siguientes factores:

-   Tipo de texto o scripts.
-   El modelo de implementación, por ejemplo, el diseño de texto y el control de salto de línea por parte de la aplicación.
-   Actualización de una aplicación existente frente a la creación de una nueva aplicación.

En general, una aplicación que realiza el procesamiento de scripts relativamente sencillos puede elegir cualquier opción para procesar scripts complejos. Sin embargo, para obtener el control más completo del procesamiento complejo de scripts, se recomienda.

## <a name="complex-script-processing-using-text-functions"></a>Procesamiento complejo de scripts mediante funciones de texto

Las aplicaciones que usan principalmente texto sin formato, es decir, texto que usa el mismo tipo de letra, peso, color, etc., han escrito tradicionalmente texto y miden longitudes de línea mediante funciones de texto estándar, como [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)y [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa). Estas funciones admiten el procesamiento de scripts complejos y de efectos tipográficos finos. Para obtener más información, vea [fuentes y texto](../gdi/fonts-and-text.md).

En general, la compatibilidad de texto estándar es transparente para las aplicaciones que procesan scripts complejos. Sin embargo, debe tener en cuenta algunas reglas específicas que deben seguirse para escribir aplicaciones que admitan la tipografía y el procesamiento de scripts complejos:

-   La aplicación debe guardar los caracteres en un búfer y mostrar una línea de texto completa al mismo tiempo en lugar de, por ejemplo, llamar a [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) en cada carácter tal como lo escriba el usuario. Este mecanismo permite a los módulos de modelado de texto avanzados usar el contexto para reordenar y generar los [glifos](uniscribe-glossary.md) correctamente.
-   La aplicación debe usar [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) para determinar la longitud de la línea, en lugar de calcular la longitud de la línea de los anchos de caracteres almacenados en memoria caché, ya que el ancho de un glifo puede variar en función del contexto.
-   Opcionalmente, la aplicación debe agregar compatibilidad con el orden de lectura de derecha a izquierda y la alineación a la derecha.
-   La reordenación y el procesamiento contextual necesarios para los scripts complejos o la tipografía precisa requieren un aumento significativo en el procesamiento de la presentación de texto básico para los scripts simples. Por lo tanto, para evitar problemas de rendimiento, la aplicación no debe procesar grandes cantidades de texto antes de mostrar los resultados y devolver el control al usuario.

## <a name="complex-script-processing-using-edit-controls"></a>Procesamiento complejo de scripts mediante controles de edición

Los controles de edición estándar de Windows se han ampliado para admitir texto multilingüe y scripts complejos. El soporte extendido incluye entrada y visualización, así como el movimiento de cursor correcto a través de los clústeres de caracteres, por ejemplo, en los scripts tailandés y Devanagari. Para obtener más información, vea [controles de edición](../controls/edit-controls.md).

## <a name="complex-script-processing-using-rich-edit-controls"></a>Procesamiento complejo de scripts mediante controles Rich Edit

Rich Edit 3,0 es una colección de nivel superior de interfaces que aprovecha la funcionalidad de Uniscribe para aislar las aplicaciones de diseño de texto de las complejidades de ciertos scripts. La edición enriquecida es la forma más sencilla de que las aplicaciones muestren scripts complejos aunque su finalidad principal no sea necesariamente el diseño del texto. Rich Edit proporciona una edición rápida y versátil de texto multilingüe de Unicode enriquecido y texto simple sin formato. Incluye extensas interfaces de mensajes y COM, edición de texto, formato, salto de línea, diseño de tabla simple, diseño de texto vertical, diseño de texto bidireccional, compatibilidad con India y tailandés, una interfaz de usuario de edición muy similar a la de Microsoft Word y las interfaces del modelo de objetos de texto.

Junto con las interfaces Rich Edit, las aplicaciones pueden utilizar la función de edición enriquecida [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta) para analizar, dar forma, colocar y romper líneas automáticamente. Para obtener más información, vea [controles Rich Edit](../controls/rich-edit-controls.md).

## <a name="complex-script-processing-using-uniscribe"></a>Procesamiento complejo de scripts mediante Uniscribe

[Uniscribe](uniscribe.md) proporciona la compatibilidad más amplia para el procesamiento de texto que implica efectos tipográficos finos y scripts complejos. Admite las reglas complejas que se encuentran en scripts como árabe, devanagari y tailandés. Controla los scripts que se escriben de derecha a izquierda, como el árabe y el hebreo, y admite la combinación de scripts. También expone características de fuentes [OpenType](opentype-font-format.md) que las aplicaciones pueden utilizar para controlar los efectos tipográficos finos. Para obtener más información, vea [procesar scripts complejos](processing-complex-scripts.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Uniscribe](about-uniscribe.md)
</dt> <dt>

[Procesamiento de scripts complejos](processing-complex-scripts.md)
</dt> </dl>

 

 
