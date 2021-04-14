---
description: 'El método QueryVendorInfo recupera una cadena que contiene información del proveedor. Este método implementa el método IBaseFilter:: QueryVendorInfo.'
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: Método CBaseFilter. QueryVendorInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryVendorInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1786477c042bb1d9ecc6340056a771141d0a3c74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661368"
---
# <a name="cbasefilterqueryvendorinfo-method"></a><span data-ttu-id="20cba-104">CBaseFilter. QueryVendorInfo, método</span><span class="sxs-lookup"><span data-stu-id="20cba-104">CBaseFilter.QueryVendorInfo method</span></span>

<span data-ttu-id="20cba-105">El `QueryVendorInfo` método recupera una cadena que contiene información del proveedor.</span><span class="sxs-lookup"><span data-stu-id="20cba-105">The `QueryVendorInfo` method retrieves a string containing vendor information.</span></span> <span data-ttu-id="20cba-106">Este método implementa el método [**IBaseFilter:: QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) .</span><span class="sxs-lookup"><span data-stu-id="20cba-106">This method implements the [**IBaseFilter::QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="20cba-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20cba-107">Syntax</span></span>


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a><span data-ttu-id="20cba-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20cba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20cba-109">*pVendorInfo*</span><span class="sxs-lookup"><span data-stu-id="20cba-109">*pVendorInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="20cba-110">Dirección de una variable que recibe un puntero a una cadena de caracteres anchos que contiene la información del proveedor.</span><span class="sxs-lookup"><span data-stu-id="20cba-110">Address of a variable that receives a pointer to a wide-character string containing the vendor information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20cba-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20cba-111">Return value</span></span>

<span data-ttu-id="20cba-112">Devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="20cba-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="20cba-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20cba-113">Remarks</span></span>

<span data-ttu-id="20cba-114">Para proporcionar información de proveedor para un filtro, Invalide este método.</span><span class="sxs-lookup"><span data-stu-id="20cba-114">To provide vendor information for a filter, override this method.</span></span> <span data-ttu-id="20cba-115">Si implementa este método, utilice la función **CoTaskMemAlloc** para asignar memoria para la cadena.</span><span class="sxs-lookup"><span data-stu-id="20cba-115">If you implement this method, use the **CoTaskMemAlloc** function to allocate memory for the string.</span></span> <span data-ttu-id="20cba-116">El autor de la llamada es responsable de llamar a la función **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="20cba-116">The caller is responsible for calling the **CoTaskMemFree** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="20cba-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20cba-117">Requirements</span></span>



| <span data-ttu-id="20cba-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="20cba-118">Requirement</span></span> | <span data-ttu-id="20cba-119">Value</span><span class="sxs-lookup"><span data-stu-id="20cba-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20cba-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20cba-120">Header</span></span><br/>  | <dl> <span data-ttu-id="20cba-121"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20cba-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="20cba-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20cba-122">Library</span></span><br/> | <dl> <span data-ttu-id="20cba-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="20cba-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20cba-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="20cba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20cba-125">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="20cba-125">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




