---
description: La función DeletePrinter elimina el objeto de impresora especificado.
ms.assetid: 04d9c073-b795-4307-ba89-d4984bc5b354
title: Función DeletePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 16d82a263b09c87f5c9b9725db48dd6634404ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697134"
---
# <a name="deleteprinter-function"></a><span data-ttu-id="b86d0-103">DeletePrinter función)</span><span class="sxs-lookup"><span data-stu-id="b86d0-103">DeletePrinter function</span></span>

<span data-ttu-id="b86d0-104">La función **DeletePrinter** elimina el objeto de impresora especificado.</span><span class="sxs-lookup"><span data-stu-id="b86d0-104">The **DeletePrinter** function deletes the specified printer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b86d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b86d0-105">Syntax</span></span>


```C++
BOOL DeletePrinter(
  _Inout_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="b86d0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b86d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b86d0-107">*hPrinter* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b86d0-107">*hPrinter* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b86d0-108">Identificador de un objeto de impresora que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="b86d0-108">Handle to a printer object that will be deleted.</span></span> <span data-ttu-id="b86d0-109">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="b86d0-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b86d0-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b86d0-110">Return value</span></span>

<span data-ttu-id="b86d0-111">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b86d0-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b86d0-112">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="b86d0-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b86d0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b86d0-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b86d0-114">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b86d0-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b86d0-115">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b86d0-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b86d0-116">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="b86d0-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b86d0-117">Si quedan trabajos de impresión para su procesamiento en la impresora especificada, **DeletePrinter** marca la impresora para su eliminación pendiente y, a continuación, la elimina cuando se hayan impreso todos los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="b86d0-117">If there are print jobs remaining to be processed for the specified printer, **DeletePrinter** marks the printer for pending deletion, and then deletes it when all the print jobs have been printed.</span></span> <span data-ttu-id="b86d0-118">No se puede agregar ningún trabajo de impresión a una impresora marcada para eliminación pendiente.</span><span class="sxs-lookup"><span data-stu-id="b86d0-118">No print jobs can be added to a printer that is marked for pending deletion.</span></span>

<span data-ttu-id="b86d0-119">No se puede mantener una impresora marcada para eliminación pendiente, pero sus trabajos de impresión se pueden mantener, reanudar y reiniciar.</span><span class="sxs-lookup"><span data-stu-id="b86d0-119">A printer marked for pending deletion cannot be held, but its print jobs can be held, resumed, and restarted.</span></span> <span data-ttu-id="b86d0-120">Si la impresora está contenida y hay trabajos para la impresora, **DeletePrinter** produce un error de \_ acceso \_ denegado.</span><span class="sxs-lookup"><span data-stu-id="b86d0-120">If the printer is held and there are jobs for the printer, **DeletePrinter** fails with ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="b86d0-121">Tenga en cuenta que **DeletePrinter** no cierra el identificador que se le ha pasado.</span><span class="sxs-lookup"><span data-stu-id="b86d0-121">Note that **DeletePrinter** does not close the handle that is passed to it.</span></span> <span data-ttu-id="b86d0-122">Por lo tanto, la aplicación debe seguir llamando a [**ClosePrinter**](closeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="b86d0-122">Thus, the application must still call [**ClosePrinter**](closeprinter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b86d0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b86d0-123">Requirements</span></span>



| <span data-ttu-id="b86d0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b86d0-124">Requirement</span></span> | <span data-ttu-id="b86d0-125">Value</span><span class="sxs-lookup"><span data-stu-id="b86d0-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b86d0-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b86d0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b86d0-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b86d0-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b86d0-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b86d0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b86d0-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b86d0-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b86d0-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b86d0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b86d0-131"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b86d0-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b86d0-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b86d0-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="b86d0-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b86d0-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b86d0-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b86d0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b86d0-135"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b86d0-135"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="b86d0-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="b86d0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b86d0-137">Impresión</span><span class="sxs-lookup"><span data-stu-id="b86d0-137">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b86d0-138">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="b86d0-138">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b86d0-139">**AddPrinter (**</span><span class="sxs-lookup"><span data-stu-id="b86d0-139">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="b86d0-140">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="b86d0-140">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="b86d0-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="b86d0-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




