---
title: Atributo ReGroupID de VML
description: Atributo ReGroupID de VML
ms.assetid: 2fbcc8c5-6e31-4301-9fb8-c2618bb17a1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384703d3fc5675013de09c4e3b5dec7505cf4164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420829"
---
# <a name="vml-regroupid-attribute"></a><span data-ttu-id="664a4-103">Atributo ReGroupID de VML</span><span class="sxs-lookup"><span data-stu-id="664a4-103">VML ReGroupID Attribute</span></span>

<span data-ttu-id="664a4-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="664a4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="664a4-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="664a4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="664a4-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="664a4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="664a4-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="664a4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="664a4-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="664a4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="664a4-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="664a4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="664a4-110">Define un grupo anterior para una forma.</span><span class="sxs-lookup"><span data-stu-id="664a4-110">Defines a previous group for a shape.</span></span> <span data-ttu-id="664a4-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="664a4-111">Read/write.</span></span> <span data-ttu-id="664a4-112">**VgInteger**.</span><span class="sxs-lookup"><span data-stu-id="664a4-112">**VgInteger**.</span></span>

<span data-ttu-id="664a4-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="664a4-113">**Applies To**</span></span>

[<span data-ttu-id="664a4-114">Forma</span><span class="sxs-lookup"><span data-stu-id="664a4-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="664a4-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="664a4-115">**Tag Syntax**</span></span>

<span data-ttu-id="664a4-116"><v: *Element* o:regroupid = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="664a4-116"><v: *element* o:regroupid=" *expression* "></span></span>

<span data-ttu-id="664a4-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="664a4-117">**Remarks**</span></span>

<span data-ttu-id="664a4-118">Se usa un número de identificación para identificar grupos de formas que ya no están agrupadas.</span><span class="sxs-lookup"><span data-stu-id="664a4-118">An ID number is used to identify groups of shapes that are no longer grouped.</span></span> <span data-ttu-id="664a4-119">Permite que las formas se reagrupen mediante programación.</span><span class="sxs-lookup"><span data-stu-id="664a4-119">Allows shapes to be regrouped programmatically.</span></span>

<span data-ttu-id="664a4-120">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="664a4-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="664a4-121">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="664a4-121">**Example**</span></span>

<span data-ttu-id="664a4-122">La forma formaba parte de un grupo indicado por el ID. de grupo 040754.</span><span class="sxs-lookup"><span data-stu-id="664a4-122">The shape was part of a group denoted by the group ID 040754.</span></span>


```HTML
   <v:shape id="rect01" ReGroupID="040754"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 