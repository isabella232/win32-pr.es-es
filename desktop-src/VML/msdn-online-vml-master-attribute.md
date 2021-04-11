---
title: Atributo maestro VML
description: Atributo maestro VML
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d6c34fe49c107ed7ee1b4c1fb90d31bb07f17a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149611"
---
# <a name="vml-master-attribute"></a><span data-ttu-id="9a264-103">Atributo maestro VML</span><span class="sxs-lookup"><span data-stu-id="9a264-103">VML Master Attribute</span></span>

<span data-ttu-id="9a264-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9a264-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9a264-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="9a264-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9a264-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="9a264-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9a264-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="9a264-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9a264-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9a264-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9a264-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9a264-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9a264-110">Determina si un elemento **TipoForma** es un elemento principal.</span><span class="sxs-lookup"><span data-stu-id="9a264-110">Determines whether a **ShapeType** element is a master element.</span></span> <span data-ttu-id="9a264-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9a264-111">Read/write.</span></span> <span data-ttu-id="9a264-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="9a264-112">**VgTriState**.</span></span>

<span data-ttu-id="9a264-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="9a264-113">**Applies To**</span></span>

[<span data-ttu-id="9a264-114">TipoForma</span><span class="sxs-lookup"><span data-stu-id="9a264-114">ShapeType</span></span>](msdn-online-vml-shapetype-element.md)

<span data-ttu-id="9a264-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="9a264-115">**Tag Syntax**</span></span>

<span data-ttu-id="9a264-116"><v: *Element* o:Master = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="9a264-116"><v: *element* o:master=" *expression* "></span></span>

<span data-ttu-id="9a264-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="9a264-117">**Remarks**</span></span>

<span data-ttu-id="9a264-118">Si es **true**, la forma **TipoForma** la representa el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="9a264-118">If **True**, the **ShapeType** shape is rendered by the rendering engine.</span></span> <span data-ttu-id="9a264-119">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="9a264-119">The default value is **False**.</span></span>

<span data-ttu-id="9a264-120">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="9a264-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="9a264-121">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="9a264-121">**Example**</span></span>

<span data-ttu-id="9a264-122">El elemento **TipoForma** es una forma maestra.</span><span class="sxs-lookup"><span data-stu-id="9a264-122">The **ShapeType** element is a master shape.</span></span>


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 