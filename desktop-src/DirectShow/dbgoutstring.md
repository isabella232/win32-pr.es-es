---
description: La función DbgOutString envía una cadena a la ubicación de salida de depuración. Se omite en las compilaciones comerciales.
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: Función DbgOutString (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgOutString
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc12d4b73080f00a3d32c80074a801146ea4a74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660500"
---
# <a name="dbgoutstring-function"></a><span data-ttu-id="a412d-104">DbgOutString función)</span><span class="sxs-lookup"><span data-stu-id="a412d-104">DbgOutString function</span></span>

<span data-ttu-id="a412d-105">La función **DbgOutString** envía una cadena a la ubicación de salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="a412d-105">The **DbgOutString** function sends a string to the debug output location.</span></span> <span data-ttu-id="a412d-106">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="a412d-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="a412d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a412d-107">Syntax</span></span>


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a><span data-ttu-id="a412d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a412d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a412d-109">*psz*</span><span class="sxs-lookup"><span data-stu-id="a412d-109">*psz*</span></span> 
</dt> <dd>

<span data-ttu-id="a412d-110">Cadena que se va a generar.</span><span class="sxs-lookup"><span data-stu-id="a412d-110">String to output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a412d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a412d-111">Return value</span></span>

<span data-ttu-id="a412d-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a412d-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a412d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a412d-113">Remarks</span></span>

<span data-ttu-id="a412d-114">En las compilaciones de depuración, esta función siempre genera la cadena, independientemente de los niveles de salida de depuración actuales.</span><span class="sxs-lookup"><span data-stu-id="a412d-114">In debug builds, this function always outputs the string, regardless of the current debug output levels.</span></span> <span data-ttu-id="a412d-115">Para obtener un mayor control sobre la salida, use la macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="a412d-115">For finer control over the output, use the [**DbgLog**](dbglog.md) macro.</span></span>

## <a name="examples"></a><span data-ttu-id="a412d-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a412d-116">Examples</span></span>


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a><span data-ttu-id="a412d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a412d-117">Requirements</span></span>



| <span data-ttu-id="a412d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a412d-118">Requirement</span></span> | <span data-ttu-id="a412d-119">Value</span><span class="sxs-lookup"><span data-stu-id="a412d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a412d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a412d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a412d-121"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a412d-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a412d-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a412d-122">Library</span></span><br/> | <dl> <span data-ttu-id="a412d-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a412d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a412d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a412d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a412d-125">Funciones de salida de depuración</span><span class="sxs-lookup"><span data-stu-id="a412d-125">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




