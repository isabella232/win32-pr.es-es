---
description: Dibujar texto
ms.assetid: 8a06f659-4e08-4738-b7a9-956b599c1344
title: Dibujar texto (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52508e5a0825a3f43a62f5cce7905a767513f007555eb430c26dbc2d914f372
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062275"
---
# <a name="drawing-text-windows-gdi"></a>Dibujar texto (Windows GDI)

Una vez que una aplicación selecciona la fuente adecuada, establece las opciones de formato de texto necesarias y calcula los valores de ancho y alto de caracteres necesarios para una cadena de texto, puede empezar a dibujar caracteres y símbolos llamando a cualquiera de las funciones de salida de texto:

-   [Drawtext](/windows/desktop/api/Winuser/nf-winuser-drawtext)
-   [DrawTextEx](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)
-   [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [PolyTextOut](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)
-   [TabbedTextOut](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)
-   [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

Cuando una aplicación llama a una de estas funciones, el sistema operativo pasa la llamada al motor de gráficos, que a su vez pasa la llamada al controlador de dispositivo adecuado. En el nivel de controlador de dispositivo, todas estas llamadas son compatibles con una o varias llamadas a la propia función [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) o [TextOut del](/windows/desktop/api/Wingdi/nf-wingdi-textouta) controlador. Una aplicación logrará la ejecución más rápida mediante una llamada a [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), que se convierte rápidamente en una **llamada ExtTextOut** para el dispositivo. Sin embargo, hay instancias en las que una aplicación debe llamar a una de las otras tres funciones. Por ejemplo, para dibujar varias líneas de texto dentro de los bordes de una región rectangular especificada, es más eficaz llamar a [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). Para crear una tabla de varias columnas con columnas de texto justificadas, es más eficaz llamar a [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).

 

 
