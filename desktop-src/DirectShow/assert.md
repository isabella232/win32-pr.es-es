---
description: Evalúa una expresión y muestra un mensaje de diagnóstico si la expresión es falsa. Se omite en las compilaciones comerciales.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: Macro Assert (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 8617d1c86f655cc9b44ea6619931f73888ae2a67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680226"
---
# <a name="assert-macro"></a><span data-ttu-id="647df-104">ASSERT (macro)</span><span class="sxs-lookup"><span data-stu-id="647df-104">ASSERT macro</span></span>

<span data-ttu-id="647df-105">Evalúa una expresión y muestra un mensaje de diagnóstico si la expresión es **falsa**.</span><span class="sxs-lookup"><span data-stu-id="647df-105">Evaluates an expression, and displays a diagnostic message if the expression is **FALSE**.</span></span> <span data-ttu-id="647df-106">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="647df-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="647df-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="647df-107">Syntax</span></span>


```C++
void ASSERT(
   BOOL cond
);
```



## <a name="parameters"></a><span data-ttu-id="647df-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="647df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="647df-109">*Cond*</span><span class="sxs-lookup"><span data-stu-id="647df-109">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="647df-110">Expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="647df-110">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="647df-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="647df-111">Return value</span></span>

<span data-ttu-id="647df-112">Esta macro no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="647df-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="647df-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="647df-113">Remarks</span></span>

<span data-ttu-id="647df-114">En las compilaciones de depuración, si la expresión es **false**, esta macro muestra un cuadro de mensaje con el texto de la expresión, el nombre del archivo de código fuente y el número de línea.</span><span class="sxs-lookup"><span data-stu-id="647df-114">In debug builds, if the expression is **FALSE**, this macro displays a message box with the text of the expression, the name of the source file, and the line number.</span></span> <span data-ttu-id="647df-115">El usuario puede omitir la aserción, entrar en el depurador o salir de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="647df-115">The user can ignore the assertion, enter the debugger, or quit the application.</span></span>

## <a name="examples"></a><span data-ttu-id="647df-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="647df-116">Examples</span></span>


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a><span data-ttu-id="647df-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="647df-117">Requirements</span></span>



| <span data-ttu-id="647df-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="647df-118">Requirement</span></span> | <span data-ttu-id="647df-119">Value</span><span class="sxs-lookup"><span data-stu-id="647df-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="647df-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="647df-120">Header</span></span><br/> | <dl> <span data-ttu-id="647df-121"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="647df-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="647df-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="647df-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="647df-123">Macros Assert y Breakpoint</span><span class="sxs-lookup"><span data-stu-id="647df-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




