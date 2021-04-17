---
description: Los descodificadores que utilizan la aceleración de vídeo de DirectX (DXVA) usan los siguientes subtipos.
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: Subtipos de vídeo de aceleración de vídeo de DirectX (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0df0f079e795638c6802570c95e2468209a7256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680269"
---
# <a name="directx-video-acceleration-video-subtypes"></a><span data-ttu-id="72784-103">Subtipos de vídeo de aceleración de vídeo de DirectX</span><span class="sxs-lookup"><span data-stu-id="72784-103">DirectX Video Acceleration Video Subtypes</span></span>

<span data-ttu-id="72784-104">Los descodificadores que utilizan la aceleración de vídeo de DirectX (DXVA) usan los siguientes subtipos.</span><span class="sxs-lookup"><span data-stu-id="72784-104">The following subtypes are used by decoders that are using DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="72784-105">AI44 y IA44 son superficies con un valor de bits por píxel de 8.</span><span class="sxs-lookup"><span data-stu-id="72784-105">AI44 and IA44 are surfaces with a bits-per-pixel value of 8.</span></span> <span data-ttu-id="72784-106">Hay 4 bits de I y 4 bits de *un*. *I* representa un índice en una paleta YUV de 16 entradas.</span><span class="sxs-lookup"><span data-stu-id="72784-106">There are 4 bits of I and 4 bits of *A*. *I* represents an index into a 16-entry YUV palette.</span></span> <span data-ttu-id="72784-107">*Representa 4* bits de información de transparencia (también conocido como alfa por píxel).</span><span class="sxs-lookup"><span data-stu-id="72784-107">*A* represents 4 bits of transparency information (also known as per-pixel-alpha).</span></span> <span data-ttu-id="72784-108">Por lo tanto, las superficies AI44 y IA44 permiten 16 colores diferentes con 16 valores de transparencia distintos, o 256 representaciones de píxeles diferentes.</span><span class="sxs-lookup"><span data-stu-id="72784-108">Therefore, AI44 and IA44 surfaces allow for 16 different colors at 16 different transparency values, or 256 different pixel representations.</span></span> <span data-ttu-id="72784-109">Con AI44, el alfa se almacena en el HI-Nibble, en IA44, el alfa se almacena en el medio de recorte.</span><span class="sxs-lookup"><span data-stu-id="72784-109">With AI44 the alpha is stored in the hi-nibble, in IA44 the alpha is stored in the lo-nibble.</span></span> <span data-ttu-id="72784-110">Ambos formatos son muy útiles para imágenes de subimagen de DVD e imágenes de Line21 e teletexto.</span><span class="sxs-lookup"><span data-stu-id="72784-110">Both formats are very useful for DVD sub-picture images and Line21 and Teletext images.</span></span> <span data-ttu-id="72784-111">Microsoft prefiere la versión de AI44 porque es algo más fácil generar texto con este formato.</span><span class="sxs-lookup"><span data-stu-id="72784-111">Microsoft prefers the AI44 version because it is slightly easier to generate text using this format.</span></span>

| <span data-ttu-id="72784-112">Subtype</span><span class="sxs-lookup"><span data-stu-id="72784-112">Subtype</span></span>            | <span data-ttu-id="72784-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="72784-113">Description</span></span>                                                 |
|--------------------|-------------------------------------------------------------|
| <span data-ttu-id="72784-114">MEDIASUBTYPE \_ AI44</span><span class="sxs-lookup"><span data-stu-id="72784-114">MEDIASUBTYPE\_AI44</span></span> | <span data-ttu-id="72784-115">Para subimágenes y superposiciones de texto.</span><span class="sxs-lookup"><span data-stu-id="72784-115">For subpicture and text overlays.</span></span> <span data-ttu-id="72784-116">Vea la descripción anterior.</span><span class="sxs-lookup"><span data-stu-id="72784-116">See previous description.</span></span> |
| <span data-ttu-id="72784-117">MEDIASUBTYPE \_ IA44</span><span class="sxs-lookup"><span data-stu-id="72784-117">MEDIASUBTYPE\_IA44</span></span> | <span data-ttu-id="72784-118">Para subimágenes y superposiciones de texto.</span><span class="sxs-lookup"><span data-stu-id="72784-118">For subpicture and text overlays.</span></span> <span data-ttu-id="72784-119">Vea la descripción anterior.</span><span class="sxs-lookup"><span data-stu-id="72784-119">See previous description.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="72784-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72784-120">Requirements</span></span>



| <span data-ttu-id="72784-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="72784-121">Requirement</span></span> | <span data-ttu-id="72784-122">Value</span><span class="sxs-lookup"><span data-stu-id="72784-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="72784-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72784-123">Header</span></span><br/> | <dl> <span data-ttu-id="72784-124"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="72784-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72784-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="72784-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72784-126">Subtipos de vídeo</span><span class="sxs-lookup"><span data-stu-id="72784-126">Video Subtypes</span></span>](video-subtypes.md)
</dt> </dl>

 

 




