---
description: El atributo de estilo especifica el patrón de línea que aparece cuando se usa un lápiz cosmético o geométrico determinado. Hay ocho estilos de lápiz predefinidos. En la ilustración siguiente se muestran los siete estilos definidos por el sistema.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Estilo de pluma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447839627f97d7662fdef35bd7088ef7b0dcba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001518"
---
# <a name="pen-style"></a><span data-ttu-id="d45a4-105">Estilo de pluma</span><span class="sxs-lookup"><span data-stu-id="d45a4-105">Pen Style</span></span>

<span data-ttu-id="d45a4-106">El atributo de estilo especifica el patrón de línea que aparece cuando se usa un lápiz cosmético o geométrico determinado.</span><span class="sxs-lookup"><span data-stu-id="d45a4-106">The style attribute specifies the line pattern that appears when a particular cosmetic or geometric pen is used.</span></span> <span data-ttu-id="d45a4-107">Hay ocho estilos de lápiz predefinidos.</span><span class="sxs-lookup"><span data-stu-id="d45a4-107">There are eight predefined pen styles.</span></span> <span data-ttu-id="d45a4-108">En la ilustración siguiente se muestran los siete estilos definidos por el sistema.</span><span class="sxs-lookup"><span data-stu-id="d45a4-108">The following illustration shows the seven of these styles that are defined by the system.</span></span>

![Ilustración que muestra siete líneas, cada una dibujada con un estilo predefinido diferente](images/cspen-01.png)

<span data-ttu-id="d45a4-110">El estilo interior-Frame es idéntico al estilo sólido para los lápices estéticos.</span><span class="sxs-lookup"><span data-stu-id="d45a4-110">The inside-frame style is identical to the solid style for cosmetic pens.</span></span> <span data-ttu-id="d45a4-111">Sin embargo, funciona de forma diferente cuando se usa con un lápiz geométrico.</span><span class="sxs-lookup"><span data-stu-id="d45a4-111">However, it operates differently when used with a geometric pen.</span></span> <span data-ttu-id="d45a4-112">Si el lápiz geométrico es más ancho que un solo píxel y una función de dibujo usa el lápiz para dibujar un borde alrededor de un objeto relleno, el sistema dibuja el borde dentro del marco del objeto.</span><span class="sxs-lookup"><span data-stu-id="d45a4-112">If the geometric pen is wider than a single pixel and a drawing function uses the pen to draw a border around a filled object, the system draws the border inside the object's frame.</span></span> <span data-ttu-id="d45a4-113">Con el estilo interior-Frame, una aplicación puede asegurarse de que un objeto aparece completamente dentro de las dimensiones especificadas, independientemente del ancho del lápiz geométrico.</span><span class="sxs-lookup"><span data-stu-id="d45a4-113">By using the inside-frame style, an application can ensure that an object appears entirely within the specified dimensions, regardless of the geometric pen width.</span></span>

<span data-ttu-id="d45a4-114">Además de los siete estilos definidos por el sistema, hay un octavo estilo definido por el usuario (o aplicación).</span><span class="sxs-lookup"><span data-stu-id="d45a4-114">In addition to the seven styles defined by the system, there is an eighth style that is user (or application) defined.</span></span> <span data-ttu-id="d45a4-115">Un estilo definido por el usuario genera líneas con una serie personalizada de guiones y puntos.</span><span class="sxs-lookup"><span data-stu-id="d45a4-115">A user-defined style generates lines with a customized series of dashes and dots.</span></span>

<span data-ttu-id="d45a4-116">Use la función [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) para crear un lápiz que tenga los estilos definidos por el sistema.</span><span class="sxs-lookup"><span data-stu-id="d45a4-116">Use the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function to create a pen that has the system-defined styles.</span></span> <span data-ttu-id="d45a4-117">Utilice la función **ExtCreatePen** para crear un lápiz que tenga un estilo definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d45a4-117">Use the **ExtCreatePen** function to create a pen that has a user-defined style.</span></span>

 

 



