---
description: Las aplicaciones deben recuperar datos de ancho de caracteres cuando realizan tareas como ajustar cadenas de texto a anchos de página o columna.
ms.assetid: 0c84f5f9-71cd-4077-bc99-f23a393c1c4d
title: Anchos de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822ae01ea1ccd5a2a7ec118cb1b93211b1c2e5c0a215737a600d9450b8996117
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117888108"
---
# <a name="character-widths"></a>Anchos de caracteres

Las aplicaciones deben recuperar datos de ancho de caracteres cuando realizan tareas como ajustar cadenas de texto a anchos de página o columna. Hay cuatro funciones que una aplicación puede usar para recuperar datos de ancho de caracteres. Dos de estas funciones recuperan el ancho de avance de caracteres y dos de estas funciones recuperan datos reales de ancho de caracteres.

Una aplicación puede usar las funciones [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) y [GetCharWidthFloat](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata) para recuperar el ancho de avance de caracteres individuales o símbolos en una cadena de texto. El ancho de avance es la distancia que el cursor en una pantalla de vídeo o el titular de impresión de una impresora deben avanzar antes de imprimir el carácter siguiente en una cadena de texto. La [**función GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) devuelve el ancho de avance como un valor entero. Si se requiere mayor precisión, una aplicación puede usar la función [**GetCharWidthFloat**](/windows/win32/api/wingdi/nf-wingdi-getcharwidthfloata) para recuperar valores fraccionales de ancho de avance.

Una aplicación puede recuperar datos reales de ancho de caracteres mediante las funciones [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) y [**GetCharABCWidthsFloat.**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata) La **función GetCharABCWidthsFloat** funciona con todas las fuentes. La [**función GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) solo funciona con fuentes TrueType y OpenType. Para obtener más información sobre las fuentes TrueType y OpenType, vea [Fuentes Raster, Vector, TrueType y OpenType.](raster--vector--truetype--and-opentype-fonts.md)

En la ilustración siguiente se muestran los tres componentes de un ancho de caracteres:

![ilustración que muestra el espaciado, el espaciado b y el espaciado c de dos caracteres adyacentes](images/csftx-02.png)

El espaciado A es el ancho que se va a agregar a la posición actual antes de colocar el carácter. El espaciado B es el ancho del propio carácter. El espaciado de C es el espacio en blanco situado a la derecha del carácter. El ancho de avance total se determina calculando la suma de A+B+C. La celda de caracteres es un rectángulo imaginario que rodea cada carácter o símbolo de una fuente. Dado que los caracteres pueden sobresal lado o debajo de la celda de caracteres, o ambos incrementos A y C pueden ser un número negativo.

 

 
