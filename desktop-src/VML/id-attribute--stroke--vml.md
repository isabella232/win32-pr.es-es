---
title: ID (atributo, Stroke) (VML)
description: ID (atributo, Stroke) (VML)
ms.assetid: 584b0e90-9d66-471b-a1d2-33a236c2ed8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efc9cfda1b7ddb359812d9ad28b37b851315da8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792405"
---
# <a name="id-attribute-strokevml"></a><span data-ttu-id="b23af-103">ID (atributo, Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="b23af-103">ID Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="b23af-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b23af-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b23af-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="b23af-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b23af-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="b23af-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b23af-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="b23af-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b23af-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b23af-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b23af-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b23af-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b23af-110">Nombre que proporciona un identificador único para un trazo.</span><span class="sxs-lookup"><span data-stu-id="b23af-110">A name that provides a unique identifier for a stroke.</span></span> <span data-ttu-id="b23af-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b23af-111">Read/write.</span></span> <span data-ttu-id="b23af-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="b23af-112">**String**.</span></span>

<span data-ttu-id="b23af-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="b23af-113">**Applies To**</span></span>

[<span data-ttu-id="b23af-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="b23af-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="b23af-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="b23af-115">**Tag Syntax**</span></span>

<span data-ttu-id="b23af-116"><v: ID. de *elemento* = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="b23af-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="b23af-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="b23af-117">**Script Syntax**</span></span>

<span data-ttu-id="b23af-118">*Element* . ID = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="b23af-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="b23af-119">*expresión* = de identificador de *elemento*</span><span class="sxs-lookup"><span data-stu-id="b23af-119">*expression*=*element*.id</span></span>

<span data-ttu-id="b23af-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="b23af-120">**Remarks**</span></span>

<span data-ttu-id="b23af-121">Use el **identificador** para hacer referencia a un trazo específico.</span><span class="sxs-lookup"><span data-stu-id="b23af-121">Use **ID** to refer to a specific stroke.</span></span> <span data-ttu-id="b23af-122">Una vez que haya creado un trazo y dado un identificador, puede utilizar el nombre de identificador cuando desee manipular el trazo.</span><span class="sxs-lookup"><span data-stu-id="b23af-122">Once you have created a stroke and given it an ID, you can use the ID name when you want to manipulate the stroke.</span></span>

<span data-ttu-id="b23af-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="b23af-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="b23af-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b23af-124">**Example**</span></span>

<span data-ttu-id="b23af-125">La forma tiene un ID. de trazo denominado "Stroke".</span><span class="sxs-lookup"><span data-stu-id="b23af-125">The shape has a stroke ID called "mystroke".</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke id="mystroke"/>
   </v:shape>
```



 

 