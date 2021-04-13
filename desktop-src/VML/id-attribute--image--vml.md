---
title: Atributo ID (imagen) (VML)
description: Atributo ID (imagen) (VML)
ms.assetid: d85a6d56-5896-4ac0-85c7-0edc72928c62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40ac489331699ca6fe040cddc0bebb408d524de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421371"
---
# <a name="id-attribute-imagevml"></a><span data-ttu-id="d4e3b-103">Atributo ID (imagen) (VML)</span><span class="sxs-lookup"><span data-stu-id="d4e3b-103">ID Attribute (Image)(VML)</span></span>

<span data-ttu-id="d4e3b-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d4e3b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d4e3b-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="d4e3b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d4e3b-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="d4e3b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d4e3b-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="d4e3b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d4e3b-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d4e3b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d4e3b-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d4e3b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d4e3b-110">Define un nombre que proporciona un identificador único para una imagen.</span><span class="sxs-lookup"><span data-stu-id="d4e3b-110">Defines a name that provides a unique identifier for an image.</span></span> <span data-ttu-id="d4e3b-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d4e3b-111">Read/write.</span></span> <span data-ttu-id="d4e3b-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="d4e3b-112">**String**.</span></span>

<span data-ttu-id="d4e3b-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="d4e3b-113">**Applies To**</span></span>

[<span data-ttu-id="d4e3b-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="d4e3b-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="d4e3b-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="d4e3b-115">**Tag Syntax**</span></span>

<span data-ttu-id="d4e3b-116"><v: ID. de *elemento* = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="d4e3b-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="d4e3b-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="d4e3b-117">**Script Syntax**</span></span>

<span data-ttu-id="d4e3b-118">*Element* . ID = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="d4e3b-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="d4e3b-119">*expresión* = de identificador de *elemento*</span><span class="sxs-lookup"><span data-stu-id="d4e3b-119">*expression*=*element*.id</span></span>

<span data-ttu-id="d4e3b-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="d4e3b-120">**Remarks**</span></span>

<span data-ttu-id="d4e3b-121">Use el **identificador** para hacer referencia a una imagen específica.</span><span class="sxs-lookup"><span data-stu-id="d4e3b-121">Use **ID** to refer to a specific image.</span></span> <span data-ttu-id="d4e3b-122">Una vez que haya creado una imagen y dado un identificador, puede utilizar el nombre de identificador cuando desee manipular la imagen.</span><span class="sxs-lookup"><span data-stu-id="d4e3b-122">Once you have created an image and given it an ID, you can use the ID name when you want to manipulate the image.</span></span>

<span data-ttu-id="d4e3b-123">**Atributo estándar de VML**</span><span class="sxs-lookup"><span data-stu-id="d4e3b-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="d4e3b-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="d4e3b-124">**Example**</span></span>

<span data-ttu-id="d4e3b-125">La forma tiene un identificador de **ImageData** denominado "mi imagen".</span><span class="sxs-lookup"><span data-stu-id="d4e3b-125">The shape has an **ImageData** ID called "myimage".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata id="myimage" src="kids.jpg"/>
   </v:shape>
```



 

 