---
description: En la tabla siguiente se especifican las métricas de fuentes más importantes para las aplicaciones que requieren documentos portátiles y las funciones que permiten que una aplicación las recupere.
ms.assetid: 61f6d244-7397-42af-af58-0ab9d07bf19e
title: Métricas para documentos portátiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c840b1b8e8014086b97098a44890f170a6bd11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984938"
---
# <a name="metrics-for-portable-documents"></a>Métricas para documentos portátiles

En la tabla siguiente se especifican las métricas de fuentes más importantes para las aplicaciones que requieren documentos portátiles y las funciones que permiten que una aplicación las recupere.



| Función                                               | Métrica                | Uso                                                                                                          |
|--------------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)           | **ntmSizeEM**         | Recuperación de las métricas de diseño; conversión a métricas de dispositivo.                                                   |
| [**GetCharABCWidths**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)           | **ABCWidths**         | Colocación exacta de los caracteres al principio y al final de los márgenes, los límites de la imagen y otros saltos de texto. |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)               | **AdvanceWidths**     | Posición de los caracteres en una línea.                                                                           |
| [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) | **otmfsType**         | Bits de incrustación de fuentes.                                                                                         |
|                                                        | **otmsCharSlopeRise** | Componente y para la pendiente del cursor para fuentes en cursiva.                                                            |
|                                                        | **otmsCharSlopeRun**  | Componente X para la pendiente del cursor para fuentes en cursiva.                                                            |
|                                                        | **otmAscent**         | Espaciado de línea.                                                                                                |
|                                                        | **otmDescent**        | Espaciado de línea.                                                                                                |
|                                                        | **otmLineGap**        | Espaciado de línea.                                                                                                |
|                                                        | **otmpFamilyName**    | Identificación de fuente.                                                                                         |
|                                                        | **otmpStyleName**     | Identificación de fuente.                                                                                         |
|                                                        | **otmpFullName**      | Identificación de fuente (normalmente, nombre de familia y estilo).                                                      |



 

Los miembros **otmsCharSlopeRise**, **otmsCharSlopeRun**, **otmAscent**, **otmDescent** y **otmLineGap** de la estructura [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) se escalan o transforman para que se correspondan con el modo de dispositivo actual y con el alto físico (según se especifica en el miembro **tmHeight** de la estructura [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) ).

La identificación de fuente es importante en esas instancias cuando una aplicación debe seleccionar la misma fuente, por ejemplo, cuando un documento se vuelve a abrir o se mueve a otro sistema operativo. El asignador de fuentes siempre selecciona la fuente correcta cuando una aplicación solicita una fuente por su nombre completo. Los nombres de familia y estilo proporcionan la entrada al cuadro de diálogo fuente estándar, que garantiza que las barras de selección se colocan correctamente.

Los valores **otmsCharSlopeRise** y **otmsCharSlopeRun** se usan para producir una aproximación aproximada del ángulo de cursiva principal de la fuente. En el caso de las fuentes romanos típicas, **otmsCharSlopeRise** es 1 y **otmsCharSlopeRun** es 0. En el caso de las fuentes en cursiva, los valores intentan aproximar el seno y el coseno del ángulo de cursiva principal de la fuente (en los grados en sentido contrario a las agujas del reloj vertical); Tenga en cuenta que el ángulo en cursiva para las fuentes verticales es 0. Dado que estos valores no se expresan en unidades de diseño, no se deben convertir en unidades de dispositivo.

La posición de caracteres y las métricas de espaciado de líneas permiten a una aplicación calcular saltos de línea independientes del dispositivo que son portátiles entre pantallas, impresoras, typesetters e incluso plataformas.

**Para realizar el diseño de página independiente del dispositivo**

1.  Normalizar todas las métricas de diseño a un valor común de resolución ultra alta (UHR) (por ejemplo, 65.536 PPP); Esto evita los errores de redondeo.
2.  Calcular los saltos de línea en función de las métricas de UHR y el ancho de página físico; Esto produce un punto inicial y un punto final de una línea dentro de la secuencia de texto.
3.  Calcule el ancho de página del dispositivo en unidades de dispositivo (por ejemplo, píxeles).
4.  Ajuste cada línea de texto en el ancho de página del dispositivo, usando los saltos de línea calculados en el paso 2.
5.  Calcular los saltos de página mediante métricas de UHR y la longitud de página física; Esto da como resultado el número de líneas por página.
6.  Calcular el alto de línea en unidades de dispositivo.
7.  Ajuste las líneas de texto en la página, usando las líneas por página del paso 5 y el alto de línea del paso 6.

Si todas las aplicaciones adoptan estas técnicas, los desarrolladores pueden garantizar prácticamente que los documentos que se mueven de una aplicación a otra conservarán su aspecto y formato originales.

 

 



