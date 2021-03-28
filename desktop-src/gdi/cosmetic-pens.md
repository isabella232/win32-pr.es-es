---
description: Las dimensiones de un lápiz cosmético se especifican en unidades de dispositivo.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Bolígrafos cosméticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb312ed0b3825397ff79ebc32d363956ad04519
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812001"
---
# <a name="cosmetic-pens"></a><span data-ttu-id="94373-103">Bolígrafos cosméticas</span><span class="sxs-lookup"><span data-stu-id="94373-103">Cosmetic Pens</span></span>

<span data-ttu-id="94373-104">Las dimensiones de un lápiz cosmético se especifican en unidades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94373-104">The dimensions of a cosmetic pen are specified in device units.</span></span> <span data-ttu-id="94373-105">Por lo tanto, las líneas dibujadas con un lápiz cosmético siempre tienen un ancho fijo.</span><span class="sxs-lookup"><span data-stu-id="94373-105">Therefore, lines drawn with a cosmetic pen always have a fixed width.</span></span> <span data-ttu-id="94373-106">Las líneas dibujadas con un lápiz cosmético generalmente se dibujan de 3 a 10 veces más rápido que las líneas dibujadas con un lápiz geométrico.</span><span class="sxs-lookup"><span data-stu-id="94373-106">Lines drawn with a cosmetic pen are generally drawn 3 to 10 times faster than lines drawn with a geometric pen.</span></span> <span data-ttu-id="94373-107">Los lápices estéticos tienen tres atributos: ancho, estilo y color.</span><span class="sxs-lookup"><span data-stu-id="94373-107">Cosmetic pens have three attributes: width, style, and color.</span></span> <span data-ttu-id="94373-108">Para obtener más información sobre estos atributos, vea [Pen Attributes](pen-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="94373-108">For more information about these attributes, see [Pen Attributes](pen-attributes.md).</span></span>

<span data-ttu-id="94373-109">Para crear un lápiz cosmético, use la función [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) .</span><span class="sxs-lookup"><span data-stu-id="94373-109">To create a cosmetic pen, use the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="94373-110">Para recuperar una de las tres plumillas cosméticas de acciones administradas por el sistema, use la función [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) .</span><span class="sxs-lookup"><span data-stu-id="94373-110">To retrieve one of the three stock cosmetic pens managed by the system, use the [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function.</span></span>

<span data-ttu-id="94373-111">Después de crear un lápiz (u obtener un identificador a uno de los lápices de bolsa), seleccione el lápiz en el contexto de dispositivo (DC) de la aplicación mediante la función [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="94373-111">After you create a pen (or obtain a handle to one of the stock pens), select the pen into the application's device context (DC) using the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span> <span data-ttu-id="94373-112">A partir de este punto, la aplicación usa este lápiz para todas las operaciones de dibujo de líneas en su área de cliente.</span><span class="sxs-lookup"><span data-stu-id="94373-112">From this point on, the application uses this pen for any line-drawing operations in its client area.</span></span>

 

 



