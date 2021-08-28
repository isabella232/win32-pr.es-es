---
description: Además de recuperar datos de ancho de caracteres para caracteres individuales, las aplicaciones también necesitan calcular el ancho y el alto de cadenas enteras.
ms.assetid: 0c1d9142-258a-447f-8950-8d684645383b
title: Anchos y alturas de cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5a9ee485cbc163cc7cbb9dbd296f15db0e9e622f4be6ad8dcb251b583099f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778831"
---
# <a name="string-widths-and-heights"></a>Anchos y alturas de cadena

Además de recuperar datos de ancho de caracteres para caracteres individuales, las aplicaciones también necesitan calcular el ancho y el alto de cadenas enteras. Dos funciones recuperan las medidas de ancho y alto de cadena: [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)y [**GetTabbedTextExtent.**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) Si la cadena no contiene caracteres de tabulación, una aplicación puede usar la función **GetTextExtentPoint32** para recuperar el ancho y alto de una cadena especificada. Si la cadena contiene caracteres de tabulación, una aplicación debe llamar a la función GetTabbedTextExtent.

Las aplicaciones pueden usar [**la función GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) para las operaciones de ajuste de palabras. Esta función devuelve el número de caracteres de una cadena especificada que caben dentro de un espacio especificado.

## <a name="font-ascenders-and-descenders"></a>Ascendentes y descendientes de fuentes

Algunas aplicaciones determinan el espaciado de línea entre líneas de texto de distintos tamaños mediante el ascendente y el descendiente máximos de una fuente. Una aplicación puede recuperar estos valores llamando a la función [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) y, a continuación, comprobando los miembros **tmAscent** y **tmDescent** de [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica).

El descenso y el descenso máximos son diferentes de los de la subida y el descenso tipográficos. En las fuentes TrueType y OpenType, el ascent y el descenso tipográficos suelen ser la parte superior del glifo f y la parte inferior del glifo g. Una aplicación puede recuperar el ascendente tipográfico y el descendiente de una fuente TrueType o OpenType llamando a la función [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) y comprobando los valores de los miembros **otmMacAscent** y **otmMacDescent** de la estructura [**OUTLINETEXTMETRIC.**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica)

En la ilustración siguiente se muestra la diferencia entre los valores de métrica de texto vertical devueltos en las [**estructuras NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) [**y OUTLINETEXTMETRIC.**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica) (Los nombres que comienzan por otm son miembros de la **estructura OUTLINETEXTMETRIC).**

![ilustración que muestra cómo los valores de las métricas de texto contrastan con los valores de las métricas de texto de esquema](images/csftx-03.png)

## <a name="font-dimensions"></a>Dimensiones de fuente

Una aplicación puede recuperar las dimensiones físicas de una fuente TrueType o OpenType llamando a la [**función GetOutlineTextMetrics.**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) Una aplicación puede recuperar las dimensiones físicas de cualquier otra fuente llamando a la [**función GetTextMetrics.**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) Para determinar las dimensiones de un dispositivo de salida, una aplicación puede llamar a la [**función GetDeviceCaps.**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) **GetDeviceCaps** devuelve dimensiones físicas y lógicas.

Una pulgada lógica es una medida que el sistema usa para presentar fuentes legibles en la pantalla y es aproximadamente entre un 30 y un 40 % mayor que una pulgada física. El uso de pulgadas lógicas impide una coincidencia exacta entre la salida de la pantalla y la impresora. Los desarrolladores deben tener en cuenta que el texto de una pantalla no es simplemente una versión a escala del texto que aparecerá en la página, especialmente si se incorporan gráficos al texto.

 

 
