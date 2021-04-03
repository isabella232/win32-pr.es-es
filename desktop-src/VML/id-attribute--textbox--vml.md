---
title: Atributo ID (TextBox) (VML)
description: Atributo ID (TextBox) (VML)
ms.assetid: b9eb75cc-4d0a-4e83-a897-e35995ae7c53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b39ac566e7b619c31cb12f4657bd86020dc12cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904682"
---
# <a name="id-attribute-textboxvml"></a><span data-ttu-id="4a2e9-103">Atributo ID (TextBox) (VML)</span><span class="sxs-lookup"><span data-stu-id="4a2e9-103">ID Attribute (TextBox)(VML)</span></span>

<span data-ttu-id="4a2e9-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4a2e9-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4a2e9-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4a2e9-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4a2e9-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4a2e9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4a2e9-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4a2e9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4a2e9-110">Nombre que proporciona un identificador único para un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-110">A name that provides a unique identifier for a textbox.</span></span> <span data-ttu-id="4a2e9-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4a2e9-111">Read/write.</span></span> <span data-ttu-id="4a2e9-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-112">**String**.</span></span>

<span data-ttu-id="4a2e9-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="4a2e9-113">**Applies To**</span></span>

[<span data-ttu-id="4a2e9-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="4a2e9-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="4a2e9-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="4a2e9-115">**Tag Syntax**</span></span>

<span data-ttu-id="4a2e9-116"><v: ID. de *elemento* = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="4a2e9-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="4a2e9-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="4a2e9-117">**Script Syntax**</span></span>

<span data-ttu-id="4a2e9-118">*Element* . ID = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="4a2e9-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="4a2e9-119">*expresión* = de identificador de *elemento*</span><span class="sxs-lookup"><span data-stu-id="4a2e9-119">*expression*=*element*.id</span></span>

<span data-ttu-id="4a2e9-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="4a2e9-120">**Remarks**</span></span>

<span data-ttu-id="4a2e9-121">Use el **identificador** para hacer referencia a un cuadro de texto específico.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-121">Use **ID** to refer to a specific textbox.</span></span> <span data-ttu-id="4a2e9-122">Una vez que haya creado un cuadro de texto y dado un identificador, puede utilizar el nombre de identificador cuando desee manipular el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="4a2e9-122">Once you have created a textbox and given it an ID, you can use the ID name when you want to manipulate the textbox.</span></span>

<span data-ttu-id="4a2e9-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="4a2e9-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="4a2e9-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="4a2e9-124">**Example**</span></span>

<span data-ttu-id="4a2e9-125">La forma tiene un ID. de cuadro de texto denominado "mytextbox".</span><span class="sxs-lookup"><span data-stu-id="4a2e9-125">The shape has a textbox ID called "mytextbox".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 