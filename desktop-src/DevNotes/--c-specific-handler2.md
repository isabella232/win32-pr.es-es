---
description: Lo llama el compilador para implementar extensiones de control de excepciones estructurado.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: __C_specific_handler función (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __C_specific_handler
- __C_specific_handler
api_type:
- DllExport
api_location:
- ntoskrnl.exe
- NTDll.dll
- wpdupfltr.sys
ms.openlocfilehash: fc89105a6a68c920fccb123dd95a08ed4ddee696
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660413"
---
# <a name="__c_specific_handler-function"></a><span data-ttu-id="7d010-103">\_\_\_Función de controlador específica de C \_</span><span class="sxs-lookup"><span data-stu-id="7d010-103">\_\_C\_specific\_handler function</span></span>

<span data-ttu-id="7d010-104">Lo llama el compilador para implementar extensiones de control de excepciones estructurado.</span><span class="sxs-lookup"><span data-stu-id="7d010-104">Called by the compiler to implement structured exception handling extensions.</span></span>

<span data-ttu-id="7d010-105">La dirección relativa del controlador específico del lenguaje está presente en la información de desenredo \_ cada vez que se establecen marcas UNW Flag \_ \_ EHANDLER o UNW \_ Flag \_ UHANDLER.</span><span class="sxs-lookup"><span data-stu-id="7d010-105">The relative address of the language specific handler is present in the UNWIND\_INFO whenever flags UNW\_FLAG\_EHANDLER or UNW\_FLAG\_UHANDLER are set.</span></span> <span data-ttu-id="7d010-106">Se llama al controlador específico del lenguaje como parte de la búsqueda de un controlador de excepciones o como parte de un desenredado.</span><span class="sxs-lookup"><span data-stu-id="7d010-106">The language specific handler is called as part of the search for an exception handler or as part of an unwind.</span></span> <span data-ttu-id="7d010-107">Para obtener más información, consulte [controlador específico del lenguaje](/cpp/build/language-specific-handler).</span><span class="sxs-lookup"><span data-stu-id="7d010-107">For more information see [Language Specific Handler](/cpp/build/language-specific-handler).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d010-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d010-108">Syntax</span></span>


```C++
_CRTIMP  __C_specific_handler(
  _In_    struct _EXCEPTION_RECORD   *ExceptionRecord,
  _In_    void                       *EstablisherFrame,
  _Inout_ struct _CONTEXT            *ContextRecord,
  _Inout_ struct _DISPATCHER_CONTEXT *DispatcherContext
);
```



## <a name="parameters"></a><span data-ttu-id="7d010-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d010-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d010-110">*ExceptionRecord* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d010-110">*ExceptionRecord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d010-111">Proporciona un puntero a un registro de excepción, que tiene la definición estándar de Win64.</span><span class="sxs-lookup"><span data-stu-id="7d010-111">Supplies a pointer to an exception record, which has the standard Win64 definition.</span></span>

</dd> <dt>

<span data-ttu-id="7d010-112">*EstablisherFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d010-112">*EstablisherFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d010-113">Dirección de la base de la asignación de pila fija para esta función.</span><span class="sxs-lookup"><span data-stu-id="7d010-113">The address of the base of the fixed stack allocation for this function.</span></span>

</dd> <dt>

<span data-ttu-id="7d010-114">*ContextRecord* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7d010-114">*ContextRecord* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d010-115">Apunta al contexto de la excepción en el momento en que se produjo la excepción (en el caso del controlador de excepciones) o en el contexto de "desenredo" actual (en el caso del controlador de terminación).</span><span class="sxs-lookup"><span data-stu-id="7d010-115">Points to the exception context at the time the exception was raised (in the exception handler case) or the current "unwind" context (in the termination handler case).</span></span>

</dd> <dt>

<span data-ttu-id="7d010-116">*DispatcherContext* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7d010-116">*DispatcherContext* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d010-117">Apunta al contexto del distribuidor para esta función.</span><span class="sxs-lookup"><span data-stu-id="7d010-117">Points to the dispatcher context for this function.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d010-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d010-118">Requirements</span></span>



| <span data-ttu-id="7d010-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d010-119">Requirement</span></span> | <span data-ttu-id="7d010-120">Value</span><span class="sxs-lookup"><span data-stu-id="7d010-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d010-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d010-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7d010-122"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d010-122"><dt>Wdm.h</dt></span></span> </dl>        |
| <span data-ttu-id="7d010-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7d010-123">Library</span></span><br/> | <dl> <span data-ttu-id="7d010-124"><dt>NtosKrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d010-124"><dt>NtosKrnl.lib</dt></span></span> </dl> |
| <span data-ttu-id="7d010-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7d010-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="7d010-126"><dt>Ntoskrnl.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7d010-126"><dt>Ntoskrnl.exe</dt></span></span> </dl> |



 

