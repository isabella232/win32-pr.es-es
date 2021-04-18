---
title: Atributo VML XScale
description: Atributo VML XScale
ms.assetid: b876201d-87d1-4795-8f7f-33712a8bf493
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3221ab44cad9eb9f422ce451f618eb8eeba55bcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359030"
---
# <a name="vml-xscale-attribute"></a><span data-ttu-id="93ca8-103">Atributo VML XScale</span><span class="sxs-lookup"><span data-stu-id="93ca8-103">VML XScale Attribute</span></span>

<span data-ttu-id="93ca8-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="93ca8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="93ca8-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="93ca8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="93ca8-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="93ca8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="93ca8-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="93ca8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="93ca8-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="93ca8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="93ca8-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="93ca8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="93ca8-110">Determina si se utilizará un textpath recto en lugar de la ruta de acceso de la forma.</span><span class="sxs-lookup"><span data-stu-id="93ca8-110">Determines whether a straight textpath will be used instead of the shape path.</span></span> <span data-ttu-id="93ca8-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="93ca8-111">Read/write.</span></span> <span data-ttu-id="93ca8-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="93ca8-112">**VgTriState**.</span></span>

<span data-ttu-id="93ca8-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="93ca8-113">**Applies To**</span></span>

[<span data-ttu-id="93ca8-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="93ca8-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="93ca8-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="93ca8-115">**Tag Syntax**</span></span>

<span data-ttu-id="93ca8-116"><v: *Element* style = "XScale: *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="93ca8-116"><v: *element* style="xscale: *expression* "></span></span>

<span data-ttu-id="93ca8-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="93ca8-117">**Script Syntax**</span></span>

<span data-ttu-id="93ca8-118">*Element* . Style. XScale = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="93ca8-118">*element* .style.xscale="*expression*"</span></span>

<span data-ttu-id="93ca8-119">*expresión* = de *Element*. Style. XScale</span><span class="sxs-lookup"><span data-stu-id="93ca8-119">*expression*=*element*.style.xscale</span></span>

<span data-ttu-id="93ca8-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="93ca8-120">**Remarks**</span></span>

<span data-ttu-id="93ca8-121">Si **es true**, el texto se ejecuta a lo largo de apath de izquierda a derecha a lo largo del valor x del límite inferior de la forma.</span><span class="sxs-lookup"><span data-stu-id="93ca8-121">If **True**, the text runs along apath from left to right along the x value of the lower boundary of the shape.</span></span> <span data-ttu-id="93ca8-122">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="93ca8-122">The default value is **False**.</span></span>

<span data-ttu-id="93ca8-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="93ca8-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="93ca8-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="93ca8-124">**Example**</span></span>

<span data-ttu-id="93ca8-125">El texto aparecerá como si se dibujara en una línea horizontal, aunque la ruta de la forma sea una diagonal.</span><span class="sxs-lookup"><span data-stu-id="93ca8-125">The text will appear as if it were drawn on a horizontal line, even though the shape path is a diagonal.</span></span>


```HTML
   <v:line from="100 100" to="400 400">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="xscale:true;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 