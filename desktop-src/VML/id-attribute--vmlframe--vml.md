---
title: Atributo ID (VMLFrame) (VML)
description: Atributo ID (VMLFrame) (VML)
ms.assetid: 3580fad7-b49e-44d7-b266-90fbfc2a02c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f9c5254a2dca186651bb49b677febe747f37c4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077966"
---
# <a name="id-attribute-vmlframevml"></a><span data-ttu-id="41834-103">Atributo ID (VMLFrame) (VML)</span><span class="sxs-lookup"><span data-stu-id="41834-103">ID Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="41834-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="41834-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="41834-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="41834-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="41834-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="41834-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="41834-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="41834-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="41834-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="41834-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="41834-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="41834-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="41834-110">Define un identificador único para el marco.</span><span class="sxs-lookup"><span data-stu-id="41834-110">Defines a unique identifier for the frame.</span></span> <span data-ttu-id="41834-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="41834-111">Read/write.</span></span> <span data-ttu-id="41834-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="41834-112">**String**.</span></span>

<span data-ttu-id="41834-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="41834-113">**Applies To**</span></span>

[<span data-ttu-id="41834-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="41834-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="41834-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="41834-115">**Tag Syntax**</span></span>

<span data-ttu-id="41834-116"><v: ID. de *elemento* = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="41834-116"><v: *element* ID=" *expression* "></span></span>

<span data-ttu-id="41834-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="41834-117">**Script Syntax**</span></span>

<span data-ttu-id="41834-118">*Element* . ID = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="41834-118">*element* .ID="*expression*"</span></span>

<span data-ttu-id="41834-119">*expresión* = de identificador de *elemento*</span><span class="sxs-lookup"><span data-stu-id="41834-119">*expression*=*element*.ID</span></span>

<span data-ttu-id="41834-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="41834-120">**Remarks**</span></span>

<span data-ttu-id="41834-121">Use el **identificador** para hacer referencia a un marco.</span><span class="sxs-lookup"><span data-stu-id="41834-121">Use **ID** to reference a frame.</span></span> <span data-ttu-id="41834-122">Por ejemplo, puede mover el marco en la página cambiando la posición del marco al que hace referencia el **identificador**.</span><span class="sxs-lookup"><span data-stu-id="41834-122">For example, you can move the frame around on the page by changing the frame position referenced by the **ID**.</span></span>

<span data-ttu-id="41834-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="41834-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="41834-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="41834-124">**Example**</span></span>

<span data-ttu-id="41834-125">El **identificador** del marco es "frame01".</span><span class="sxs-lookup"><span data-stu-id="41834-125">The **ID** of the frame is "frame01".</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 