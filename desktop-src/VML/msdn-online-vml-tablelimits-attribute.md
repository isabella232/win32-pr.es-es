---
title: Atributo TableLimits de VML
description: Atributo TableLimits de VML
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b35a7449cc2f348e6040161c1fb599c29972803
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791835"
---
# <a name="vml-tablelimits-attribute"></a><span data-ttu-id="f0418-103">Atributo TableLimits de VML</span><span class="sxs-lookup"><span data-stu-id="f0418-103">VML TableLimits Attribute</span></span>

<span data-ttu-id="f0418-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f0418-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f0418-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="f0418-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f0418-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="f0418-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f0418-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="f0418-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f0418-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f0418-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f0418-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f0418-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f0418-110">Lista de valores de alto mínimo para cada fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="f0418-110">List of minimum height values for each row in a table.</span></span> <span data-ttu-id="f0418-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0418-111">Read/write.</span></span> <span data-ttu-id="f0418-112">**VgLengthArray**.</span><span class="sxs-lookup"><span data-stu-id="f0418-112">**VgLengthArray**.</span></span>

<span data-ttu-id="f0418-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="f0418-113">**Applies To**</span></span>

[<span data-ttu-id="f0418-114">Forma</span><span class="sxs-lookup"><span data-stu-id="f0418-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="f0418-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="f0418-115">**Tag Syntax**</span></span>

<span data-ttu-id="f0418-116"><v: *Element* o:tablelimits = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="f0418-116"><v: *element* o:tablelimits=" *expression* "></span></span>

<span data-ttu-id="f0418-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="f0418-117">**Remarks**</span></span>

<span data-ttu-id="f0418-118">Usado por Microsoft PowerPoint para tablas nativas.</span><span class="sxs-lookup"><span data-stu-id="f0418-118">Used by Microsoft PowerPoint for native tables.</span></span> <span data-ttu-id="f0418-119">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="f0418-119">Default value is **Null**.</span></span>

<span data-ttu-id="f0418-120">Aunque el valor se almacena en una forma, el atributo solo es útil cuando la tabla está formada por formas agrupadas.</span><span class="sxs-lookup"><span data-stu-id="f0418-120">Even though the value is stored in a shape, the attribute is only useful when the table is made up of shapes that are grouped.</span></span> <span data-ttu-id="f0418-121">Cuando se agrega texto a las celdas de la tabla, puede aumentar el alto de la fila.</span><span class="sxs-lookup"><span data-stu-id="f0418-121">When text is added to table cells, the row height may increase.</span></span> <span data-ttu-id="f0418-122">El atributo **TableLimits** almacena el alto de la fila original para que, si se elimina el texto, el alto de la fila no se sitúe por debajo del valor original.</span><span class="sxs-lookup"><span data-stu-id="f0418-122">The **TableLimits** attribute stores the original row height so that if text is deleted, the row height will not fall below the original value.</span></span>

<span data-ttu-id="f0418-123">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="f0418-123">*Microsoft Office Extensions Attribute*</span></span>

 

 