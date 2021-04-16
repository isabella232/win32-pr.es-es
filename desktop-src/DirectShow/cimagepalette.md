---
description: La clase CImagePalette administra las paletas de representadores de vídeo. Se puede usar para crear una paleta lógica a partir de un formato de vídeo. Esta clase está pensada para usarse con las clases CBaseWindow y CDrawImage, por lo que es algo especializado.
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: Clase CImagePalette
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette
api_type:
- COM
api_location: ''
ms.openlocfilehash: 696c51e4918815e18accbadd66c764493dc0b98e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677061"
---
# <a name="cimagepalette-class"></a><span data-ttu-id="d2f78-105">Clase CImagePalette</span><span class="sxs-lookup"><span data-stu-id="d2f78-105">CImagePalette class</span></span>

<span data-ttu-id="d2f78-106">La `CImagePalette` clase administra las paletas para los representadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d2f78-106">The `CImagePalette` class manages palettes for video renderers.</span></span> <span data-ttu-id="d2f78-107">Se puede usar para crear una paleta lógica a partir de un formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d2f78-107">It can be used to create a logical palette from a video format.</span></span> <span data-ttu-id="d2f78-108">Esta clase está pensada para usarse con las clases [**CBaseWindow**](cbasewindow.md) y [**CDrawImage**](cdrawimage.md) , por lo que es algo especializado.</span><span class="sxs-lookup"><span data-stu-id="d2f78-108">This class is intended to be used with the [**CBaseWindow**](cbasewindow.md) and [**CDrawImage**](cdrawimage.md) classes, so it is somewhat specialized.</span></span>



| <span data-ttu-id="d2f78-109">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="d2f78-109">Protected Member Variables</span></span>                                       | <span data-ttu-id="d2f78-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2f78-110">Description</span></span>                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2f78-111">**m \_ hPalette**</span><span class="sxs-lookup"><span data-stu-id="d2f78-111">**m\_hPalette**</span></span>](cimagepalette-m-hpalette.md)                  | <span data-ttu-id="d2f78-112">Identificador de la paleta lógica que este objeto administra.</span><span class="sxs-lookup"><span data-stu-id="d2f78-112">Handle to the logical palette that this object manages.</span></span>                                        |
| [<span data-ttu-id="d2f78-113">**m \_ pBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="d2f78-113">**m\_pBaseWindow**</span></span>](cimagepalette-m-pbasewindow.md)            | <span data-ttu-id="d2f78-114">Puntero al objeto **CBaseWindow** que administra la ventana.</span><span class="sxs-lookup"><span data-stu-id="d2f78-114">Pointer to the **CBaseWindow** object that manages the window.</span></span>                                 |
| [<span data-ttu-id="d2f78-115">**m \_ pDrawImage**</span><span class="sxs-lookup"><span data-stu-id="d2f78-115">**m\_pDrawImage**</span></span>](cimagepalette-m-pdrawimage.md)              | <span data-ttu-id="d2f78-116">Puntero al objeto **CDrawImage** que dibuja la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d2f78-116">Pointer to the **CDrawImage** object that draws the video image.</span></span>                               |
| [<span data-ttu-id="d2f78-117">**m \_ pFilter**</span><span class="sxs-lookup"><span data-stu-id="d2f78-117">**m\_pFilter**</span></span>](cimagepalette-m-pfilter.md)                    | <span data-ttu-id="d2f78-118">Puntero al filtro propietario.</span><span class="sxs-lookup"><span data-stu-id="d2f78-118">Pointer to the owning filter.</span></span>                                                                  |
| <span data-ttu-id="d2f78-119">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="d2f78-119">Public Methods</span></span>                                                   | <span data-ttu-id="d2f78-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2f78-120">Description</span></span>                                                                                    |
| [<span data-ttu-id="d2f78-121">**CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="d2f78-121">**CImagePalette**</span></span>](cimagepalette-cimagepalette.md)             | <span data-ttu-id="d2f78-122">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="d2f78-122">Constructor method.</span></span>                                                                            |
| [<span data-ttu-id="d2f78-123">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="d2f78-123">**CopyPalette**</span></span>](cimagepalette-copypalette.md)                 | <span data-ttu-id="d2f78-124">Copia la paleta de cualquier estructura de **videoinfo** en cualquier estructura de **videoinformación** de paleta.</span><span class="sxs-lookup"><span data-stu-id="d2f78-124">Copies the palette from any **VIDEOINFO** structure to any palettized **VIDEOINFO** structure.</span></span> |
| [<span data-ttu-id="d2f78-125">**MakeIdentityPalette**</span><span class="sxs-lookup"><span data-stu-id="d2f78-125">**MakeIdentityPalette**</span></span>](cimagepalette-makeidentitypalette.md) | <span data-ttu-id="d2f78-126">Intenta crear una paleta que se asigna directamente a la paleta seleccionada en el dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="d2f78-126">Attempts to make a palette that maps directly to the palette selected in the display device.</span></span>   |
| [<span data-ttu-id="d2f78-127">**MakePalette**</span><span class="sxs-lookup"><span data-stu-id="d2f78-127">**MakePalette**</span></span>](cimagepalette-makepalette.md)                 | <span data-ttu-id="d2f78-128">Crea una paleta lógica a partir de la tabla de colores en un formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d2f78-128">Creates a logical palette from the color table in a video format.</span></span>                              |
| [<span data-ttu-id="d2f78-129">**PreparePalette**</span><span class="sxs-lookup"><span data-stu-id="d2f78-129">**PreparePalette**</span></span>](cimagepalette-preparepalette.md)           | <span data-ttu-id="d2f78-130">Configura una paleta basada en un tipo de medio del filtro propietario.</span><span class="sxs-lookup"><span data-stu-id="d2f78-130">Sets up a palette, based on a media type from the owning filter.</span></span>                               |
| [<span data-ttu-id="d2f78-131">**RemovePalette**</span><span class="sxs-lookup"><span data-stu-id="d2f78-131">**RemovePalette**</span></span>](cimagepalette-removepalette.md)             | <span data-ttu-id="d2f78-132">Elimina la paleta lógica existente.</span><span class="sxs-lookup"><span data-stu-id="d2f78-132">Deletes the existing logical palette.</span></span>                                                          |



 

 

 



