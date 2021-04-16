---
title: Título (forma) (VML)
description: Título (forma) (VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075b1cf078617abd3486ba55008794e1342efa63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488239"
---
# <a name="title-attribute-shapevml"></a><span data-ttu-id="81f28-103">Título (forma) (VML)</span><span class="sxs-lookup"><span data-stu-id="81f28-103">Title Attribute (Shape)(VML)</span></span>

<span data-ttu-id="81f28-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="81f28-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="81f28-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="81f28-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="81f28-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="81f28-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="81f28-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="81f28-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="81f28-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="81f28-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="81f28-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="81f28-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="81f28-110">Define el texto que se muestra cuando el puntero del mouse se mueve sobre la forma.</span><span class="sxs-lookup"><span data-stu-id="81f28-110">Defines the text displayed when the mouse pointer moves over the shape.</span></span> <span data-ttu-id="81f28-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="81f28-111">Read/write.</span></span> <span data-ttu-id="81f28-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="81f28-112">**String**.</span></span>

<span data-ttu-id="81f28-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="81f28-113">**Applies To**</span></span>

[<span data-ttu-id="81f28-114">Forma</span><span class="sxs-lookup"><span data-stu-id="81f28-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="81f28-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="81f28-115">**Tag Syntax**</span></span>

<span data-ttu-id="81f28-116"><v: *elemento* title = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="81f28-116"><v: *element* title=" *expression* "></span></span>

<span data-ttu-id="81f28-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="81f28-117">**Script Syntax**</span></span>

<span data-ttu-id="81f28-118">*Element* . title = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="81f28-118">*element* .title="*expression*"</span></span>

<span data-ttu-id="81f28-119">*expresión* = de *elemento*. title</span><span class="sxs-lookup"><span data-stu-id="81f28-119">*expression*=*element*.title</span></span>

<span data-ttu-id="81f28-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="81f28-120">**Remarks**</span></span>

<span data-ttu-id="81f28-121">El atributo **title** es similar al atributo **title** de HTML estándar.</span><span class="sxs-lookup"><span data-stu-id="81f28-121">The **Title** attribute is similar to the standard HTML **Title** attribute.</span></span> <span data-ttu-id="81f28-122">El comportamiento de un título es similar a la información sobre herramientas de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="81f28-122">The behavior of a title is similar to a Microsoft Windows ToolTip.</span></span>

<span data-ttu-id="81f28-123">**Atributo estándar de VML**</span><span class="sxs-lookup"><span data-stu-id="81f28-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="81f28-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="81f28-124">**Example**</span></span>

<span data-ttu-id="81f28-125">El título de la forma es "visualización de la información sobre herramientas" y aparecerá cuando el puntero del mouse se mueva sobre la forma.</span><span class="sxs-lookup"><span data-stu-id="81f28-125">The title of the shape is "ToolTip display" and will appear when the mouse pointer moves over the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="81f28-126">[Ejemplo de atributo de título](/previous-versions/bb264097(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81f28-126">[Title Attribute Example](/previous-versions/bb264097(v=vs.85)).</span></span> <span data-ttu-id="81f28-127">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="81f28-127">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 