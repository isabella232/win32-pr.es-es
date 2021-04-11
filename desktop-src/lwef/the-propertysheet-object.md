---
title: El objeto hoja
description: El objeto hoja
ms.assetid: 9d15d198-a4fe-4c05-a7be-0807a179cd9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ae4ded2625440ba34170df605b60287f105800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148790"
---
# <a name="the-propertysheet-object"></a><span data-ttu-id="9ac0e-103">El objeto hoja</span><span class="sxs-lookup"><span data-stu-id="9ac0e-103">The PropertySheet Object</span></span>

<span data-ttu-id="9ac0e-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9ac0e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="9ac0e-105">El objeto [**hoja**](https://www.bing.com/search?q=**PropertySheet**) proporciona varias propiedades que puede usar si desea manipular el carácter relativo a la hoja de propiedades del agente de Microsoft (también conocido como la ventana Opciones de carácter avanzadas).</span><span class="sxs-lookup"><span data-stu-id="9ac0e-105">The [**PropertySheet**](https://www.bing.com/search?q=**PropertySheet**) object provides several properties you can use if you want to manipulate the character relative to the Microsoft Agent property sheet (also known as the Advanced Character Options window).</span></span>

-   [<span data-ttu-id="9ac0e-106">**Height**</span><span class="sxs-lookup"><span data-stu-id="9ac0e-106">**Height**</span></span>](height-property-pso.md)
-   [<span data-ttu-id="9ac0e-107">**Salido**</span><span class="sxs-lookup"><span data-stu-id="9ac0e-107">**Left**</span></span>](left-property-pso.md)
-   [<span data-ttu-id="9ac0e-108">**Página**</span><span class="sxs-lookup"><span data-stu-id="9ac0e-108">**Page**</span></span>](page-property.md)
-   [<span data-ttu-id="9ac0e-109">**Arriba**</span><span class="sxs-lookup"><span data-stu-id="9ac0e-109">**Top**</span></span>](top-property-pso.md)
-   [<span data-ttu-id="9ac0e-110">**Visible**</span><span class="sxs-lookup"><span data-stu-id="9ac0e-110">**Visible**</span></span>](visible-property.md)
-   [<span data-ttu-id="9ac0e-111">**Width**</span><span class="sxs-lookup"><span data-stu-id="9ac0e-111">**Width**</span></span>](width-property-pso.md)

<span data-ttu-id="9ac0e-112">Si consulta las propiedades de [**alto**](height-property-pso.md), [**izquierda**](left-property-pso.md), [**superior**](top-property-pso.md)y [**ancho**](width-property-pso.md) antes de que se haya mostrado alguna vez la hoja de propiedades, sus valores devuelven el valor cero (0).</span><span class="sxs-lookup"><span data-stu-id="9ac0e-112">If you query [**Height**](height-property-pso.md), [**Left**](left-property-pso.md), [**Top**](top-property-pso.md), and [**Width**](width-property-pso.md) properties before the property sheet has ever been shown, their values return as zero (0).</span></span> <span data-ttu-id="9ac0e-113">Una vez que se muestran, estas propiedades devuelven la última posición y el tamaño de la ventana (con respecto a la resolución de pantalla actual).</span><span class="sxs-lookup"><span data-stu-id="9ac0e-113">Once shown, these properties return the last position and size of the window (relative to your current screen resolution).</span></span>

 

 




