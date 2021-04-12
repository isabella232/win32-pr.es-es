---
title: Atributo FitPath de VML
description: Atributo FitPath de VML
ms.assetid: f15775ed-f7b7-45d9-83ed-e307daf7451b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1805e59a50c63248ed936f6a849869057a34a6e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271367"
---
# <a name="vml-fitpath-attribute"></a><span data-ttu-id="4757c-103">Atributo FitPath de VML</span><span class="sxs-lookup"><span data-stu-id="4757c-103">VML FitPath Attribute</span></span>

<span data-ttu-id="4757c-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4757c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4757c-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="4757c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4757c-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="4757c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4757c-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="4757c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4757c-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4757c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4757c-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4757c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4757c-110">Define si el texto se ajusta a la ruta de acceso de una forma.</span><span class="sxs-lookup"><span data-stu-id="4757c-110">Defines whether the text fits the path of a shape.</span></span> <span data-ttu-id="4757c-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4757c-111">Read/write.</span></span> <span data-ttu-id="4757c-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="4757c-112">**VgTriState**.</span></span>

<span data-ttu-id="4757c-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="4757c-113">**Applies To**</span></span>

[<span data-ttu-id="4757c-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="4757c-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="4757c-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="4757c-115">**Tag Syntax**</span></span>

<span data-ttu-id="4757c-116"><v: *Element* fitpath = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="4757c-116"><v: *element* fitpath=" *expression* "></span></span>

<span data-ttu-id="4757c-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="4757c-117">**Script Syntax**</span></span>

<span data-ttu-id="4757c-118">*Element* . fitpath = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="4757c-118">*element* .fitpath="*expression*"</span></span>

<span data-ttu-id="4757c-119">*expresión* = de *elemento*. fitpath</span><span class="sxs-lookup"><span data-stu-id="4757c-119">*expression*=*element*.fitpath</span></span>

<span data-ttu-id="4757c-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="4757c-120">**Remarks**</span></span>

<span data-ttu-id="4757c-121">Si **es true**, ajusta el tamaño del texto para rellenar la ruta de acceso en la que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="4757c-121">If **True**, sizes the text to fill the path it lies out on.</span></span> <span data-ttu-id="4757c-122">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="4757c-122">The default is **False**.</span></span>

<span data-ttu-id="4757c-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="4757c-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="4757c-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="4757c-124">**Example**</span></span>

<span data-ttu-id="4757c-125">El texto se ajustará a la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="4757c-125">The text will fit the path.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitpath="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 