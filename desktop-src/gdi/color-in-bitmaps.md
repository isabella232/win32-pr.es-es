---
description: El sistema controla los colores de los mapas de bits de forma distinta a los colores de los lápices, los pinceles y el texto.
ms.assetid: c315dd6e-87ee-4905-b193-186ea580ac0a
title: Color en mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 834744f35ccc8bd0c8714fa5bbb438b59c8b8db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155664"
---
# <a name="color-in-bitmaps"></a><span data-ttu-id="85e3a-103">Color en mapas de bits</span><span class="sxs-lookup"><span data-stu-id="85e3a-103">Color in Bitmaps</span></span>

<span data-ttu-id="85e3a-104">El sistema controla los colores de los mapas de bits de forma distinta a los colores de los lápices, los pinceles y el texto.</span><span class="sxs-lookup"><span data-stu-id="85e3a-104">The system handles colors in bitmaps differently than colors in pens, brushes, and text.</span></span> <span data-ttu-id="85e3a-105">Los mapas de bits compatibles, creados mediante la función [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) o [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , son específicos del dispositivo y conservan la información de color en un formato dependiente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85e3a-105">Compatible bitmaps, created by using the [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) or [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function, are device specific and retain color information in a device-dependent format.</span></span> <span data-ttu-id="85e3a-106">No se usan valores de color y los colores no están sujetos a las aproximaciones y al tramado.</span><span class="sxs-lookup"><span data-stu-id="85e3a-106">No color values are used, and the colors are not subject to approximations and dithering.</span></span>

<span data-ttu-id="85e3a-107">Los mapas de bits independientes del dispositivo (DIB) conservan la información de color como valores de color o índices de paleta de colores.</span><span class="sxs-lookup"><span data-stu-id="85e3a-107">Device-independent bitmaps (DIBs) retain color information either as color values or color palette indexes.</span></span> <span data-ttu-id="85e3a-108">Si se usan valores de color, los colores están sujetos a la aproximación, pero no a la interpolación.</span><span class="sxs-lookup"><span data-stu-id="85e3a-108">If color values are used, the colors are subject to approximation, but not dithering.</span></span> <span data-ttu-id="85e3a-109">Los índices de paleta de colores solo se pueden usar con dispositivos que admiten paletas de colores.</span><span class="sxs-lookup"><span data-stu-id="85e3a-109">Color palette indexes can only be used with devices that support color palettes.</span></span> <span data-ttu-id="85e3a-110">Aunque el sistema no aproxima ni trama los colores identificados por los índices, el color resultante puede ser diferente del previsto, ya que los índices producen resultados válidos solo en el contexto de la paleta de colores que era actual en el momento en que se creó el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="85e3a-110">Although the system does not approximate or dither colors identified by indexes, the resulting color may be different than that intended, because the indexes yield valid results only in the context of the color palette that was current at the time the bitmap was created.</span></span> <span data-ttu-id="85e3a-111">Si la paleta cambia, haga lo mismo con los colores del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="85e3a-111">If the palette changes, so do the colors in the bitmap.</span></span> <span data-ttu-id="85e3a-112">Para obtener más información sobre los índices de paleta, vea [paleta predeterminada](default-palette.md) y [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).</span><span class="sxs-lookup"><span data-stu-id="85e3a-112">For more information on palette indexes, see [Default Palette](default-palette.md) and [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).</span></span>

<span data-ttu-id="85e3a-113">Además de hacer referencia a la paleta lógica, una aplicación también puede hacer referencia a un valor en una tabla de colores DIB.</span><span class="sxs-lookup"><span data-stu-id="85e3a-113">In addition to referencing the logical palette, an application can also reference a value in a DIB color table.</span></span> <span data-ttu-id="85e3a-114">Para seleccionar un color en una tabla de colores DIB, llame a [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex).</span><span class="sxs-lookup"><span data-stu-id="85e3a-114">To select a color in a DIB color table, call [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex).</span></span> <span data-ttu-id="85e3a-115">Tenga en cuenta que esto solo es posible para un contexto de dispositivo que tenga un DIB seleccionado en él.</span><span class="sxs-lookup"><span data-stu-id="85e3a-115">Note that this is only possible for a device context that has a DIB selected into it.</span></span>

 

 



