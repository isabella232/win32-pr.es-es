---
title: Atributo StartArrowLength de VML
description: Atributo StartArrowLength de VML
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a57e10c9cf7b9a8683f4b1856355232afc16be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420983"
---
# <a name="vml-startarrowlength-attribute"></a><span data-ttu-id="90c4f-103">Atributo StartArrowLength de VML</span><span class="sxs-lookup"><span data-stu-id="90c4f-103">VML StartArrowLength Attribute</span></span>

<span data-ttu-id="90c4f-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="90c4f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="90c4f-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="90c4f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="90c4f-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="90c4f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="90c4f-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="90c4f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="90c4f-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="90c4f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="90c4f-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="90c4f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="90c4f-110">Define la longitud de la punta de flecha para el inicio de una línea.</span><span class="sxs-lookup"><span data-stu-id="90c4f-110">Defines the arrowhead length for the start of a line.</span></span> <span data-ttu-id="90c4f-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="90c4f-111">Read/write.</span></span> <span data-ttu-id="90c4f-112">**VgArrowheadLength**.</span><span class="sxs-lookup"><span data-stu-id="90c4f-112">**VgArrowheadLength**.</span></span>

<span data-ttu-id="90c4f-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="90c4f-113">**Applies To**</span></span>

[<span data-ttu-id="90c4f-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="90c4f-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="90c4f-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="90c4f-115">**Tag Syntax**</span></span>

<span data-ttu-id="90c4f-116"><v: *Element* startarrowlength = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="90c4f-116"><v: *element* startarrowlength=" *expression* "></span></span>

<span data-ttu-id="90c4f-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="90c4f-117">**Script Syntax**</span></span>

<span data-ttu-id="90c4f-118">*Element* . startarrowlength = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="90c4f-118">*element* .startarrowlength="*expression*"</span></span>

<span data-ttu-id="90c4f-119">*expresión* = de *elemento*. startarrowlength</span><span class="sxs-lookup"><span data-stu-id="90c4f-119">*expression*=*element*.startarrowlength</span></span>

<span data-ttu-id="90c4f-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="90c4f-120">**Remarks**</span></span>

<span data-ttu-id="90c4f-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="90c4f-121">Values include:</span></span>

-   <span data-ttu-id="90c4f-122">Short</span><span class="sxs-lookup"><span data-stu-id="90c4f-122">Short</span></span>
-   <span data-ttu-id="90c4f-123">Media (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="90c4f-123">Medium (default)</span></span>
-   <span data-ttu-id="90c4f-124">long</span><span class="sxs-lookup"><span data-stu-id="90c4f-124">Long</span></span>

<span data-ttu-id="90c4f-125">Atributo estándar de VML</span><span class="sxs-lookup"><span data-stu-id="90c4f-125">VML Standard Attribute</span></span>

<span data-ttu-id="90c4f-126">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="90c4f-126">**Example**</span></span>

<span data-ttu-id="90c4f-127">Una línea se dibuja con una punta de flecha clásica corta en el inicio del trazo.</span><span class="sxs-lookup"><span data-stu-id="90c4f-127">A line is drawn with a short classic arrowhead on the start of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 