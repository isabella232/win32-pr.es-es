---
title: Atributo Focus de VML
description: Atributo Focus de VML
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062b2900c2f980c9a1433e5e790a34d463def9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078347"
---
# <a name="vml-focus-attribute"></a><span data-ttu-id="a179d-103">Atributo Focus de VML</span><span class="sxs-lookup"><span data-stu-id="a179d-103">VML Focus Attribute</span></span>

<span data-ttu-id="a179d-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a179d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a179d-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="a179d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a179d-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="a179d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a179d-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="a179d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a179d-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a179d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a179d-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a179d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a179d-110">Define el centro de un relleno de degradado lineal.</span><span class="sxs-lookup"><span data-stu-id="a179d-110">Defines the center of a linear gradient fill.</span></span> <span data-ttu-id="a179d-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a179d-111">Read/write.</span></span> <span data-ttu-id="a179d-112">**VgFraction**.</span><span class="sxs-lookup"><span data-stu-id="a179d-112">**VgFraction**.</span></span>

<span data-ttu-id="a179d-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="a179d-113">**Applies To**</span></span>

[<span data-ttu-id="a179d-114">Fill</span><span class="sxs-lookup"><span data-stu-id="a179d-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="a179d-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="a179d-115">**Tag Syntax**</span></span>

<span data-ttu-id="a179d-116"><v: *elemento* Focus = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="a179d-116"><v: *element* focus=" *expression* "></span></span>

<span data-ttu-id="a179d-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="a179d-117">**Script Syntax**</span></span>

<span data-ttu-id="a179d-118">*Element* . Focus = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="a179d-118">*element* .focus="*expression*"</span></span>

<span data-ttu-id="a179d-119">*expresión* = de *elemento*. Focus</span><span class="sxs-lookup"><span data-stu-id="a179d-119">*expression*=*element*.focus</span></span>

<span data-ttu-id="a179d-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="a179d-120">**Remarks**</span></span>

<span data-ttu-id="a179d-121">Define la posición inicial del centro de la mezcla.</span><span class="sxs-lookup"><span data-stu-id="a179d-121">Defines the center starting position of the blend.</span></span> <span data-ttu-id="a179d-122">Los valores van del 100% a-100%.</span><span class="sxs-lookup"><span data-stu-id="a179d-122">Values range from 100% to -100%.</span></span> <span data-ttu-id="a179d-123">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="a179d-123">The default value is 0.</span></span> <span data-ttu-id="a179d-124">Un valor de 100% (o-100%) desplazará el foco para que la dirección de la mezcla se revierta (en efecto, el **color** y el **color2**).</span><span class="sxs-lookup"><span data-stu-id="a179d-124">A value of 100% (or -100%) will shift the focus so that the direction of the blend will reverse (in effect reversing **Color** and **Color2**).</span></span> <span data-ttu-id="a179d-125">Un valor de 50% cambiará la mezcla para que el **color** esté en ambos extremos y el **color2** esté en el centro.</span><span class="sxs-lookup"><span data-stu-id="a179d-125">A value of 50% will change the blend so that **Color** is at both ends and **Color2** is in the middle.</span></span> <span data-ttu-id="a179d-126">Un valor de-50% cambiará la mezcla para que **color2** esté en ambos extremos y el **color** esté en el medio.</span><span class="sxs-lookup"><span data-stu-id="a179d-126">A value of -50% will change the blend so that **Color2** is at both ends and **Color** is in the middle.</span></span>

<span data-ttu-id="a179d-127">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="a179d-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="a179d-128">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="a179d-128">**Example**</span></span>

<span data-ttu-id="a179d-129">El foco de degradado del relleno se desplaza para que el rojo (**color**) sea una banda en el centro de la forma y que la parte superior e inferior sean azules (**color2**).</span><span class="sxs-lookup"><span data-stu-id="a179d-129">The gradient focus of the fill is shifted so that red (**Color**) will be a band in the center of the shape and that the top and bottom will be blue (**Color2**).</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 