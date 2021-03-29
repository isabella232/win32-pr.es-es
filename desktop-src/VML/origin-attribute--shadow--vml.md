---
title: Atributo de origen (sombra) (VML)
description: Atributo de origen (sombra) (VML)
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481c3df832ec08bc193db021244049fae96d9e34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793647"
---
# <a name="origin-attribute-shadowvml"></a><span data-ttu-id="bf6f9-103">Atributo de origen (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="bf6f9-103">Origin Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="bf6f9-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bf6f9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bf6f9-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="bf6f9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bf6f9-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="bf6f9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bf6f9-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="bf6f9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bf6f9-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bf6f9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bf6f9-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bf6f9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bf6f9-110">Define el centro de la sombra.</span><span class="sxs-lookup"><span data-stu-id="bf6f9-110">Defines the center of the shadow.</span></span> <span data-ttu-id="bf6f9-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bf6f9-111">Read/write.</span></span> <span data-ttu-id="bf6f9-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="bf6f9-112">**VgVector2D**.</span></span>

<span data-ttu-id="bf6f9-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-113">**Applies To**</span></span>

[<span data-ttu-id="bf6f9-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="bf6f9-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="bf6f9-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-115">**Tag Syntax**</span></span>

<span data-ttu-id="bf6f9-116"><v: *elemento* Origin = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="bf6f9-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="bf6f9-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-117">**Script Syntax**</span></span>

<span data-ttu-id="bf6f9-118">*Element* . Origin = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="bf6f9-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="bf6f9-119">*expresión* = de *elemento*. Origin</span><span class="sxs-lookup"><span data-stu-id="bf6f9-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="bf6f9-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-120">**Remarks**</span></span>

<span data-ttu-id="bf6f9-121">Un par de valores fraccionarios de la forma, que van de 50% a-50%.</span><span class="sxs-lookup"><span data-stu-id="bf6f9-121">A pair of fractional values of the shape, ranging from 50% to -50%.</span></span> <span data-ttu-id="bf6f9-122">El valor predeterminado es 0,0.</span><span class="sxs-lookup"><span data-stu-id="bf6f9-122">The default value is 0,0.</span></span>

<span data-ttu-id="bf6f9-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="bf6f9-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="bf6f9-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="bf6f9-124">**Example**</span></span>

<span data-ttu-id="bf6f9-125">La sombra tiene un origen que está por debajo del 20% y un 20% a la derecha del origen de la forma.</span><span class="sxs-lookup"><span data-stu-id="bf6f9-125">The shadow has an origin that is 20% down and 20% to the right of the shape's origin.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 