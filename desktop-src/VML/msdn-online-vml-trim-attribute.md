---
title: Atributo Trim de VML
description: Atributo Trim de VML
ms.assetid: c8038361-00bd-4787-9759-506a8a47b19a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f7aa2ce17d5b2b8df772954cee323e3d5ea2db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904785"
---
# <a name="vml-trim-attribute"></a><span data-ttu-id="9736b-103">Atributo Trim de VML</span><span class="sxs-lookup"><span data-stu-id="9736b-103">VML Trim Attribute</span></span>

<span data-ttu-id="9736b-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9736b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9736b-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="9736b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9736b-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="9736b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9736b-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="9736b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9736b-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9736b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9736b-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9736b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9736b-110">Determina si el espacio adicional se quita por encima y por debajo del texto.</span><span class="sxs-lookup"><span data-stu-id="9736b-110">Determines whether extra space is removed above and below the text.</span></span> <span data-ttu-id="9736b-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9736b-111">Read/write.</span></span> <span data-ttu-id="9736b-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="9736b-112">**VgTriState**.</span></span>

<span data-ttu-id="9736b-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="9736b-113">**Applies To**</span></span>

[<span data-ttu-id="9736b-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="9736b-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="9736b-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="9736b-115">**Tag Syntax**</span></span>

<span data-ttu-id="9736b-116"><v: *Element* style = "Trim: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="9736b-116"><v: *element* style="trim: *expression* "></span></span>

<span data-ttu-id="9736b-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="9736b-117">**Script Syntax**</span></span>

<span data-ttu-id="9736b-118">*Element* . Style. Trim = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="9736b-118">*element* .style.trim="*expression*"</span></span>

<span data-ttu-id="9736b-119">*expresión* = de *Element*. Style. Trim</span><span class="sxs-lookup"><span data-stu-id="9736b-119">*expression*=*element*.style.trim</span></span>

<span data-ttu-id="9736b-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="9736b-120">**Remarks**</span></span>

<span data-ttu-id="9736b-121">Si es **true**, se quita el espacio reservado para ascendentes y descendentes.</span><span class="sxs-lookup"><span data-stu-id="9736b-121">If **True**, space reserved for ascenders and descenders is removed.</span></span> <span data-ttu-id="9736b-122">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="9736b-122">The default value is **False**.</span></span>

<span data-ttu-id="9736b-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="9736b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="9736b-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="9736b-124">**Example**</span></span>

<span data-ttu-id="9736b-125">Se recorta el espacio adicional por encima y debajo de.</span><span class="sxs-lookup"><span data-stu-id="9736b-125">The extra space above and below is trimmed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="trim:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 