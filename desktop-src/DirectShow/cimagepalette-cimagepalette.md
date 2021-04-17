---
description: Método de constructor.
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Constructor CImagePalette. CImagePalette (Winutil. h)
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
ms.openlocfilehash: 38b5766617e1d17fa3917048c2fb845b5194cc42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681007"
---
# <a name="cimagepalettecimagepalette-constructor"></a><span data-ttu-id="0bcf5-103">Constructor CImagePalette. CImagePalette</span><span class="sxs-lookup"><span data-stu-id="0bcf5-103">CImagePalette.CImagePalette constructor</span></span>

<span data-ttu-id="0bcf5-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="0bcf5-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bcf5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bcf5-105">Syntax</span></span>


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a><span data-ttu-id="0bcf5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0bcf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bcf5-107">*pBaseFilter*</span><span class="sxs-lookup"><span data-stu-id="0bcf5-107">*pBaseFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="0bcf5-108">Puntero al filtro propietario.</span><span class="sxs-lookup"><span data-stu-id="0bcf5-108">Pointer to owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="0bcf5-109">*pBaseWindow*</span><span class="sxs-lookup"><span data-stu-id="0bcf5-109">*pBaseWindow*</span></span> 
</dt> <dd>

<span data-ttu-id="0bcf5-110">Puntero a un objeto **CBaseWindow** , que administra la ventana donde se realiza la paleta.</span><span class="sxs-lookup"><span data-stu-id="0bcf5-110">Pointer to a **CBaseWindow** object, which manages the window where the palette is realized.</span></span> <span data-ttu-id="0bcf5-111">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0bcf5-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0bcf5-112">*pDrawImage*</span><span class="sxs-lookup"><span data-stu-id="0bcf5-112">*pDrawImage*</span></span> 
</dt> <dd>

<span data-ttu-id="0bcf5-113">Puntero a un objeto **CDrawImage** que dibuja la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0bcf5-113">Pointer to a **CDrawImage** object, which draws the video image.</span></span> <span data-ttu-id="0bcf5-114">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0bcf5-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0bcf5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bcf5-115">Requirements</span></span>



| <span data-ttu-id="0bcf5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bcf5-116">Requirement</span></span> | <span data-ttu-id="0bcf5-117">Value</span><span class="sxs-lookup"><span data-stu-id="0bcf5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bcf5-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0bcf5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0bcf5-119"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0bcf5-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0bcf5-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0bcf5-120">Library</span></span><br/> | <dl> <span data-ttu-id="0bcf5-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0bcf5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bcf5-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bcf5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bcf5-123">**Clase CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="0bcf5-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




