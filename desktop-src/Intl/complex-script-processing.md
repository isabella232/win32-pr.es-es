---
description: 'A continuación se muestran las opciones para mostrar y el procesamiento relacionado de texto para admitir efectos de tipografía finos o scripts complejos: Funciones de textoEditar controles Controles de ediciónRichUniscribe'
ms.assetid: 337bc798-e75d-4389-8fea-577eb82a0ed5
title: Procesamiento de scripts complejos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15671aed99e0c596d83bd65a2f4a0925ff61293cf90ed37e2aed371f23f114fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754915"
---
# <a name="complex-script-processing"></a>Procesamiento de scripts complejos

A continuación se muestran las opciones para mostrar y el procesamiento relacionado de texto para admitir efectos de tipografía finos o scripts complejos:

-   Funciones de texto
-   Editar controles
-   Controles de edición enriquecciones
-   Unscribe

Las opciones que elija dependen de los siguientes factores:

-   Tipo de texto o scripts.
-   El modelo de implementación, por ejemplo, el diseño de texto y el control de la separación de líneas por parte de la aplicación.
-   Actualización de una aplicación existente frente a creación de una nueva aplicación.

En general, una aplicación que realiza un procesamiento de scripts relativamente sencillo puede elegir cualquier opción para procesar scripts complejos. Sin embargo, para el control más completo del procesamiento de scripts complejos, se recomienda Uniscribe.

## <a name="complex-script-processing-using-text-functions"></a>Procesamiento de scripts complejos mediante funciones de texto

Las aplicaciones que usan principalmente texto sin formato, es decir, texto que usa el mismo tipo de letra, peso, color, entre otros, han escrito tradicionalmente texto y longitudes de línea medidas mediante funciones de texto estándar, como [**TextOut,**](/windows/win32/api/wingdi/nf-wingdi-textouta) [**ExtTextOut,**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) [**TabbedTextOut,**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta) [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)y [**GetTextExtentExPoint.**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) Estas funciones admiten el procesamiento de scripts complejos y efectos de tipografía finas. Para obtener más información, vea [Fuentes y texto.](../gdi/fonts-and-text.md)

En general, la compatibilidad con texto estándar es transparente para las aplicaciones que procesa scripts complejos. Sin embargo, debe tener en cuenta algunas reglas específicas que se deben seguir al escribir aplicaciones que admitan tipografía fina y procese scripts complejos:

-   La aplicación debe guardar caracteres en un búfer y mostrar una línea de texto completa a la vez en lugar de, por ejemplo, llamar a [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) en cada carácter a medida que el usuario lo escribe. Este mecanismo permite que los módulos avanzados de modelado de texto usen el contexto para reordenar y generar [glifos](uniscribe-glossary.md) correctamente.
-   La aplicación debe usar [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) para determinar la longitud de línea, en lugar de calcular las longitudes de línea de los anchos de caracteres almacenados en caché, ya que el ancho de un glifo puede variar según el contexto.
-   Opcionalmente, la aplicación debe agregar compatibilidad con el orden de lectura de derecha a izquierda y la alineación derecha.
-   La reordenación y el procesamiento contextual necesarios para scripts complejos o tipografía fina requiere un aumento significativo del procesamiento sobre la presentación de texto básica para scripts simples. Por lo tanto, para evitar problemas de rendimiento, la aplicación no debe procesar grandes cantidades de texto antes de mostrar los resultados y devolver el control al usuario.

## <a name="complex-script-processing-using-edit-controls"></a>Procesamiento de scripts complejos mediante controles edit

Los controles Windows edición estándar se han ampliado para admitir texto multilingüe y scripts complejos. La compatibilidad ampliada incluye la entrada y la presentación, así como el movimiento correcto del cursor sobre los clústeres de caracteres, por ejemplo, en scripts tailandeses y devaplacei. Para obtener más información, vea [Editar controles](../controls/edit-controls.md).

## <a name="complex-script-processing-using-rich-edit-controls"></a>Procesamiento de scripts complejos mediante controles Rich Edit

Rich Edit 3.0 es una colección de interfaces de nivel superior que aprovecha Uniscribe para aislar las aplicaciones de diseño de texto de las complejidades de determinados scripts. Rich Edit es la manera más sencilla para que las aplicaciones muestren scripts complejos, aunque su propósito principal no sea necesariamente el diseño de texto. Rich Edit proporciona una edición rápida y versátil de texto multilingüe unicode enriquecido y texto sin formato simple. Incluye interfaces COM y mensajes extensos, edición de texto, formato, separación de líneas, diseño de tabla simple, diseño de texto vertical, diseño de texto bidireccional, compatibilidad con Indic y Tailandés, una interfaz de usuario de edición muy parecido a Microsoft Word e interfaces de modelo de objetos de texto.

Junto con las interfaces Rich Edit, las aplicaciones pueden usar la función Rich Edit [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta) para analizar, dar forma, colocar y interrumpir líneas automáticamente. Para obtener más información, vea [Rich Edit Controls](../controls/rich-edit-controls.md).

## <a name="complex-script-processing-using-uniscribe"></a>Procesamiento de scripts complejos mediante Uniscribe

[Uniscribe](uniscribe.md) proporciona la compatibilidad más amplia para el procesamiento de texto que implica efectos de tipografía finos y scripts complejos. Admite las reglas complejas que se encuentran en scripts como árabe, devavalai y tailandés. Controla los scripts escritos de derecha a izquierda, como árabe y hebreo, y admite la combinación de scripts. Uniscribe también expone características [de fuente OpenType](opentype-font-format.md) que las aplicaciones pueden usar para controlar efectos de tipografía precisos. Para obtener más información, vea [Procesar scripts complejos.](processing-complex-scripts.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Uniscribe](about-uniscribe.md)
</dt> <dt>

[Procesamiento de scripts complejos](processing-complex-scripts.md)
</dt> </dl>

 

 
