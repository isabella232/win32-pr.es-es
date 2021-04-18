---
description: Las siguientes funciones se usan con los pinceles.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: Funciones de pincel (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2170ff5c4b743e19da669bd76b340ca95ac2ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544550"
---
# <a name="brush-functions-windows-gdi"></a><span data-ttu-id="bdeb6-103">Funciones de pincel (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="bdeb6-103">Brush Functions (Windows GDI)</span></span>

<span data-ttu-id="bdeb6-104">Las siguientes funciones se usan con los pinceles.</span><span class="sxs-lookup"><span data-stu-id="bdeb6-104">The following functions are used with brushes.</span></span>



| <span data-ttu-id="bdeb6-105">Función</span><span class="sxs-lookup"><span data-stu-id="bdeb6-105">Function</span></span>                                                   | <span data-ttu-id="bdeb6-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdeb6-106">Description</span></span>                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="bdeb6-107">**CreateBrushIndirect**</span><span class="sxs-lookup"><span data-stu-id="bdeb6-107">**CreateBrushIndirect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | <span data-ttu-id="bdeb6-108">Crea un pincel con un estilo, color y patrón especificados</span><span class="sxs-lookup"><span data-stu-id="bdeb6-108">Creates a brush with a specified style, color, and pattern</span></span> |
| [<span data-ttu-id="bdeb6-109">**CreateDIBPatternBrushPt**</span><span class="sxs-lookup"><span data-stu-id="bdeb6-109">**CreateDIBPatternBrushPt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | <span data-ttu-id="bdeb6-110">Crea un pincel con el modelo a partir de un DIB</span><span class="sxs-lookup"><span data-stu-id="bdeb6-110">Creates a brush with the pattern from a DIB</span></span>                |
| [<span data-ttu-id="bdeb6-111">**CreateHatchBrush**</span><span class="sxs-lookup"><span data-stu-id="bdeb6-111">**CreateHatchBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | <span data-ttu-id="bdeb6-112">Crea un pincel con un patrón de trama y un color</span><span class="sxs-lookup"><span data-stu-id="bdeb6-112">Creates a brush with a hatch pattern and color</span></span>             |
| [<span data-ttu-id="bdeb6-113">**CreatePatternBrush**</span><span class="sxs-lookup"><span data-stu-id="bdeb6-113">**CreatePatternBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | <span data-ttu-id="bdeb6-114">Crea un pincel con un modelo de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="bdeb6-114">Creates a brush with a bitmap pattern</span></span>                      |
| [<span data-ttu-id="bdeb6-115">**CreateSolidBrush**</span><span class="sxs-lookup"><span data-stu-id="bdeb6-115">**CreateSolidBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | <span data-ttu-id="bdeb6-116">Crea un pincel con un color sólido.</span><span class="sxs-lookup"><span data-stu-id="bdeb6-116">Creates a brush with a solid color</span></span>                         |
| [<span data-ttu-id="bdeb6-117">**GetBrushOrgEx**</span><span class="sxs-lookup"><span data-stu-id="bdeb6-117">**GetBrushOrgEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | <span data-ttu-id="bdeb6-118">Obtiene el origen del pincel para un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bdeb6-118">Gets the brush origin for a device context</span></span>                 |
| [<span data-ttu-id="bdeb6-119">**GetSysColorBrush**</span><span class="sxs-lookup"><span data-stu-id="bdeb6-119">**GetSysColorBrush**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | <span data-ttu-id="bdeb6-120">Obtiene un identificador para un pincel que corresponde a un índice de color.</span><span class="sxs-lookup"><span data-stu-id="bdeb6-120">Gets a handle to a brush that corresponds to a color index</span></span> |
| [<span data-ttu-id="bdeb6-121">**PatBlt**</span><span class="sxs-lookup"><span data-stu-id="bdeb6-121">**PatBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | <span data-ttu-id="bdeb6-122">Dibuja un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="bdeb6-122">Paints a rectangle</span></span>                                         |
| [<span data-ttu-id="bdeb6-123">**SetBrushOrgEx**</span><span class="sxs-lookup"><span data-stu-id="bdeb6-123">**SetBrushOrgEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | <span data-ttu-id="bdeb6-124">Establece el origen del pincel para un contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="bdeb6-124">Sets the brush origin for a device context</span></span>                 |
| [<span data-ttu-id="bdeb6-125">**SetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="bdeb6-125">**SetDCBrushColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | <span data-ttu-id="bdeb6-126">Establece el color del pincel de contexto del dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="bdeb6-126">Sets the current device context brush color.</span></span>               |



 

## <a name="obsolete-functions"></a><span data-ttu-id="bdeb6-127">Funciones obsoletas</span><span class="sxs-lookup"><span data-stu-id="bdeb6-127">Obsolete Functions</span></span>

<span data-ttu-id="bdeb6-128">Las siguientes funciones solo se proporcionan por compatibilidad con las versiones de 16 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="bdeb6-128">The following functions are provided only for compatibility with 16-bit versions of Windows.</span></span>

[<span data-ttu-id="bdeb6-129">**CreateDIBPatternBrush**</span><span class="sxs-lookup"><span data-stu-id="bdeb6-129">**CreateDIBPatternBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



