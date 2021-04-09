---
title: Atributo gamma de VML
description: Atributo gamma de VML
ms.assetid: 47a4d10e-f5ef-457b-92dd-bce5dae59b1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b74c80739d694038601588eee4c8ad7ed90923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149441"
---
# <a name="vml-gamma-attribute"></a><span data-ttu-id="0c5bc-103">Atributo gamma de VML</span><span class="sxs-lookup"><span data-stu-id="0c5bc-103">VML Gamma Attribute</span></span>

<span data-ttu-id="0c5bc-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0c5bc-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0c5bc-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0c5bc-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0c5bc-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0c5bc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0c5bc-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0c5bc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0c5bc-110">Define la cantidad de contraste de una imagen.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-110">Defines the amount of contrast for an image.</span></span> <span data-ttu-id="0c5bc-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0c5bc-111">Read/write.</span></span> <span data-ttu-id="0c5bc-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-112">**VgNumber**.</span></span>

<span data-ttu-id="0c5bc-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="0c5bc-113">**Applies To**</span></span>

[<span data-ttu-id="0c5bc-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="0c5bc-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="0c5bc-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="0c5bc-115">**Tag Syntax**</span></span>

<span data-ttu-id="0c5bc-116"><v: *elemento* gamma = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="0c5bc-116"><v: *element* gamma=" *expression* "></span></span>

<span data-ttu-id="0c5bc-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="0c5bc-117">**Script Syntax**</span></span>

<span data-ttu-id="0c5bc-118">*Element* . gamma = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="0c5bc-118">*element* .gamma="*expression*"</span></span>

<span data-ttu-id="0c5bc-119">*expresión* = de *Element*. gamma</span><span class="sxs-lookup"><span data-stu-id="0c5bc-119">*expression*=*element*.gamma</span></span>

<span data-ttu-id="0c5bc-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="0c5bc-120">**Remarks**</span></span>

<span data-ttu-id="0c5bc-121">Al reducir el valor gamma inferior a 1 se modifica una imagen para que sea más contrastada, mientras que los valores mayores que 1 disminuyen el contraste.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-121">Decreasing the gamma below 1 modifies an image to make it more contrasty, while values greater than 1 decrease the contrast.</span></span> <span data-ttu-id="0c5bc-122">Los valores útiles son de 0,3 a aproximadamente 3.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-122">Useful values are from 0.3 to about 3.</span></span> <span data-ttu-id="0c5bc-123">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="0c5bc-123">The default value is 0.</span></span>

<span data-ttu-id="0c5bc-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="0c5bc-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="0c5bc-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="0c5bc-125">**Example**</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gamma=".7" src="gamera.jpg"/>
   </v:shape>
```



 

 