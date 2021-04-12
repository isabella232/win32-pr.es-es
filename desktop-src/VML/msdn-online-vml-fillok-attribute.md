---
title: Atributo FillOK de VML
description: Atributo FillOK de VML
ms.assetid: 6855544d-0f12-4e21-8101-1bbf45795777
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 667524be103b7c641643a52a85368a82a1289e5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359399"
---
# <a name="vml-fillok-attribute"></a><span data-ttu-id="73fc6-103">Atributo FillOK de VML</span><span class="sxs-lookup"><span data-stu-id="73fc6-103">VML FillOK Attribute</span></span>

<span data-ttu-id="73fc6-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="73fc6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="73fc6-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="73fc6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="73fc6-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="73fc6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="73fc6-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="73fc6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="73fc6-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="73fc6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="73fc6-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="73fc6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="73fc6-110">Determina si se mostrará un relleno.</span><span class="sxs-lookup"><span data-stu-id="73fc6-110">Determines whether a fill will be displayed.</span></span> <span data-ttu-id="73fc6-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="73fc6-111">Read/write.</span></span> <span data-ttu-id="73fc6-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="73fc6-112">**VgTriState**.</span></span>

<span data-ttu-id="73fc6-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="73fc6-113">**Applies To**</span></span>

[<span data-ttu-id="73fc6-114">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="73fc6-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="73fc6-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="73fc6-115">**Tag Syntax**</span></span>

<span data-ttu-id="73fc6-116"><v: *Element* fillok = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="73fc6-116"><v: *element* fillok=" *expression* "></span></span>

<span data-ttu-id="73fc6-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="73fc6-117">**Script Syntax**</span></span>

<span data-ttu-id="73fc6-118">*Element* . fillok = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="73fc6-118">*element* .fillok="*expression*"</span></span>

<span data-ttu-id="73fc6-119">*expresión* = de *elemento*. fillok</span><span class="sxs-lookup"><span data-stu-id="73fc6-119">*expression*=*element*.fillok</span></span>

<span data-ttu-id="73fc6-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="73fc6-120">**Remarks**</span></span>

<span data-ttu-id="73fc6-121">Si **es false**, no se puede rellenar la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="73fc6-121">If **False**, the path cannot be filled.</span></span> <span data-ttu-id="73fc6-122">El valor predeterminado es **True**.</span><span class="sxs-lookup"><span data-stu-id="73fc6-122">The default is **True**.</span></span> <span data-ttu-id="73fc6-123">Este atributo invalida todos los demás atributos de relleno en el elemento primario o **relleno** .</span><span class="sxs-lookup"><span data-stu-id="73fc6-123">This attribute overrides all other fill attributes in the parent or **Fill** element.</span></span>

<span data-ttu-id="73fc6-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="73fc6-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="73fc6-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="73fc6-125">**Example**</span></span>

<span data-ttu-id="73fc6-126">La ruta de acceso no se rellenará.</span><span class="sxs-lookup"><span data-stu-id="73fc6-126">The path will not be filled.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" fillok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 