---
title: Atributo ShadowOK de VML
description: Atributo ShadowOK de VML
ms.assetid: 88400bf5-f41c-4495-a5d0-9b35c1cae9f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e6b4ca6b98ce66208e906c45fd560324121e8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077785"
---
# <a name="vml-shadowok-attribute"></a><span data-ttu-id="5cb6c-103">Atributo ShadowOK de VML</span><span class="sxs-lookup"><span data-stu-id="5cb6c-103">VML ShadowOK Attribute</span></span>

<span data-ttu-id="5cb6c-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5cb6c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5cb6c-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="5cb6c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5cb6c-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="5cb6c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5cb6c-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="5cb6c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5cb6c-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5cb6c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5cb6c-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5cb6c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5cb6c-110">Determina si se mostrará una sombra.</span><span class="sxs-lookup"><span data-stu-id="5cb6c-110">Determines whether a shadow will be displayed.</span></span> <span data-ttu-id="5cb6c-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5cb6c-111">Read/write.</span></span> <span data-ttu-id="5cb6c-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="5cb6c-112">**VgTriState**.</span></span>

<span data-ttu-id="5cb6c-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="5cb6c-113">**Applies To**</span></span>

[<span data-ttu-id="5cb6c-114">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="5cb6c-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="5cb6c-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="5cb6c-115">**Tag Syntax**</span></span>

<span data-ttu-id="5cb6c-116"><v: *Element* shadowok = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="5cb6c-116"><v: *element* shadowok=" *expression* "></span></span>

<span data-ttu-id="5cb6c-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="5cb6c-117">**Script Syntax**</span></span>

<span data-ttu-id="5cb6c-118">*Element* . shadowok = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="5cb6c-118">*element* .shadowok="*expression*"</span></span>

<span data-ttu-id="5cb6c-119">*expresión* = de *elemento*. shadowok</span><span class="sxs-lookup"><span data-stu-id="5cb6c-119">*expression*=*element*.shadowok</span></span>

<span data-ttu-id="5cb6c-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="5cb6c-120">**Remarks**</span></span>

<span data-ttu-id="5cb6c-121">Si **es false**, la ruta de acceso no puede tener una sombra.</span><span class="sxs-lookup"><span data-stu-id="5cb6c-121">If **False**, the path cannot have a shadow.</span></span> <span data-ttu-id="5cb6c-122">El valor predeterminado es **True**.</span><span class="sxs-lookup"><span data-stu-id="5cb6c-122">The default is **True**.</span></span> <span data-ttu-id="5cb6c-123">Este atributo invalida todos los demás atributos de sombra del elemento primario o de **sombra** .</span><span class="sxs-lookup"><span data-stu-id="5cb6c-123">This attribute overrides all other shadow attributes in the parent or **Shadow** element.</span></span>

<span data-ttu-id="5cb6c-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="5cb6c-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="5cb6c-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="5cb6c-125">**Example**</span></span>

<span data-ttu-id="5cb6c-126">La forma no tendrá una sombra.</span><span class="sxs-lookup"><span data-stu-id="5cb6c-126">The shape will not have a shadow.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True" offset="5pt,5pt" color="blue"/>
   <v:path id= "myPath" shadowok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 