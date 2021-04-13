---
title: Atributo V-Text-Anchor de VML
description: Atributo V-Text-Anchor de VML
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603f118a260c8ce9c271128fa642e9e2ae569806
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421065"
---
# <a name="vml-v-text-anchor-attribute"></a><span data-ttu-id="1d5cc-103">Atributo V-Text-Anchor de VML</span><span class="sxs-lookup"><span data-stu-id="1d5cc-103">VML V-Text-Anchor Attribute</span></span>

<span data-ttu-id="1d5cc-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1d5cc-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1d5cc-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1d5cc-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1d5cc-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1d5cc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1d5cc-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1d5cc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1d5cc-110">Define la delimitación vertical del texto en un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-110">Defines the vertical anchoring of text in a textbox.</span></span> <span data-ttu-id="1d5cc-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1d5cc-111">Read/write.</span></span> <span data-ttu-id="1d5cc-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-112">**String**.</span></span>

<span data-ttu-id="1d5cc-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-113">**Applies To**</span></span>

[<span data-ttu-id="1d5cc-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="1d5cc-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="1d5cc-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-115">**Tag Syntax**</span></span>

<span data-ttu-id="1d5cc-116"><v: *elemento* v-Text-Anchor = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="1d5cc-116"><v: *element* v-text-anchor=" *expression* "></span></span>

<span data-ttu-id="1d5cc-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-117">**Remarks**</span></span>

<span data-ttu-id="1d5cc-118">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="1d5cc-118">Values include:</span></span>

-   <span data-ttu-id="1d5cc-119">**Top** (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="1d5cc-119">**top** (default)</span></span>
-   <span data-ttu-id="1d5cc-120">**Apellido**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-120">**middle**</span></span>
-   <span data-ttu-id="1d5cc-121">**descendente**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-121">**bottom**</span></span>
-   <span data-ttu-id="1d5cc-122">**Centro superior**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-122">**top-center**</span></span>
-   <span data-ttu-id="1d5cc-123">**Centro central**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-123">**middle-center**</span></span>
-   <span data-ttu-id="1d5cc-124">**centro inferior**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-124">**bottom-center**</span></span>
-   <span data-ttu-id="1d5cc-125">**línea de base superior**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-125">**top-baseline**</span></span>
-   <span data-ttu-id="1d5cc-126">**línea de base inferior**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-126">**bottom-baseline**</span></span>
-   <span data-ttu-id="1d5cc-127">**Centro de la línea de base superior**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-127">**top-center-baseline**</span></span>
-   <span data-ttu-id="1d5cc-128">**línea central inferior**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-128">**bottom-center-baseline**</span></span>

<span data-ttu-id="1d5cc-129">El texto se delimitará a una posición vertical en el cuadro de texto tal y como se indica en el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-129">The text will be anchored to a vertical position in the textbox as indicated by the attribute value.</span></span> <span data-ttu-id="1d5cc-130">La alineación de un delimitador de texto solo es evidente si [MSO-Fit-Text-to-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) es **false**.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-130">The alignment of a text anchor only becomes evident if [MSO-Fit-Text-To-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) is **False**.</span></span> <span data-ttu-id="1d5cc-131">Este atributo es diferente del atributo de estilo **vertical-align** , que se usa para los Idiomas ideográficos.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-131">This attribute is different from the **Vertical-Align** Style attribute, which is used for ideographic languages.</span></span>

<span data-ttu-id="1d5cc-132">Este atributo lo usa Microsoft Office para almacenar datos en documentos web, pero no se representa en Microsoft Internet Explorer 5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-132">This attribute is used by Microsoft Office to store data in Web documents but does not render in Microsoft Internet Explorer 5 or greater.</span></span>

<span data-ttu-id="1d5cc-133">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="1d5cc-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="1d5cc-134">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="1d5cc-134">**Example**</span></span>

<span data-ttu-id="1d5cc-135">El texto se alinea en la parte inferior del cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="1d5cc-135">The text is aligned to the bottom of the textbox.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox style="v-text-anchor:bottom" id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 