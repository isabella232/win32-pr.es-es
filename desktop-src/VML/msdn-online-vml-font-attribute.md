---
title: Atributo de fuente VML
description: Atributo de fuente VML
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bace73b90cac7519ea6abacb73c80506c655e133
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695746"
---
# <a name="vml-font-attribute"></a><span data-ttu-id="ec531-103">Atributo de fuente VML</span><span class="sxs-lookup"><span data-stu-id="ec531-103">VML Font Attribute</span></span>

<span data-ttu-id="ec531-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ec531-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ec531-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="ec531-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ec531-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="ec531-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ec531-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="ec531-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ec531-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ec531-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ec531-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ec531-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ec531-110">Especifica un valor compuesto de atributos de fuente.</span><span class="sxs-lookup"><span data-stu-id="ec531-110">Specifies a compound value of font attributes.</span></span> <span data-ttu-id="ec531-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ec531-111">Read/write.</span></span> <span data-ttu-id="ec531-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="ec531-112">**String**.</span></span>

<span data-ttu-id="ec531-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="ec531-113">**Applies To**</span></span>

[<span data-ttu-id="ec531-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="ec531-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="ec531-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="ec531-115">**Tag Syntax**</span></span>

<span data-ttu-id="ec531-116"><v: *Element* style = "Font: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ec531-116"><v: *element* style="font: *expression* "></span></span>

<span data-ttu-id="ec531-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="ec531-117">**Script Syntax**</span></span>

<span data-ttu-id="ec531-118">*Element* . Style. Font = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="ec531-118">*element* .style.font="*expression*"</span></span>

<span data-ttu-id="ec531-119">*expresión* = de *elemento*. Style. Font</span><span class="sxs-lookup"><span data-stu-id="ec531-119">*expression*=*element*.style.font</span></span>

<span data-ttu-id="ec531-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="ec531-120">**Remarks**</span></span>

<span data-ttu-id="ec531-121">Define los atributos de una fuente, como familia, estilo, peso, tamaño y variante.</span><span class="sxs-lookup"><span data-stu-id="ec531-121">Defines the attributes of a font, including family, style, weight, size, and variant.</span></span> <span data-ttu-id="ec531-122">El orden de las definiciones en la cadena es: tipo de **fuente**, **fuente-variante**, fuente **-peso**, **fuente-tamaño**, **ancho de línea** y **familia de fuentes**.</span><span class="sxs-lookup"><span data-stu-id="ec531-122">The order of definitions in the string is: **font-style**, **font-variant**, **font-weight**, **font-size**, **line-height**, and **font-family**.</span></span> <span data-ttu-id="ec531-123">Los valores son los mismos que los atributos de estilo HTML estándar.</span><span class="sxs-lookup"><span data-stu-id="ec531-123">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="ec531-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="ec531-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="ec531-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="ec531-125">**Example**</span></span>

<span data-ttu-id="ec531-126">La fuente del texto textpath es cursiva, Versalitas, negrita, 36 punto Arial.</span><span class="sxs-lookup"><span data-stu-id="ec531-126">The font of the textpath text is italic, small-caps, bold, 36 point Arial.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 