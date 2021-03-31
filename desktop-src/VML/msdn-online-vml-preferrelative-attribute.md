---
title: Atributo PreferRelative de VML
description: Atributo PreferRelative de VML
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa425321c1937c4df1bb766c554dbd73cc384b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077846"
---
# <a name="vml-preferrelative-attribute"></a><span data-ttu-id="1f0b5-103">Atributo PreferRelative de VML</span><span class="sxs-lookup"><span data-stu-id="1f0b5-103">VML PreferRelative Attribute</span></span>

<span data-ttu-id="1f0b5-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1f0b5-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1f0b5-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1f0b5-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1f0b5-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1f0b5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1f0b5-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1f0b5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1f0b5-110">Determina si el tamaño original de un objeto se guarda después de volver a aplicar el formato.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-110">Determines whether the original size of an object is saved after reformatting.</span></span> <span data-ttu-id="1f0b5-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1f0b5-111">Read/write.</span></span> <span data-ttu-id="1f0b5-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-112">**VgTriState**.</span></span>

<span data-ttu-id="1f0b5-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-113">**Applies To**</span></span>

[<span data-ttu-id="1f0b5-114">Forma</span><span class="sxs-lookup"><span data-stu-id="1f0b5-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="1f0b5-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-115">**Tag Syntax**</span></span>

<span data-ttu-id="1f0b5-116"><v: *Element* o:preferrelative = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="1f0b5-116"><v: *element* o:preferrelative=" *expression* "></span></span>

<span data-ttu-id="1f0b5-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-117">**Remarks**</span></span>

<span data-ttu-id="1f0b5-118">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-118">The default is **False**.</span></span> <span data-ttu-id="1f0b5-119">Si **es true**, el tamaño original del objeto se almacenará y todo el cambio de tamaño se basará en un porcentaje de ese tamaño original.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-119">If **True**, the original size of the object will be stored and all resizing will be based on a percentage of that original size.</span></span> <span data-ttu-id="1f0b5-120">De lo contrario, cada cambio de tamaño restablecerá la escala al 100%.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-120">Otherwise, each resizing will reset the scale to 100%.</span></span>

<span data-ttu-id="1f0b5-121">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="1f0b5-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="1f0b5-122">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="1f0b5-122">**Example**</span></span>

<span data-ttu-id="1f0b5-123">Si se cambia el tamaño de la forma, no se almacenará el tamaño original.</span><span class="sxs-lookup"><span data-stu-id="1f0b5-123">If the shape is resized, the original size will not be stored.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 