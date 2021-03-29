---
description: Evalúa una expresión en las compilaciones de depuración y comerciales. En compilaciones de depuración, muestra un mensaje de diagnóstico si la expresión es falsa.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: Macro EXECUTE_ASSERT (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXECUTE_ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 5db5e78d198cc9f66aa5de6fdb0160e325b82591
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654001"
---
# <a name="execute_assert-macro"></a><span data-ttu-id="5e122-104">EJECUTAR \_ macro Assert</span><span class="sxs-lookup"><span data-stu-id="5e122-104">EXECUTE\_ASSERT macro</span></span>

<span data-ttu-id="5e122-105">Evalúa una expresión en las compilaciones de depuración y comerciales.</span><span class="sxs-lookup"><span data-stu-id="5e122-105">Evaluates an expression in debug and retail builds.</span></span> <span data-ttu-id="5e122-106">En compilaciones de depuración, muestra un mensaje de diagnóstico si la expresión es **falsa**.</span><span class="sxs-lookup"><span data-stu-id="5e122-106">In debug builds, displays a diagnostic message if the expression is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e122-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e122-107">Syntax</span></span>


```C++
void EXECUTE_ASSERT(
    cond
);
```



## <a name="parameters"></a><span data-ttu-id="5e122-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e122-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e122-109">*Cond*</span><span class="sxs-lookup"><span data-stu-id="5e122-109">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="5e122-110">Expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="5e122-110">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e122-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e122-111">Return value</span></span>

<span data-ttu-id="5e122-112">Esta macro no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5e122-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e122-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e122-113">Remarks</span></span>

<span data-ttu-id="5e122-114">A diferencia de la macro [**Assert**](assert.md) , esta macro evalúa la expresión en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="5e122-114">Unlike the [**ASSERT**](assert.md) macro, this macro evaluates the expression in retail builds.</span></span> <span data-ttu-id="5e122-115">En las compilaciones de depuración, si la expresión es **falsa**, la macro muestra un cuadro de mensaje con el texto de la expresión, el nombre del archivo de código fuente y el número de línea.</span><span class="sxs-lookup"><span data-stu-id="5e122-115">In debug builds, if the expression is **FALSE**, the macro displays a message box with the text of the expression, the name of the source file, and the line number.</span></span> <span data-ttu-id="5e122-116">El usuario puede omitir la aserción, entrar en el depurador o salir de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e122-116">The user can ignore the assertion, enter the debugger, or quit the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e122-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e122-117">Requirements</span></span>



| <span data-ttu-id="5e122-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e122-118">Requirement</span></span> | <span data-ttu-id="5e122-119">Value</span><span class="sxs-lookup"><span data-stu-id="5e122-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e122-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e122-120">Header</span></span><br/> | <dl> <span data-ttu-id="5e122-121"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e122-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e122-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e122-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e122-123">Macros Assert y Breakpoint</span><span class="sxs-lookup"><span data-stu-id="5e122-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




