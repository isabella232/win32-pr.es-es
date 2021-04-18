---
description: El método SetRealize especifica si la ventana observa las paletas.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: Método CBaseWindow. SetRealize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 587e54cdbbbf57ddb4cf52e2d5dfb916acaee22d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681178"
---
# <a name="cbasewindowsetrealize-method"></a><span data-ttu-id="852d9-103">CBaseWindow. SetRealize, método</span><span class="sxs-lookup"><span data-stu-id="852d9-103">CBaseWindow.SetRealize method</span></span>

<span data-ttu-id="852d9-104">El `SetRealize` método especifica si la ventana observa las paletas.</span><span class="sxs-lookup"><span data-stu-id="852d9-104">The `SetRealize` method specifies whether the window realizes palettes.</span></span>

## <a name="syntax"></a><span data-ttu-id="852d9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="852d9-105">Syntax</span></span>


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a><span data-ttu-id="852d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="852d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="852d9-107">*bRealize*</span><span class="sxs-lookup"><span data-stu-id="852d9-107">*bRealize*</span></span> 
</dt> <dd>

<span data-ttu-id="852d9-108">Valor booleano que especifica si se deben obtener las paletas.</span><span class="sxs-lookup"><span data-stu-id="852d9-108">Boolean value that specifies whether to realize palettes.</span></span> <span data-ttu-id="852d9-109">Si **es true**, el método [**CBaseWindow:: SetPalette**](cbasewindow-setpalette.md) obtiene las paletas.</span><span class="sxs-lookup"><span data-stu-id="852d9-109">If **TRUE**, the [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) method realizes palettes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="852d9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="852d9-110">Return value</span></span>

<span data-ttu-id="852d9-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="852d9-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="852d9-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="852d9-112">Remarks</span></span>

<span data-ttu-id="852d9-113">De forma predeterminada, el método **SetPalette** obtiene la paleta especificada.</span><span class="sxs-lookup"><span data-stu-id="852d9-113">By default, the **SetPalette** method realizes the specified palette.</span></span> <span data-ttu-id="852d9-114">Llame a este método para cambiar el comportamiento predeterminado, de modo que las paletas estén seleccionadas pero no se hayan realizado.</span><span class="sxs-lookup"><span data-stu-id="852d9-114">Call this method to change the default behavior, so that palettes are selected but not realized.</span></span> <span data-ttu-id="852d9-115">Este método establece la variable miembro [**CBaseWindow:: m \_ bNoRealize**](cbasewindow-m-bnorealize.md) .</span><span class="sxs-lookup"><span data-stu-id="852d9-115">This method sets the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="852d9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="852d9-116">Requirements</span></span>



| <span data-ttu-id="852d9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="852d9-117">Requirement</span></span> | <span data-ttu-id="852d9-118">Value</span><span class="sxs-lookup"><span data-stu-id="852d9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="852d9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="852d9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="852d9-120"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="852d9-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="852d9-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="852d9-121">Library</span></span><br/> | <dl> <span data-ttu-id="852d9-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="852d9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="852d9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="852d9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="852d9-124">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="852d9-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




