---
description: Obsoleto. Use AMovieSetupRegisterFilter2 en su lugar.
ms.assetid: 42278829-d09e-46c7-8f1a-fa4572f7cc00
title: Función AMovieSetupRegisterFilter (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieSetupRegisterFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 398d2d727e26feaca23d6bddbdcbc8a578d096eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690518"
---
# <a name="amoviesetupregisterfilter-function"></a><span data-ttu-id="70630-104">AMovieSetupRegisterFilter función)</span><span class="sxs-lookup"><span data-stu-id="70630-104">AMovieSetupRegisterFilter function</span></span>

<span data-ttu-id="70630-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="70630-105">Obsolete.</span></span> <span data-ttu-id="70630-106">Use [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="70630-106">Use [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="70630-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70630-107">Syntax</span></span>


```C++
HRESULT AMovieSetupRegisterFilter(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper              *pIFM,
         BOOL                       bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="70630-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70630-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70630-109">*psetupdata*</span><span class="sxs-lookup"><span data-stu-id="70630-109">*psetupdata*</span></span> 
</dt> <dd>

<span data-ttu-id="70630-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="70630-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="70630-111">*pIFM*</span><span class="sxs-lookup"><span data-stu-id="70630-111">*pIFM*</span></span> 
</dt> <dd>

<span data-ttu-id="70630-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="70630-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="70630-113">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="70630-113">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="70630-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="70630-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70630-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70630-115">Return value</span></span>

<span data-ttu-id="70630-116">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="70630-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="70630-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="70630-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="70630-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70630-118">Requirements</span></span>



| <span data-ttu-id="70630-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="70630-119">Requirement</span></span> | <span data-ttu-id="70630-120">Value</span><span class="sxs-lookup"><span data-stu-id="70630-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70630-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70630-121">Header</span></span><br/>  | <dl> <span data-ttu-id="70630-122"><dt>Dllsetup. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70630-122"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="70630-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70630-123">Library</span></span><br/> | <dl> <span data-ttu-id="70630-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="70630-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70630-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="70630-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70630-126">**Funciones de instalación de DLL**</span><span class="sxs-lookup"><span data-stu-id="70630-126">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




