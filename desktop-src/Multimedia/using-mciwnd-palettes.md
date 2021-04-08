---
title: Usar las paletas MCIWnd
description: Usar las paletas MCIWnd
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- MCIWndGetPalette (macro)
- MCIWndSetPalette (macro)
- MCIWndRealize (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970e0e33c9dd03c7f1133576f371b713f7174df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995223"
---
# <a name="using-mciwnd-palettes"></a><span data-ttu-id="b42b0-106">Usar las paletas MCIWnd</span><span class="sxs-lookup"><span data-stu-id="b42b0-106">Using MCIWnd Palettes</span></span>

<span data-ttu-id="b42b0-107">La reproducción de clips de vídeo con una profundidad de color de 8 bits (256: capacidad de color) requiere una paleta para definir los colores que se usan.</span><span class="sxs-lookup"><span data-stu-id="b42b0-107">Playing video clips with 8-bit color depth (256-color capacity) requires a palette to define the colors being used.</span></span> <span data-ttu-id="b42b0-108">A veces, la paleta incluida con un clip de vídeo no es la más adecuada para su uso durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="b42b0-108">Sometimes, the palette included with a video clip is not the most appropriate palette to use during playback.</span></span> <span data-ttu-id="b42b0-109">En este caso, MCIWnd proporciona tres maneras de administrar las paletas para la reproducción:</span><span class="sxs-lookup"><span data-stu-id="b42b0-109">In this case, MCIWnd provides three ways to manage palettes for playback:</span></span>

-   <span data-ttu-id="b42b0-110">Recupera un identificador de la paleta asociada a una ventana de MCIWnd mediante la macro [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="b42b0-110">Retrieve a handle to the palette associated with an MCIWnd window by using the [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) macro.</span></span> <span data-ttu-id="b42b0-111">La paleta no se asocia necesariamente exclusivamente con la ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="b42b0-111">The palette is not necessarily associated exclusively with the MCIWnd window.</span></span> <span data-ttu-id="b42b0-112">Otras aplicaciones pueden tener acceso al identificador de la paleta e incluso invalidarlo.</span><span class="sxs-lookup"><span data-stu-id="b42b0-112">Other applications can access, and even invalidate, the palette handle.</span></span> <span data-ttu-id="b42b0-113">Por consiguiente, la aplicación debe prever el uso global de la paleta y, cuando termine con la paleta, no debe liberarla.</span><span class="sxs-lookup"><span data-stu-id="b42b0-113">Consequently, your application should anticipate the global use of the palette and, when finished with the palette, should not free it.</span></span>
-   <span data-ttu-id="b42b0-114">Especifique una nueva paleta para usarla con el clip de vídeo asociado a una ventana de MCIWnd mediante la macro [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .</span><span class="sxs-lookup"><span data-stu-id="b42b0-114">Specify a new palette to use with the video clip associated with an MCIWnd window by using the [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) macro.</span></span>
-   <span data-ttu-id="b42b0-115">Observe la paleta asociada a una ventana de MCIWnd de la paleta del sistema mediante la macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .</span><span class="sxs-lookup"><span data-stu-id="b42b0-115">Realize the palette associated with an MCIWnd window to the system palette by using the [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) macro.</span></span> <span data-ttu-id="b42b0-116">Esta macro llama a la función [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) con la paleta asociada a la ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="b42b0-116">This macro calls the [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) function with the palette associated with the MCIWnd window.</span></span> <span data-ttu-id="b42b0-117">Si los controladores de mensajes de la aplicación para [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) y [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) solo llaman a **RealizePalette** o **MCIWndRealize**, debe reenviar estos mensajes a MCIWnd si no los administra usted mismo.</span><span class="sxs-lookup"><span data-stu-id="b42b0-117">If your application message handlers for [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) call only **RealizePalette** or **MCIWndRealize**, you must forward these messages to MCIWnd if you do not handle them yourself.</span></span>

> [!Note]  
> <span data-ttu-id="b42b0-118">Cuando se carga un clip de vídeo con una profundidad de color de 8 bits en la ventana de MCIWnd, la paleta incluida con ese clip reemplaza la paleta asociada a la ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="b42b0-118">When a video clip with 8-bit color depth is loaded into the MCIWnd window, the palette included with that clip replaces the palette associated with the MCIWnd window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b42b0-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b42b0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b42b0-120">Mejoras en la reproducción</span><span class="sxs-lookup"><span data-stu-id="b42b0-120">Playback Enhancements</span></span>](playback-enhancements.md)
</dt> </dl>

 

 