---
description: La función DeletePrintProcessor quita un procesador de impresión agregado por la función AddPrintProcessor.
ms.assetid: 65c77874-aa2c-4b4c-b218-fad361270a3e
title: Función DeletePrintProcessor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProcessor
- DeletePrintProcessorA
- DeletePrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 241efaad91e1587209f2ef2a905bc0e095c6b40c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276667"
---
# <a name="deleteprintprocessor-function"></a><span data-ttu-id="6ccbf-103">DeletePrintProcessor función)</span><span class="sxs-lookup"><span data-stu-id="6ccbf-103">DeletePrintProcessor function</span></span>

<span data-ttu-id="6ccbf-104">La función **DeletePrintProcessor** quita un procesador de impresión agregado por la función [**AddPrintProcessor**](addprintprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="6ccbf-104">The **DeletePrintProcessor** function removes a print processor added by the [**AddPrintProcessor**](addprintprocessor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ccbf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ccbf-105">Syntax</span></span>


```C++
BOOL DeletePrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a><span data-ttu-id="6ccbf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ccbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ccbf-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ccbf-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ccbf-108">Puntero a una cadena terminada en null que especifica el nombre del servidor desde el que se va a quitar el procesador.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-108">A pointer to a null-terminated string that specifies the name of the server from which the processor is to be removed.</span></span> <span data-ttu-id="6ccbf-109">Si este parámetro es **null**, el procesador de la impresora se quita de forma local.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-109">If this parameter is **NULL**, the printer processor is removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="6ccbf-110">*pEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ccbf-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ccbf-111">Puntero a una cadena terminada en null que especifica el entorno desde el que se va a quitar el procesador (por ejemplo, Windows NT x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="6ccbf-111">A pointer to a null-terminated string that specifies the environment from which the processor is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="6ccbf-112">Si este parámetro es **null**, el procesador se quita del entorno actual de la aplicación que realiza la llamada y del equipo cliente (no de la aplicación de destino y del servidor de impresión).</span><span class="sxs-lookup"><span data-stu-id="6ccbf-112">If this parameter is **NULL**, the processor is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span> <span data-ttu-id="6ccbf-113">**Null** es el valor recomendado, ya que proporciona la máxima portabilidad.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-113">**NULL** is the recommended value, as it provides maximum portability.</span></span>

</dd> <dt>

<span data-ttu-id="6ccbf-114">*pPrintProcessorName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ccbf-114">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ccbf-115">Puntero a una cadena terminada en null que especifica el nombre del procesador que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-115">A pointer to a null-terminated string that specifies the name of the processor to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ccbf-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ccbf-116">Return value</span></span>

<span data-ttu-id="6ccbf-117">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6ccbf-118">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ccbf-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ccbf-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6ccbf-120">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6ccbf-121">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6ccbf-122">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6ccbf-123">El autor de la llamada debe tener [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="6ccbf-123">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ccbf-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ccbf-124">Requirements</span></span>



| <span data-ttu-id="6ccbf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ccbf-125">Requirement</span></span> | <span data-ttu-id="6ccbf-126">Value</span><span class="sxs-lookup"><span data-stu-id="6ccbf-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ccbf-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ccbf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6ccbf-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6ccbf-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6ccbf-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ccbf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6ccbf-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6ccbf-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6ccbf-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ccbf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ccbf-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ccbf-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6ccbf-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ccbf-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ccbf-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ccbf-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6ccbf-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ccbf-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ccbf-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="6ccbf-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="6ccbf-137">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="6ccbf-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6ccbf-138">**DeletePrintProcessorW** (Unicode) y **DeletePrintProcessorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6ccbf-138">**DeletePrintProcessorW** (Unicode) and **DeletePrintProcessorA** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="6ccbf-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ccbf-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ccbf-140">Impresión</span><span class="sxs-lookup"><span data-stu-id="6ccbf-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6ccbf-141">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="6ccbf-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6ccbf-142">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="6ccbf-142">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> </dl>

 

