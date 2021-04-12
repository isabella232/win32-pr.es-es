---
title: Atributo limo de VML
description: Atributo limo de VML
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364aebfc2384ac9e19c9dc5f2f0ae52f09228a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420777"
---
# <a name="vml-limo-attribute"></a><span data-ttu-id="0447f-103">Atributo limo de VML</span><span class="sxs-lookup"><span data-stu-id="0447f-103">VML Limo Attribute</span></span>

<span data-ttu-id="0447f-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0447f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0447f-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="0447f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0447f-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="0447f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0447f-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="0447f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0447f-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0447f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0447f-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0447f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0447f-110">Define un punto de estiramiento en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="0447f-110">Defines a stretch point on the path.</span></span> <span data-ttu-id="0447f-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0447f-111">Read/write.</span></span> <span data-ttu-id="0447f-112">**Vector2D**.</span><span class="sxs-lookup"><span data-stu-id="0447f-112">**Vector2D**.</span></span>

<span data-ttu-id="0447f-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="0447f-113">**Applies To**</span></span>

[<span data-ttu-id="0447f-114">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="0447f-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="0447f-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="0447f-115">**Tag Syntax**</span></span>

<span data-ttu-id="0447f-116"><v: *Element* limo = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="0447f-116"><v: *element* limo=" *expression* "></span></span>

<span data-ttu-id="0447f-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="0447f-117">**Script Syntax**</span></span>

<span data-ttu-id="0447f-118">*Element* . limo = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="0447f-118">*element* .limo="*expression*"</span></span>

<span data-ttu-id="0447f-119">*expresión* = de *elemento*. limo</span><span class="sxs-lookup"><span data-stu-id="0447f-119">*expression*=*element*.limo</span></span>

<span data-ttu-id="0447f-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="0447f-120">**Remarks**</span></span>

<span data-ttu-id="0447f-121">El valor predeterminado es "0 0".</span><span class="sxs-lookup"><span data-stu-id="0447f-121">The default value is "0 0".</span></span> <span data-ttu-id="0447f-122">Limo stretchs son puntos en el borde de una forma que definen dónde y cómo un usuario puede ajustar una forma en un editor gráfico.</span><span class="sxs-lookup"><span data-stu-id="0447f-122">Limo stretches are points on a shape's edge that define where and how a shape may be stretched by a user in a graphical editor.</span></span>

<span data-ttu-id="0447f-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="0447f-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="0447f-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="0447f-124">**Example**</span></span>

<span data-ttu-id="0447f-125">Un punto de estiramiento de limo se define A la mitad de la línea horizontal.</span><span class="sxs-lookup"><span data-stu-id="0447f-125">A limo stretch point is defined halfway along the horizontal line.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 