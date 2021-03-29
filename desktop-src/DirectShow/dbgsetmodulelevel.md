---
description: La función DbgSetModuleLevel establece el nivel de registro para uno o más tipos de mensaje. Se omite en las compilaciones comerciales.
ms.assetid: 89d25106-8018-4089-8b77-d3c87529e984
title: Función DbgSetModuleLevel (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d6623793b150c600eb00f0c0843dd72c68deb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660499"
---
# <a name="dbgsetmodulelevel-function"></a><span data-ttu-id="608ab-104">DbgSetModuleLevel función)</span><span class="sxs-lookup"><span data-stu-id="608ab-104">DbgSetModuleLevel function</span></span>

<span data-ttu-id="608ab-105">La función **DbgSetModuleLevel** establece el nivel de registro para uno o más tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="608ab-105">The **DbgSetModuleLevel** function sets the logging level for one or more message types.</span></span> <span data-ttu-id="608ab-106">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="608ab-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="608ab-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="608ab-107">Syntax</span></span>


```C++
void DbgSetModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="608ab-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="608ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="608ab-109">*Tipos*</span><span class="sxs-lookup"><span data-stu-id="608ab-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="608ab-110">Combinación bit a bit de uno o varios tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="608ab-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="608ab-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="608ab-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="608ab-112">Nivel de registro de los tipos de mensaje especificados.</span><span class="sxs-lookup"><span data-stu-id="608ab-112">Logging level for the specified message types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="608ab-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="608ab-113">Return value</span></span>

<span data-ttu-id="608ab-114">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="608ab-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="608ab-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="608ab-115">Requirements</span></span>



| <span data-ttu-id="608ab-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="608ab-116">Requirement</span></span> | <span data-ttu-id="608ab-117">Value</span><span class="sxs-lookup"><span data-stu-id="608ab-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="608ab-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="608ab-118">Header</span></span><br/>  | <dl> <span data-ttu-id="608ab-119"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="608ab-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="608ab-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="608ab-120">Library</span></span><br/> | <dl> <span data-ttu-id="608ab-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="608ab-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="608ab-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="608ab-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="608ab-123">Funciones de salida de depuración</span><span class="sxs-lookup"><span data-stu-id="608ab-123">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




