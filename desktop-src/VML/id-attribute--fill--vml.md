---
title: ID (atributo, Fill) (VML)
description: ID (atributo, Fill) (VML)
ms.assetid: 56865772-51bd-4729-8e56-6b00e3c6bed0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820c4f7a23cf940c199f27243d8ad5601390a84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078026"
---
# <a name="id-attribute-fillvml"></a><span data-ttu-id="bc5fa-103">ID (atributo, Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="bc5fa-103">ID Attribute (Fill)(VML)</span></span>

<span data-ttu-id="bc5fa-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bc5fa-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bc5fa-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="bc5fa-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bc5fa-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="bc5fa-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bc5fa-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="bc5fa-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bc5fa-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bc5fa-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bc5fa-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bc5fa-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bc5fa-110">Nombre que proporciona un identificador único para un relleno.</span><span class="sxs-lookup"><span data-stu-id="bc5fa-110">A name that provides a unique identifier for a fill.</span></span> <span data-ttu-id="bc5fa-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bc5fa-111">Read/write.</span></span> <span data-ttu-id="bc5fa-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="bc5fa-112">**String**.</span></span>

<span data-ttu-id="bc5fa-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="bc5fa-113">**Applies To**</span></span>

[<span data-ttu-id="bc5fa-114">Fill</span><span class="sxs-lookup"><span data-stu-id="bc5fa-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="bc5fa-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="bc5fa-115">**Tag Syntax**</span></span>

<span data-ttu-id="bc5fa-116"><v: ID. de *elemento* = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="bc5fa-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="bc5fa-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="bc5fa-117">**Script Syntax**</span></span>

<span data-ttu-id="bc5fa-118">*Element* . ID = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="bc5fa-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="bc5fa-119">*expresión* = de identificador de *elemento*</span><span class="sxs-lookup"><span data-stu-id="bc5fa-119">*expression*=*element*.id</span></span>

<span data-ttu-id="bc5fa-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="bc5fa-120">**Remarks**</span></span>

<span data-ttu-id="bc5fa-121">Use el **identificador** para hacer referencia a un relleno específico.</span><span class="sxs-lookup"><span data-stu-id="bc5fa-121">Use **ID** to refer to a specific fill.</span></span> <span data-ttu-id="bc5fa-122">Una vez que haya creado un relleno y dado un identificador, puede utilizar el nombre de identificador cuando desee manipular el relleno.</span><span class="sxs-lookup"><span data-stu-id="bc5fa-122">Once you have created a fill and given it an ID, you can use the ID name when you want to manipulate the fill.</span></span>

<span data-ttu-id="bc5fa-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="bc5fa-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="bc5fa-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="bc5fa-124">**Example**</span></span>

<span data-ttu-id="bc5fa-125">La forma tiene un ID. de relleno denominado "alfill".</span><span class="sxs-lookup"><span data-stu-id="bc5fa-125">The shape has a fill ID called "myfill".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill id="myfill"/>
   </v:shape>
```



 

 