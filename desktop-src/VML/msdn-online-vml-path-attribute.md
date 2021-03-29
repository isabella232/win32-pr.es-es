---
title: Atributo de ruta de acceso VML
description: Atributo de ruta de acceso VML
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43e453e982327549475de4643cc0ad21bc0b4db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904805"
---
# <a name="vml-path-attribute"></a><span data-ttu-id="f58ad-103">Atributo de ruta de acceso VML</span><span class="sxs-lookup"><span data-stu-id="f58ad-103">VML Path Attribute</span></span>

<span data-ttu-id="f58ad-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f58ad-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f58ad-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="f58ad-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f58ad-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="f58ad-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f58ad-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="f58ad-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f58ad-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f58ad-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f58ad-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f58ad-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f58ad-110">Especifica la línea que constituye los bordes de una forma.</span><span class="sxs-lookup"><span data-stu-id="f58ad-110">Specifies the line that makes up the edges of a shape.</span></span> <span data-ttu-id="f58ad-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f58ad-111">Read/write.</span></span> <span data-ttu-id="f58ad-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="f58ad-112">**String**.</span></span>

<span data-ttu-id="f58ad-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="f58ad-113">**Applies To**</span></span>

[<span data-ttu-id="f58ad-114">Forma</span><span class="sxs-lookup"><span data-stu-id="f58ad-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="f58ad-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="f58ad-115">**Tag Syntax**</span></span>

<span data-ttu-id="f58ad-116"><v: *elemento* path = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="f58ad-116"><v: *element* path=" *expression* "></span></span>

<span data-ttu-id="f58ad-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="f58ad-117">**Script Syntax**</span></span>

<span data-ttu-id="f58ad-118">*Element* . Path = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="f58ad-118">*element* .path="*expression*"</span></span>

<span data-ttu-id="f58ad-119">*expresión* = de *Element*. Path</span><span class="sxs-lookup"><span data-stu-id="f58ad-119">*expression*=*element*.path</span></span>

<span data-ttu-id="f58ad-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="f58ad-120">**Remarks**</span></span>

<span data-ttu-id="f58ad-121">Si una forma contiene el elemento [path](msdn-online-vml-path-element.md) , los comandos path del elemento path tienen prioridad sobre el valor del atributo Shape.</span><span class="sxs-lookup"><span data-stu-id="f58ad-121">If a shape contains the [Path](msdn-online-vml-path-element.md) element, the path commands of the Path element take precedence over the shape attribute value.</span></span> <span data-ttu-id="f58ad-122">Vea el tema del elemento path para obtener más información sobre el conjunto de comandos que se usa para las rutas de **acceso** .</span><span class="sxs-lookup"><span data-stu-id="f58ad-122">See the **Path** element topic for details on the command set used for paths.</span></span>

<span data-ttu-id="f58ad-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="f58ad-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="f58ad-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="f58ad-124">**Example**</span></span>

<span data-ttu-id="f58ad-125">Una ruta de acceso cuadrada cerrada se define en la cadena del atributo path.</span><span class="sxs-lookup"><span data-stu-id="f58ad-125">A closed square path is defined in the string of the path attribute.</span></span> <span data-ttu-id="f58ad-126">Un punto inicial se define con `m` (se usa para el comando **moveTo** ) en 1, 1 y se dibuja una línea con `l` (la letra "L" usada para la **línea** de comandos) desde la posición inicial (1,1) hasta los otros tres puntos (en orden): 1.200; 200.200; 200, 1.</span><span class="sxs-lookup"><span data-stu-id="f58ad-126">An initial point is defined with `m` (used for the **moveto** command) at 1,1 and a line is drawn with `l` (the letter "L" used for the command **lineto**) from the starting position (1,1) to the other three points (in order): 1,200; 200,200; 200,1.</span></span> <span data-ttu-id="f58ad-127">La línea se cierra con `x` (**Close**) y termina con `e` (**End**).</span><span class="sxs-lookup"><span data-stu-id="f58ad-127">The line is closed with `x` (**close**) and ended with `e` (**end**).</span></span> <span data-ttu-id="f58ad-128">Tenga en cuenta que las coordenadas se proporcionan en el espacio de coordenadas relativo y que el **ancho** y el **alto** determinan el tamaño real.</span><span class="sxs-lookup"><span data-stu-id="f58ad-128">Note that coordinates are given in the relative coordinate space and that the real size is determined by the **width** and **height**.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="f58ad-129">[Ejemplo de atributo de ruta de acceso](/previous-versions/bb264089(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f58ad-129">[Path Attribute Example](/previous-versions/bb264089(v=vs.85)).</span></span> <span data-ttu-id="f58ad-130">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="f58ad-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 