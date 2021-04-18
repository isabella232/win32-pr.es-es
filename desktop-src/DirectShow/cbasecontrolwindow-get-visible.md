---
description: El \_ método get visible recupera la visibilidad de la ventana actual.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: Método CBaseControlWindow.get_Visible (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bc38a0b35f46de223ed84174c3b10f5300cc94d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671566"
---
# <a name="cbasecontrolwindowget_visible-method"></a><span data-ttu-id="8da31-103">CBaseControlWindow. get ( \_ método visible)</span><span class="sxs-lookup"><span data-stu-id="8da31-103">CBaseControlWindow.get\_Visible method</span></span>

<span data-ttu-id="8da31-104">El `get_Visible` método recupera la visibilidad de la ventana actual.</span><span class="sxs-lookup"><span data-stu-id="8da31-104">The `get_Visible` method retrieves the current window visibility.</span></span>

## <a name="syntax"></a><span data-ttu-id="8da31-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8da31-105">Syntax</span></span>


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a><span data-ttu-id="8da31-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8da31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8da31-107">*pVisible*</span><span class="sxs-lookup"><span data-stu-id="8da31-107">*pVisible*</span></span> 
</dt> <dd>

<span data-ttu-id="8da31-108">Puntero a una marca booleana de Automation (0 es OFF, 1 es ON).</span><span class="sxs-lookup"><span data-stu-id="8da31-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8da31-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8da31-109">Return value</span></span>

<span data-ttu-id="8da31-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8da31-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8da31-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8da31-111">Remarks</span></span>

<span data-ttu-id="8da31-112">Esta función miembro devuelve 1 si la ventana tiene el \_ estilo visible de WS; en caso contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="8da31-112">This member function returns  1 if the window has the WS\_VISIBLE style; 0 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8da31-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8da31-113">Requirements</span></span>



| <span data-ttu-id="8da31-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8da31-114">Requirement</span></span> | <span data-ttu-id="8da31-115">Value</span><span class="sxs-lookup"><span data-stu-id="8da31-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8da31-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8da31-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8da31-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8da31-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8da31-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8da31-118">Library</span></span><br/> | <dl> <span data-ttu-id="8da31-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8da31-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8da31-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="8da31-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da31-121">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="8da31-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




