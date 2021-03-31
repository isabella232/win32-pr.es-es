---
description: El método ShowMenu muestra el menú especificado en la pantalla.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: Método ShowMenu
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c64b2a08c8881001cc47c972ad8cc865af8a174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806241"
---
# <a name="showmenu-method"></a><span data-ttu-id="f4539-103">Método ShowMenu</span><span class="sxs-lookup"><span data-stu-id="f4539-103">ShowMenu Method</span></span>

> [!Note]  
> <span data-ttu-id="f4539-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f4539-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f4539-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="f4539-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f4539-106">El `ShowMenu` método muestra el menú especificado en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="f4539-106">The `ShowMenu` method displays the specified menu on the screen.</span></span>

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a><span data-ttu-id="f4539-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4539-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4539-108"><span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*</span><span class="sxs-lookup"><span data-stu-id="f4539-108"><span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*</span></span>
</dt> <dd>

<span data-ttu-id="f4539-109">Especifica el identificador de menú como un entero.</span><span class="sxs-lookup"><span data-stu-id="f4539-109">Specifies the menu ID as an Integer.</span></span>



| <span data-ttu-id="f4539-110">Value</span><span class="sxs-lookup"><span data-stu-id="f4539-110">Value</span></span> | <span data-ttu-id="f4539-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4539-111">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="f4539-112">2</span><span class="sxs-lookup"><span data-stu-id="f4539-112">2</span></span>     | <span data-ttu-id="f4539-113">Título (superior)</span><span class="sxs-lookup"><span data-stu-id="f4539-113">Title (Top)</span></span> |
| <span data-ttu-id="f4539-114">3</span><span class="sxs-lookup"><span data-stu-id="f4539-114">3</span></span>     | <span data-ttu-id="f4539-115">Root</span><span class="sxs-lookup"><span data-stu-id="f4539-115">Root</span></span>        |
| <span data-ttu-id="f4539-116">4</span><span class="sxs-lookup"><span data-stu-id="f4539-116">4</span></span>     | <span data-ttu-id="f4539-117">Subimagen</span><span class="sxs-lookup"><span data-stu-id="f4539-117">Subpicture</span></span>  |
| <span data-ttu-id="f4539-118">5</span><span class="sxs-lookup"><span data-stu-id="f4539-118">5</span></span>     | <span data-ttu-id="f4539-119">Audio</span><span class="sxs-lookup"><span data-stu-id="f4539-119">Audio</span></span>       |
| <span data-ttu-id="f4539-120">6</span><span class="sxs-lookup"><span data-stu-id="f4539-120">6</span></span>     | <span data-ttu-id="f4539-121">Ángulo</span><span class="sxs-lookup"><span data-stu-id="f4539-121">Angle</span></span>       |
| <span data-ttu-id="f4539-122">7</span><span class="sxs-lookup"><span data-stu-id="f4539-122">7</span></span>     | <span data-ttu-id="f4539-123">Capítulo</span><span class="sxs-lookup"><span data-stu-id="f4539-123">Chapter</span></span>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4539-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4539-124">Return Value</span></span>

<span data-ttu-id="f4539-125">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f4539-125">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4539-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4539-126">Remarks</span></span>

<span data-ttu-id="f4539-127">Los nombres de los menús de DVD pueden resultar confusos.</span><span class="sxs-lookup"><span data-stu-id="f4539-127">DVD menu names can be somewhat confusing.</span></span> <span data-ttu-id="f4539-128">El menú de título es otro nombre para el menú administrador de vídeo, el menú principal para todo el disco; en general, se enumeran todos los conjuntos de títulos de vídeo disponibles en el disco. El menú raíz es el menú de un conjunto de títulos de vídeo, que puede contener un título o un grupo de títulos.</span><span class="sxs-lookup"><span data-stu-id="f4539-128">The title menu is another name for the Video Manager Menu, the main menu for the entire disc; it generally lists all the video title sets available on the disc. The root menu is the menu for one video title set, which can contain one title or a group of titles.</span></span> <span data-ttu-id="f4539-129">Todos los títulos de un conjunto de títulos comparten los mismos menús de subimagen, audio y ángulo.</span><span class="sxs-lookup"><span data-stu-id="f4539-129">All the titles in a title set share the same Subpicture, Audio, and Angle menus.</span></span>

 

 



