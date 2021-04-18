---
description: El método GetOwner recupera un puntero a la interfaz IUnknown del componente propietario. Para un componente agregado, el propietario es el componente externo. De lo contrario, el componente es el propietario.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: Método CUnknown. GetOwner (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.GetOwner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e3cb1cd1d5b183857b6d75db79ee0fcdc6cb2d30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661059"
---
# <a name="cunknowngetowner-method"></a><span data-ttu-id="2c275-105">CUnknown. GetOwner, método</span><span class="sxs-lookup"><span data-stu-id="2c275-105">CUnknown.GetOwner method</span></span>

<span data-ttu-id="2c275-106">El `GetOwner` método recupera un puntero a la interfaz **IUnknown** del componente propietario.</span><span class="sxs-lookup"><span data-stu-id="2c275-106">The `GetOwner` method retrieves a pointer to the **IUnknown** interface of the owning component.</span></span> <span data-ttu-id="2c275-107">Para un componente agregado, el propietario es el componente externo.</span><span class="sxs-lookup"><span data-stu-id="2c275-107">For an aggregated component, the owner is the outer component.</span></span> <span data-ttu-id="2c275-108">De lo contrario, el componente es el propietario.</span><span class="sxs-lookup"><span data-stu-id="2c275-108">Otherwise, the component owns itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c275-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c275-109">Syntax</span></span>


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a><span data-ttu-id="2c275-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c275-110">Parameters</span></span>

<span data-ttu-id="2c275-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2c275-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c275-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c275-112">Return value</span></span>

<span data-ttu-id="2c275-113">Devuelve un puntero a la interfaz **IUnknown** de control.</span><span class="sxs-lookup"><span data-stu-id="2c275-113">Returns a pointer to the controlling **IUnknown** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c275-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c275-114">Requirements</span></span>



| <span data-ttu-id="2c275-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c275-115">Requirement</span></span> | <span data-ttu-id="2c275-116">Value</span><span class="sxs-lookup"><span data-stu-id="2c275-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c275-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c275-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2c275-118"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c275-118"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2c275-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c275-119">Library</span></span><br/> | <dl> <span data-ttu-id="2c275-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2c275-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




