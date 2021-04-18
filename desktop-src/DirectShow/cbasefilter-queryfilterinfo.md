---
description: 'El método QueryFilterInfo recupera información sobre el filtro. Este método implementa el método IBaseFilter:: QueryFilterInfo.'
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Método CBaseFilter. QueryFilterInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a706663c1fb39e0e2e84b4097ec620f9e608843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661369"
---
# <a name="cbasefilterqueryfilterinfo-method"></a><span data-ttu-id="2acf3-104">CBaseFilter. QueryFilterInfo, método</span><span class="sxs-lookup"><span data-stu-id="2acf3-104">CBaseFilter.QueryFilterInfo method</span></span>

<span data-ttu-id="2acf3-105">El `QueryFilterInfo` método recupera información sobre el filtro.</span><span class="sxs-lookup"><span data-stu-id="2acf3-105">The `QueryFilterInfo` method retrieves information about the filter.</span></span> <span data-ttu-id="2acf3-106">Este método implementa el método [**IBaseFilter:: QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) .</span><span class="sxs-lookup"><span data-stu-id="2acf3-106">This method implements the [**IBaseFilter::QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2acf3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2acf3-107">Syntax</span></span>


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="2acf3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2acf3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2acf3-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="2acf3-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="2acf3-110">Puntero a una estructura de [**\_ información de filtro**](/windows/win32/api/strmif/ns-strmif-filter_info) .</span><span class="sxs-lookup"><span data-stu-id="2acf3-110">Pointer to a [**FILTER\_INFO**](/windows/win32/api/strmif/ns-strmif-filter_info) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2acf3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2acf3-111">Return value</span></span>

<span data-ttu-id="2acf3-112">Devuelve el \_ puntero S o E \_ .</span><span class="sxs-lookup"><span data-stu-id="2acf3-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="2acf3-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2acf3-113">Remarks</span></span>

<span data-ttu-id="2acf3-114">Este método copia el nombre del filtro de la variable miembro [**CBaseFilter:: m \_ pName**](cbasefilter-m-pname.md) en el miembro **achName** de la estructura de información de filtro \_ .</span><span class="sxs-lookup"><span data-stu-id="2acf3-114">This method copies the filter's name from the [**CBaseFilter::m\_pName**](cbasefilter-m-pname.md) member variable into the **achName** member of the FILTER\_INFO structure.</span></span> <span data-ttu-id="2acf3-115">Si **m \_ PName** es **null**, el método establece **achName** en L " \\ 0".</span><span class="sxs-lookup"><span data-stu-id="2acf3-115">If **m\_pName** is **NULL**, the method sets **achName** to L'\\0'.</span></span>

<span data-ttu-id="2acf3-116">El método establece el miembro **pGraph** de la estructura de información de filtro \_ igual a la variable de miembro [**CBaseFilter:: m \_ pGraph**](cbasefilter-m-pgraph.md) e incrementa el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="2acf3-116">The method sets the **pGraph** member of the FILTER\_INFO structure equal to the [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md) member variable, and increments the reference count.</span></span> <span data-ttu-id="2acf3-117">El llamador debe liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="2acf3-117">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="2acf3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2acf3-118">Requirements</span></span>



| <span data-ttu-id="2acf3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2acf3-119">Requirement</span></span> | <span data-ttu-id="2acf3-120">Value</span><span class="sxs-lookup"><span data-stu-id="2acf3-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2acf3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2acf3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2acf3-122"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2acf3-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2acf3-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2acf3-123">Library</span></span><br/> | <dl> <span data-ttu-id="2acf3-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2acf3-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2acf3-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2acf3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2acf3-126">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="2acf3-126">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




