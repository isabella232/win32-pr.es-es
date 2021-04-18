---
title: ID (atributo, Path) (VML)
description: ID (atributo, Path) (VML)
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbd5d8d9acdcafaf015354dc4c99f3703034e89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149286"
---
# <a name="id-attribute-pathvml"></a><span data-ttu-id="691bf-103">ID (atributo, Path) (VML)</span><span class="sxs-lookup"><span data-stu-id="691bf-103">ID Attribute (Path)(VML)</span></span>

<span data-ttu-id="691bf-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="691bf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="691bf-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="691bf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="691bf-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="691bf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="691bf-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="691bf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="691bf-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="691bf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="691bf-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="691bf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="691bf-110">Nombre que proporciona un identificador único para una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="691bf-110">A name that provides a unique identifier for a path.</span></span> <span data-ttu-id="691bf-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="691bf-111">Read/write.</span></span> <span data-ttu-id="691bf-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="691bf-112">**String**.</span></span>

<span data-ttu-id="691bf-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="691bf-113">**Applies To**</span></span>

[<span data-ttu-id="691bf-114">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="691bf-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="691bf-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="691bf-115">**Tag Syntax**</span></span>

<span data-ttu-id="691bf-116"><v: ID. de *elemento* = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="691bf-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="691bf-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="691bf-117">**Script Syntax**</span></span>

<span data-ttu-id="691bf-118">*Element* . ID = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="691bf-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="691bf-119">*expresión* = de identificador de *elemento*</span><span class="sxs-lookup"><span data-stu-id="691bf-119">*expression*=*element*.id</span></span>

<span data-ttu-id="691bf-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="691bf-120">**Remarks**</span></span>

<span data-ttu-id="691bf-121">Use el **identificador** para hacer referencia a una ruta de acceso específica.</span><span class="sxs-lookup"><span data-stu-id="691bf-121">Use **ID** to refer to a specific path.</span></span> <span data-ttu-id="691bf-122">Una vez que haya creado una ruta de acceso y dado un identificador, puede utilizar el nombre de identificador cuando desee manipular la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="691bf-122">Once you have created a path and given it an ID, you can use the ID name when you want to manipulate the path.</span></span>

<span data-ttu-id="691bf-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="691bf-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="691bf-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="691bf-124">**Example**</span></span>

<span data-ttu-id="691bf-125">La forma tiene un identificador de ruta de acceso denominado "myPath".</span><span class="sxs-lookup"><span data-stu-id="691bf-125">The shape has a path ID called "myPath".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 