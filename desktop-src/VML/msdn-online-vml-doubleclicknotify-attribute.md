---
title: Atributo DoubleClickNotify de VML
description: Atributo DoubleClickNotify de VML
ms.assetid: 003a87f5-29c1-484e-ac15-2e4cb8e854ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16be329952cfff23957f961fb6d29198ad173898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359007"
---
# <a name="vml-doubleclicknotify-attribute"></a><span data-ttu-id="6b6eb-103">Atributo DoubleClickNotify de VML</span><span class="sxs-lookup"><span data-stu-id="6b6eb-103">VML DoubleClickNotify Attribute</span></span>

<span data-ttu-id="6b6eb-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6b6eb-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6b6eb-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="6b6eb-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6b6eb-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="6b6eb-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6b6eb-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="6b6eb-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6b6eb-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6b6eb-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6b6eb-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6b6eb-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6b6eb-110">Envía un mensaje de evento cuando se hace doble clic en una forma.</span><span class="sxs-lookup"><span data-stu-id="6b6eb-110">Sends an event message when a shape is double-clicked.</span></span> <span data-ttu-id="6b6eb-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b6eb-111">Read/write.</span></span> <span data-ttu-id="6b6eb-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="6b6eb-112">**VgTriState**.</span></span>

<span data-ttu-id="6b6eb-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="6b6eb-113">**Applies To**</span></span>

[<span data-ttu-id="6b6eb-114">Forma</span><span class="sxs-lookup"><span data-stu-id="6b6eb-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="6b6eb-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="6b6eb-115">**Tag Syntax**</span></span>

<span data-ttu-id="6b6eb-116"><v: *Element* o:doubleclicknotify = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="6b6eb-116"><v: *element* o:doubleclicknotify=" *expression* "></span></span>

<span data-ttu-id="6b6eb-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="6b6eb-117">**Remarks**</span></span>

<span data-ttu-id="6b6eb-118">El valor predeterminado es **false**, lo que indica que no se desencadenará el evento.</span><span class="sxs-lookup"><span data-stu-id="6b6eb-118">The default value is **False**, indicating that the event will not be fired.</span></span>

<span data-ttu-id="6b6eb-119">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="6b6eb-119">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="6b6eb-120">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="6b6eb-120">**Example**</span></span>

<span data-ttu-id="6b6eb-121">Cuando se hace doble clic en la forma, se desencadena un evento de doble clic.</span><span class="sxs-lookup"><span data-stu-id="6b6eb-121">The shape will trigger a double-click event when double-clicked.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:doubleclicknotify="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 