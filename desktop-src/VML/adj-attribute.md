---
title: ADJ (atributo)
description: ADJ (atributo)
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff83371cbca29ee687875343976b312466d6a78c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676408"
---
# <a name="adj-attribute"></a><span data-ttu-id="8391d-103">ADJ (atributo)</span><span class="sxs-lookup"><span data-stu-id="8391d-103">Adj Attribute</span></span>

<span data-ttu-id="8391d-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8391d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8391d-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="8391d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8391d-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="8391d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8391d-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="8391d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8391d-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8391d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8391d-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8391d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8391d-110">Especifica un valor de ajuste que se usa para definir los valores de una fórmula.</span><span class="sxs-lookup"><span data-stu-id="8391d-110">Specifies an adjustment value used to define values for a formula.</span></span> <span data-ttu-id="8391d-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8391d-111">Read/write.</span></span> <span data-ttu-id="8391d-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="8391d-112">**String**.</span></span>

<span data-ttu-id="8391d-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="8391d-113">**Applies To**</span></span>

[<span data-ttu-id="8391d-114">Forma</span><span class="sxs-lookup"><span data-stu-id="8391d-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="8391d-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="8391d-115">**Tag Syntax**</span></span>

<span data-ttu-id="8391d-116"><v: *elemento* ADJ = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="8391d-116"><v: *element* adj=" *expression* "></span></span>

<span data-ttu-id="8391d-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="8391d-117">**Script Syntax**</span></span>

<span data-ttu-id="8391d-118">*Element* . ADJ = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="8391d-118">*element* .adj="*expression*"</span></span>

<span data-ttu-id="8391d-119">*expresión* = de *elemento*. ADJ</span><span class="sxs-lookup"><span data-stu-id="8391d-119">*expression*=*element*.adj</span></span>

<span data-ttu-id="8391d-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="8391d-120">**Remarks**</span></span>

<span data-ttu-id="8391d-121">**ADJ** se utiliza para proporcionar puntos ajustables para una fórmula.</span><span class="sxs-lookup"><span data-stu-id="8391d-121">**Adj** is used to provide adjustable points for a formula.</span></span> <span data-ttu-id="8391d-122">Si se usa en etiquetas, **ADJ** es una cadena delimitada por comas de hasta 8 valores.</span><span class="sxs-lookup"><span data-stu-id="8391d-122">If used in tags, **Adj** is a comma-delimited string of up to 8 values.</span></span> <span data-ttu-id="8391d-123">Algunos valores se pueden omitir.</span><span class="sxs-lookup"><span data-stu-id="8391d-123">Some values may be omitted.</span></span> <span data-ttu-id="8391d-124">Por ejemplo, "0, 1, 2, 4, 5, 7" sería una cadena válida pero la cuarta y la séptima parte de los elementos no tendrían valores (los elementos se cuentan a partir de 0).</span><span class="sxs-lookup"><span data-stu-id="8391d-124">For example, "0,1,2,,4,5,,7" would be a valid string but the fourth and seventh items would not have values (items are counted starting from 0).</span></span>

<span data-ttu-id="8391d-125">En el caso de scripting, **ADJ** usa el tipo de datos [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="8391d-125">For scripting, **Adj** uses the [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) data type.</span></span>

<span data-ttu-id="8391d-126">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="8391d-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="8391d-127">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="8391d-127">**See Also**</span></span>

[<span data-ttu-id="8391d-128">Fórmula</span><span class="sxs-lookup"><span data-stu-id="8391d-128">Formula</span></span>](msdn-online-vml-formulas-element.md)

<span data-ttu-id="8391d-129">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="8391d-129">**Example**</span></span>

<span data-ttu-id="8391d-130">Se crea un cuadrado simple con ajustes.</span><span class="sxs-lookup"><span data-stu-id="8391d-130">A simple square is created with adjustments.</span></span> <span data-ttu-id="8391d-131">En primer lugar, se crea la cadena de **ajust** para definir ocho valores de ajuste.</span><span class="sxs-lookup"><span data-stu-id="8391d-131">First the **Adj** string is created to define eight adjustment values.</span></span> <span data-ttu-id="8391d-132">A continuación, se hace referencia a cada valor de ajuste en una de las ocho fórmulas, con cada valor de ajuste precedido por un signo de número ( \# ).</span><span class="sxs-lookup"><span data-stu-id="8391d-132">Then each adjustment value is referenced by one of the eight formulas, with each adjustment value preceeded by a number sign (\#) symbol.</span></span> <span data-ttu-id="8391d-133">Por último, una ruta de acceso se define mediante una cadena que hace referencia a las fórmulas, con cada fórmula precedida por el símbolo de arroba (@).</span><span class="sxs-lookup"><span data-stu-id="8391d-133">Finally a path is defined by a string that references the formulas, with each formula preceeded by the "at" sign (@) symbol.</span></span>


```HTML
   <v:shape id="rect01" type="#myshape"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:30;left:30;width:20;height:20"
   adj="1, 1, 1, 200, 200, 200, 200, 1">
   <v:path v="m @0,@1 l @2,@3, @4,@5, @6,@7 x e"/>
   <v:formulas>
   <v:f eqn="val #0"/>
   <v:f eqn="val #1"/>
   <v:f eqn="val #2"/>
   <v:f eqn="val #3"/>
   <v:f eqn="val #4"/>
   <v:f eqn="val #5"/>
   <v:f eqn="val #6"/>
   <v:f eqn="val #7"/>
   </v:formulas>
   </v:shape>
```



<span data-ttu-id="8391d-134">[Ejemplo del atributo ADJ](/previous-versions/bb229662(v=vs.85)) (requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="8391d-134">[Adj Attribute Example](/previous-versions/bb229662(v=vs.85)) (Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 