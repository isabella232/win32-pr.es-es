---
title: Atributo Rotation (forma) (VML)
description: Atributo Rotation (forma) (VML)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03b114c885cbeaf5392068e79cd7f63bbc1fc52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078318"
---
# <a name="rotation-attribute-shapevml"></a><span data-ttu-id="76c92-103">Atributo Rotation (forma) (VML)</span><span class="sxs-lookup"><span data-stu-id="76c92-103">Rotation Attribute (Shape)(VML)</span></span>

<span data-ttu-id="76c92-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="76c92-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="76c92-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="76c92-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="76c92-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="76c92-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="76c92-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="76c92-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="76c92-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="76c92-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="76c92-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="76c92-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="76c92-110">Define el ángulo en el que se gira una forma.</span><span class="sxs-lookup"><span data-stu-id="76c92-110">Defines the angle that a shape is rotated.</span></span> <span data-ttu-id="76c92-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="76c92-111">Read/write.</span></span> <span data-ttu-id="76c92-112">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="76c92-112">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span>

<span data-ttu-id="76c92-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="76c92-113">**Applies To**</span></span>

[<span data-ttu-id="76c92-114">Forma</span><span class="sxs-lookup"><span data-stu-id="76c92-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="76c92-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="76c92-115">**Tag Syntax**</span></span>

<span data-ttu-id="76c92-116"><v: *Element* style = "Rotation: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="76c92-116"><v: *element* style="rotation: *expression* "></span></span>

<span data-ttu-id="76c92-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="76c92-117">**Script Syntax**</span></span>

<span data-ttu-id="76c92-118">*Element* . Rotation = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="76c92-118">*element* .rotation="*expression*"</span></span>

<span data-ttu-id="76c92-119">*expresión* = de *elemento*. Rotation</span><span class="sxs-lookup"><span data-stu-id="76c92-119">*expression*=*element*.rotation</span></span>

<span data-ttu-id="76c92-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="76c92-120">**Remarks**</span></span>

<span data-ttu-id="76c92-121">El valor en grados puede ser positivo o negativo, y los valores mayores que 360 se pueden dividir en un círculo de 360 grados.</span><span class="sxs-lookup"><span data-stu-id="76c92-121">The value in degrees can be positive or negative, and values greater than 360 are modularized to a 360-degree circle.</span></span> <span data-ttu-id="76c92-122">Los ángulos positivos están a la derecha.</span><span class="sxs-lookup"><span data-stu-id="76c92-122">Positive angles are clockwise.</span></span> <span data-ttu-id="76c92-123">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="76c92-123">The default value is 0.</span></span>

<span data-ttu-id="76c92-124">Tenga en cuenta que se cambia la posición de la forma después de la rotación para reflejar las nuevas coordenadas del cuadro de límite.</span><span class="sxs-lookup"><span data-stu-id="76c92-124">Note that the shape is repositioned after the rotation to reflect the new bounding box coordinates.</span></span>

<span data-ttu-id="76c92-125">Tenga en cuenta también que para el scripting, no se utiliza el atributo de **estilo** y ese **giro** se trata como un atributo directo de la forma.</span><span class="sxs-lookup"><span data-stu-id="76c92-125">Also note that for scripting, the **style** attribute is not used and that **Rotation** is treated as a direct attribute of the shape.</span></span>

<span data-ttu-id="76c92-126">El atributo **Rotation** es similar al atributo **rotación** HTML estándar para los estilos.</span><span class="sxs-lookup"><span data-stu-id="76c92-126">The **Rotation** attribute is similar to the standard HTML **Rotation** attribute for styles.</span></span>

<span data-ttu-id="76c92-127">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="76c92-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="76c92-128">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="76c92-128">**See Also**</span></span>

<span data-ttu-id="76c92-129">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="76c92-129">**Example**</span></span>

<span data-ttu-id="76c92-130">El rectángulo se inclinará 45 grados.</span><span class="sxs-lookup"><span data-stu-id="76c92-130">The rectangle will be tilted 45 degrees.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



<span data-ttu-id="76c92-131">[Ejemplo del atributo Rotation](/previous-versions/bb264091(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76c92-131">[Rotation Attribute Example](/previous-versions/bb264091(v=vs.85)).</span></span> <span data-ttu-id="76c92-132">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="76c92-132">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 