---
description: Lee los datos del filtro de la secuencia especificada.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Método CPersistStream. ReadFromStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.ReadFromStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce6c037fbce9fbaeabf7491b1b840000f67e25d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670997"
---
# <a name="cpersiststreamreadfromstream-method"></a><span data-ttu-id="af332-103">CPersistStream. ReadFromStream, método</span><span class="sxs-lookup"><span data-stu-id="af332-103">CPersistStream.ReadFromStream method</span></span>

<span data-ttu-id="af332-104">Lee los datos del filtro de la secuencia especificada.</span><span class="sxs-lookup"><span data-stu-id="af332-104">Reads the filter's data from the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="af332-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af332-105">Syntax</span></span>


```C++
virtual HRESULT ReadFromStream(
   IStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="af332-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af332-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af332-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="af332-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="af332-108">Puntero a una interfaz **IStream** desde la que se leerán los datos.</span><span class="sxs-lookup"><span data-stu-id="af332-108">Pointer to an **IStream** interface from which data is to be read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af332-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af332-109">Return value</span></span>

<span data-ttu-id="af332-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="af332-110">Returns S\_OK.</span></span> <span data-ttu-id="af332-111">La clase derivada debe devolver un valor **HRESULT** válido.</span><span class="sxs-lookup"><span data-stu-id="af332-111">The derived class should return a valid **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af332-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af332-112">Remarks</span></span>

<span data-ttu-id="af332-113">La versión predeterminada no es nada; se puede invalidar para leer datos específicos de la clase.</span><span class="sxs-lookup"><span data-stu-id="af332-113">The default version reads nothing; it can be overridden to read data specific to your class.</span></span>

## <a name="requirements"></a><span data-ttu-id="af332-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af332-114">Requirements</span></span>



| <span data-ttu-id="af332-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="af332-115">Requirement</span></span> | <span data-ttu-id="af332-116">Value</span><span class="sxs-lookup"><span data-stu-id="af332-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af332-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af332-117">Header</span></span><br/>  | <dl> <span data-ttu-id="af332-118"><dt>PStream. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af332-118"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="af332-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af332-119">Library</span></span><br/> | <dl> <span data-ttu-id="af332-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="af332-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af332-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="af332-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af332-122">**Clase CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="af332-122">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




