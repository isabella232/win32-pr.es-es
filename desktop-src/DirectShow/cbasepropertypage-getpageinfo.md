---
description: 'El método GetPageInfo recupera información sobre la página de propiedades. Este método implementa el método IPropertyPage:: GetPageInfo.'
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: Método CBasePropertyPage. GetPageInfo (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.GetPageInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27faecf50381b098dfcbee34d1494e37c77a36ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671323"
---
# <a name="cbasepropertypagegetpageinfo-method"></a><span data-ttu-id="1d704-104">CBasePropertyPage. GetPageInfo (método)</span><span class="sxs-lookup"><span data-stu-id="1d704-104">CBasePropertyPage.GetPageInfo method</span></span>

<span data-ttu-id="1d704-105">El `GetPageInfo` método recupera información sobre la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="1d704-105">The `GetPageInfo` method retrieves information about the property page.</span></span> <span data-ttu-id="1d704-106">Este método implementa el método **IPropertyPage:: GetPageInfo** .</span><span class="sxs-lookup"><span data-stu-id="1d704-106">This method implements the **IPropertyPage::GetPageInfo** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d704-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d704-107">Syntax</span></span>


```C++
HRESULT GetPageInfo(
   LPPROPPAGEINFO pPageInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1d704-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d704-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d704-109">*pPageInfo*</span><span class="sxs-lookup"><span data-stu-id="1d704-109">*pPageInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="1d704-110">Puntero a una estructura **PROPPAGEINFO** asignada por el llamador.</span><span class="sxs-lookup"><span data-stu-id="1d704-110">Pointer to a caller-allocated **PROPPAGEINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d704-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d704-111">Return value</span></span>

<span data-ttu-id="1d704-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1d704-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1d704-113">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="1d704-113">Possible values include the following.</span></span>



| <span data-ttu-id="1d704-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1d704-114">Return code</span></span>                                                                                   | <span data-ttu-id="1d704-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d704-115">Description</span></span>                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="1d704-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1d704-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1d704-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1d704-117">Success.</span></span><br/>             |
| <dl> <span data-ttu-id="1d704-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1d704-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1d704-119">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="1d704-119">Insufficient memory.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1d704-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d704-120">Requirements</span></span>



| <span data-ttu-id="1d704-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d704-121">Requirement</span></span> | <span data-ttu-id="1d704-122">Value</span><span class="sxs-lookup"><span data-stu-id="1d704-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d704-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d704-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1d704-124"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d704-124"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="1d704-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d704-125">Library</span></span><br/> | <dl> <span data-ttu-id="1d704-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1d704-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d704-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d704-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d704-128">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="1d704-128">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




