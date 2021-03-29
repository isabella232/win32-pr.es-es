---
title: Atributo RuleInitiator de VML
description: Atributo RuleInitiator de VML
ms.assetid: 2c9b1131-b088-4b70-b132-bdb4296433ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80201ad80fbb8dc5bbff2e8ed4e0b8db2863fdad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359381"
---
# <a name="vml-ruleinitiator-attribute"></a><span data-ttu-id="edd9d-103">Atributo RuleInitiator de VML</span><span class="sxs-lookup"><span data-stu-id="edd9d-103">VML RuleInitiator Attribute</span></span>

<span data-ttu-id="edd9d-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="edd9d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="edd9d-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="edd9d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="edd9d-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="edd9d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="edd9d-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="edd9d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="edd9d-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="edd9d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="edd9d-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="edd9d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="edd9d-110">Determina si se utilizará un motor de reglas.</span><span class="sxs-lookup"><span data-stu-id="edd9d-110">Determines whether a rules engine will be used.</span></span> <span data-ttu-id="edd9d-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="edd9d-111">Read/write.</span></span> <span data-ttu-id="edd9d-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="edd9d-112">**VgTriState**.</span></span>

<span data-ttu-id="edd9d-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="edd9d-113">**Applies To**</span></span>

[<span data-ttu-id="edd9d-114">Forma</span><span class="sxs-lookup"><span data-stu-id="edd9d-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="edd9d-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="edd9d-115">**Tag Syntax**</span></span>

<span data-ttu-id="edd9d-116"><v: *Element* o:ruleinitiator = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="edd9d-116"><v: *element* o:ruleinitiator=" *expression* "></span></span>

<span data-ttu-id="edd9d-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="edd9d-117">**Remarks**</span></span>

<span data-ttu-id="edd9d-118">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="edd9d-118">The default value is **False**.</span></span> <span data-ttu-id="edd9d-119">Si el valor es **true**, se utiliza un motor de reglas.</span><span class="sxs-lookup"><span data-stu-id="edd9d-119">If the value is **True**, a rules engine is used.</span></span>

<span data-ttu-id="edd9d-120">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="edd9d-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="edd9d-121">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="edd9d-121">**Example**</span></span>

<span data-ttu-id="edd9d-122">Un motor de reglas procesará la forma.</span><span class="sxs-lookup"><span data-stu-id="edd9d-122">The shape will be processed by a rules engine.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" rulesinitiator="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 