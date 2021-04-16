---
description: La función ResetPrinter especifica el tipo de datos y los valores de modo de dispositivo que se van a usar para imprimir documentos enviados por la función StartDocPrinter. Estos valores se pueden invalidar mediante la función SetJob una vez iniciada la impresión del documento.
ms.assetid: 9efc6629-dbb7-4320-90b9-07c66f0add47
title: Función ResetPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResetPrinter
- ResetPrinterA
- ResetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8bdfef0229a646e802878a96370d27d49a6bfc2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706353"
---
# <a name="resetprinter-function"></a><span data-ttu-id="228e0-104">ResetPrinter función)</span><span class="sxs-lookup"><span data-stu-id="228e0-104">ResetPrinter function</span></span>

<span data-ttu-id="228e0-105">La función **ResetPrinter** especifica el tipo de datos y los valores de modo de dispositivo que se van a usar para imprimir documentos enviados por la función [**StartDocPrinter**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="228e0-105">The **ResetPrinter** function specifies the data type and device mode values to be used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="228e0-106">Estos valores se pueden invalidar mediante la función [**SetJob**](setjob.md) una vez iniciada la impresión del documento.</span><span class="sxs-lookup"><span data-stu-id="228e0-106">These values can be overridden by using the [**SetJob**](setjob.md) function after document printing has started.</span></span>

## <a name="syntax"></a><span data-ttu-id="228e0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="228e0-107">Syntax</span></span>


```C++
BOOL ResetPrinter(
  _In_ HANDLE             hPrinter,
  _In_ LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a><span data-ttu-id="228e0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="228e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="228e0-109">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="228e0-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="228e0-110">Identificador de la impresora.</span><span class="sxs-lookup"><span data-stu-id="228e0-110">Handle to the printer.</span></span> <span data-ttu-id="228e0-111">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="228e0-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="228e0-112">*pDefault* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="228e0-112">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="228e0-113">Puntero a una estructura de [**\_ valores predeterminados de impresora**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="228e0-113">Pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span>

<span data-ttu-id="228e0-114">La función **ResetPrinter** omite el miembro **DesiredAccess** de la estructura [**de \_ valores predeterminados**](printer-defaults.md) de la impresora.</span><span class="sxs-lookup"><span data-stu-id="228e0-114">The **ResetPrinter** function ignores the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="228e0-115">Establezca ese miembro en cero.</span><span class="sxs-lookup"><span data-stu-id="228e0-115">Set that member to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="228e0-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="228e0-116">Return value</span></span>

<span data-ttu-id="228e0-117">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="228e0-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="228e0-118">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="228e0-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="228e0-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="228e0-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="228e0-120">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="228e0-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="228e0-121">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="228e0-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="228e0-122">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="228e0-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="228e0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="228e0-123">Requirements</span></span>



| <span data-ttu-id="228e0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="228e0-124">Requirement</span></span> | <span data-ttu-id="228e0-125">Value</span><span class="sxs-lookup"><span data-stu-id="228e0-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="228e0-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="228e0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="228e0-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="228e0-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="228e0-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="228e0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="228e0-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="228e0-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="228e0-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="228e0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="228e0-131"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="228e0-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="228e0-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="228e0-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="228e0-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="228e0-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="228e0-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="228e0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="228e0-135"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="228e0-135"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="228e0-136">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="228e0-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="228e0-137">**ResetPrinterW** (Unicode) y **ResetPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="228e0-137">**ResetPrinterW** (Unicode) and **ResetPrinterA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="228e0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="228e0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="228e0-139">Impresión</span><span class="sxs-lookup"><span data-stu-id="228e0-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="228e0-140">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="228e0-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="228e0-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="228e0-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="228e0-142">**\_valores predeterminados de impresora**</span><span class="sxs-lookup"><span data-stu-id="228e0-142">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="228e0-143">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="228e0-143">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="228e0-144">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="228e0-144">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

 




