---
description: El método CheckConnect determina si una conexión de PIN es adecuada.
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Método CTransformFilter. CheckConnect (Transfrm. h)
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
ms.openlocfilehash: 0d41c50323bae7cb4eaca52a87d8c1b936237ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660302"
---
# <a name="ctransformfiltercheckconnect-method"></a><span data-ttu-id="a3dde-103">CTransformFilter. CheckConnect, método</span><span class="sxs-lookup"><span data-stu-id="a3dde-103">CTransformFilter.CheckConnect method</span></span>

<span data-ttu-id="a3dde-104">El `CheckConnect` método determina si una conexión de PIN es adecuada.</span><span class="sxs-lookup"><span data-stu-id="a3dde-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3dde-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3dde-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="a3dde-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3dde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3dde-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="a3dde-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="a3dde-108">Miembro del tipo enumerado de [**\_ dirección del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , que especifica el PIN del filtro que realiza la conexión.</span><span class="sxs-lookup"><span data-stu-id="a3dde-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="a3dde-109">*pPin*</span><span class="sxs-lookup"><span data-stu-id="a3dde-109">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="a3dde-110">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro PIN en este intento de conexión.</span><span class="sxs-lookup"><span data-stu-id="a3dde-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3dde-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3dde-111">Return value</span></span>

<span data-ttu-id="a3dde-112">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="a3dde-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3dde-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3dde-113">Remarks</span></span>

<span data-ttu-id="a3dde-114">Los métodos [**CTransformInputPin:: CheckConnect**](ctransforminputpin-checkconnect.md) y [**CTransformOutputPin:: CheckConnect**](ctransformoutputpin-checkconnect.md) llaman a este método durante el proceso de conexión del PIN.</span><span class="sxs-lookup"><span data-stu-id="a3dde-114">The [**CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) and [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="a3dde-115">Este método no hace nada en la clase base.</span><span class="sxs-lookup"><span data-stu-id="a3dde-115">This method does nothing in the base class.</span></span> <span data-ttu-id="a3dde-116">La clase derivada puede invalidarla.</span><span class="sxs-lookup"><span data-stu-id="a3dde-116">The derived class can override it.</span></span> <span data-ttu-id="a3dde-117">Por ejemplo, la clase derivada podría consultar el otro PIN para una interfaz determinada.</span><span class="sxs-lookup"><span data-stu-id="a3dde-117">For example, the derived class might query the other pin for a particular interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3dde-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3dde-118">Requirements</span></span>



| <span data-ttu-id="a3dde-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3dde-119">Requirement</span></span> | <span data-ttu-id="a3dde-120">Value</span><span class="sxs-lookup"><span data-stu-id="a3dde-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3dde-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3dde-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a3dde-122"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3dde-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a3dde-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3dde-123">Library</span></span><br/> | <dl> <span data-ttu-id="a3dde-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a3dde-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3dde-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3dde-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3dde-126">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="a3dde-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




