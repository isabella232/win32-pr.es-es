---
description: La función ClosePrinter cierra el objeto de impresora especificado.
ms.assetid: 95cc3eca-e65c-4fa6-8975-479e8e728dca
title: Función ClosePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClosePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bd21268b86a07357065d4f33b60d1af4b05fa019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278915"
---
# <a name="closeprinter-function"></a><span data-ttu-id="bb374-103">ClosePrinter función)</span><span class="sxs-lookup"><span data-stu-id="bb374-103">ClosePrinter function</span></span>

<span data-ttu-id="bb374-104">La función **ClosePrinter** cierra el objeto de impresora especificado.</span><span class="sxs-lookup"><span data-stu-id="bb374-104">The **ClosePrinter** function closes the specified printer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb374-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb374-105">Syntax</span></span>


```C++
BOOL ClosePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="bb374-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb374-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb374-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb374-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb374-108">Identificador del objeto de impresora que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="bb374-108">A handle to the printer object to be closed.</span></span> <span data-ttu-id="bb374-109">Este identificador es devuelto por la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="bb374-109">This handle is returned by the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb374-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb374-110">Return value</span></span>

<span data-ttu-id="bb374-111">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="bb374-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="bb374-112">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="bb374-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb374-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb374-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bb374-114">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="bb374-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="bb374-115">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="bb374-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="bb374-116">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="bb374-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="bb374-117">Cuando la función **ClosePrinter** devuelve, el identificador *hPrinter* no es válido, independientemente de si la función se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="bb374-117">When the **ClosePrinter** function returns, the handle *hPrinter* is invalid, regardless of whether the function has succeeded or failed.</span></span>

## <a name="examples"></a><span data-ttu-id="bb374-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bb374-118">Examples</span></span>

<span data-ttu-id="bb374-119">Para obtener un programa de ejemplo que usa esta función, consulte [Cómo: imprimir con la API de impresión de GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="bb374-119">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb374-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb374-120">Requirements</span></span>



| <span data-ttu-id="bb374-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb374-121">Requirement</span></span> | <span data-ttu-id="bb374-122">Value</span><span class="sxs-lookup"><span data-stu-id="bb374-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb374-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb374-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bb374-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bb374-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bb374-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb374-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bb374-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb374-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bb374-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb374-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb374-128"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb374-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bb374-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb374-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb374-130"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb374-130"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="bb374-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bb374-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb374-132"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb374-132"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="bb374-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb374-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb374-134">Impresión</span><span class="sxs-lookup"><span data-stu-id="bb374-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bb374-135">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="bb374-135">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="bb374-136">**AddPrinter (**</span><span class="sxs-lookup"><span data-stu-id="bb374-136">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="bb374-137">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="bb374-137">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




