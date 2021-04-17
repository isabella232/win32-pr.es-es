---
description: Recupera el identificador de clase para este filtro.
ms.assetid: f0559437-5d0d-4522-a3dc-947e3494b576
title: Método CPersistStream. GetClassID (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7603541eae4f431327a91777488a740afb7f628b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680377"
---
# <a name="cpersiststreamgetclassid-method"></a><span data-ttu-id="6bdc3-103">CPersistStream. GetClassID (método)</span><span class="sxs-lookup"><span data-stu-id="6bdc3-103">CPersistStream.GetClassID method</span></span>

<span data-ttu-id="6bdc3-104">Recupera el identificador de clase para este filtro.</span><span class="sxs-lookup"><span data-stu-id="6bdc3-104">Retrieves the class identifier for this filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bdc3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6bdc3-105">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="6bdc3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6bdc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bdc3-107">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="6bdc3-107">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="6bdc3-108">Puntero a una estructura CLSID.</span><span class="sxs-lookup"><span data-stu-id="6bdc3-108">Pointer to a CLSID structure.</span></span> <span data-ttu-id="6bdc3-109">Copie el identificador de clase aquí.</span><span class="sxs-lookup"><span data-stu-id="6bdc3-109">Copy your class ID to here.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bdc3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6bdc3-110">Return value</span></span>

<span data-ttu-id="6bdc3-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6bdc3-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bdc3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bdc3-112">Requirements</span></span>



| <span data-ttu-id="6bdc3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bdc3-113">Requirement</span></span> | <span data-ttu-id="6bdc3-114">Value</span><span class="sxs-lookup"><span data-stu-id="6bdc3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bdc3-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6bdc3-115">Header</span></span><br/>  | <dl> <span data-ttu-id="6bdc3-116"><dt>PStream. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bdc3-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6bdc3-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bdc3-117">Library</span></span><br/> | <dl> <span data-ttu-id="6bdc3-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6bdc3-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bdc3-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bdc3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bdc3-120">**Clase CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="6bdc3-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




