---
description: Recupera la versión de software para esta secuencia.
ms.assetid: f54153df-5593-4784-acc5-3e0dcef424b5
title: Método CPersistStream. GetSoftwareVersion (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSoftwareVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0954e9a113342217dd389c64ec4fc6c04a6f767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680375"
---
# <a name="cpersiststreamgetsoftwareversion-method"></a><span data-ttu-id="75e44-103">CPersistStream. GetSoftwareVersion, método</span><span class="sxs-lookup"><span data-stu-id="75e44-103">CPersistStream.GetSoftwareVersion method</span></span>

<span data-ttu-id="75e44-104">Recupera la versión de software para esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="75e44-104">Retrieves the software version for this stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="75e44-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75e44-105">Syntax</span></span>


```C++
virtual DWORD GetSoftwareVersion();
```



## <a name="parameters"></a><span data-ttu-id="75e44-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75e44-106">Parameters</span></span>

<span data-ttu-id="75e44-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="75e44-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75e44-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75e44-108">Return value</span></span>

<span data-ttu-id="75e44-109">Devuelve un **valor DWORD** que contiene el número de versión.</span><span class="sxs-lookup"><span data-stu-id="75e44-109">Returns a **DWORD** containing the version number.</span></span> <span data-ttu-id="75e44-110">Cada vez que se cambia el formato de la secuencia, esta función se debe modificar para que devuelva un número mayor que antes.</span><span class="sxs-lookup"><span data-stu-id="75e44-110">Each time the format of the stream is changed, this function should be altered to return a larger number than before.</span></span>

## <a name="requirements"></a><span data-ttu-id="75e44-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75e44-111">Requirements</span></span>



| <span data-ttu-id="75e44-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="75e44-112">Requirement</span></span> | <span data-ttu-id="75e44-113">Value</span><span class="sxs-lookup"><span data-stu-id="75e44-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75e44-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75e44-114">Header</span></span><br/>  | <dl> <span data-ttu-id="75e44-115"><dt>PStream. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75e44-115"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="75e44-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75e44-116">Library</span></span><br/> | <dl> <span data-ttu-id="75e44-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="75e44-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75e44-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="75e44-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75e44-119">**Clase CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="75e44-119">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




