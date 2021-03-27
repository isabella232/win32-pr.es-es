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
# <a name="drawing-text-windows-gdi"></a><span data-ttu-id="9ff04-103">Dibujar texto (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="9ff04-103">Drawing Text (Windows GDI)</span></span>

<span data-ttu-id="9ff04-104">Después de que una aplicación seleccione la fuente adecuada, establezca las opciones de formato de texto necesarias y calcule los valores de ancho y alto de caracteres necesarios para una cadena de texto, puede empezar a dibujar caracteres y símbolos mediante una llamada a cualquiera de las funciones de salida de texto:</span><span class="sxs-lookup"><span data-stu-id="9ff04-104">After an application selects the appropriate font, sets the required text-formatting options, and computes the necessary character width and height values for a string of text, it can begin drawing characters and symbols by calling any of the text-output functions:</span></span>

-   [<span data-ttu-id="9ff04-105">DrawText</span><span class="sxs-lookup"><span data-stu-id="9ff04-105">DrawText</span></span>](/windows/desktop/api/Winuser/nf-winuser-drawtext)
-   [<span data-ttu-id="9ff04-106">DrawTextEx</span><span class="sxs-lookup"><span data-stu-id="9ff04-106">DrawTextEx</span></span>](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)
-   [<span data-ttu-id="9ff04-107">ExtTextOut</span><span class="sxs-lookup"><span data-stu-id="9ff04-107">ExtTextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [<span data-ttu-id="9ff04-108">PolyTextOut</span><span class="sxs-lookup"><span data-stu-id="9ff04-108">PolyTextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)
-   [<span data-ttu-id="9ff04-109">TabbedTextOut</span><span class="sxs-lookup"><span data-stu-id="9ff04-109">TabbedTextOut</span></span>](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)
-   [<span data-ttu-id="9ff04-110">TextOut</span><span class="sxs-lookup"><span data-stu-id="9ff04-110">TextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

<span data-ttu-id="9ff04-111">Cuando una aplicación llama a una de estas funciones, el sistema operativo pasa la llamada al motor de gráficos, que a su vez pasa la llamada al controlador de dispositivo adecuado.</span><span class="sxs-lookup"><span data-stu-id="9ff04-111">When an application calls one of these functions, the operating system passes the call to the graphics engine, which in turn passes the call to the appropriate device driver.</span></span> <span data-ttu-id="9ff04-112">En el nivel de controlador de dispositivo, todas estas llamadas se admiten en una o varias llamadas a la propia función [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) o [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) del controlador.</span><span class="sxs-lookup"><span data-stu-id="9ff04-112">At the device driver level, all of these calls are supported by one or more calls to the driver's own [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) or [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) function.</span></span> <span data-ttu-id="9ff04-113">Una aplicación obtendrá la ejecución más rápida mediante una llamada a [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), que se convierte rápidamente en una llamada **ExtTextOut** para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ff04-113">An application will achieve the fastest execution by calling [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), which is quickly converted into an **ExtTextOut** call for the device.</span></span> <span data-ttu-id="9ff04-114">Sin embargo, hay instancias cuando una aplicación debe llamar a una de las otras tres funciones; por ejemplo, para dibujar varias líneas de texto dentro de los bordes de una región rectangular especificada, es más eficaz llamar a [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="9ff04-114">However, there are instances when an application should call one of the other three functions; for example, to draw multiple lines of text within the borders of a specified rectangular region, it is more efficient to call [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="9ff04-115">Para crear una tabla de varias columnas con columnas justificadas de texto, es más eficaz llamar a [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).</span><span class="sxs-lookup"><span data-stu-id="9ff04-115">To create a multicolumn table with justified columns of text, it is more efficient to call [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).</span></span>

 

 
