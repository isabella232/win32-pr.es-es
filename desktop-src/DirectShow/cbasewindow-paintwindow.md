---
description: El método PaintWindow hace que se vuelva a dibujar la ventana.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: Método CBaseWindow. PaintWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PaintWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0932422f85cb31d587485976dfacbaa51e2bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661233"
---
# <a name="cbasewindowpaintwindow-method"></a><span data-ttu-id="a22f0-103">CBaseWindow. PaintWindow, método</span><span class="sxs-lookup"><span data-stu-id="a22f0-103">CBaseWindow.PaintWindow method</span></span>

<span data-ttu-id="a22f0-104">El `PaintWindow` método hace que se vuelva a dibujar la ventana.</span><span class="sxs-lookup"><span data-stu-id="a22f0-104">The `PaintWindow` method causes the window to be repainted.</span></span>

## <a name="syntax"></a><span data-ttu-id="a22f0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a22f0-105">Syntax</span></span>


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a><span data-ttu-id="a22f0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a22f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a22f0-107">*bErase*</span><span class="sxs-lookup"><span data-stu-id="a22f0-107">*bErase*</span></span> 
</dt> <dd>

<span data-ttu-id="a22f0-108">Valor booleano que especifica si se borra el fondo.</span><span class="sxs-lookup"><span data-stu-id="a22f0-108">Boolean value that specifies whether the background is erased.</span></span> <span data-ttu-id="a22f0-109">Si el valor es **true**, se borra el fondo.</span><span class="sxs-lookup"><span data-stu-id="a22f0-109">If the value is **TRUE**, the background is erased.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a22f0-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a22f0-110">Return value</span></span>

<span data-ttu-id="a22f0-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a22f0-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a22f0-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a22f0-112">Remarks</span></span>

<span data-ttu-id="a22f0-113">Este método genera un mensaje de dibujo de WM \_ invalidando el área de cliente completa de la ventana.</span><span class="sxs-lookup"><span data-stu-id="a22f0-113">This method generates a WM\_PAINT message by invalidating the window's entire client area.</span></span>

## <a name="requirements"></a><span data-ttu-id="a22f0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a22f0-114">Requirements</span></span>



| <span data-ttu-id="a22f0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a22f0-115">Requirement</span></span> | <span data-ttu-id="a22f0-116">Value</span><span class="sxs-lookup"><span data-stu-id="a22f0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a22f0-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a22f0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a22f0-118"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a22f0-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a22f0-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a22f0-119">Library</span></span><br/> | <dl> <span data-ttu-id="a22f0-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a22f0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a22f0-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a22f0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22f0-122">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="a22f0-122">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




