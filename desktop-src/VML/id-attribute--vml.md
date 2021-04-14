---
title: ID (atributo) (VML)
description: ID (atributo) (VML)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a3925166a735b7813efd4cb9bc68f50bb8fa52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487902"
---
# <a name="id-attribute-vml"></a><span data-ttu-id="50cb5-103">ID (atributo) (VML)</span><span class="sxs-lookup"><span data-stu-id="50cb5-103">ID Attribute (VML)</span></span>

<span data-ttu-id="50cb5-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="50cb5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="50cb5-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="50cb5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="50cb5-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="50cb5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="50cb5-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="50cb5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="50cb5-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="50cb5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="50cb5-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="50cb5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="50cb5-110">Proporciona un identificador único para un elemento.</span><span class="sxs-lookup"><span data-stu-id="50cb5-110">Provides a unique identifier for an element.</span></span> <span data-ttu-id="50cb5-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="50cb5-111">Read/write.</span></span> <span data-ttu-id="50cb5-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="50cb5-112">**String**.</span></span>

<span data-ttu-id="50cb5-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="50cb5-113">**Applies To**</span></span>

<span data-ttu-id="50cb5-114">Todos los elementos VML.</span><span class="sxs-lookup"><span data-stu-id="50cb5-114">All VML elements.</span></span>

<span data-ttu-id="50cb5-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="50cb5-115">**Tag Syntax**</span></span>

<span data-ttu-id="50cb5-116"><v: *ElementName* ID = " *idname* " ></span><span class="sxs-lookup"><span data-stu-id="50cb5-116"><v: *elementname* id=" *idname* "></span></span>

<span data-ttu-id="50cb5-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="50cb5-117">**Script Syntax**</span></span>

<span data-ttu-id="50cb5-118">*ElementName* . ID = " *idname* "</span><span class="sxs-lookup"><span data-stu-id="50cb5-118">*elementname* .id =" *idname* "</span></span>

<span data-ttu-id="50cb5-119">*expresión* = de *ElementName*. ID</span><span class="sxs-lookup"><span data-stu-id="50cb5-119">*expression*=*elementname*.id</span></span>

<span data-ttu-id="50cb5-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="50cb5-120">**Remarks**</span></span>

<span data-ttu-id="50cb5-121">Use **ID** para hacer referencia a un elemento específico.</span><span class="sxs-lookup"><span data-stu-id="50cb5-121">Use **ID** to refer to a specific element.</span></span> <span data-ttu-id="50cb5-122">Una vez que haya creado una forma y dado un identificador, puede utilizar el nombre de identificador cuando desee manipular el elemento.</span><span class="sxs-lookup"><span data-stu-id="50cb5-122">Once you have created a shape and given it an ID, you can use the ID name when you want to manipulate the element.</span></span>

<span data-ttu-id="50cb5-123">El **identificador** es necesario para usar el elemento [TipoForma](msdn-online-vml-shapetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="50cb5-123">**ID** is required to use the [ShapeType](msdn-online-vml-shapetype-element.md) element.</span></span>

<span data-ttu-id="50cb5-124">Cuando Microsoft Office genera VML, si se asigna un nombre de modelo de objetos a la forma, **ID** se establece en este nombre.</span><span class="sxs-lookup"><span data-stu-id="50cb5-124">When VML is generated by Microsoft Office, if an object model name is assigned to the shape, then **ID** is set to this name.</span></span> <span data-ttu-id="50cb5-125">Si no se establece el nombre del modelo de objetos, el nombre se genera mediante el *SPID* (ID. de forma interna) más un prefijo (S para la forma, M para la forma maestra, T para TipoForma).</span><span class="sxs-lookup"><span data-stu-id="50cb5-125">If the object model name is not set, then the name is generated using the *Spid* (internal shape ID) plus a prefix (S for shape, M for master shape, T for shapetype).</span></span>

<span data-ttu-id="50cb5-126">*Atributo estándar de VML*.</span><span class="sxs-lookup"><span data-stu-id="50cb5-126">*VML Standard Attribute*.</span></span>

<span data-ttu-id="50cb5-127">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="50cb5-127">**Example**</span></span>

<span data-ttu-id="50cb5-128">Para cambiar los atributos de una forma, primero debe proporcionar un identificador a la forma; por ejemplo, "trirect".</span><span class="sxs-lookup"><span data-stu-id="50cb5-128">To change the attributes of a shape, you must first give the shape an ID; for example, "myrect".</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```




```HTML
   myrect.style.width = 80
   myrect.style.height = 80
   myrect.fillColor = "green"
```



<span data-ttu-id="50cb5-129">[Ejemplo del atributo ID](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example).</span><span class="sxs-lookup"><span data-stu-id="50cb5-129">[ID Attribute Example](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example).</span></span> <span data-ttu-id="50cb5-130">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="50cb5-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 