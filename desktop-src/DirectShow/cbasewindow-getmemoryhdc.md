---
description: El método GetMemoryHDC recupera un identificador para el contexto de dispositivo de memoria (DC).
ms.assetid: 2c22015f-5948-4e1a-92c7-36f232816175
title: Método CBaseWindow. GetMemoryHDC (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetMemoryHDC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c255ac8734f364597c09fc15b4aa543b1ec0a0da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679567"
---
# <a name="cbasewindowgetmemoryhdc-method"></a><span data-ttu-id="b8b3b-103">CBaseWindow. GetMemoryHDC, método</span><span class="sxs-lookup"><span data-stu-id="b8b3b-103">CBaseWindow.GetMemoryHDC method</span></span>

<span data-ttu-id="b8b3b-104">El `GetMemoryHDC` método recupera un identificador para el contexto de dispositivo de memoria (DC).</span><span class="sxs-lookup"><span data-stu-id="b8b3b-104">The `GetMemoryHDC` method retrieves a handle to the memory device context (DC).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8b3b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8b3b-105">Syntax</span></span>


```C++
virtual HDC GetMemoryHDC();
```



## <a name="parameters"></a><span data-ttu-id="b8b3b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8b3b-106">Parameters</span></span>

<span data-ttu-id="b8b3b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b8b3b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8b3b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8b3b-108">Return value</span></span>

<span data-ttu-id="b8b3b-109">Devuelve un identificador para el controlador de dominio de memoria.</span><span class="sxs-lookup"><span data-stu-id="b8b3b-109">Returns a handle to the memory DC.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8b3b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8b3b-110">Requirements</span></span>



| <span data-ttu-id="b8b3b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8b3b-111">Requirement</span></span> | <span data-ttu-id="b8b3b-112">Value</span><span class="sxs-lookup"><span data-stu-id="b8b3b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b3b-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8b3b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="b8b3b-114"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8b3b-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b8b3b-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8b3b-115">Library</span></span><br/> | <dl> <span data-ttu-id="b8b3b-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b8b3b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8b3b-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8b3b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8b3b-118">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="b8b3b-118">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




