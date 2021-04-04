---
title: Atributo de tipo (forma) (VML)
description: Atributo de tipo (forma) (VML)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e53b275d6b6327b3d3783704dbd06156e643f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077910"
---
# <a name="type-attribute-shapevml"></a><span data-ttu-id="f48d0-103">Atributo de tipo (forma) (VML)</span><span class="sxs-lookup"><span data-stu-id="f48d0-103">Type Attribute (Shape)(VML)</span></span>

<span data-ttu-id="f48d0-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f48d0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f48d0-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="f48d0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f48d0-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="f48d0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f48d0-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="f48d0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f48d0-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f48d0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f48d0-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f48d0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f48d0-110">Define una referencia al identificador de un elemento [TipoForma](msdn-online-vml-shapetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f48d0-110">Defines a reference to the ID of a [ShapeType](msdn-online-vml-shapetype-element.md) element.</span></span> <span data-ttu-id="f48d0-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f48d0-111">Read/write.</span></span> <span data-ttu-id="f48d0-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="f48d0-112">**String**.</span></span>

<span data-ttu-id="f48d0-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="f48d0-113">**Applies To**</span></span>

[<span data-ttu-id="f48d0-114">Forma</span><span class="sxs-lookup"><span data-stu-id="f48d0-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="f48d0-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="f48d0-115">**Tag Syntax**</span></span>

``` syntax
<v:
          element 
          type=" expression ">
```

<span data-ttu-id="f48d0-116">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="f48d0-116">**Script Syntax**</span></span>

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

<span data-ttu-id="f48d0-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="f48d0-117">**Remarks**</span></span>

<span data-ttu-id="f48d0-118">Si el atributo de **tipo** hace referencia al identificador de un elemento **TipoForma** , los rellenos, rutas de acceso y trazos del **TipoForma** se usan como plantillas para crear la forma.</span><span class="sxs-lookup"><span data-stu-id="f48d0-118">If the **Type** attribute references the ID of a **ShapeType** element, the fills, paths, and strokes of the **ShapeType** are used as templates to create the shape.</span></span> <span data-ttu-id="f48d0-119">Los valores que se derivan de **TipoForma** se pueden reemplazar por valores de forma individuales.</span><span class="sxs-lookup"><span data-stu-id="f48d0-119">Values derived from **ShapeType** can be overridden by individual shape values.</span></span>

<span data-ttu-id="f48d0-120">Si se utiliza en etiquetas, el valor de cadena debe comenzar por un símbolo de número ( \# ).</span><span class="sxs-lookup"><span data-stu-id="f48d0-120">If used in tags, the string value must begin with a number sign (\#) symbol.</span></span>

<span data-ttu-id="f48d0-121">**Atributo estándar de VML**</span><span class="sxs-lookup"><span data-stu-id="f48d0-121">**VML Standard Attribute**</span></span>

<span data-ttu-id="f48d0-122">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="f48d0-122">**Example**</span></span>

<span data-ttu-id="f48d0-123">Una forma **TipoForma** se crea con el "tipo" como identificador.</span><span class="sxs-lookup"><span data-stu-id="f48d0-123">A **ShapeType** shape is created with the "mytype" as an ID.</span></span>


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



<span data-ttu-id="f48d0-124">A continuación, si crea una forma con los valores de **TipoForma** , la forma tendrá los atributos de "mi tipo" **TipoForma**; es decir, "shape01" tendrá un relleno rojo con un trazo azul.</span><span class="sxs-lookup"><span data-stu-id="f48d0-124">Then if you create a shape using the **ShapeType** values, the shape will have the attributes of the "mytype" **ShapeType**; that is, "shape01" will have a red fill with a blue stroke.</span></span>


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



<span data-ttu-id="f48d0-125">Puede invalidar los valores heredados, por ejemplo, cambiando el color a verde.</span><span class="sxs-lookup"><span data-stu-id="f48d0-125">You can override the inherited values, for example, by changing the color to green.</span></span>


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



<span data-ttu-id="f48d0-126">[Ejemplo de atributo de tipo](/previous-versions/bb264099(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f48d0-126">[Type Attribute Example](/previous-versions/bb264099(v=vs.85)).</span></span> <span data-ttu-id="f48d0-127">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="f48d0-127">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 