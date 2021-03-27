---
description: El sistema proporciona seis fuentes estándar.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Usar una fuente estándar para dibujar texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a7e580175956185bcc26a7ebbae8d46dfff078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002731"
---
# <a name="using-a-stock-font-to-draw-text"></a><span data-ttu-id="e232f-103">Usar una fuente estándar para dibujar texto</span><span class="sxs-lookup"><span data-stu-id="e232f-103">Using a Stock Font to Draw Text</span></span>

<span data-ttu-id="e232f-104">El sistema proporciona seis fuentes estándar.</span><span class="sxs-lookup"><span data-stu-id="e232f-104">The system provides six stock fonts.</span></span> <span data-ttu-id="e232f-105">Una fuente estándar es una fuente lógica que una aplicación puede obtener llamando a la función [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) y especificando la fuente solicitada.</span><span class="sxs-lookup"><span data-stu-id="e232f-105">A stock font is a logical font that an application can obtain by calling the [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function and specifying the requested font.</span></span> <span data-ttu-id="e232f-106">La lista siguiente contiene los valores que se pueden especificar para obtener una fuente estándar.</span><span class="sxs-lookup"><span data-stu-id="e232f-106">The following list contains the values that you can specify to obtain a stock font.</span></span>



| <span data-ttu-id="e232f-107">Value</span><span class="sxs-lookup"><span data-stu-id="e232f-107">Value</span></span>                 | <span data-ttu-id="e232f-108">Significado</span><span class="sxs-lookup"><span data-stu-id="e232f-108">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e232f-109">\_fuente ANSI fija \_</span><span class="sxs-lookup"><span data-stu-id="e232f-109">ANSI\_FIXED\_FONT</span></span>     | <span data-ttu-id="e232f-110">Especifica una fuente monoespaciada basada en el juego de caracteres de Windows.</span><span class="sxs-lookup"><span data-stu-id="e232f-110">Specifies a monospace font based on the Windows character set.</span></span> <span data-ttu-id="e232f-111">Normalmente se utiliza una fuente Courier.</span><span class="sxs-lookup"><span data-stu-id="e232f-111">A Courier font is typically used.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="e232f-112">\_fuente ANSI var \_</span><span class="sxs-lookup"><span data-stu-id="e232f-112">ANSI\_VAR\_FONT</span></span>       | <span data-ttu-id="e232f-113">Especifica una fuente proporcional basada en el juego de caracteres de Windows.</span><span class="sxs-lookup"><span data-stu-id="e232f-113">Specifies a proportional font based on the Windows character set.</span></span> <span data-ttu-id="e232f-114">Normalmente se utiliza MS Sans Serif.</span><span class="sxs-lookup"><span data-stu-id="e232f-114">MS Sans Serif is typically used.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="e232f-115">\_fuente predeterminada del dispositivo \_</span><span class="sxs-lookup"><span data-stu-id="e232f-115">DEVICE\_DEFAULT\_FONT</span></span> | <span data-ttu-id="e232f-116">Especifica la fuente preferida para el dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e232f-116">Specifies the preferred font for the specified device.</span></span> <span data-ttu-id="e232f-117">Suele ser la fuente del sistema para los dispositivos de visualización; sin embargo, para algunas impresoras matriciales se trata de una fuente que reside en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e232f-117">This is typically the System font for display devices; however, for some dot-matrix printers this is a font that is resident on the device.</span></span> <span data-ttu-id="e232f-118">(La impresión con esta fuente suele ser más rápida que la impresión con una fuente de mapa de bits descargada).</span><span class="sxs-lookup"><span data-stu-id="e232f-118">(Printing with this font is usually faster than printing with a downloaded, bitmap font).</span></span>    |
| <span data-ttu-id="e232f-119">\_fuente fija \_ OEM</span><span class="sxs-lookup"><span data-stu-id="e232f-119">OEM\_FIXED\_FONT</span></span>      | <span data-ttu-id="e232f-120">Especifica una fuente monoespaciada basada en un juego de caracteres OEM.</span><span class="sxs-lookup"><span data-stu-id="e232f-120">Specifies a monospace font based on an OEM character set.</span></span> <span data-ttu-id="e232f-121">En el caso de los equipos de IBM y los compatibles, la fuente OEM se basa en el juego de caracteres de IBM PC.</span><span class="sxs-lookup"><span data-stu-id="e232f-121">For IBM computers and compatibles, the OEM font is based on the IBM PC character set.</span></span>                                                                                                                                                 |
| <span data-ttu-id="e232f-122">fuente del sistema \_</span><span class="sxs-lookup"><span data-stu-id="e232f-122">SYSTEM\_FONT</span></span>          | <span data-ttu-id="e232f-123">Especifica la fuente del sistema.</span><span class="sxs-lookup"><span data-stu-id="e232f-123">Specifies the System font.</span></span> <span data-ttu-id="e232f-124">Se trata de una fuente proporcional basada en el juego de caracteres de Windows y que el sistema operativo utiliza para mostrar los títulos de ventana, los nombres de menú y el texto en los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e232f-124">This is a proportional font based on the Windows character set, and is used by the operating system to display window titles, menu names, and text in dialog boxes.</span></span> <span data-ttu-id="e232f-125">La fuente del sistema siempre está disponible.</span><span class="sxs-lookup"><span data-stu-id="e232f-125">The System font is always available.</span></span> <span data-ttu-id="e232f-126">Otras fuentes solo están disponibles si se han instalado.</span><span class="sxs-lookup"><span data-stu-id="e232f-126">Other fonts are available only if they have been installed.</span></span> |
| <span data-ttu-id="e232f-127">\_fuente fija del sistema \_</span><span class="sxs-lookup"><span data-stu-id="e232f-127">SYSTEM\_FIXED\_FONT</span></span>   | <span data-ttu-id="e232f-128">Especifica una fuente monoespaciada compatible con la fuente del sistema en versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="e232f-128">Specifies a monospace font compatible with the System font in early versions of Windows.</span></span>                                                                                                                                                                                                        |



 

<span data-ttu-id="e232f-129">Para obtener más información sobre las fuentes, vea acerca de las [fuentes](about-fonts.md).</span><span class="sxs-lookup"><span data-stu-id="e232f-129">For more information on fonts, see [About Fonts](about-fonts.md).</span></span>

<span data-ttu-id="e232f-130">En el ejemplo siguiente se recupera un identificador de la fuente stock variable, se selecciona en un contexto de dispositivo y, a continuación, se escribe una cadena con esa fuente:</span><span class="sxs-lookup"><span data-stu-id="e232f-130">The following example retrieves a handle to the variable stock font, selects it into a device context, and then writes a string using that font:</span></span>


```C++
HFONT hFont, hOldFont; 

// Retrieve a handle to the variable stock font.  
hFont = (HFONT)GetStockObject(ANSI_VAR_FONT); 

// Select the variable stock font into the specified device context. 
if (hOldFont = (HFONT)SelectObject(hdc, hFont)) 
{
    // Display the text string.  
    TextOut(hdc, 10, 50, L"Sample ANSI_VAR_FONT text", 25); 

    // Restore the original font.        
    SelectObject(hdc, hOldFont); 
}
```



<span data-ttu-id="e232f-131">Si otras fuentes bursátiles no están disponibles, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) devuelve un identificador a la fuente del sistema (fuente del sistema \_ ).</span><span class="sxs-lookup"><span data-stu-id="e232f-131">If other stock fonts are not available, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) returns a handle to the System font (SYSTEM\_FONT).</span></span> <span data-ttu-id="e232f-132">Solo debe usar fuentes estándar si el modo de asignación del contexto de dispositivo de la aplicación es \_ texto mm.</span><span class="sxs-lookup"><span data-stu-id="e232f-132">You should use stock fonts only if the mapping mode for your application's device context is MM\_TEXT.</span></span>

 

 



