---
description: 'Constructor CBaseControlWindow.CBaseControlWindow: método constructor.'
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: Constructor CBaseControlWindow.CBaseControlWindow (Ctlutil.h)
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
ms.openlocfilehash: 47c8277a76dbf0fbb9e05262eea5b419466044cc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096343"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a><span data-ttu-id="1d987-103">Constructor CBaseControlWindow.CBaseControlWindow</span><span class="sxs-lookup"><span data-stu-id="1d987-103">CBaseControlWindow.CBaseControlWindow constructor</span></span>

<span data-ttu-id="1d987-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="1d987-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d987-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d987-105">Syntax</span></span>


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a><span data-ttu-id="1d987-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d987-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d987-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="1d987-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="1d987-108">Puntero al objeto de filtro multimedia propietario.</span><span class="sxs-lookup"><span data-stu-id="1d987-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="1d987-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="1d987-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="1d987-110">Puntero a la sección crítica que se usará para el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="1d987-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="1d987-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="1d987-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1d987-112">Puntero a la descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d987-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="1d987-113">*Punk*</span><span class="sxs-lookup"><span data-stu-id="1d987-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="1d987-114">Puntero a la **interfaz IUnknown de control,** si el objeto forma parte de un agregado; de lo contrario, debe ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="1d987-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1d987-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="1d987-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="1d987-116">Puntero a una variable que recibe un valor HRESULT que indica el éxito o error del método constructor.</span><span class="sxs-lookup"><span data-stu-id="1d987-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d987-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d987-117">Requirements</span></span>



| <span data-ttu-id="1d987-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d987-118">Requirement</span></span> | <span data-ttu-id="1d987-119">Value</span><span class="sxs-lookup"><span data-stu-id="1d987-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d987-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d987-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1d987-121"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d987-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1d987-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d987-122">Library</span></span><br/> | <dl> <span data-ttu-id="1d987-123"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1d987-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d987-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1d987-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d987-125">**CBaseControlWindow (clase)**</span><span class="sxs-lookup"><span data-stu-id="1d987-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




