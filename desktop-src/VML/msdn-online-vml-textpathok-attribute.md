---
title: Atributo TextPathOK de VML
description: Atributo TextPathOK de VML
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06046a4f29c147ef109f0e4670d9965bab77a9fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904628"
---
# <a name="vml-textpathok-attribute"></a><span data-ttu-id="3554e-103">Atributo TextPathOK de VML</span><span class="sxs-lookup"><span data-stu-id="3554e-103">VML TextPathOK Attribute</span></span>

<span data-ttu-id="3554e-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3554e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3554e-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="3554e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3554e-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="3554e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3554e-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="3554e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3554e-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3554e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3554e-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3554e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3554e-110">Determina si se mostrará una ruta de acceso de texto.</span><span class="sxs-lookup"><span data-stu-id="3554e-110">Determines whether a text path will be displayed.</span></span> <span data-ttu-id="3554e-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3554e-111">Read/write.</span></span> <span data-ttu-id="3554e-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="3554e-112">**VgTriState**.</span></span>

<span data-ttu-id="3554e-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="3554e-113">**Applies To**</span></span>

[<span data-ttu-id="3554e-114">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="3554e-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="3554e-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="3554e-115">**Tag Syntax**</span></span>

<span data-ttu-id="3554e-116"><v: *Element* textpathok = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="3554e-116"><v: *element* textpathok=" *expression* "></span></span>

<span data-ttu-id="3554e-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="3554e-117">**Script Syntax**</span></span>

<span data-ttu-id="3554e-118">*elemento* .</span><span class="sxs-lookup"><span data-stu-id="3554e-118">*element* .</span></span> <span data-ttu-id="3554e-119">textpathok = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="3554e-119">textpathok= "*expression*"</span></span>

<span data-ttu-id="3554e-120">*expresión* = de *elemento*.</span><span class="sxs-lookup"><span data-stu-id="3554e-120">*expression*=*element*.</span></span> <span data-ttu-id="3554e-121">textpathok</span><span class="sxs-lookup"><span data-stu-id="3554e-121">textpathok</span></span>

<span data-ttu-id="3554e-122">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="3554e-122">**Remarks**</span></span>

<span data-ttu-id="3554e-123">Si **es false**, la ruta de acceso no puede tener una ruta de acceso de texto.</span><span class="sxs-lookup"><span data-stu-id="3554e-123">If **False**, the path cannot have a text path.</span></span> <span data-ttu-id="3554e-124">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="3554e-124">The default is **False**.</span></span> <span data-ttu-id="3554e-125">Debe tener este atributo establecido en **true** para mostrar texto en una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="3554e-125">You must have this attribute set to **True** to display text on a path.</span></span>

<span data-ttu-id="3554e-126">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="3554e-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="3554e-127">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="3554e-127">**Example**</span></span>

<span data-ttu-id="3554e-128">La forma tiene una ruta de acceso de texto.</span><span class="sxs-lookup"><span data-stu-id="3554e-128">The shape has a text path.</span></span> <span data-ttu-id="3554e-129">El texto "Hola VML" se muestra a lo largo de una curva en forma de sonrisa.</span><span class="sxs-lookup"><span data-stu-id="3554e-129">The text "Hello VML" is displayed along a smile-shaped curve.</span></span>


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 