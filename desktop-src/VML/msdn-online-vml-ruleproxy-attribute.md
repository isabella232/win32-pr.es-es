---
title: Atributo RuleProxy de VML
description: Atributo RuleProxy de VML
ms.assetid: 040e80f8-65b6-491d-812d-421800801374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c76116fc1f31c379f15c3229fcbe70dc7938f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676489"
---
# <a name="vml-ruleproxy-attribute"></a><span data-ttu-id="3888d-103">Atributo RuleProxy de VML</span><span class="sxs-lookup"><span data-stu-id="3888d-103">VML RuleProxy Attribute</span></span>

<span data-ttu-id="3888d-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3888d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3888d-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="3888d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3888d-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="3888d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3888d-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="3888d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3888d-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3888d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3888d-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3888d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3888d-110">Determina si se utilizará un proxy para el motor de reglas.</span><span class="sxs-lookup"><span data-stu-id="3888d-110">Determines whether a proxy for the rules engine will be used.</span></span> <span data-ttu-id="3888d-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3888d-111">Read/write.</span></span> <span data-ttu-id="3888d-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="3888d-112">**VgTriState**.</span></span>

<span data-ttu-id="3888d-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="3888d-113">**Applies To**</span></span>

[<span data-ttu-id="3888d-114">Forma</span><span class="sxs-lookup"><span data-stu-id="3888d-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3888d-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="3888d-115">**Tag Syntax**</span></span>

<span data-ttu-id="3888d-116"><v: *Element* ruleproxy = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="3888d-116"><v: *element* ruleproxy=" *expression* "></span></span>

<span data-ttu-id="3888d-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="3888d-117">**Remarks**</span></span>

<span data-ttu-id="3888d-118">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="3888d-118">The default value is **False**.</span></span> <span data-ttu-id="3888d-119">Si es **true**, se utiliza un proxy.</span><span class="sxs-lookup"><span data-stu-id="3888d-119">If **True**, a proxy is used.</span></span>

<span data-ttu-id="3888d-120">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="3888d-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="3888d-121">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="3888d-121">**Example**</span></span>

<span data-ttu-id="3888d-122">Se usa un proxy para procesar la forma.</span><span class="sxs-lookup"><span data-stu-id="3888d-122">A proxy is used to process the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" ruleproxy="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 