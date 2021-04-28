---
description: 'Constructor CBaseStreamControl.CBaseStreamControl: método constructor.'
ms.assetid: c0eff80f-04d3-4919-bb27-1b76c1bd1cce
title: Constructor CBaseStreamControl.CBaseStreamControl (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4c6521bec65e0182b8eb48eb5d3efe9ea609c6a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095853"
---
# <a name="cbasestreamcontrolcbasestreamcontrol-constructor"></a><span data-ttu-id="f50b3-103">Constructor CBaseStreamControl.CBaseStreamControl</span><span class="sxs-lookup"><span data-stu-id="f50b3-103">CBaseStreamControl.CBaseStreamControl constructor</span></span>

<span data-ttu-id="f50b3-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="f50b3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f50b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f50b3-105">Syntax</span></span>


```C++
CBaseStreamControl(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="f50b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f50b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f50b3-107">*Phr*</span><span class="sxs-lookup"><span data-stu-id="f50b3-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f50b3-108">Puntero a un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="f50b3-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="f50b3-109">Si se produce un error en el constructor, este parámetro recibe un código de error.</span><span class="sxs-lookup"><span data-stu-id="f50b3-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="f50b3-110">Si esto ocurre, el objeto no está en un estado válido.</span><span class="sxs-lookup"><span data-stu-id="f50b3-110">If this occurs, the object is not in a valid state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f50b3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f50b3-111">Requirements</span></span>



| <span data-ttu-id="f50b3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f50b3-112">Requirement</span></span> | <span data-ttu-id="f50b3-113">Value</span><span class="sxs-lookup"><span data-stu-id="f50b3-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f50b3-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f50b3-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f50b3-115"><dt>Strmctl.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f50b3-115"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f50b3-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f50b3-116">Library</span></span><br/> | <dl> <span data-ttu-id="f50b3-117"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f50b3-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f50b3-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f50b3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f50b3-119">**CBaseStreamControl (clase)**</span><span class="sxs-lookup"><span data-stu-id="f50b3-119">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




