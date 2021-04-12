---
title: Atributo ArrowOK de VML
description: Atributo ArrowOK de VML
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8807b802370f81ddd084df8a171f95e8496c7ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420942"
---
# <a name="vml-arrowok-attribute"></a><span data-ttu-id="2c620-103">Atributo ArrowOK de VML</span><span class="sxs-lookup"><span data-stu-id="2c620-103">VML ArrowOK Attribute</span></span>

<span data-ttu-id="2c620-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2c620-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2c620-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="2c620-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2c620-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="2c620-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2c620-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="2c620-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2c620-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2c620-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2c620-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2c620-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2c620-110">Determina si se mostrarán las puntas de flecha.</span><span class="sxs-lookup"><span data-stu-id="2c620-110">Determines whether arrowheads will be displayed.</span></span> <span data-ttu-id="2c620-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2c620-111">Read/write.</span></span> <span data-ttu-id="2c620-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="2c620-112">**VgTriState**.</span></span>

<span data-ttu-id="2c620-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="2c620-113">**Applies To**</span></span>

[<span data-ttu-id="2c620-114">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="2c620-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="2c620-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="2c620-115">**Tag Syntax**</span></span>

<span data-ttu-id="2c620-116"><v: *Element* arrowok = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="2c620-116"><v: *element* arrowok=" *expression* "></span></span>

<span data-ttu-id="2c620-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="2c620-117">**Script Syntax**</span></span>

<span data-ttu-id="2c620-118">*Element* . arrowok = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="2c620-118">*element* .arrowok="*expression*"</span></span>

<span data-ttu-id="2c620-119">*expresión* = de *elemento*. arrowok</span><span class="sxs-lookup"><span data-stu-id="2c620-119">*expression*=*element*.arrowok</span></span>

<span data-ttu-id="2c620-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="2c620-120">**Remarks**</span></span>

<span data-ttu-id="2c620-121">Si **es false**, la ruta de acceso no tendrá puntas de flecha.</span><span class="sxs-lookup"><span data-stu-id="2c620-121">If **False**, the path will not have arrowheads.</span></span> <span data-ttu-id="2c620-122">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="2c620-122">The default is **False**.</span></span> <span data-ttu-id="2c620-123">Este atributo invalida todos los demás atributos de la punta de flecha en el elemento primario o de **trazo** .</span><span class="sxs-lookup"><span data-stu-id="2c620-123">This attribute overrides all other arrowhead attributes in the parent or **Stroke** element.</span></span>

<span data-ttu-id="2c620-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="2c620-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="2c620-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="2c620-125">**Example**</span></span>

<span data-ttu-id="2c620-126">La ruta de acceso no tendrá una punta de flecha.</span><span class="sxs-lookup"><span data-stu-id="2c620-126">The path will not have an arrowhead.</span></span>


```HTML
   <v:line id="whatsmyline"
   style="position:relative"
   from="114pt,66pt" to="402pt,66pt"
   strokecolor="black">
   <v:stroke startarrow="block" endarrow="block"/>
   <v:path arrowok="False"/>
   </v:line>
```



 

 