---
description: El método CreateInstance crea una nueva instancia de este objeto.
ms.assetid: 5c62f781-0f22-4d8f-8517-272405dd07c5
title: Método CSystemClock. CreateInstance (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 264997448aea028c5725d207ce4b301d369a092c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661392"
---
# <a name="csystemclockcreateinstance-method"></a><span data-ttu-id="d57ab-103">CSystemClock. CreateInstance (método)</span><span class="sxs-lookup"><span data-stu-id="d57ab-103">CSystemClock.CreateInstance method</span></span>

<span data-ttu-id="d57ab-104">El `CreateInstance` método crea una nueva instancia de este objeto.</span><span class="sxs-lookup"><span data-stu-id="d57ab-104">The `CreateInstance` method creates a new instance of this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d57ab-105">Syntax</span></span>


```C++
static CUnknown* WINAPI CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="d57ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d57ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d57ab-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="d57ab-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="d57ab-108">Puntero a la interfaz **IUnknown** de agregación.</span><span class="sxs-lookup"><span data-stu-id="d57ab-108">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="d57ab-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="d57ab-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d57ab-110">Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="d57ab-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d57ab-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d57ab-111">Return value</span></span>

<span data-ttu-id="d57ab-112">Devuelve un puntero a una nueva instancia de este objeto.</span><span class="sxs-lookup"><span data-stu-id="d57ab-112">Returns a pointer to a new instance of this object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d57ab-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d57ab-113">Remarks</span></span>

<span data-ttu-id="d57ab-114">El generador de clases llama a este método para crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="d57ab-114">The class factory calls this method to create the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d57ab-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d57ab-115">Requirements</span></span>



| <span data-ttu-id="d57ab-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d57ab-116">Requirement</span></span> | <span data-ttu-id="d57ab-117">Value</span><span class="sxs-lookup"><span data-stu-id="d57ab-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d57ab-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d57ab-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d57ab-119"><dt>Sysclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d57ab-119"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d57ab-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d57ab-120">Library</span></span><br/> | <dl> <span data-ttu-id="d57ab-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d57ab-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




