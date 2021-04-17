---
description: La función DbgCheckModuleLevel comprueba si el registro está habilitado para los tipos de mensaje y el nivel especificados. Se omite en las compilaciones comerciales.
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: Función DbgCheckModuleLevel (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgCheckModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79df8cd06617cf9b17fa9933d4d7a87954a6e2b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681053"
---
# <a name="dbgcheckmodulelevel-function"></a><span data-ttu-id="c0c84-104">DbgCheckModuleLevel función)</span><span class="sxs-lookup"><span data-stu-id="c0c84-104">DbgCheckModuleLevel function</span></span>

<span data-ttu-id="c0c84-105">La `DbgCheckModuleLevel` función comprueba si el registro está habilitado para los tipos de mensaje y el nivel especificados.</span><span class="sxs-lookup"><span data-stu-id="c0c84-105">The `DbgCheckModuleLevel` function checks whether logging is enabled for the given message types and level.</span></span> <span data-ttu-id="c0c84-106">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="c0c84-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0c84-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0c84-107">Syntax</span></span>


```C++
BOOL DbgCheckModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="c0c84-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0c84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0c84-109">*Tipos*</span><span class="sxs-lookup"><span data-stu-id="c0c84-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="c0c84-110">Combinación bit a bit de uno o varios tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c0c84-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="c0c84-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="c0c84-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="c0c84-112">Nivel de registro</span><span class="sxs-lookup"><span data-stu-id="c0c84-112">Logging level</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0c84-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0c84-113">Return value</span></span>

<span data-ttu-id="c0c84-114">Devuelve **true** si el registro de cualquiera de los tipos de mensaje especificados está establecido en el nivel especificado o superior.</span><span class="sxs-lookup"><span data-stu-id="c0c84-114">Returns **TRUE** if logging for any of the specified message types is set to the specified level or higher.</span></span> <span data-ttu-id="c0c84-115">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="c0c84-115">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0c84-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0c84-116">Requirements</span></span>



| <span data-ttu-id="c0c84-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0c84-117">Requirement</span></span> | <span data-ttu-id="c0c84-118">Value</span><span class="sxs-lookup"><span data-stu-id="c0c84-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c84-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0c84-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c0c84-120"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0c84-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c0c84-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0c84-121">Library</span></span><br/> | <dl> <span data-ttu-id="c0c84-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c0c84-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0c84-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0c84-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0c84-124">Funciones de salida de depuración</span><span class="sxs-lookup"><span data-stu-id="c0c84-124">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




