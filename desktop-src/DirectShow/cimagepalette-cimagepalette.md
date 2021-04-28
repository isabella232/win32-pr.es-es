---
description: 'Constructor CImagePalette.CImagePalette: método constructor.'
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Constructor CImagePalette.CImagePalette (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CImagePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5021b165a8fa47bedc7961657d7cdbfa07af301d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085683"
---
# <a name="cimagepalettecimagepalette-constructor"></a><span data-ttu-id="450a1-103">Constructor CImagePalette.CImagePalette</span><span class="sxs-lookup"><span data-stu-id="450a1-103">CImagePalette.CImagePalette constructor</span></span>

<span data-ttu-id="450a1-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="450a1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="450a1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="450a1-105">Syntax</span></span>


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a><span data-ttu-id="450a1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="450a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="450a1-107">*pBaseFilter*</span><span class="sxs-lookup"><span data-stu-id="450a1-107">*pBaseFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="450a1-108">Puntero al filtro propietario.</span><span class="sxs-lookup"><span data-stu-id="450a1-108">Pointer to owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="450a1-109">*pBaseWindow*</span><span class="sxs-lookup"><span data-stu-id="450a1-109">*pBaseWindow*</span></span> 
</dt> <dd>

<span data-ttu-id="450a1-110">Puntero a un **objeto CBaseWindow,** que administra la ventana donde se realiza la paleta.</span><span class="sxs-lookup"><span data-stu-id="450a1-110">Pointer to a **CBaseWindow** object, which manages the window where the palette is realized.</span></span> <span data-ttu-id="450a1-111">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="450a1-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="450a1-112">*pDrawImage*</span><span class="sxs-lookup"><span data-stu-id="450a1-112">*pDrawImage*</span></span> 
</dt> <dd>

<span data-ttu-id="450a1-113">Puntero a un **objeto CDrawImage,** que dibuja la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="450a1-113">Pointer to a **CDrawImage** object, which draws the video image.</span></span> <span data-ttu-id="450a1-114">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="450a1-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="450a1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="450a1-115">Requirements</span></span>



| <span data-ttu-id="450a1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="450a1-116">Requirement</span></span> | <span data-ttu-id="450a1-117">Value</span><span class="sxs-lookup"><span data-stu-id="450a1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="450a1-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="450a1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="450a1-119"><dt>Winutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="450a1-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="450a1-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="450a1-120">Library</span></span><br/> | <dl> <span data-ttu-id="450a1-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="450a1-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="450a1-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="450a1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="450a1-123">**CImagePalette (clase)**</span><span class="sxs-lookup"><span data-stu-id="450a1-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




