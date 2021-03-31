---
title: Atributo de clase VML
description: Atributo de clase VML
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94bdc723ba9be335afc43023ab89b88834c55474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995419"
---
# <a name="vml-class-attribute"></a><span data-ttu-id="8a669-103">Atributo de clase VML</span><span class="sxs-lookup"><span data-stu-id="8a669-103">VML Class Attribute</span></span>

<span data-ttu-id="8a669-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8a669-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8a669-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="8a669-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8a669-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="8a669-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8a669-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="8a669-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8a669-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8a669-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8a669-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8a669-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8a669-110">Hace referencia a una definición de un estilo CSS.</span><span class="sxs-lookup"><span data-stu-id="8a669-110">Refers to a definition of a CSS style.</span></span> <span data-ttu-id="8a669-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8a669-111">Read/write.</span></span> <span data-ttu-id="8a669-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="8a669-112">**String**.</span></span>

<span data-ttu-id="8a669-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="8a669-113">**Applies To**</span></span>

[<span data-ttu-id="8a669-114">Forma</span><span class="sxs-lookup"><span data-stu-id="8a669-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="8a669-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="8a669-115">**Tag Syntax**</span></span>

<span data-ttu-id="8a669-116"><v: *Element* Class = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="8a669-116"><v: *element* class=" *expression* "></span></span>

<span data-ttu-id="8a669-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="8a669-117">**Script Syntax**</span></span>

<span data-ttu-id="8a669-118">*Element* . className = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="8a669-118">*element* .classname="*expression*"</span></span>

<span data-ttu-id="8a669-119">*expresión* = de *elemento*. ClassName</span><span class="sxs-lookup"><span data-stu-id="8a669-119">*expression*=*element*.classname</span></span>

<span data-ttu-id="8a669-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="8a669-120">**Remarks**</span></span>

<span data-ttu-id="8a669-121">El atributo **Class** es similar al atributo de **clase** HTML estándar que se usa con hojas de estilos CSS.</span><span class="sxs-lookup"><span data-stu-id="8a669-121">The **class** attribute is similar to the standard HTML **class** attribute used with CSS style sheets.</span></span>

<span data-ttu-id="8a669-122">Tenga en cuenta que **className** se usa en lugar de la **clase** para el scripting.</span><span class="sxs-lookup"><span data-stu-id="8a669-122">Note that **classname** is used instead of **class** for scripting.</span></span> <span data-ttu-id="8a669-123">Tenga en cuenta también que para el scripting, **className** solo se puede leer; Si se cambia el valor de **className** , no se cambiará la representación de la forma.</span><span class="sxs-lookup"><span data-stu-id="8a669-123">Also note that for scripting, the **classname** can only be read; changing the value of **classname** will not change the rendering of the shape.</span></span>

<span data-ttu-id="8a669-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="8a669-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="8a669-125">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="8a669-125">**See Also**</span></span>

[<span data-ttu-id="8a669-126">Forma</span><span class="sxs-lookup"><span data-stu-id="8a669-126">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="8a669-127">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="8a669-127">**Example**</span></span>

<span data-ttu-id="8a669-128">Una clase para el **ancho** se crea con el estilo</span><span class="sxs-lookup"><span data-stu-id="8a669-128">A class for **width** is created with the style</span></span>


```HTML
   .narrowstyle {width:50;height:100}
```



<span data-ttu-id="8a669-129">A continuación, se hace referencia al ancho incluyendo el estilo.</span><span class="sxs-lookup"><span data-stu-id="8a669-129">Then the width is referenced by including the style.</span></span> <span data-ttu-id="8a669-130">Tenga en cuenta que el ancho andheight no está definido en el atributo de **estilo** , pero lo definirá el estilo.</span><span class="sxs-lookup"><span data-stu-id="8a669-130">Note that the width andheight is not defined in the **style** attribute, but will be defined by the style.</span></span>


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="8a669-131">Tenga en cuenta que la **clase** solo se aplica a los atributos de tipo CSS.</span><span class="sxs-lookup"><span data-stu-id="8a669-131">Note that **Class** only applies to CSS-type attributes.</span></span>

 

 