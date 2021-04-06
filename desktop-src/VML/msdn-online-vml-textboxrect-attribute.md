---
title: Atributo TextBoxRect de VML
description: Atributo TextBoxRect de VML
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23e955c8dc929a442fe147d5401fd597534242e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077820"
---
# <a name="vml-textboxrect-attribute"></a><span data-ttu-id="86295-103">Atributo TextBoxRect de VML</span><span class="sxs-lookup"><span data-stu-id="86295-103">VML TextBoxRect Attribute</span></span>

<span data-ttu-id="86295-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="86295-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="86295-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="86295-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="86295-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="86295-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="86295-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="86295-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="86295-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="86295-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="86295-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="86295-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="86295-110">Define uno o varios cuadros de texto dentro de una forma.</span><span class="sxs-lookup"><span data-stu-id="86295-110">Defines one or more text boxes inside a shape.</span></span> <span data-ttu-id="86295-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="86295-111">Read/write.</span></span> <span data-ttu-id="86295-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="86295-112">**String**.</span></span>

<span data-ttu-id="86295-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="86295-113">**Applies To**</span></span>

[<span data-ttu-id="86295-114">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="86295-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="86295-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="86295-115">**Tag Syntax**</span></span>

<span data-ttu-id="86295-116"><v: *Element* textboxrect = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="86295-116"><v: *element* textboxrect=" *expression* "></span></span>

<span data-ttu-id="86295-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="86295-117">**Script Syntax**</span></span>

<span data-ttu-id="86295-118">*Element* . textboxrect = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="86295-118">*element* .textboxrect="*expression*"</span></span>

<span data-ttu-id="86295-119">*expresión* = de *elemento*. textboxrect</span><span class="sxs-lookup"><span data-stu-id="86295-119">*expression*=*element*.textboxrect</span></span>

<span data-ttu-id="86295-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="86295-120">**Remarks**</span></span>

<span data-ttu-id="86295-121">Un cuadro de texto se define mediante uno o más conjuntos de números que especifican (en orden) los puntos izquierdo, superior, derecho e inferior del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="86295-121">A textbox is defined by one or more sets of numbers specifying (in order) the left, top, right, and bottom points of the rectangle.</span></span> <span data-ttu-id="86295-122">Varios conjuntos se delimitan mediante un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="86295-122">Multiple sets are delimited by a semicolon.</span></span> <span data-ttu-id="86295-123">El valor predeterminado es el mismo valor de dimensión que el rectángulo que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="86295-123">The default value is the same dimension value as the containing rectangle.</span></span> <span data-ttu-id="86295-124">Si se define más de un TextBox, los conjuntos cuádruples separados por comas que definen cada TextBox se separan mediante signos de punto y coma.</span><span class="sxs-lookup"><span data-stu-id="86295-124">If more than one textbox is defined, the comma-delimited quadruple sets that define each textbox are separated by semicolons.</span></span> <span data-ttu-id="86295-125">Normalmente, los cuadros de texto aparecen en conjuntos de 1, 2, 3 o 6 rectángulos en una forma.</span><span class="sxs-lookup"><span data-stu-id="86295-125">Normally textboxes come in sets of 1, 2, 3, or 6 rectangles on a shape.</span></span>

<span data-ttu-id="86295-126">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="86295-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="86295-127">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="86295-127">**Example**</span></span>

<span data-ttu-id="86295-128">Se define un cuadro de texto de 95 unidades por 95 unidades y se colocan 5 unidades dentro de la esquina superior izquierda de la forma.</span><span class="sxs-lookup"><span data-stu-id="86295-128">A textbox of 95 units by 95 units is defined and placed 5 units inside the top left corner of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 