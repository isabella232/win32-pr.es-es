---
title: Atributo de Font-Family VML
description: Atributo de Font-Family VML
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29aa72775e8f00e195462cf3df06097d267b908
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078346"
---
# <a name="vml-font-family-attribute"></a><span data-ttu-id="792d9-103">Atributo de Font-Family VML</span><span class="sxs-lookup"><span data-stu-id="792d9-103">VML Font-Family Attribute</span></span>

<span data-ttu-id="792d9-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="792d9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="792d9-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="792d9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="792d9-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="792d9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="792d9-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="792d9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="792d9-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="792d9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="792d9-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="792d9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="792d9-110">Define la familia de la fuente textpath.</span><span class="sxs-lookup"><span data-stu-id="792d9-110">Defines the family of the textpath font.</span></span> <span data-ttu-id="792d9-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="792d9-111">Read/write.</span></span> <span data-ttu-id="792d9-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="792d9-112">**String**.</span></span>

<span data-ttu-id="792d9-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="792d9-113">**Applies To**</span></span>

[<span data-ttu-id="792d9-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="792d9-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="792d9-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="792d9-115">**Tag Syntax**</span></span>

<span data-ttu-id="792d9-116"><v: *Element* style = "font-family: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="792d9-116"><v: *element* style="font-family: *expression* "></span></span>

<span data-ttu-id="792d9-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="792d9-117">**Script Syntax**</span></span>

<span data-ttu-id="792d9-118">*Element* . Style. FontFamily = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="792d9-118">*element* .style.fontfamily="*expression*"</span></span>

<span data-ttu-id="792d9-119">*expresión* = de *Element*. Style. FontFamily</span><span class="sxs-lookup"><span data-stu-id="792d9-119">*expression*=*element*.style.fontfamily</span></span>

<span data-ttu-id="792d9-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="792d9-120">**Remarks**</span></span>

<span data-ttu-id="792d9-121">Define el nombre de la fuente.</span><span class="sxs-lookup"><span data-stu-id="792d9-121">Defines the font name.</span></span> <span data-ttu-id="792d9-122">Se pueden usar nombres específicos como Arial o tipos genéricos como serif, sans-serif, cursiva, fantasía o monoespacio.</span><span class="sxs-lookup"><span data-stu-id="792d9-122">Specific names such as Arial can be used or generic types such as serif, sans-serif, cursive, fantasy, or monospace.</span></span> <span data-ttu-id="792d9-123">Los valores son los mismos que los atributos de estilo HTML estándar.</span><span class="sxs-lookup"><span data-stu-id="792d9-123">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="792d9-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="792d9-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="792d9-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="792d9-125">**Example**</span></span>

<span data-ttu-id="792d9-126">La familia de fuentes del texto es Arial.</span><span class="sxs-lookup"><span data-stu-id="792d9-126">The font family of the text is Arial.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 