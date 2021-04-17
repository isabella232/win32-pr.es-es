---
description: Escribe los datos del filtro en la secuencia especificada.
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: Método CPersistStream. WriteToStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 893d58986db92e50cbafefe74676481162808abf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680368"
---
# <a name="cpersiststreamwritetostream-method"></a><span data-ttu-id="0423c-103">CPersistStream. WriteToStream, método</span><span class="sxs-lookup"><span data-stu-id="0423c-103">CPersistStream.WriteToStream method</span></span>

<span data-ttu-id="0423c-104">Escribe los datos del filtro en la secuencia especificada.</span><span class="sxs-lookup"><span data-stu-id="0423c-104">Writes the filter's data to the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="0423c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0423c-105">Syntax</span></span>


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="0423c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0423c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0423c-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="0423c-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="0423c-108">Puntero a una interfaz **IStream** que especifica la secuencia de destino de los datos del filtro.</span><span class="sxs-lookup"><span data-stu-id="0423c-108">Pointer to an **IStream** interface that specifies the filter data's destination stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0423c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0423c-109">Return value</span></span>

<span data-ttu-id="0423c-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="0423c-110">Returns S\_OK.</span></span> <span data-ttu-id="0423c-111">La clase derivada debe devolver un valor **HRESULT** válido.</span><span class="sxs-lookup"><span data-stu-id="0423c-111">The derived class should return a valid **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0423c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0423c-112">Remarks</span></span>

<span data-ttu-id="0423c-113">La versión predeterminada no escribe nada; se puede invalidar para escribir datos específicos de la clase.</span><span class="sxs-lookup"><span data-stu-id="0423c-113">The default version writes nothing; it can be overridden to write data specific to your class.</span></span>

## <a name="requirements"></a><span data-ttu-id="0423c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0423c-114">Requirements</span></span>



| <span data-ttu-id="0423c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0423c-115">Requirement</span></span> | <span data-ttu-id="0423c-116">Value</span><span class="sxs-lookup"><span data-stu-id="0423c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0423c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0423c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0423c-118"><dt>PStream. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0423c-118"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0423c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0423c-119">Library</span></span><br/> | <dl> <span data-ttu-id="0423c-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0423c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0423c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0423c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0423c-122">**Clase CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="0423c-122">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




