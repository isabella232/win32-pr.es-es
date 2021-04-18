---
description: Evalúa una expresión y produce una excepción de punto de interrupción Si la expresión es falsa. El texto de la expresión, el nombre del archivo de código fuente y el número de línea se registran con la macro DbgLog. Se omite en las compilaciones comerciales.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: Macro KASSERT (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: f797e60a6175a86f2c1c9d675e9607a48a58c14a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681185"
---
# <a name="kassert-macro"></a><span data-ttu-id="623f5-105">KASSERT (macro)</span><span class="sxs-lookup"><span data-stu-id="623f5-105">KASSERT macro</span></span>

<span data-ttu-id="623f5-106">Evalúa una expresión y produce una excepción de punto de interrupción Si la expresión es **falsa**.</span><span class="sxs-lookup"><span data-stu-id="623f5-106">Evaluates an expression, and causes a breakpoint exception if the expression is **FALSE**.</span></span> <span data-ttu-id="623f5-107">El texto de la expresión, el nombre del archivo de código fuente y el número de línea se registran con la macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="623f5-107">The text of the expression, the name of the source file, and the line number are logged using the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="623f5-108">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="623f5-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="623f5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="623f5-109">Syntax</span></span>


```C++
void KASSERT(
    cond
);
```



## <a name="parameters"></a><span data-ttu-id="623f5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="623f5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="623f5-111">*Cond*</span><span class="sxs-lookup"><span data-stu-id="623f5-111">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="623f5-112">Expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="623f5-112">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="623f5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="623f5-113">Return value</span></span>

<span data-ttu-id="623f5-114">Esta macro no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="623f5-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="623f5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="623f5-115">Remarks</span></span>

<span data-ttu-id="623f5-116">A diferencia de las macros [**Assert**](assert.md) y [**Execute \_ Assert**](execute-assert.md) , esta macro no muestra un cuadro de mensaje que pide al usuario.</span><span class="sxs-lookup"><span data-stu-id="623f5-116">Unlike the [**ASSERT**](assert.md) and [**EXECUTE\_ASSERT**](execute-assert.md) macros, this macro does not display a message box prompting the user.</span></span> <span data-ttu-id="623f5-117">En las compilaciones de depuración, si la expresión es **falsa**, la macro provoca automáticamente que se produzca una excepción de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="623f5-117">In debug builds, if the expression is **FALSE**, the macro automatically causes a breakpoint exception to occur.</span></span>

## <a name="requirements"></a><span data-ttu-id="623f5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="623f5-118">Requirements</span></span>



| <span data-ttu-id="623f5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="623f5-119">Requirement</span></span> | <span data-ttu-id="623f5-120">Value</span><span class="sxs-lookup"><span data-stu-id="623f5-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="623f5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="623f5-121">Header</span></span><br/> | <dl> <span data-ttu-id="623f5-122"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="623f5-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="623f5-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="623f5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="623f5-124">Macros Assert y Breakpoint</span><span class="sxs-lookup"><span data-stu-id="623f5-124">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




