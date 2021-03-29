---
title: Atributo ForceDash de VML
description: Atributo ForceDash de VML
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bcec4a694a6449412aa07ec69aa9a817aa917c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078062"
---
# <a name="vml-forcedash-attribute"></a><span data-ttu-id="b39f8-103">Atributo ForceDash de VML</span><span class="sxs-lookup"><span data-stu-id="b39f8-103">VML ForceDash Attribute</span></span>

<span data-ttu-id="b39f8-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b39f8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b39f8-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="b39f8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b39f8-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="b39f8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b39f8-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="b39f8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b39f8-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b39f8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b39f8-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b39f8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b39f8-110">Determina si un contorno discontinuo se usa para dibujar una forma cuando una forma no tiene línea ni relleno.</span><span class="sxs-lookup"><span data-stu-id="b39f8-110">Determines whether a dashed outline is used to draw a shape when a shape has no line or fill.</span></span> <span data-ttu-id="b39f8-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b39f8-111">Read/write.</span></span> <span data-ttu-id="b39f8-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="b39f8-112">**VgTriState**.</span></span>

<span data-ttu-id="b39f8-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="b39f8-113">**Applies To**</span></span>

[<span data-ttu-id="b39f8-114">Forma</span><span class="sxs-lookup"><span data-stu-id="b39f8-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b39f8-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="b39f8-115">**Tag Syntax**</span></span>

<span data-ttu-id="b39f8-116"><v: *Element* o:forcedash = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="b39f8-116"><v: *element* o:forcedash=" *expression* "></span></span>

<span data-ttu-id="b39f8-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="b39f8-117">**Remarks**</span></span>

<span data-ttu-id="b39f8-118">Lo usan los marcadores de posición de Microsoft PowerPoint para dibujar un contorno discontinuo cuando no hay ninguna línea y ningún relleno para una forma.</span><span class="sxs-lookup"><span data-stu-id="b39f8-118">Used by Microsoft PowerPoint placeholders to draw a dashed outline when there is no line and no fill for a shape.</span></span> <span data-ttu-id="b39f8-119">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="b39f8-119">Default is **False**.</span></span> <span data-ttu-id="b39f8-120">Si **es true**, se utilizará un contorno discontinuo para indicar un marcador de posición.</span><span class="sxs-lookup"><span data-stu-id="b39f8-120">If **True**, a dashed outline will be used to indicate a placeholder.</span></span>

<span data-ttu-id="b39f8-121">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="b39f8-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="b39f8-122">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b39f8-122">**Example**</span></span>

<span data-ttu-id="b39f8-123">Se utilizará una línea discontinua para representar la forma si no hay ninguna línea o relleno.</span><span class="sxs-lookup"><span data-stu-id="b39f8-123">A dashed line will be used to render the shape if there is no line or fill.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 