---
title: Atributo de opacidad (sombra) (VML)
description: Atributo de opacidad (sombra) (VML)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d09ca038a187c4a4ed1f914f5d05bcfd63e4a4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420846"
---
# <a name="opacity-attribute-shadowvml"></a><span data-ttu-id="3fd46-103">Atributo de opacidad (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="3fd46-103">Opacity Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="3fd46-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3fd46-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3fd46-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="3fd46-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3fd46-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="3fd46-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3fd46-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="3fd46-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3fd46-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3fd46-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3fd46-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3fd46-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3fd46-110">Determina la transparencia de una sombra.</span><span class="sxs-lookup"><span data-stu-id="3fd46-110">Determines the transparency of a shadow.</span></span> <span data-ttu-id="3fd46-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3fd46-111">Read/write.</span></span> <span data-ttu-id="3fd46-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="3fd46-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span></span>

<span data-ttu-id="3fd46-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="3fd46-113">**Applies To**</span></span>

[<span data-ttu-id="3fd46-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="3fd46-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="3fd46-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="3fd46-115">**Tag Syntax**</span></span>

<span data-ttu-id="3fd46-116"><v: *elemento* Opacity = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="3fd46-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="3fd46-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="3fd46-117">**Script Syntax**</span></span>

<span data-ttu-id="3fd46-118">*elemento* . Opacity = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="3fd46-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="3fd46-119">*expresión* = de *elemento*. Opacity</span><span class="sxs-lookup"><span data-stu-id="3fd46-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="3fd46-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="3fd46-120">**Remarks**</span></span>

<span data-ttu-id="3fd46-121">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="3fd46-121">The default value is 1.</span></span> <span data-ttu-id="3fd46-122">Un valor de 0 hará una sombra completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="3fd46-122">A value of 0 will make a completely transparent shadow.</span></span>

<span data-ttu-id="3fd46-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="3fd46-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3fd46-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="3fd46-124">**Example**</span></span>

<span data-ttu-id="3fd46-125">La forma tiene una sombra que es 50% transparente.</span><span class="sxs-lookup"><span data-stu-id="3fd46-125">The shape has a shadow that is 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 