---
description: 'Recupera un puntero de interfaz e incrementa el recuento de referencias. Este método implementa el método INonDelegatingUnknown:: NonDelegatingQueryInterface.'
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: Método CUnknown. NonDelegatingQueryInterface (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingQueryInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41810eb52db38644bda472907228cd812f76f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680877"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a><span data-ttu-id="a91c8-104">CUnknown. NonDelegatingQueryInterface, método</span><span class="sxs-lookup"><span data-stu-id="a91c8-104">CUnknown.NonDelegatingQueryInterface method</span></span>

<span data-ttu-id="a91c8-105">Recupera un puntero de interfaz e incrementa el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="a91c8-105">Retrieves an interface pointer and increments the reference count.</span></span> <span data-ttu-id="a91c8-106">Este método implementa el método **INonDelegatingUnknown:: NonDelegatingQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="a91c8-106">This method implements the **INonDelegatingUnknown::NonDelegatingQueryInterface** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a91c8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a91c8-107">Syntax</span></span>


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="a91c8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a91c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a91c8-109">*riid*</span><span class="sxs-lookup"><span data-stu-id="a91c8-109">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="a91c8-110">Identificador de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="a91c8-110">Identifier of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="a91c8-111">*PPV*</span><span class="sxs-lookup"><span data-stu-id="a91c8-111">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="a91c8-112">Dirección de un puntero para recibir la interfaz.</span><span class="sxs-lookup"><span data-stu-id="a91c8-112">Address of a pointer to receive the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a91c8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a91c8-113">Return value</span></span>

<span data-ttu-id="a91c8-114">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a91c8-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a91c8-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a91c8-115">Return code</span></span>                                                                                   | <span data-ttu-id="a91c8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a91c8-116">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="a91c8-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a91c8-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a91c8-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="a91c8-118">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="a91c8-119"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="a91c8-119"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="a91c8-120">El objeto no admite esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="a91c8-120">Object does not support this interface.</span></span><br/> |
| <dl> <span data-ttu-id="a91c8-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="a91c8-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a91c8-122">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="a91c8-122">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="a91c8-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a91c8-123">Remarks</span></span>

<span data-ttu-id="a91c8-124">La clase **CUnknown** expone solo la interfaz **IUknown** .</span><span class="sxs-lookup"><span data-stu-id="a91c8-124">The **CUnknown** class exposes only the **IUknown** interface.</span></span> <span data-ttu-id="a91c8-125">Invalide este método para exponer interfaces adicionales.</span><span class="sxs-lookup"><span data-stu-id="a91c8-125">Override this method to expose additional interfaces.</span></span> <span data-ttu-id="a91c8-126">Para obtener información sobre cómo invalidar este método, consulte [How to implement IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="a91c8-126">For information on how to override this method, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a91c8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a91c8-127">Requirements</span></span>



| <span data-ttu-id="a91c8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a91c8-128">Requirement</span></span> | <span data-ttu-id="a91c8-129">Value</span><span class="sxs-lookup"><span data-stu-id="a91c8-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a91c8-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a91c8-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a91c8-131"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a91c8-131"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a91c8-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a91c8-132">Library</span></span><br/> | <dl> <span data-ttu-id="a91c8-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a91c8-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




