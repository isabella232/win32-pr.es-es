---
title: Atributo VML V
description: Atributo VML V
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690518e998163f7e47fb326b3037e6a4ec397e8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149369"
---
# <a name="vml-v-attribute"></a><span data-ttu-id="ae146-103">Atributo VML V</span><span class="sxs-lookup"><span data-stu-id="ae146-103">VML V Attribute</span></span>

<span data-ttu-id="ae146-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ae146-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ae146-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="ae146-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ae146-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="ae146-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ae146-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="ae146-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ae146-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ae146-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ae146-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ae146-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ae146-110">Define los comandos que componen una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="ae146-110">Defines the commands that make up a path.</span></span> <span data-ttu-id="ae146-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ae146-111">Read/write.</span></span> <span data-ttu-id="ae146-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="ae146-112">**String**.</span></span>

<span data-ttu-id="ae146-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="ae146-113">**Applies To**</span></span>

[<span data-ttu-id="ae146-114">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="ae146-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="ae146-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="ae146-115">**Tag Syntax**</span></span>

<span data-ttu-id="ae146-116"><v: *elemento* v = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="ae146-116"><v: *element* v=" *expression* "></span></span>

<span data-ttu-id="ae146-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="ae146-117">**Script Syntax**</span></span>

<span data-ttu-id="ae146-118">*Element* . v = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="ae146-118">*element* .v="*expression*"</span></span>

<span data-ttu-id="ae146-119">*expresión* = de *elemento*. v</span><span class="sxs-lookup"><span data-stu-id="ae146-119">*expression*=*element*.v</span></span>

<span data-ttu-id="ae146-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="ae146-120">**Remarks**</span></span>

<span data-ttu-id="ae146-121">Invalida el atributo de **ruta de acceso** de una forma.</span><span class="sxs-lookup"><span data-stu-id="ae146-121">Overrides the **Path** attribute of a shape.</span></span> <span data-ttu-id="ae146-122">Las coordenadas pueden ser números fijos, números relativos o referencias a fórmulas (usando el formato " @n ", donde n es un número de fórmula; por ejemplo, " @2 " hace referencia a la segunda fórmula de la matriz de fórmulas).</span><span class="sxs-lookup"><span data-stu-id="ae146-122">Coordinates can be fixed numbers, relative numbers, or references to formulas (by using the format of "@n" where n is a formula number; for example, "@2" refers to the second formula in the formula array).</span></span>

<span data-ttu-id="ae146-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="ae146-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="ae146-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="ae146-124">**Example**</span></span>

<span data-ttu-id="ae146-125">Se crea un rectángulo mediante el atributo **V** .</span><span class="sxs-lookup"><span data-stu-id="ae146-125">A rectangle is created using the **V** attribute.</span></span> <span data-ttu-id="ae146-126">Tenga en cuenta que se usa una letra minúscula L (comando **lineTo** ) después del primer conjunto de coordenadas delimitadas por comas.</span><span class="sxs-lookup"><span data-stu-id="ae146-126">Note that a lowercase letter L (**lineto** command) is used after the first set of comma-delimited coordinates.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 