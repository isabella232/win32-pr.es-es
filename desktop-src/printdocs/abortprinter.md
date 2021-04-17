---
description: La función AbortPrinter elimina un archivo de cola de impresión si la impresora está configurada para la puesta en cola.
ms.assetid: b361fba5-e4e7-4c9e-ab32-b8ab88dcb1dc
title: Función AbortPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbortPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f28e0c921db8fd075b6cad0e1df07401faaaffb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667107"
---
# <a name="abortprinter-function"></a><span data-ttu-id="f52fe-103">AbortPrinter función)</span><span class="sxs-lookup"><span data-stu-id="f52fe-103">AbortPrinter function</span></span>

<span data-ttu-id="f52fe-104">La función **AbortPrinter** elimina el archivo de cola de impresión de una impresora si la impresora está configurada para la puesta en cola.</span><span class="sxs-lookup"><span data-stu-id="f52fe-104">The **AbortPrinter** function deletes a printer's spool file if the printer is configured for spooling.</span></span>

## <a name="syntax"></a><span data-ttu-id="f52fe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f52fe-105">Syntax</span></span>


```C++
BOOL AbortPrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="f52fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f52fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f52fe-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f52fe-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f52fe-108">Identificador de la impresora desde la que se elimina el archivo de cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="f52fe-108">Handle to the printer from which the spool file is deleted.</span></span> <span data-ttu-id="f52fe-109">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="f52fe-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f52fe-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f52fe-110">Return value</span></span>

<span data-ttu-id="f52fe-111">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="f52fe-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f52fe-112">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="f52fe-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f52fe-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f52fe-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f52fe-114">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f52fe-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f52fe-115">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f52fe-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f52fe-116">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="f52fe-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f52fe-117">Si la impresora no está configurada para la puesta en cola, la función **AbortPrinter** no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="f52fe-117">If the printer is not configured for spooling, the **AbortPrinter** function has no effect.</span></span>

<span data-ttu-id="f52fe-118">La secuencia de un trabajo de impresión es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="f52fe-118">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="f52fe-119">Para iniciar un trabajo de impresión, llame a [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="f52fe-119">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="f52fe-120">Para comenzar cada página, llame a [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="f52fe-120">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="f52fe-121">Para escribir datos en una página, llame a [**WritePrinter**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="f52fe-121">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="f52fe-122">Para finalizar cada página, llame a [**EndPagePrinter**](endpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="f52fe-122">To end each page, call [**EndPagePrinter**](endpageprinter.md).</span></span>
5.  <span data-ttu-id="f52fe-123">Repita 2, 3 y 4 para tantas páginas como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f52fe-123">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="f52fe-124">Para finalizar el trabajo de impresión, llame a [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="f52fe-124">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="f52fe-125">Cuando una página de un archivo en cola supera aproximadamente 350 MB, puede no imprimirse y no enviar un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="f52fe-125">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="f52fe-126">Por ejemplo, esto puede ocurrir cuando se imprimen archivos EMF de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="f52fe-126">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="f52fe-127">El límite de tamaño de página depende de muchos factores, como la cantidad de memoria virtual disponible, la cantidad de memoria asignada mediante la llamada a procesos y la cantidad de fragmentación en el montón del proceso.</span><span class="sxs-lookup"><span data-stu-id="f52fe-127">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="requirements"></a><span data-ttu-id="f52fe-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f52fe-128">Requirements</span></span>



| <span data-ttu-id="f52fe-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f52fe-129">Requirement</span></span> | <span data-ttu-id="f52fe-130">Value</span><span class="sxs-lookup"><span data-stu-id="f52fe-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f52fe-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f52fe-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f52fe-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f52fe-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f52fe-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f52fe-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f52fe-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f52fe-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f52fe-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f52fe-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f52fe-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f52fe-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f52fe-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f52fe-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="f52fe-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f52fe-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f52fe-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f52fe-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f52fe-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f52fe-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="f52fe-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="f52fe-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f52fe-142">Impresión</span><span class="sxs-lookup"><span data-stu-id="f52fe-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f52fe-143">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="f52fe-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f52fe-144">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="f52fe-144">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="f52fe-145">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="f52fe-145">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="f52fe-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f52fe-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="f52fe-147">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="f52fe-147">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="f52fe-148">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="f52fe-148">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="f52fe-149">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="f52fe-149">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




