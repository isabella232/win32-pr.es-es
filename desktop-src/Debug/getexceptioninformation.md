---
description: Recupera una descripción independiente del equipo de una excepción e información sobre el estado del equipo que existe para el subproceso cuando se produce la excepción. Solo se puede llamar a esta función desde dentro de la expresión de filtro de un controlador de excepciones.
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: GetExceptionInformation (macro)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 243831a94a26b86df29d3a50413bfa9d6830a0e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807819"
---
# <a name="getexceptioninformation-macro"></a><span data-ttu-id="5482e-104">GetExceptionInformation (macro)</span><span class="sxs-lookup"><span data-stu-id="5482e-104">GetExceptionInformation macro</span></span>

<span data-ttu-id="5482e-105">Recupera una descripción independiente del equipo de una excepción e información sobre el estado del equipo que existe para el subproceso cuando se produce la excepción.</span><span class="sxs-lookup"><span data-stu-id="5482e-105">Retrieves a computer-independent description of an exception, and information about the computer state that exists for the thread when the exception occurs.</span></span> <span data-ttu-id="5482e-106">Solo se puede llamar a esta función desde dentro de la expresión de filtro de un controlador de excepciones.</span><span class="sxs-lookup"><span data-stu-id="5482e-106">This function can be called only from within the filter expression of an exception handler.</span></span>

> [!Note]  
> <span data-ttu-id="5482e-107">El compilador de optimización de C/C++ de Microsoft interpreta esta función como una palabra clave y su uso fuera de la sintaxis de control de excepciones adecuada genera un error del compilador.</span><span class="sxs-lookup"><span data-stu-id="5482e-107">The Microsoft C/C++ Optimizing Compiler interprets this function as a keyword, and its use outside the appropriate exception-handling syntax generates a compiler error.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5482e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5482e-108">Syntax</span></span>


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a><span data-ttu-id="5482e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5482e-109">Parameters</span></span>

<span data-ttu-id="5482e-110">Esta macro no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5482e-110">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5482e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5482e-111">Return value</span></span>

<span data-ttu-id="5482e-112">Un puntero a una estructura de [**\_ punteros de excepción**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) que contiene punteros a las dos estructuras siguientes:</span><span class="sxs-lookup"><span data-stu-id="5482e-112">A pointer to an [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) structure that contains pointers to the following two structures:</span></span>

-   <span data-ttu-id="5482e-113">[**Excepción \_ de**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Estructura de registro que contiene una descripción de la excepción.</span><span class="sxs-lookup"><span data-stu-id="5482e-113">[**EXCEPTION\_RECORD**](/windows/desktop/api/WinNT/ns-winnt-exception_record) structure that contains a description of the exception.</span></span>
-   <span data-ttu-id="5482e-114">Estructura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) que contiene la información de estado del equipo.</span><span class="sxs-lookup"><span data-stu-id="5482e-114">[**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure that contains the computer state information.</span></span>

## <a name="remarks"></a><span data-ttu-id="5482e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5482e-115">Remarks</span></span>

<span data-ttu-id="5482e-116">La expresión de filtro (desde la que se llama a la función) se evalúa si se produce una excepción durante la ejecución del bloque **\_ \_ try** y determina si se ejecuta el bloque **\_ \_ Except** .</span><span class="sxs-lookup"><span data-stu-id="5482e-116">The filter expression (from which the function is called) is evaluated if an exception occurs during execution of the **\_\_try** block, and it determines whether or not the **\_\_except** block is executed.</span></span>

<span data-ttu-id="5482e-117">La expresión de filtro puede invocar una función de filtro.</span><span class="sxs-lookup"><span data-stu-id="5482e-117">The filter expression can invoke a filter function.</span></span> <span data-ttu-id="5482e-118">La función Filter no puede llamar a **GetExceptionInformation**.</span><span class="sxs-lookup"><span data-stu-id="5482e-118">The filter function cannot call **GetExceptionInformation**.</span></span> <span data-ttu-id="5482e-119">Sin embargo, el valor devuelto de **GetExceptionInformation** se puede pasar como un parámetro a una función de filtro.</span><span class="sxs-lookup"><span data-stu-id="5482e-119">However, the return value of **GetExceptionInformation** can be passed as a parameter to a filter function.</span></span>

<span data-ttu-id="5482e-120">Para pasar la información de [**\_ punteros de excepción**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) al bloque de controlador de excepciones, la expresión de filtro o la función de filtro deben copiar el puntero o los datos en un almacenamiento seguro al que el controlador puede tener acceso más adelante.</span><span class="sxs-lookup"><span data-stu-id="5482e-120">To pass the [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) information to the exception-handler block, the filter expression or filter function must copy the pointer or the data to safe storage that the handler can later access.</span></span>

<span data-ttu-id="5482e-121">En el caso de los controladores anidados, cada expresión de filtro se evalúa hasta que se evalúa una como **\_ \_ controlador de ejecución de excepción** o continuación de la **\_ \_ ejecución** de la excepción.</span><span class="sxs-lookup"><span data-stu-id="5482e-121">In the case of nested handlers, each filter expression is evaluated until one is evaluated as **EXCEPTION\_EXECUTE\_HANDLER** or **EXCEPTION\_CONTINUE\_EXECUTION**.</span></span> <span data-ttu-id="5482e-122">Cada expresión de filtro puede invocar **GetExceptionInformation** para obtener la información de la excepción.</span><span class="sxs-lookup"><span data-stu-id="5482e-122">Each filter expression can invoke **GetExceptionInformation** to get exception information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5482e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5482e-123">Requirements</span></span>



| <span data-ttu-id="5482e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5482e-124">Requirement</span></span> | <span data-ttu-id="5482e-125">Value</span><span class="sxs-lookup"><span data-stu-id="5482e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5482e-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5482e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5482e-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5482e-127">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5482e-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5482e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5482e-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5482e-129">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5482e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5482e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5482e-131">**CONTEXTO**</span><span class="sxs-lookup"><span data-stu-id="5482e-131">**CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[<span data-ttu-id="5482e-132">**\_punteros de excepción**</span><span class="sxs-lookup"><span data-stu-id="5482e-132">**EXCEPTION\_POINTERS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[<span data-ttu-id="5482e-133">**registro de excepción \_**</span><span class="sxs-lookup"><span data-stu-id="5482e-133">**EXCEPTION\_RECORD**</span></span>](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[<span data-ttu-id="5482e-134">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="5482e-134">**GetExceptionCode**</span></span>](getexceptioncode.md)
</dt> <dt>

[<span data-ttu-id="5482e-135">**GetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="5482e-135">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[<span data-ttu-id="5482e-136">Funciones de control de excepciones estructurado</span><span class="sxs-lookup"><span data-stu-id="5482e-136">Structured Exception Handling Functions</span></span>](structured-exception-handling-functions.md)
</dt> <dt>

[<span data-ttu-id="5482e-137">Información general sobre el control estructurado de excepciones</span><span class="sxs-lookup"><span data-stu-id="5482e-137">Structured Exception Handling Overview</span></span>](structured-exception-handling.md)
</dt> <dt>

[<span data-ttu-id="5482e-138">Habilitar la compatibilidad con Windows para Intel AVX</span><span class="sxs-lookup"><span data-stu-id="5482e-138">Enable Windows Support for Intel AVX</span></span>](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
