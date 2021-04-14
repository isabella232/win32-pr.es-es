---
description: El método IsCursorHidden recupera el estado actual del \_ miembro de datos m bCursorHidden.
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: Método CBaseControlWindow. IsCursorHidden (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsCursorHidden
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90f02c6cac5fb3ef1edeaa8e03f7bc54a03acb49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661387"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a><span data-ttu-id="5fd39-103">CBaseControlWindow. IsCursorHidden, método</span><span class="sxs-lookup"><span data-stu-id="5fd39-103">CBaseControlWindow.IsCursorHidden method</span></span>

<span data-ttu-id="5fd39-104">El `IsCursorHidden` método recupera el estado actual del miembro de datos **m \_ bCursorHidden** .</span><span class="sxs-lookup"><span data-stu-id="5fd39-104">The `IsCursorHidden` method retrieves the current state of the **m\_bCursorHidden** data member.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd39-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5fd39-105">Syntax</span></span>


```C++
HRESULT IsCursorHidden(
   long *CursorHidden
);
```



## <a name="parameters"></a><span data-ttu-id="5fd39-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5fd39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd39-107">*CursorHidden*</span><span class="sxs-lookup"><span data-stu-id="5fd39-107">*CursorHidden*</span></span> 
</dt> <dd>

<span data-ttu-id="5fd39-108">Puntero al valor de **m \_ bCursorHidden**.</span><span class="sxs-lookup"><span data-stu-id="5fd39-108">Pointer to the value of **m\_bCursorHidden**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd39-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5fd39-109">Return value</span></span>

<span data-ttu-id="5fd39-110">Cuando se llama sin un parámetro, devuelve OATRUE si el cursor está oculto, o OAFALSE si el cursor está visible.</span><span class="sxs-lookup"><span data-stu-id="5fd39-110">When called without a parameter, returns OATRUE if the cursor is hidden, or OAFALSE if the cursor is visible.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fd39-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5fd39-111">Remarks</span></span>

<span data-ttu-id="5fd39-112">Los objetos internos deben llamar a esta función miembro sin el parámetro *CursorHidden* para evitar el bloqueo de la sección crítica.</span><span class="sxs-lookup"><span data-stu-id="5fd39-112">Internal objects should call this member function without the *CursorHidden* parameter to avoid locking the critical section.</span></span> <span data-ttu-id="5fd39-113">Los objetos externos acceden a esta función miembro con el parámetro *CursorHidden* a través del método [**IVideoWindow:: IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) .</span><span class="sxs-lookup"><span data-stu-id="5fd39-113">External objects access this member function with the *CursorHidden* parameter through the [**IVideoWindow::IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd39-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fd39-114">Requirements</span></span>



| <span data-ttu-id="5fd39-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fd39-115">Requirement</span></span> | <span data-ttu-id="5fd39-116">Value</span><span class="sxs-lookup"><span data-stu-id="5fd39-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd39-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fd39-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5fd39-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fd39-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5fd39-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5fd39-119">Library</span></span><br/> | <dl> <span data-ttu-id="5fd39-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5fd39-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fd39-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fd39-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fd39-122">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="5fd39-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




