---
description: Identificador de la instancia de módulo.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: 'Miembro CBaseWindow:: m_hInstance (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hInstance
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6482aac80c1298ea403019f43ddc4effdc30b00a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660323"
---
# <a name="cbasewindowm_hinstance-member"></a><span data-ttu-id="e46a0-103">Miembro hInstance CBaseWindow:: m \_</span><span class="sxs-lookup"><span data-stu-id="e46a0-103">CBaseWindow::m\_hInstance member</span></span>

<span data-ttu-id="e46a0-104">Identificador de la instancia de módulo.</span><span class="sxs-lookup"><span data-stu-id="e46a0-104">Handle to the module instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="e46a0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e46a0-105">Syntax</span></span>


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a><span data-ttu-id="e46a0-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e46a0-106">Remarks</span></span>

<span data-ttu-id="e46a0-107">La función de punto de entrada de DLL establece una variable global con un identificador para la instancia de módulo.</span><span class="sxs-lookup"><span data-stu-id="e46a0-107">The DLL entry point function sets a global variable with a handle to the module instance.</span></span> <span data-ttu-id="e46a0-108">La clase **CBaseWindow** almacena este identificador en su método constructor.</span><span class="sxs-lookup"><span data-stu-id="e46a0-108">The **CBaseWindow** class stores this handle in its constructor method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e46a0-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e46a0-109">Requirements</span></span>



| <span data-ttu-id="e46a0-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="e46a0-110">Requirement</span></span> | <span data-ttu-id="e46a0-111">Value</span><span class="sxs-lookup"><span data-stu-id="e46a0-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e46a0-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e46a0-112">Header</span></span><br/>  | <dl> <span data-ttu-id="e46a0-113"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e46a0-113"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e46a0-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e46a0-114">Library</span></span><br/> | <dl> <span data-ttu-id="e46a0-115"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e46a0-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e46a0-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="e46a0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e46a0-117">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="e46a0-117">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




