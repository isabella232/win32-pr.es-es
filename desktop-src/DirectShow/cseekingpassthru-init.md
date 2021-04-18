---
description: El método init inicializa el objeto.
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: Método CSeekingPassThru.Init (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78176a6966f379240b5b7edd1ef5b73d7fa75b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660179"
---
# <a name="cseekingpassthruinit-method"></a><span data-ttu-id="656b3-103">CSeekingPassThru.Init (método)</span><span class="sxs-lookup"><span data-stu-id="656b3-103">CSeekingPassThru.Init method</span></span>

<span data-ttu-id="656b3-104">El `Init` método inicializa el objeto.</span><span class="sxs-lookup"><span data-stu-id="656b3-104">The `Init` method initializes the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="656b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="656b3-105">Syntax</span></span>


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="656b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="656b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="656b3-107">*bSupportRendering* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="656b3-107">*bSupportRendering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656b3-108">Valor booleano que especifica si el filtro es un representador.</span><span class="sxs-lookup"><span data-stu-id="656b3-108">Boolean value that specifies whether the filter is a renderer.</span></span> <span data-ttu-id="656b3-109">Use el valor **true** si el filtro es un representador o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="656b3-109">Use the value **TRUE** if the filter is a renderer, or **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="656b3-110">*pPin*</span><span class="sxs-lookup"><span data-stu-id="656b3-110">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="656b3-111">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) en el PIN de entrada del filtro.</span><span class="sxs-lookup"><span data-stu-id="656b3-111">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface on the filter's input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="656b3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="656b3-112">Return value</span></span>

<span data-ttu-id="656b3-113">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="656b3-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="656b3-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="656b3-114">Return code</span></span>                                                                                   | <span data-ttu-id="656b3-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="656b3-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="656b3-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="656b3-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="656b3-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="656b3-117">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="656b3-118"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="656b3-118"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="656b3-119">El objeto ya se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="656b3-119">Object was already initialized.</span></span><br/>         |
| <dl> <span data-ttu-id="656b3-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="656b3-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="656b3-121">Memoria insuficiente para crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="656b3-121">Not enough memory to create the object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="656b3-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="656b3-122">Remarks</span></span>

<span data-ttu-id="656b3-123">Si el valor de *bSupportRendering* es **true**, este método crea una instancia de la clase [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="656b3-123">If the value of *bSupportRendering* is **TRUE**, this method creates an instance of the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span> <span data-ttu-id="656b3-124">De lo contrario, crea una instancia de la clase [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="656b3-124">Otherwise, it creates an instance of the [**CPosPassThru**](cpospassthru.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="656b3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="656b3-125">Requirements</span></span>



| <span data-ttu-id="656b3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="656b3-126">Requirement</span></span> | <span data-ttu-id="656b3-127">Value</span><span class="sxs-lookup"><span data-stu-id="656b3-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="656b3-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="656b3-128">Header</span></span><br/>  | <dl> <span data-ttu-id="656b3-129"><dt>Seekpt. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="656b3-129"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="656b3-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="656b3-130">Library</span></span><br/> | <dl> <span data-ttu-id="656b3-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="656b3-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="656b3-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="656b3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656b3-133">**Clase CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="656b3-133">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




