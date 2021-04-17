---
description: Puntero a una función a la que se llama desde el punto de entrada de DLL. Puede ser NULL.
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: 'Miembro CFactoryTemplate:: m_lpfnInit (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnInit
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b44181f926f77ecc7cc22673622d4a0d3dcb7d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660848"
---
# <a name="cfactorytemplatem_lpfninit-member"></a><span data-ttu-id="b6c0b-104">Miembro lpfnInit CFactoryTemplate:: m \_</span><span class="sxs-lookup"><span data-stu-id="b6c0b-104">CFactoryTemplate::m\_lpfnInit member</span></span>

<span data-ttu-id="b6c0b-105">Puntero a una función a la que se llama desde el punto de entrada de DLL.</span><span class="sxs-lookup"><span data-stu-id="b6c0b-105">Pointer to a function that gets called from the DLL entry point.</span></span> <span data-ttu-id="b6c0b-106">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="b6c0b-106">Can be **NULL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c0b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6c0b-107">Syntax</span></span>


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a><span data-ttu-id="b6c0b-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6c0b-108">Remarks</span></span>

<span data-ttu-id="b6c0b-109">El tipo de puntero de función es [**LPFNInitRoutine**](lpfninitroutine.md).</span><span class="sxs-lookup"><span data-stu-id="b6c0b-109">The function pointer type is [**LPFNInitRoutine**](lpfninitroutine.md).</span></span> <span data-ttu-id="b6c0b-110">Si proporciona esta función en el archivo DLL, la función de punto de entrada del archivo DLL lo llama con los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="b6c0b-110">If you provide this function in your DLL, the DLL entry-point function calls it with following parameters:</span></span>

-   <span data-ttu-id="b6c0b-111">*bLoading*: **true** cuando se carga el archivo dll, **false** cuando se descarga el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="b6c0b-111">*bLoading*: **TRUE** when the DLL is loaded, **FALSE** when the DLL is unloaded.</span></span>
-   <span data-ttu-id="b6c0b-112">*rclsid*: puntero a la CLISD del objeto, que se especifica en la variable miembro de [**\_ ClsID CFactoryTemplate:: m**](cfactorytemplate-m-clsid.md) .</span><span class="sxs-lookup"><span data-stu-id="b6c0b-112">*rclsid*: Pointer to the object's CLISD, specified in the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c0b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6c0b-113">Requirements</span></span>



| <span data-ttu-id="b6c0b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6c0b-114">Requirement</span></span> | <span data-ttu-id="b6c0b-115">Value</span><span class="sxs-lookup"><span data-stu-id="b6c0b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c0b-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6c0b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b6c0b-117"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6c0b-117"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b6c0b-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6c0b-118">Library</span></span><br/> | <dl> <span data-ttu-id="b6c0b-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b6c0b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6c0b-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6c0b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c0b-121">**Clase CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="b6c0b-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




