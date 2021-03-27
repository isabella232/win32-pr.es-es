---
description: Cada monitor puede tener su propia profundidad de color.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Colores en varios monitores de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50410631cf0ea3ac0a1b9967f1116809be0a4851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001526"
---
# <a name="colors-on-multiple-display-monitors"></a><span data-ttu-id="66ce0-103">Colores en varios monitores de pantalla</span><span class="sxs-lookup"><span data-stu-id="66ce0-103">Colors on Multiple Display Monitors</span></span>

<span data-ttu-id="66ce0-104">Cada monitor puede tener su propia profundidad de color.</span><span class="sxs-lookup"><span data-stu-id="66ce0-104">Each monitor can have its own color depth.</span></span> <span data-ttu-id="66ce0-105">El sistema ajusta automáticamente los colores a medida que las ventanas se mueven por los monitores con diferentes profundidades de color.</span><span class="sxs-lookup"><span data-stu-id="66ce0-105">The system automatically adjusts colors as windows move across monitors with different color depths.</span></span> <span data-ttu-id="66ce0-106">En general, esto produce buenos resultados.</span><span class="sxs-lookup"><span data-stu-id="66ce0-106">In general, this produces good results.</span></span> <span data-ttu-id="66ce0-107">Sin embargo, esto no es siempre óptimo.</span><span class="sxs-lookup"><span data-stu-id="66ce0-107">However, this is not always optimal.</span></span> <span data-ttu-id="66ce0-108">Para aprovechar las capacidades de color de los distintos monitores, consulte la sección [pintar en varios monitores de pantalla](painting-on-multiple-display-monitors.md) siguiente.</span><span class="sxs-lookup"><span data-stu-id="66ce0-108">To take advantage of the color capabilities of different monitors, see the [Painting on Multiple Display Monitors](painting-on-multiple-display-monitors.md) section that follows.</span></span>

<span data-ttu-id="66ce0-109">Para determinar si todos los monitores tienen el mismo formato de color, llame a [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con SM \_ SAMEDISPLAYFORMAT.</span><span class="sxs-lookup"><span data-stu-id="66ce0-109">To determine if all monitors have the same color format, call [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_SAMEDISPLAYFORMAT.</span></span>

<span data-ttu-id="66ce0-110">Si el monitor principal está en la paleta, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) y [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) funcionan igual que antes, pero en todos los monitores.</span><span class="sxs-lookup"><span data-stu-id="66ce0-110">If the primary monitor is palettized, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) and [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) work the same as before, but across all monitors.</span></span> <span data-ttu-id="66ce0-111">Además, las paletas de todos los dispositivos de paleta están sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="66ce0-111">In addition, the palettes of all palettized devices are synchronized.</span></span> <span data-ttu-id="66ce0-112">Si el monitor principal no es de paleta, **SelectPalette** y **RealizePalette** seleccionarán la paleta en segundo plano y los dispositivos de paleta no se sincronizarán.</span><span class="sxs-lookup"><span data-stu-id="66ce0-112">If the primary monitor is not palettized, **SelectPalette** and **RealizePalette** will select the palette into the background and palettized devices will not be synchronized.</span></span>

 

 
