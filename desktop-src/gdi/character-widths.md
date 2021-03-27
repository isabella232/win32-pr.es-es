---
description: Las aplicaciones necesitan recuperar datos de ancho de caracteres cuando realizan tareas como la instalación de cadenas de texto en anchos de página o de columna.
ms.assetid: 0c84f5f9-71cd-4077-bc99-f23a393c1c4d
title: Ancho de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950fbb7e6ad1e5f4ef12f2abd9e528ce3158a869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908509"
---
# <a name="character-widths"></a>Ancho de caracteres

Las aplicaciones necesitan recuperar datos de ancho de caracteres cuando realizan tareas como la instalación de cadenas de texto en anchos de página o de columna. Hay cuatro funciones que una aplicación puede usar para recuperar datos de ancho de caracteres. Dos de estas funciones recuperan el ancho de avance de caracteres y dos de estas funciones recuperan datos reales de ancho de caracteres.

Una aplicación puede usar las funciones [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) y [GetCharWidthFloat](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata) para recuperar el ancho de avance de caracteres individuales o símbolos en una cadena de texto. El ancho de avance es la distancia que debe avanzar el cursor en una pantalla de vídeo o el encabezado de impresión de una impresora antes de imprimir el siguiente carácter en una cadena de texto. La función [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) devuelve el ancho de avance como un valor entero. Si se requiere una mayor precisión, una aplicación puede usar la función [**GetCharWidthFloat**](/windows/win32/api/wingdi/nf-wingdi-getcharwidthfloata) para recuperar los valores de ancho de avance fraccionario.

Una aplicación puede recuperar datos de ancho de caracteres reales mediante las funciones [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) y [**GetCharABCWidthsFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata) . La función **GetCharABCWidthsFloat** funciona con todas las fuentes. La función [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) solo funciona con fuentes TrueType y OpenType. Para obtener más información acerca de las fuentes TrueType y OpenType, vea las [fuentes raster, Vector, TrueType y OpenType](raster--vector--truetype--and-opentype-fonts.md).

En la ilustración siguiente se muestran los tres componentes de un ancho de caracteres:

![Ilustración que muestra el espaciado, el espaciado b y el espaciado c de dos caracteres adyacentes](images/csftx-02.png)

Un espaciado es el ancho que se va a agregar a la posición actual antes de colocar el carácter. El espaciado B es el ancho del carácter. El espaciado C es el espacio en blanco situado a la derecha del carácter. El ancho de avance total viene determinado por el cálculo de la suma de A + B + C. La celda de carácter es un rectángulo imaginario que rodea cada carácter o símbolo de una fuente. Dado que los caracteres pueden sobresalir o quedar desbloqueados en la celda de caracteres, uno o ambos de los incrementos A y C pueden ser un número negativo.

 

 
