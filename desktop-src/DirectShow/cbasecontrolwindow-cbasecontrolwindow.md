---
description: Método de constructor.
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: Constructor CBaseControlWindow. CBaseControlWindow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9eb3e50daef8ec4ad11bf96a8f0b605f4c8fe679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660337"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a><span data-ttu-id="2be33-103">Constructor CBaseControlWindow. CBaseControlWindow</span><span class="sxs-lookup"><span data-stu-id="2be33-103">CBaseControlWindow.CBaseControlWindow constructor</span></span>

<span data-ttu-id="2be33-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="2be33-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2be33-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2be33-105">Syntax</span></span>


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a><span data-ttu-id="2be33-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2be33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2be33-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="2be33-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="2be33-108">Puntero al objeto de filtro multimedia propietario.</span><span class="sxs-lookup"><span data-stu-id="2be33-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="2be33-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="2be33-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="2be33-110">Puntero a la sección crítica que se va a usar para el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="2be33-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="2be33-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="2be33-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="2be33-112">Puntero a la descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2be33-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="2be33-113">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="2be33-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="2be33-114">Puntero a la interfaz **IUnknown** de control, si el objeto forma parte de un agregado; de lo contrario, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="2be33-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2be33-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="2be33-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="2be33-116">Puntero a una variable que recibe un valor HRESULT que indica si el método de constructor se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="2be33-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2be33-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2be33-117">Requirements</span></span>



| <span data-ttu-id="2be33-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2be33-118">Requirement</span></span> | <span data-ttu-id="2be33-119">Value</span><span class="sxs-lookup"><span data-stu-id="2be33-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2be33-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2be33-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2be33-121"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2be33-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2be33-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2be33-122">Library</span></span><br/> | <dl> <span data-ttu-id="2be33-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2be33-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2be33-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="2be33-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2be33-125">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="2be33-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




