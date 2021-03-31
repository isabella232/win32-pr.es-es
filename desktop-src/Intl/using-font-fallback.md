---
description: Usar la reserva de fuentes
ms.assetid: 952f33b6-ca52-40a2-b914-52c1c62ae0e0
title: Usar la reserva de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9afb073a01cc1c5b90d4a4861a973846d3ae9ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819003"
---
# <a name="using-font-fallback"></a>Usar la reserva de fuentes

> [!Note]  
> En este tema, todos los comentarios sobre [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) se aplican por igual a [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).

 

La aplicación debe utilizar la reserva de fuentes durante la presentación de texto si no se admiten algunos caracteres de una cadena en la fuente, o si la aplicación usa un [script complejo](uniscribe-glossary.md) no compatible con la fuente. El requisito de reserva de fuentes se detecta durante el proceso de diseño del texto, cuando la aplicación llama a la función [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) . Para obtener información acerca de la presentación de texto, consulte [Mostrar texto con Uniscribe](displaying-text-with-uniscribe.md).

## <a name="determine-the-need-for-font-fallback-for-unsupported-characters"></a>Determinar la necesidad de reserva de fuentes para los caracteres no admitidos

Si algunos de los caracteres de una cadena no se admiten en una fuente solicitada, la llamada de la aplicación a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) se realizará correctamente. Sin embargo, la aplicación debe examinar el búfer de salida del glifo para detectar la presencia de glifos que faltan. El índice del glifo del glifo que falta se puede determinar para una fuente concreta llamando a [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties). Si un glifo determinado no está disponible, la aplicación debe revertir a una fuente diferente para un glifo o representar un símbolo gráfico que indica que no hay ningún glifo disponible.

## <a name="determine-the-need-for-font-fallback-for-unsupported-complex-scripts"></a>Determinar la necesidad de reserva de fuentes para scripts complejos no admitidos

Es posible que la fuente que una aplicación prefiera para su presentación no admita un script complejo requerido por el texto. En este caso, la llamada de la aplicación a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) produce un error con el código de error E el \_ script \_ no está en la \_ \_ fuente.

## <a name="assign-a-fallback-font"></a>Asignar una fuente de reserva

Una vez que haya determinado que se requiere la reserva de fuentes, la aplicación debe asignar una fuente de reserva. La aplicación puede probar las técnicas siguientes:

-   Llame a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) para cada fuente de una lista de fuentes hasta que una llamada tenga un valor devuelto aceptable.
-   Llame a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) con cada fuente de una lista hasta que se pueda determinar que ninguna fuente se realizará correctamente. Si el código de error siempre es el \_ script E \_ no está \_ en \_ la fuente, las fuentes no admiten un script complejo. Puede representar un símbolo gráfico que indica que no hay glifo disponible o volver a especificar el script como no definido (sin procesamiento de scripts) y volver a iniciarlo. Para establecer el script como sin definir, establezca el miembro **eScript** de la estructura de [**\_ análisis de script**](/windows/win32/api/usp10/ns-usp10-script_analysis) en script \_ sin definir.
-   Llame a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) con cada fuente de una lista hasta que se pueda determinar que ninguna fuente se realizará correctamente. Si el código de error indica que algunos de los caracteres están asignando a los glifos que faltan, divida la cadena en intervalos más pequeños. Se pueden asignar fuentes diferentes a los subintervalos para que se puedan representar más caracteres.

## <a name="generate-glyph-information"></a>Generar información de glifo

Una vez que la aplicación ha asignado una fuente que se ejecuta correctamente en las llamadas a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), puede realizar llamadas a [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) para generar el ancho de avance del glifo y la información de desplazamiento bidimensional a partir de la salida de **ScriptShape**. La fuente debe realizarse correctamente en estas llamadas. Un error de fuente en una llamada a **ScriptPlace** después de que se realiza correctamente en una llamada a **ScriptShape** indica una fuente rota.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



