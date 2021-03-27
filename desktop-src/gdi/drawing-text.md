---
description: Dibujar texto
ms.assetid: 8a06f659-4e08-4738-b7a9-956b599c1344
title: Dibujar texto (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7db44a756ff211bcae7605cb87bdac77005b34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811966"
---
# <a name="drawing-text-windows-gdi"></a>Dibujar texto (Windows GDI)

Después de que una aplicación seleccione la fuente adecuada, establezca las opciones de formato de texto necesarias y calcule los valores de ancho y alto de caracteres necesarios para una cadena de texto, puede empezar a dibujar caracteres y símbolos mediante una llamada a cualquiera de las funciones de salida de texto:

-   [DrawText](/windows/desktop/api/Winuser/nf-winuser-drawtext)
-   [DrawTextEx](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)
-   [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [PolyTextOut](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)
-   [TabbedTextOut](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)
-   [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

Cuando una aplicación llama a una de estas funciones, el sistema operativo pasa la llamada al motor de gráficos, que a su vez pasa la llamada al controlador de dispositivo adecuado. En el nivel de controlador de dispositivo, todas estas llamadas se admiten en una o varias llamadas a la propia función [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) o [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) del controlador. Una aplicación obtendrá la ejecución más rápida mediante una llamada a [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), que se convierte rápidamente en una llamada **ExtTextOut** para el dispositivo. Sin embargo, hay instancias cuando una aplicación debe llamar a una de las otras tres funciones; por ejemplo, para dibujar varias líneas de texto dentro de los bordes de una región rectangular especificada, es más eficaz llamar a [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). Para crear una tabla de varias columnas con columnas justificadas de texto, es más eficaz llamar a [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).

 

 
