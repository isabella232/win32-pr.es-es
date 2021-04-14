---
description: 'El método GetClassID recupera el identificador de clase (CLSID) del objeto. Este método implementa el método IPersist:: GetClassID.'
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: Método CSystemClock. GetClassID (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2f83d3e3c2efcbcb5d4604bc5c50a37dc020f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661391"
---
# <a name="csystemclockgetclassid-method"></a><span data-ttu-id="32805-104">CSystemClock. GetClassID (método)</span><span class="sxs-lookup"><span data-stu-id="32805-104">CSystemClock.GetClassID method</span></span>

<span data-ttu-id="32805-105">El `GetClassID` método recupera el identificador de clase (CLSID) del objeto.</span><span class="sxs-lookup"><span data-stu-id="32805-105">The `GetClassID` method retrieves the class identifier (CLSID) of the object.</span></span> <span data-ttu-id="32805-106">Este método implementa el método **IPersist:: GetClassID** .</span><span class="sxs-lookup"><span data-stu-id="32805-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="32805-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32805-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="32805-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32805-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32805-109">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="32805-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="32805-110">Puntero a una variable que recibe el valor CLSID \_ SystemClock.</span><span class="sxs-lookup"><span data-stu-id="32805-110">Pointer to a variable that receives the value CLSID\_SystemClock.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32805-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32805-111">Return value</span></span>

<span data-ttu-id="32805-112">Devuelve el \_ puntero S o E \_ .</span><span class="sxs-lookup"><span data-stu-id="32805-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="32805-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32805-113">Requirements</span></span>



| <span data-ttu-id="32805-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="32805-114">Requirement</span></span> | <span data-ttu-id="32805-115">Value</span><span class="sxs-lookup"><span data-stu-id="32805-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32805-116">Versión</span><span class="sxs-lookup"><span data-stu-id="32805-116">Version</span></span><br/> | <span data-ttu-id="32805-117">Clase CSystemClock</span><span class="sxs-lookup"><span data-stu-id="32805-117">CSystemClock Class</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="32805-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32805-118">Header</span></span><br/>  | <dl> <span data-ttu-id="32805-119"><dt>Sysclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32805-119"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="32805-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="32805-120">Library</span></span><br/> | <dl> <span data-ttu-id="32805-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="32805-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




