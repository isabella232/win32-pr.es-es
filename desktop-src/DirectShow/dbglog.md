---
description: La macro DbgLog envía una cadena a la ubicación de salida de depuración, si el registro está habilitado para el tipo y el nivel especificados. Esta macro se omite en las compilaciones comerciales.
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: Macro DbgLog (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLog
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1cd3f4e53c61fef1f030f654bbb0363cd7c97381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679496"
---
# <a name="dbglog-macro"></a><span data-ttu-id="a01d0-104">DbgLog (macro)</span><span class="sxs-lookup"><span data-stu-id="a01d0-104">DbgLog macro</span></span>

<span data-ttu-id="a01d0-105">La macro **DbgLog** envía una cadena a la ubicación de salida de depuración, si el registro está habilitado para el tipo y el nivel especificados.</span><span class="sxs-lookup"><span data-stu-id="a01d0-105">The **DbgLog** macro sends a string to the debug output location, if logging is enabled for the specified type and level.</span></span> <span data-ttu-id="a01d0-106">Esta macro se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="a01d0-106">This macro is ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="a01d0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a01d0-107">Syntax</span></span>


```C++
void DbgLog(
         DWORD Types,
         DWORD Level,
   const TCHAR *pFormat,
               ...
);
```



## <a name="parameters"></a><span data-ttu-id="a01d0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a01d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a01d0-109">*Tipos*</span><span class="sxs-lookup"><span data-stu-id="a01d0-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="a01d0-110">Combinación bit a bit de uno o varios tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a01d0-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="a01d0-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="a01d0-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="a01d0-112">Nivel de registro para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="a01d0-112">Logging level for this message.</span></span>

</dd> <dt>

<span data-ttu-id="a01d0-113">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="a01d0-113">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="a01d0-114">Una cadena de formato de estilo **printf** .</span><span class="sxs-lookup"><span data-stu-id="a01d0-114">A **printf** -style format string.</span></span>

</dd> <dt>

<span data-ttu-id="a01d0-115">*...*</span><span class="sxs-lookup"><span data-stu-id="a01d0-115">*...*</span></span> 
</dt> <dd>

<span data-ttu-id="a01d0-116">Argumentos adicionales para la cadena de formato.</span><span class="sxs-lookup"><span data-stu-id="a01d0-116">Additional arguments for the format string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a01d0-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a01d0-117">Return value</span></span>

<span data-ttu-id="a01d0-118">Esta macro no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a01d0-118">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a01d0-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a01d0-119">Remarks</span></span>

<span data-ttu-id="a01d0-120">Si el registro de depuración para cualquiera de los tipos de mensaje se establece en el nivel especificado o superior, esta macro envía la cadena con formato a la ubicación de salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="a01d0-120">If debug logging for any of the message types is set to the specified level or higher, this macro sends the formatted string to the debug output location.</span></span>

<span data-ttu-id="a01d0-121">La macro agrega automáticamente un carácter de nueva línea a la cadena de salida.</span><span class="sxs-lookup"><span data-stu-id="a01d0-121">The macro automatically adds a newline character to the output string.</span></span>

> [!Note]  
> <span data-ttu-id="a01d0-122">Un conjunto adicional de paréntesis debe incluir los parámetros de la macro:</span><span class="sxs-lookup"><span data-stu-id="a01d0-122">An additional set of parentheses must enclose the macro parameters:</span></span>

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a><span data-ttu-id="a01d0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a01d0-123">Requirements</span></span>



| <span data-ttu-id="a01d0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a01d0-124">Requirement</span></span> | <span data-ttu-id="a01d0-125">Value</span><span class="sxs-lookup"><span data-stu-id="a01d0-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a01d0-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a01d0-126">Header</span></span><br/> | <dl> <span data-ttu-id="a01d0-127"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a01d0-127"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a01d0-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a01d0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a01d0-129">Funciones de salida de depuración</span><span class="sxs-lookup"><span data-stu-id="a01d0-129">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




