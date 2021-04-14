---
description: La función ParserTemporaryLockFrame bloquea un marco cuando entra en un analizador y desbloquea el marco cuando la función sale del analizador.
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: Función ParserTemporaryLockFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserTemporaryLockFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 48fa646e709982d88093e0cbeb5e60375643351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668407"
---
# <a name="parsertemporarylockframe-function"></a><span data-ttu-id="e5e8b-103">ParserTemporaryLockFrame función)</span><span class="sxs-lookup"><span data-stu-id="e5e8b-103">ParserTemporaryLockFrame function</span></span>

<span data-ttu-id="e5e8b-104">La función **ParserTemporaryLockFrame** bloquea un marco cuando entra en un analizador y desbloquea el marco cuando la función sale del analizador.</span><span class="sxs-lookup"><span data-stu-id="e5e8b-104">The **ParserTemporaryLockFrame** function locks a frame when it enters a parser and unlocks the frame when the function exits the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5e8b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5e8b-105">Syntax</span></span>


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="e5e8b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5e8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5e8b-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e5e8b-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5e8b-108">Identificador del marco al que apunta el analizador.</span><span class="sxs-lookup"><span data-stu-id="e5e8b-108">Handle to the frame that the parser points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5e8b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5e8b-109">Return value</span></span>

<span data-ttu-id="e5e8b-110">Si la función se realiza correctamente, el valor devuelto es un puntero al primer byte de datos del marco.</span><span class="sxs-lookup"><span data-stu-id="e5e8b-110">If the function is successful, the return value is a pointer to the first byte of data in the frame.</span></span>

<span data-ttu-id="e5e8b-111">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="e5e8b-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5e8b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5e8b-112">Remarks</span></span>

<span data-ttu-id="e5e8b-113">Los analizadores no deben llamar a la función **LockFrame** .</span><span class="sxs-lookup"><span data-stu-id="e5e8b-113">Parsers should not call the **LockFrame** function.</span></span> <span data-ttu-id="e5e8b-114">Si un analizador toma un bloqueo y, a continuación, genera un error o devuelve sin desbloquear el fotograma, el analizador deja el sistema en un estado en el que no puede cambiar los protocolos ni cortar o copiar fotogramas.</span><span class="sxs-lookup"><span data-stu-id="e5e8b-114">If a parser takes a lock and then generates a fault or returns without unlocking the frame, the parser leaves the system in a state where it cannot change protocols or cut or copy frames.</span></span> <span data-ttu-id="e5e8b-115">Los analizadores deben usar la función **ParserTemporaryLockFrame** , que concede un bloqueo solo durante el contexto de la entrada de función en el analizador.</span><span class="sxs-lookup"><span data-stu-id="e5e8b-115">Parsers should use the **ParserTemporaryLockFrame** function, which grants a lock only during the context of the function entry into the parser.</span></span> <span data-ttu-id="e5e8b-116">Al salir del analizador, se libera el bloqueo para ese marco.</span><span class="sxs-lookup"><span data-stu-id="e5e8b-116">On exit from the parser, the lock for that frame is released.</span></span> <span data-ttu-id="e5e8b-117">Como resultado, el puntero será válido solo después de que el analizador vuelva de la llamada a la función **AttachProperties** o **RecognizeFrame** .</span><span class="sxs-lookup"><span data-stu-id="e5e8b-117">As a result, the pointer will be valid only after the parser returns from the call to the **AttachProperties** or **RecognizeFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5e8b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5e8b-118">Requirements</span></span>



| <span data-ttu-id="e5e8b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5e8b-119">Requirement</span></span> | <span data-ttu-id="e5e8b-120">Value</span><span class="sxs-lookup"><span data-stu-id="e5e8b-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e5e8b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5e8b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e5e8b-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e5e8b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e5e8b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5e8b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e5e8b-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e5e8b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e5e8b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5e8b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5e8b-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5e8b-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e5e8b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5e8b-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5e8b-128"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5e8b-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e5e8b-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e5e8b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5e8b-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5e8b-130"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




