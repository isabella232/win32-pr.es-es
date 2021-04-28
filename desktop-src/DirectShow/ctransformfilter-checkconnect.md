---
description: 'Método CTransformFilter.CheckConnect: el método CheckConnect determina si una conexión de pin es adecuada.'
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Método CTransformFilter.CheckConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5927aac2fa58322c93a23489a22dc96a1e2a67f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085103"
---
# <a name="ctransformfiltercheckconnect-method"></a><span data-ttu-id="490be-103">Método CTransformFilter.CheckConnect</span><span class="sxs-lookup"><span data-stu-id="490be-103">CTransformFilter.CheckConnect method</span></span>

<span data-ttu-id="490be-104">El `CheckConnect` método determina si una conexión de pin es adecuada.</span><span class="sxs-lookup"><span data-stu-id="490be-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="490be-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="490be-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="490be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="490be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="490be-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="490be-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="490be-108">Miembro del tipo [**enumerado \_ DIRECCIÓN**](/windows/win32/api/strmif/ne-strmif-pin_direction) DEL PIN, especificando qué pin en el filtro está realizando la conexión.</span><span class="sxs-lookup"><span data-stu-id="490be-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="490be-109">*pPin*</span><span class="sxs-lookup"><span data-stu-id="490be-109">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="490be-110">Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro pin en este intento de conexión.</span><span class="sxs-lookup"><span data-stu-id="490be-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="490be-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="490be-111">Return value</span></span>

<span data-ttu-id="490be-112">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="490be-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="490be-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="490be-113">Remarks</span></span>

<span data-ttu-id="490be-114">Los [**métodos CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) y [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) llaman a este método durante el proceso de conexión de pin.</span><span class="sxs-lookup"><span data-stu-id="490be-114">The [**CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) and [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="490be-115">Este método no hace nada en la clase base.</span><span class="sxs-lookup"><span data-stu-id="490be-115">This method does nothing in the base class.</span></span> <span data-ttu-id="490be-116">La clase derivada puede invalidarla.</span><span class="sxs-lookup"><span data-stu-id="490be-116">The derived class can override it.</span></span> <span data-ttu-id="490be-117">Por ejemplo, la clase derivada podría consultar el otro pin para una interfaz determinada.</span><span class="sxs-lookup"><span data-stu-id="490be-117">For example, the derived class might query the other pin for a particular interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="490be-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="490be-118">Requirements</span></span>



| <span data-ttu-id="490be-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="490be-119">Requirement</span></span> | <span data-ttu-id="490be-120">Value</span><span class="sxs-lookup"><span data-stu-id="490be-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="490be-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="490be-121">Header</span></span><br/>  | <dl> <span data-ttu-id="490be-122"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="490be-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="490be-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="490be-123">Library</span></span><br/> | <dl> <span data-ttu-id="490be-124"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="490be-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="490be-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="490be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="490be-126">**CTransformFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="490be-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




