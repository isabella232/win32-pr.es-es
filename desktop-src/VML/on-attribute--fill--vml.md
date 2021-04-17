---
title: On (atributo) (relleno) (VML)
description: On (atributo) (relleno) (VML)
ms.assetid: 9b7d42e5-4fd9-402d-8d1f-af01f6577475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e25e805be23b4678b1be828b711365a8624f10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695724"
---
# <a name="on-attribute-fillvml"></a><span data-ttu-id="8d95e-103">On (atributo) (relleno) (VML)</span><span class="sxs-lookup"><span data-stu-id="8d95e-103">On Attribute (Fill)(VML)</span></span>

<span data-ttu-id="8d95e-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8d95e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8d95e-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="8d95e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8d95e-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="8d95e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8d95e-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="8d95e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8d95e-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8d95e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8d95e-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8d95e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8d95e-110">Determina si se mostrará el relleno.</span><span class="sxs-lookup"><span data-stu-id="8d95e-110">Determines whether the fill will be displayed.</span></span> <span data-ttu-id="8d95e-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8d95e-111">Read/write.</span></span> <span data-ttu-id="8d95e-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="8d95e-112">**VgTriState**.</span></span>

<span data-ttu-id="8d95e-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="8d95e-113">**Applies To**</span></span>

[<span data-ttu-id="8d95e-114">Fill</span><span class="sxs-lookup"><span data-stu-id="8d95e-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="8d95e-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="8d95e-115">**Tag Syntax**</span></span>

<span data-ttu-id="8d95e-116"><v: *Element* on = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="8d95e-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="8d95e-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="8d95e-117">**Script Syntax**</span></span>

<span data-ttu-id="8d95e-118">*Element* . on = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="8d95e-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="8d95e-119">*expresión* = de *elemento*. on</span><span class="sxs-lookup"><span data-stu-id="8d95e-119">*expression*=*element*.on</span></span>

<span data-ttu-id="8d95e-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="8d95e-120">**Remarks**</span></span>

<span data-ttu-id="8d95e-121">Si es **false**, no se muestra el relleno.</span><span class="sxs-lookup"><span data-stu-id="8d95e-121">If **False**, the fill is not displayed.</span></span> <span data-ttu-id="8d95e-122">El valor predeterminado es **True**.</span><span class="sxs-lookup"><span data-stu-id="8d95e-122">The default is **True**.</span></span>

<span data-ttu-id="8d95e-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="8d95e-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="8d95e-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="8d95e-124">**Example**</span></span>

<span data-ttu-id="8d95e-125">Aunque el relleno se define como rojo, no se muestra.</span><span class="sxs-lookup"><span data-stu-id="8d95e-125">Even though the fill is defined to be red, it is not displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" on="False"/>
   </v:shape>
```



 

 