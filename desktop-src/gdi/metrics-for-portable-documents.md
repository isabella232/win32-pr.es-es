---
description: En la tabla siguiente se especifican las métricas de fuente más importantes para las aplicaciones que requieren documentos portátiles y las funciones que permiten a una aplicación recuperarlos.
ms.assetid: 61f6d244-7397-42af-af58-0ab9d07bf19e
title: Métricas para documentos portátiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3762846e6d8280c2680f47f3cb32cd847ea4e664dab47a8a0995f5505c393da3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558505"
---
# <a name="metrics-for-portable-documents"></a>Métricas para documentos portátiles

En la tabla siguiente se especifican las métricas de fuente más importantes para las aplicaciones que requieren documentos portátiles y las funciones que permiten a una aplicación recuperarlos.



| Función                                               | Métrica                | Usar                                                                                                          |
|--------------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)           | **ntmSizeEM**         | Recuperación de métricas de diseño; conversión a métricas de dispositivo.                                                   |
| [**GetCharABCWidths**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)           | **ABCWidths**         | Colocación precisa de caracteres al principio y al final de los márgenes, los límites de la imagen y otros saltos de texto. |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)               | **AdvanceWidths**     | Colocación de caracteres en una línea.                                                                           |
| [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) | **otmfsType**         | Bits de incrustación de fuentes.                                                                                         |
|                                                        | **otmsCharSlopeRise** | Componente Y para pendiente de cursor para fuentes en cursiva.                                                            |
|                                                        | **otmsCharSlopeRun**  | Componente X para pendiente de cursor para fuentes en cursiva.                                                            |
|                                                        | **otmAscent**         | Interlineado.                                                                                                |
|                                                        | **otmDescent**        | Interlineado.                                                                                                |
|                                                        | **otmLineGap**        | Interlineado.                                                                                                |
|                                                        | **otmpFamilyName**    | Identificación de fuente.                                                                                         |
|                                                        | **otmpStyleName**     | Identificación de fuente.                                                                                         |
|                                                        | **otmpFullName**      | Identificación de fuente (normalmente, nombre de familia y estilo).                                                      |



 

Los miembros **otmsCharSlopeRise**, **otmsCharSlopeRun**, **otmAscent**, **otmDescent** y **otmLineGap** de la estructura [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) se escalan o transforman para que se correspondan con el modo de dispositivo actual y la altura física (tal y como se especifica en el miembro **tmHeight** de la estructura [NEWTEXTMETRIC).](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)

La identificación de fuentes es importante en esos casos en los que una aplicación debe seleccionar la misma fuente, por ejemplo, cuando se vuelve a abrir un documento o se mueve a otro sistema operativo. El asignador de fuentes siempre selecciona la fuente correcta cuando una aplicación solicita una fuente por nombre completo. Los nombres de familia y estilo proporcionan entrada al cuadro de diálogo de fuente estándar, lo que garantiza que las barras de selección se colocan correctamente.

Los **valores otmsCharSlopeRise** y **otmsCharSlopeRun** se usan para generar una aproximación cercana del ángulo de cursiva principal de la fuente. Para las fuentes típicas de román, **otmsCharSlopeRise** es 1 y **otmsCharSlopeRun** es 0. En el caso de las fuentes cursivas, los valores intentan aproximarse al seno y el coseno del ángulo cursiva principal de la fuente (en grados en sentido contrario a los verticales). Tenga en cuenta que el ángulo de cursiva para las fuentes verticales es 0. Dado que estos valores no se expresan en unidades de diseño, no se deben convertir en unidades de dispositivo.

Las métricas de colocación de caracteres y espaciado de línea permiten a una aplicación calcular saltos de línea independientes del dispositivo que son portátiles en pantallas, impresoras, equipos de tipos e incluso plataformas.

**Para realizar el diseño de página independiente del dispositivo**

1.  Normalizar todas las métricas de diseño a un valor común de ultra alta resolución (UHR) (por ejemplo, 65 536 PPP); esto evita errores de redondeo.
2.  Saltos de línea de proceso basados en métricas de UHR y ancho de página físico; esto produce un punto inicial y un punto final de una línea dentro de la secuencia de texto.
3.  Calcule el ancho de página del dispositivo en unidades de dispositivo (por ejemplo, píxeles).
4.  Ajuste cada línea de texto en el ancho de página del dispositivo, mediante los saltos de línea calculados en el paso 2.
5.  Calcular saltos de página mediante métricas de UHR y la longitud de página física; esto produce el número de líneas por página.
6.  Calcule el alto de línea en unidades de dispositivo.
7.  Ajuste las líneas de texto a la página, usando las líneas por página del paso 5 y la altura de línea del paso 6.

Si todas las aplicaciones adoptan estas técnicas, los desarrolladores pueden garantizar virtualmente que los documentos movidos de una aplicación a otra conservarán su apariencia y formato originales.

 

 



