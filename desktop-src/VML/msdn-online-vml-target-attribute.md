---
title: Atributo de destino VML
description: Atributo de destino VML
ms.assetid: 2e1cc002-65c9-4945-8c07-f23dc704d867
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cb4e438cef8d10093aa2788fc1493d9e2dcc75
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676385"
---
# <a name="vml-target-attribute"></a><span data-ttu-id="6af7e-103">Atributo de destino VML</span><span class="sxs-lookup"><span data-stu-id="6af7e-103">VML Target Attribute</span></span>

<span data-ttu-id="6af7e-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6af7e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6af7e-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="6af7e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6af7e-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="6af7e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6af7e-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="6af7e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6af7e-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6af7e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6af7e-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6af7e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6af7e-110">Define un marco o una ventana en la que se muestra una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="6af7e-110">Defines a frame or window that a URL is displayed in.</span></span> <span data-ttu-id="6af7e-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6af7e-111">Read/write.</span></span> <span data-ttu-id="6af7e-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="6af7e-112">**String**.</span></span>

<span data-ttu-id="6af7e-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="6af7e-113">**Applies To**</span></span>

[<span data-ttu-id="6af7e-114">Forma</span><span class="sxs-lookup"><span data-stu-id="6af7e-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="6af7e-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="6af7e-115">**Tag Syntax**</span></span>

<span data-ttu-id="6af7e-116"><v: *Element* target = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="6af7e-116"><v: *element* target=" *expression* "></span></span>

<span data-ttu-id="6af7e-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="6af7e-117">**Remarks**</span></span>

<span data-ttu-id="6af7e-118">El atributo de **destino** es similar al atributo de **destino** HTML estándar de los delimitadores.</span><span class="sxs-lookup"><span data-stu-id="6af7e-118">The **Target** attribute is similar to the standard HTML **Target** attribute of anchors.</span></span>

<span data-ttu-id="6af7e-119">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="6af7e-119">Values include:</span></span>



| <span data-ttu-id="6af7e-120">Value</span><span class="sxs-lookup"><span data-stu-id="6af7e-120">Value</span></span>      | <span data-ttu-id="6af7e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="6af7e-121">Description</span></span>                                                                                                                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6af7e-122">TargetName</span><span class="sxs-lookup"><span data-stu-id="6af7e-122">TargetName</span></span> | <span data-ttu-id="6af7e-123">Cadena que contiene el nombre del marco o la ventana en la que se va a cargar el documento.</span><span class="sxs-lookup"><span data-stu-id="6af7e-123">String containing the name of the frame or window in which to load the document.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="6af7e-124">\_en blanco</span><span class="sxs-lookup"><span data-stu-id="6af7e-124">\_blank</span></span>    | <span data-ttu-id="6af7e-125">Especifica que el documento vinculado se carga en una nueva ventana en blanco.</span><span class="sxs-lookup"><span data-stu-id="6af7e-125">Specifies that the linked document is loaded into a new blank window.</span></span> <span data-ttu-id="6af7e-126">Esta ventana no tiene nombre.</span><span class="sxs-lookup"><span data-stu-id="6af7e-126">This window is not named.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="6af7e-127">\_soporte</span><span class="sxs-lookup"><span data-stu-id="6af7e-127">\_media</span></span>    | <span data-ttu-id="6af7e-128">A partir de Internet Explorer 6 para Windows XP Service Pack 2, el \_ atributo multimedia está obsoleto y ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="6af7e-128">As of Internet Explorer 6 for Windows XP Service Pack 2, the \_media attribute is obsolete and is no longer supported.</span></span> <span data-ttu-id="6af7e-129">En primer lugar, disponible en Internet Explorer 6, este valor especifica que el documento vinculado debe cargarse en la barra multimedia.</span><span class="sxs-lookup"><span data-stu-id="6af7e-129">First available in Internet Explorer 6, this value specified that the linked document should be loaded into the Media Bar.</span></span>                |
| <span data-ttu-id="6af7e-130">\_aérea</span><span class="sxs-lookup"><span data-stu-id="6af7e-130">\_parent</span></span>   | <span data-ttu-id="6af7e-131">Especifica que el documento vinculado se carga en el elemento primario inmediato del documento que contiene el vínculo.</span><span class="sxs-lookup"><span data-stu-id="6af7e-131">Specifies that the linked document is loaded into the immediate parent of the document containing the link.</span></span>                                                                                                                                                      |
| <span data-ttu-id="6af7e-132">\_buscan</span><span class="sxs-lookup"><span data-stu-id="6af7e-132">\_search</span></span>   | <span data-ttu-id="6af7e-133">A partir de Internet Explorer 7 para Windows XP Service Pack 2,: el \_ atributo de búsqueda está obsoleto y ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="6af7e-133">As of Internet Explorer 7 for Windows XP Service Pack 2, : The \_search attribute is obsolete and is no longer supported.</span></span> <span data-ttu-id="6af7e-134">En primer lugar, disponible en Internet Explorer 6, este valor especifica que el documento vinculado se cargará en el panel de búsqueda del explorador.</span><span class="sxs-lookup"><span data-stu-id="6af7e-134">First available in Internet Explorer 6, this value specified that the linked document was to be loaded into the browser's search pane.</span></span> |
| <span data-ttu-id="6af7e-135">\_self</span><span class="sxs-lookup"><span data-stu-id="6af7e-135">\_self</span></span>     | <span data-ttu-id="6af7e-136">Especifica que el documento vinculado se carga en la ventana en la que se hizo clic en el vínculo (la ventana activa).</span><span class="sxs-lookup"><span data-stu-id="6af7e-136">Specifies that the linked document is loaded into the window in which the link was clicked (the active window).</span></span>                                                                                                                                                  |
| <span data-ttu-id="6af7e-137">\_Arriba</span><span class="sxs-lookup"><span data-stu-id="6af7e-137">\_top</span></span>      | <span data-ttu-id="6af7e-138">Especifica que el documento vinculado se carga en la ventana de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="6af7e-138">Specifies that the linked document is loaded into the topmost window.</span></span>                                                                                                                                                                                            |



 

<span data-ttu-id="6af7e-139">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="6af7e-139">*VML Standard Attribute*</span></span>

<span data-ttu-id="6af7e-140">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="6af7e-140">**Example**</span></span>

<span data-ttu-id="6af7e-141">Cuando se hace clic en el rectángulo, el explorador carga la Página principal de Microsoft Corporation en la misma ventana.</span><span class="sxs-lookup"><span data-stu-id="6af7e-141">When the rectangle is clicked, the browser loads the Microsoft Corporation home page in the same window.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com" target="_self"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="6af7e-142">[Ejemplo de atributo de destino](/previous-versions/bb264096(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6af7e-142">[Target Attribute Example](/previous-versions/bb264096(v=vs.85)).</span></span> <span data-ttu-id="6af7e-143">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="6af7e-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 