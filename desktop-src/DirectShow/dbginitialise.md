---
description: La función DbgInitialise inicializa la biblioteca de depuración. Se omite en las compilaciones comerciales.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: Función DbgInitialise (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgInitialise
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a62c8dad7ef6e15b9b11461303b1bced977a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679497"
---
# <a name="dbginitialise-function"></a><span data-ttu-id="85cbe-104">DbgInitialise función)</span><span class="sxs-lookup"><span data-stu-id="85cbe-104">DbgInitialise function</span></span>

<span data-ttu-id="85cbe-105">La función **DbgInitialise** inicializa la biblioteca de depuración.</span><span class="sxs-lookup"><span data-stu-id="85cbe-105">The **DbgInitialise** function initializes the debug library.</span></span> <span data-ttu-id="85cbe-106">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="85cbe-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="85cbe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85cbe-107">Syntax</span></span>


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a><span data-ttu-id="85cbe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85cbe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85cbe-109">*hInst*</span><span class="sxs-lookup"><span data-stu-id="85cbe-109">*hInst*</span></span> 
</dt> <dd>

<span data-ttu-id="85cbe-110">Identificador de la instancia de módulo.</span><span class="sxs-lookup"><span data-stu-id="85cbe-110">Handle to the module instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85cbe-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85cbe-111">Return value</span></span>

<span data-ttu-id="85cbe-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="85cbe-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85cbe-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85cbe-113">Remarks</span></span>

<span data-ttu-id="85cbe-114">En un archivo ejecutable, llame a este método antes de usar las funciones de depuración de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="85cbe-114">In an executable, call this method before using the DirectShow debug facilities.</span></span> <span data-ttu-id="85cbe-115">Antes de que se cierre el archivo ejecutable, llame a la función [**DbgTerminate**](dbgterminate.md) para limpiar la biblioteca de depuración.</span><span class="sxs-lookup"><span data-stu-id="85cbe-115">Before the executable quits, call the [**DbgTerminate**](dbgterminate.md) function to clean up the debug library.</span></span>

<span data-ttu-id="85cbe-116">En un archivo DLL que se vincula a la biblioteca de clases base (Strmbase. lib), no es necesario llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="85cbe-116">In a DLL that links to the base-class library (Strmbase.lib), it is not necessary to call this function.</span></span> <span data-ttu-id="85cbe-117">Se llama a la función automáticamente cuando se carga el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="85cbe-117">The function is called automatically when the DLL is loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="85cbe-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85cbe-118">Requirements</span></span>



| <span data-ttu-id="85cbe-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="85cbe-119">Requirement</span></span> | <span data-ttu-id="85cbe-120">Value</span><span class="sxs-lookup"><span data-stu-id="85cbe-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85cbe-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85cbe-121">Header</span></span><br/>  | <dl> <span data-ttu-id="85cbe-122"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85cbe-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85cbe-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85cbe-123">Library</span></span><br/> | <dl> <span data-ttu-id="85cbe-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="85cbe-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85cbe-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="85cbe-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85cbe-126">Funciones de salida de depuración</span><span class="sxs-lookup"><span data-stu-id="85cbe-126">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




