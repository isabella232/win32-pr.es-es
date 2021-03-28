---
description: Además de recuperar los datos de ancho de caracteres de caracteres individuales, las aplicaciones también necesitan calcular el ancho y el alto de las cadenas completas.
ms.assetid: 0c1d9142-258a-447f-8950-8d684645383b
title: Ancho y alto de cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f57846d0588c518f445523361ae186e4b966bf93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908945"
---
# <a name="string-widths-and-heights"></a>Ancho y alto de cadena

Además de recuperar los datos de ancho de caracteres de caracteres individuales, las aplicaciones también necesitan calcular el ancho y el alto de las cadenas completas. Dos funciones recuperan las medidas de ancho de cadena y alto: [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)y [**GetTabbedTextExtent**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta). Si la cadena no contiene caracteres de tabulación, una aplicación puede usar la función **GetTextExtentPoint32** para recuperar el ancho y el alto de una cadena especificada. Si la cadena contiene caracteres de tabulación, una aplicación debe llamar a la función GetTabbedTextExtent.

Las aplicaciones pueden usar la función [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) para las operaciones de ajuste de texto. Esta función devuelve el número de caracteres de una cadena especificada que caben dentro de un espacio especificado.

## <a name="font-ascenders-and-descenders"></a>Fuentes ascendentes y descendentes

Algunas aplicaciones determinan el interlineado entre las líneas de texto de distintos tamaños usando el valor máximo de una fuente de forma ascendente y descendente. Una aplicación puede recuperar estos valores mediante una llamada a la función [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) y, a continuación, comprobar los miembros **tmAscent** y **tmDescent** de [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica).

El ascenso y descenso máximos son diferentes del ascenso y el descenso tipográficos. En las fuentes TrueType y OpenType, el ascenso tipográfico y el descenso suelen ser la parte superior del glifo de f y la parte inferior del glifo de g. Una aplicación puede recuperar la tipografía ascendente y descendente para una fuente TrueType o OpenType llamando a la función [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) y comprobando los valores de los miembros **otmMacAscent** y **otmMacDescent** de la estructura [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) .

En la ilustración siguiente se muestra la diferencia entre los valores de métrica de texto vertical devueltos en las estructuras [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) y [**OUTLINETEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica) . (Los nombres que empiezan por OTM son miembros de la estructura **OUTLINETEXTMETRIC** ).

![Ilustración que muestra el contraste de los valores de métrica de texto con los valores de las métricas de texto de esquema](images/csftx-03.png)

## <a name="font-dimensions"></a>Dimensiones de fuente

Una aplicación puede recuperar las dimensiones físicas de una fuente TrueType o OpenType llamando a la función [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) . Una aplicación puede recuperar las dimensiones físicas de cualquier otra fuente mediante una llamada a la función [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) . Para determinar las dimensiones de un dispositivo de salida, una aplicación puede llamar a la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) . **GetDeviceCaps** devuelve dimensiones físicas y lógicas.

Una pulgada lógica es una medida que utiliza el sistema para presentar fuentes legibles en la pantalla y tiene un tamaño aproximado de 30 a 40% mayor que una pulgada física. El uso de las pulgadas lógicas impide una coincidencia exacta entre el resultado de la pantalla y la impresora. Los desarrolladores deben tener en cuenta que el texto de una pantalla no es simplemente una versión escalada del texto que aparecerá en la página, especialmente si los gráficos se incorporan en el texto.

 

 
