---
title: Atributo de cadena VML
description: Atributo de cadena VML
ms.assetid: 99609814-29c9-4349-9509-8c91f2aaeff5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6c172b4ca1f5049a3e89528a2333378164f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420982"
---
# <a name="vml-string-attribute"></a><span data-ttu-id="a38f9-103">Atributo de cadena VML</span><span class="sxs-lookup"><span data-stu-id="a38f9-103">VML String Attribute</span></span>

<span data-ttu-id="a38f9-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a38f9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a38f9-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="a38f9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a38f9-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="a38f9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a38f9-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="a38f9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a38f9-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a38f9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a38f9-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a38f9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a38f9-110">Define el texto de la ruta de acceso del texto.</span><span class="sxs-lookup"><span data-stu-id="a38f9-110">Defines the text of the text path.</span></span> <span data-ttu-id="a38f9-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a38f9-111">Read/write.</span></span> <span data-ttu-id="a38f9-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="a38f9-112">**String**.</span></span>

<span data-ttu-id="a38f9-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="a38f9-113">**Applies To**</span></span>

[<span data-ttu-id="a38f9-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="a38f9-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="a38f9-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="a38f9-115">**Tag Syntax**</span></span>

<span data-ttu-id="a38f9-116"><v: *Element* String = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="a38f9-116"><v: *element* string=" *expression* "></span></span>

<span data-ttu-id="a38f9-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="a38f9-117">**Script Syntax**</span></span>

<span data-ttu-id="a38f9-118">*Element* . String = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="a38f9-118">*element* .string="*expression*"</span></span>

<span data-ttu-id="a38f9-119">*expresión* = de *elemento*. String</span><span class="sxs-lookup"><span data-stu-id="a38f9-119">*expression*=*element*.string</span></span>

<span data-ttu-id="a38f9-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="a38f9-120">**Remarks**</span></span>

<span data-ttu-id="a38f9-121">Debe asignar una cadena de texto para mostrar texto en una ruta de acceso de texto.</span><span class="sxs-lookup"><span data-stu-id="a38f9-121">You must assign a text string to display text on a text path.</span></span>

<span data-ttu-id="a38f9-122">Atributo estándar de VML</span><span class="sxs-lookup"><span data-stu-id="a38f9-122">VML Standard Attribute</span></span>

<span data-ttu-id="a38f9-123">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="a38f9-123">**Example**</span></span>

<span data-ttu-id="a38f9-124">La cadena que se mostrará es "texto VML".</span><span class="sxs-lookup"><span data-stu-id="a38f9-124">The string that will be displayed is "VML Text".</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 