---
description: Recupera el tamaño máximo de bytes necesario para la secuencia actual, sin incluir el número de versión.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: Método CPersistStream. SizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afa29e2c81cc454a9e85b9038486221f6f44aaf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670995"
---
# <a name="cpersiststreamsizemax-method"></a><span data-ttu-id="8fd6a-103">CPersistStream. SizeMax, método</span><span class="sxs-lookup"><span data-stu-id="8fd6a-103">CPersistStream.SizeMax method</span></span>

<span data-ttu-id="8fd6a-104">Recupera el tamaño máximo de bytes necesario para la secuencia actual, sin incluir el número de versión.</span><span class="sxs-lookup"><span data-stu-id="8fd6a-104">Retrieves the maximum byte size needed for the current stream, not including the version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fd6a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fd6a-105">Syntax</span></span>


```C++
virtual int SizeMax();
```



## <a name="parameters"></a><span data-ttu-id="8fd6a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8fd6a-106">Parameters</span></span>

<span data-ttu-id="8fd6a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8fd6a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8fd6a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8fd6a-108">Return value</span></span>

<span data-ttu-id="8fd6a-109">Devuelve el número de bytes necesarios para los datos, sin incluir el número de versión.</span><span class="sxs-lookup"><span data-stu-id="8fd6a-109">Returns the number of bytes needed for data, not including the version number.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fd6a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8fd6a-110">Remarks</span></span>

<span data-ttu-id="8fd6a-111">La versión predeterminada devuelve cero; se debe invalidar para proporcionar algún otro valor adecuado.</span><span class="sxs-lookup"><span data-stu-id="8fd6a-111">The default version returns zero; it should be overridden to provide some other appropriate value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fd6a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fd6a-112">Requirements</span></span>



| <span data-ttu-id="8fd6a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fd6a-113">Requirement</span></span> | <span data-ttu-id="8fd6a-114">Value</span><span class="sxs-lookup"><span data-stu-id="8fd6a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd6a-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8fd6a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8fd6a-116"><dt>PStream. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8fd6a-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8fd6a-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8fd6a-117">Library</span></span><br/> | <dl> <span data-ttu-id="8fd6a-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8fd6a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fd6a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fd6a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fd6a-120">**Clase CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="8fd6a-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




