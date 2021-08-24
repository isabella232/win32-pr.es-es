---
description: Uso de la reserva de fuentes
ms.assetid: 952f33b6-ca52-40a2-b914-52c1c62ae0e0
title: Uso de la reserva de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9a4e9b329e2c3257ae9fad02f1fb4774a63dc1d4b4e804c0dca8e690cbf4d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787875"
---
# <a name="using-font-fallback"></a>Uso de la reserva de fuentes

> [!Note]  
> En este tema, todos los comentarios sobre [**ScriptShape se**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) aplican igualmente [**a ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).

 

La aplicación debe usar la reserva de fuentes durante la presentación del texto si algunos caracteres de una cadena no se admiten en la fuente o si la aplicación usa un [script](uniscribe-glossary.md) complejo no compatible con la fuente. El requisito de reserva de fuentes se detecta durante el proceso de diseño de texto, cuando la aplicación llama a la [**función ScriptShape.**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) Para obtener información sobre la presentación de texto, vea [Mostrar texto con Uniscribe.](displaying-text-with-uniscribe.md)

## <a name="determine-the-need-for-font-fallback-for-unsupported-characters"></a>Determinar la necesidad de reserva de fuentes para caracteres no admitidos

Si algunos de los caracteres de una cadena no se admiten en una fuente solicitada, una llamada de aplicación a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) se realiza correctamente. Sin embargo, la aplicación debe examinar el búfer de salida del glifo en busca de la presencia de glifos que faltan. El índice de glifo del glifo que falta se puede determinar para una fuente específica mediante una llamada a [**ScriptGetFontProperties.**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties) Si un glifo determinado no está disponible, la aplicación debe volver a una fuente diferente para un glifo o representar un símbolo gráfico que indique que no hay ningún glifo disponible.

## <a name="determine-the-need-for-font-fallback-for-unsupported-complex-scripts"></a>Determinar la necesidad de reserva de fuentes para scripts complejos no admitidos

Es posible que la fuente que una aplicación prefiera para mostrar no admita un script complejo que requiera el texto. En este caso, se produce un error en la llamada de aplicación [**a ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) con el código de error E \_ SCRIPT NOT IN \_ \_ \_ FONT.

## <a name="assign-a-fallback-font"></a>Asignación de una fuente de reserva

Una vez que haya determinado que se requiere la reserva de fuentes, la aplicación debe asignar una fuente de reserva. La aplicación puede probar las técnicas siguientes:

-   Llame [**a ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) para cada fuente de una lista de fuentes hasta que una llamada tenga un valor devuelto aceptable.
-   Llame [**a ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) con cada fuente de una lista hasta que se pueda determinar que ninguna fuente se realizará correctamente. Si el código de error siempre es E SCRIPT NOT IN FONT, las fuentes no \_ \_ \_ \_ admiten un script complejo. Represente un símbolo gráfico que indique que no hay glifo disponible o vuelva a especificar el script como indefinido (sin procesamiento de scripts) y vuelva a iniciarlo. Para establecer el script como indefinido, establezca el miembro **eScript** de la estructura [**SCRIPT \_ ANALYSIS**](/windows/win32/api/usp10/ns-usp10-script_analysis) en SCRIPT \_ UNDEFINED.
-   Llame [**a ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) con cada fuente de una lista hasta que se pueda determinar que ninguna fuente se realizará correctamente. Si el código de error indica que algunos de los caracteres se están asignando a glifos que faltan, divide la cadena en intervalos más pequeños. Se pueden asignar distintas fuentes a subrangos para que se puedan representar más caracteres.

## <a name="generate-glyph-information"></a>Generar información de glifo

Una vez que la aplicación ha asignado una fuente que realiza correctamente llamadas a [**ScriptShape,**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)puede realizar llamadas a [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) para generar información de desplazamiento bidimensional y ancho de avance del glifo a partir de la salida de **ScriptShape**. La fuente debe tener éxito en estas llamadas. Un error de fuente en una llamada a **ScriptPlace después** de que se realizara correctamente en una **llamada a ScriptShape** indica una fuente rota.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



