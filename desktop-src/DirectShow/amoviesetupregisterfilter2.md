---
description: La función AMovieSetupRegisterFilter2 registra los tipos de méritos, PIN y medios de un filtro en el registro mediante la interfaz IFilterMapper2.
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: Función AMovieSetupRegisterFilter2 (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 272b781cf70f1dede9d4eea64b45d3d9d793a119
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661115"
---
# <a name="amoviesetupregisterfilter2-function"></a><span data-ttu-id="67b6f-103">AMovieSetupRegisterFilter2 función)</span><span class="sxs-lookup"><span data-stu-id="67b6f-103">AMovieSetupRegisterFilter2 function</span></span>

<span data-ttu-id="67b6f-104">La función **AMovieSetupRegisterFilter2** registra los tipos de méritos, PIN y medios de un filtro en el registro mediante la interfaz [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="67b6f-104">The **AMovieSetupRegisterFilter2** function registers a filter's merit, pins, and media types in the registry using the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="67b6f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67b6f-105">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper2             *pIFM2,
         BOOL                       bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="67b6f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67b6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67b6f-107">*psetupdata*</span><span class="sxs-lookup"><span data-stu-id="67b6f-107">*psetupdata*</span></span> 
</dt> <dd>

<span data-ttu-id="67b6f-108">Puntero a los datos del [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="67b6f-108">Pointer to the [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) data.</span></span>

</dd> <dt>

<span data-ttu-id="67b6f-109">*pIFM2*</span><span class="sxs-lookup"><span data-stu-id="67b6f-109">*pIFM2*</span></span> 
</dt> <dd>

<span data-ttu-id="67b6f-110">Puntero a la interfaz [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="67b6f-110">Pointer to [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span>

</dd> <dt>

<span data-ttu-id="67b6f-111">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="67b6f-111">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="67b6f-112">Valor que indica si se debe registrar el filtro; **True** indica que se registra el filtro; **false** indica que se anula el registro.</span><span class="sxs-lookup"><span data-stu-id="67b6f-112">Value indicating whether to register the filter; **TRUE** indicates register the filter, **FALSE** indicates unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67b6f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67b6f-113">Return value</span></span>

<span data-ttu-id="67b6f-114">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="67b6f-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="67b6f-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="67b6f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="67b6f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67b6f-116">Remarks</span></span>

<span data-ttu-id="67b6f-117">La función [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) llama a esta función auxiliar para registrar un filtro después de que se haya registrado el servidor com.</span><span class="sxs-lookup"><span data-stu-id="67b6f-117">The [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function calls this helper function to register a filter after the COM server has been registered.</span></span>

<span data-ttu-id="67b6f-118">Normalmente, un filtro usará [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) y no llamará directamente a esta función.</span><span class="sxs-lookup"><span data-stu-id="67b6f-118">Typically, a filter will use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) and will not call this function directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="67b6f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67b6f-119">Requirements</span></span>



| <span data-ttu-id="67b6f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="67b6f-120">Requirement</span></span> | <span data-ttu-id="67b6f-121">Value</span><span class="sxs-lookup"><span data-stu-id="67b6f-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67b6f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67b6f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="67b6f-123"><dt>Dllsetup. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67b6f-123"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="67b6f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67b6f-124">Library</span></span><br/> | <dl> <span data-ttu-id="67b6f-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="67b6f-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67b6f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="67b6f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67b6f-127">**Funciones de instalación de DLL**</span><span class="sxs-lookup"><span data-stu-id="67b6f-127">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




