---
description: Indica si el \_ \_ bloque try de un controlador de terminación terminó normalmente. Solo se puede llamar a la función desde dentro del \_ \_ bloque Finally de un controlador de finalización.
ms.assetid: 0ddaef1f-03f0-45fc-9c5e-8d6a26a73245
title: AbnormalTermination (macro)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbnormalTermination
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7c4869f36d8ba70c8dcd8ca526949d489f455e8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000748"
---
# <a name="abnormaltermination-macro"></a><span data-ttu-id="2a433-104">AbnormalTermination (macro)</span><span class="sxs-lookup"><span data-stu-id="2a433-104">AbnormalTermination macro</span></span>

<span data-ttu-id="2a433-105">Indica si el bloque **\_ \_ try** de un controlador de terminación terminó normalmente.</span><span class="sxs-lookup"><span data-stu-id="2a433-105">Indicates whether the **\_\_try** block of a termination handler terminated normally.</span></span> <span data-ttu-id="2a433-106">Solo se puede llamar a la función desde dentro del bloque **\_ \_ Finally** de un controlador de finalización.</span><span class="sxs-lookup"><span data-stu-id="2a433-106">The function can be called only from within the **\_\_finally** block of a termination handler.</span></span>

> [!Note]  
> <span data-ttu-id="2a433-107">El compilador de optimización de C/C++ de Microsoft interpreta esta función como una palabra clave y su uso fuera de la sintaxis de control de excepciones adecuada genera un error del compilador.</span><span class="sxs-lookup"><span data-stu-id="2a433-107">The Microsoft C/C++ Optimizing Compiler interprets this function as a keyword, and its use outside the appropriate exception-handling syntax generates a compiler error.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2a433-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a433-108">Syntax</span></span>


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a><span data-ttu-id="2a433-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a433-109">Parameters</span></span>

<span data-ttu-id="2a433-110">Esta macro no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2a433-110">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2a433-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a433-111">Return value</span></span>

<span data-ttu-id="2a433-112">Si el bloque **\_ \_ try** terminó de forma anómala, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="2a433-112">If the **\_\_try** block terminated abnormally, the return value is nonzero.</span></span>

<span data-ttu-id="2a433-113">Si el bloque **\_ \_ try** terminó normalmente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="2a433-113">If the **\_\_try** block terminated normally, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a433-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a433-114">Remarks</span></span>

<span data-ttu-id="2a433-115">El bloque **\_ \_ try** finaliza normalmente solo si la ejecución deja el bloque secuencialmente después de ejecutar la última instrucción del bloque.</span><span class="sxs-lookup"><span data-stu-id="2a433-115">The **\_\_try** block terminates normally only if execution leaves the block sequentially after executing the last statement in the block.</span></span> <span data-ttu-id="2a433-116">Las instrucciones (como **Return**, **goto**, **continue** o **break**) que provocan que la ejecución deje el bloque **\_ \_ try** dan como resultado una terminación anómala del bloque.</span><span class="sxs-lookup"><span data-stu-id="2a433-116">Statements (such as **return**, **goto**, **continue**, or **break**) that cause execution to leave the **\_\_try** block result in abnormal termination of the block.</span></span> <span data-ttu-id="2a433-117">Este es el caso incluso si dicha instrucción es la última instrucción del bloque **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="2a433-117">This is the case even if such a statement is the last statement in the **\_\_try** block.</span></span>

<span data-ttu-id="2a433-118">La terminación anómala de un bloque **\_ \_ try** hace que el sistema busque hacia atrás en todos los marcos de pila para determinar si se debe llamar a algún controlador de finalización.</span><span class="sxs-lookup"><span data-stu-id="2a433-118">Abnormal termination of a **\_\_try** block causes the system to search backward through all stack frames to determine whether any termination handlers must be called.</span></span> <span data-ttu-id="2a433-119">Esto puede dar lugar a la ejecución de cientos de instrucciones, por lo que es importante evitar la terminación anómala de un bloque **\_ \_ try** debido a una instrucción **Return**, **goto**, **continue** o **break** .</span><span class="sxs-lookup"><span data-stu-id="2a433-119">This can result in the execution of hundreds of instructions, so it is important to avoid abnormal termination of a **\_\_try** block due to a **return**, **goto**, **continue**, or **break** statement.</span></span> <span data-ttu-id="2a433-120">Tenga en cuenta que estas instrucciones no generan una excepción, aunque la terminación sea anómala.</span><span class="sxs-lookup"><span data-stu-id="2a433-120">Note that these statements do not generate an exception, even though the termination is abnormal.</span></span>

<span data-ttu-id="2a433-121">Para evitar la terminación anómala, la ejecución debería continuar hasta el final del bloque.</span><span class="sxs-lookup"><span data-stu-id="2a433-121">To avoid abnormal termination, execution should continue to the end of the block.</span></span> <span data-ttu-id="2a433-122">También puede ejecutar la instrucción **\_ \_ leave** .</span><span class="sxs-lookup"><span data-stu-id="2a433-122">You can also execute the **\_\_leave** statement.</span></span> <span data-ttu-id="2a433-123">La instrucción **\_ \_ leave** permite la terminación inmediata del bloque **\_ \_ try** sin causar una terminación anómala y su penalización en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="2a433-123">The **\_\_leave** statement allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span> <span data-ttu-id="2a433-124">Consulte la documentación del compilador para determinar si se admite la instrucción **\_ \_ leave** .</span><span class="sxs-lookup"><span data-stu-id="2a433-124">Check your compiler documentation to determine if the **\_\_leave** statement is supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a433-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a433-125">Requirements</span></span>



| <span data-ttu-id="2a433-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a433-126">Requirement</span></span> | <span data-ttu-id="2a433-127">Value</span><span class="sxs-lookup"><span data-stu-id="2a433-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2a433-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a433-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2a433-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2a433-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2a433-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a433-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2a433-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a433-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a433-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a433-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a433-133">Funciones de control de excepciones estructurado</span><span class="sxs-lookup"><span data-stu-id="2a433-133">Structured Exception Handling Functions</span></span>](structured-exception-handling-functions.md)
</dt> <dt>

[<span data-ttu-id="2a433-134">Información general sobre el control estructurado de excepciones</span><span class="sxs-lookup"><span data-stu-id="2a433-134">Structured Exception Handling Overview</span></span>](structured-exception-handling.md)
</dt> </dl>

 

 




