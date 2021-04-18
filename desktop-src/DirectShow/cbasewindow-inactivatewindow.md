---
description: El método InactivateWindow desactiva la ventana. En la clase base, este método oculta la ventana.
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: Método CBaseWindow. InactivateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d1c5e925a3d9b510918636a221d5ad6e1b7da736
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679564"
---
# <a name="cbasewindowinactivatewindow-method"></a><span data-ttu-id="c7332-104">CBaseWindow. InactivateWindow, método</span><span class="sxs-lookup"><span data-stu-id="c7332-104">CBaseWindow.InactivateWindow method</span></span>

<span data-ttu-id="c7332-105">El `InactivateWindow` método desactiva la ventana.</span><span class="sxs-lookup"><span data-stu-id="c7332-105">The `InactivateWindow` method inactivates the window.</span></span> <span data-ttu-id="c7332-106">En la clase base, este método oculta la ventana.</span><span class="sxs-lookup"><span data-stu-id="c7332-106">In the base class, this method hides the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7332-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7332-107">Syntax</span></span>


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a><span data-ttu-id="c7332-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7332-108">Parameters</span></span>

<span data-ttu-id="c7332-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c7332-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7332-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7332-110">Return value</span></span>

<span data-ttu-id="c7332-111">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c7332-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="c7332-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c7332-112">Return code</span></span>                                                                             | <span data-ttu-id="c7332-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7332-113">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="c7332-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c7332-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c7332-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c7332-115">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="c7332-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c7332-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c7332-117">La ventana ya está inactiva.</span><span class="sxs-lookup"><span data-stu-id="c7332-117">Window is already inactive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c7332-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7332-118">Requirements</span></span>



| <span data-ttu-id="c7332-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7332-119">Requirement</span></span> | <span data-ttu-id="c7332-120">Value</span><span class="sxs-lookup"><span data-stu-id="c7332-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7332-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7332-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c7332-122"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7332-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c7332-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7332-123">Library</span></span><br/> | <dl> <span data-ttu-id="c7332-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c7332-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7332-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7332-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7332-126">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="c7332-126">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




