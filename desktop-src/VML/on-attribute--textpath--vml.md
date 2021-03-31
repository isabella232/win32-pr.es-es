---
title: On (atributo) (TextPath) (VML)
description: On (atributo) (TextPath) (VML)
ms.assetid: b4a88473-6d5f-42b3-afd6-86f602c83724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ae791b1144046a1c29e92d11663cd15d696bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533477"
---
# <a name="on-attribute-textpathvml"></a><span data-ttu-id="a233b-103">On (atributo) (TextPath) (VML)</span><span class="sxs-lookup"><span data-stu-id="a233b-103">On Attribute (TextPath)(VML)</span></span>

<span data-ttu-id="a233b-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a233b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a233b-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="a233b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a233b-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="a233b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a233b-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="a233b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a233b-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a233b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a233b-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a233b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a233b-110">Define si se muestra el texto.</span><span class="sxs-lookup"><span data-stu-id="a233b-110">Defines whether the text is displayed.</span></span> <span data-ttu-id="a233b-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a233b-111">Read/write.</span></span> <span data-ttu-id="a233b-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="a233b-112">**VgTriState**.</span></span>

<span data-ttu-id="a233b-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="a233b-113">**Applies To**</span></span>

[<span data-ttu-id="a233b-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="a233b-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="a233b-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="a233b-115">**Tag Syntax**</span></span>

<span data-ttu-id="a233b-116"><v: *Element* on = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="a233b-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="a233b-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="a233b-117">**Script Syntax**</span></span>

<span data-ttu-id="a233b-118">*Element* . on = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="a233b-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="a233b-119">*expresión* = de *elemento*. on</span><span class="sxs-lookup"><span data-stu-id="a233b-119">*expression*=*element*.on</span></span>

<span data-ttu-id="a233b-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="a233b-120">**Remarks**</span></span>

<span data-ttu-id="a233b-121">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="a233b-121">Default is **False**.</span></span> <span data-ttu-id="a233b-122">Este valor debe establecerse en **true** para mostrar el texto en una ruta de acceso de texto.</span><span class="sxs-lookup"><span data-stu-id="a233b-122">This value must be set to **True** to display text on a text path.</span></span>

<span data-ttu-id="a233b-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="a233b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="a233b-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="a233b-124">**Example**</span></span>

<span data-ttu-id="a233b-125">Se mostrará el texto de la ruta de acceso del texto.</span><span class="sxs-lookup"><span data-stu-id="a233b-125">The text on the text path will be displayed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 