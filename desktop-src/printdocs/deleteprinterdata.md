---
description: La función DeletePrinterData elimina los datos de configuración especificados para una impresora. Los datos de configuración de las impresoras se componen de un conjunto de valores con nombre y con tipo. La función DeletePrinterData elimina uno de estos valores, especificado por su nombre de valor.
ms.assetid: 03c0bd75-d6de-46e3-b8e9-5a55df5135ea
title: Función DeletePrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterData
- DeletePrinterDataA
- DeletePrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a88df8484d367ae2cc50f4a465b5db1dcd53c355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360661"
---
# <a name="deleteprinterdata-function"></a><span data-ttu-id="a2b59-105">DeletePrinterData función)</span><span class="sxs-lookup"><span data-stu-id="a2b59-105">DeletePrinterData function</span></span>

<span data-ttu-id="a2b59-106">La función **DeletePrinterData** elimina los datos de configuración especificados para una impresora.</span><span class="sxs-lookup"><span data-stu-id="a2b59-106">The **DeletePrinterData** function deletes specified configuration data for a printer.</span></span> <span data-ttu-id="a2b59-107">Los datos de configuración de una impresora se componen de un conjunto de valores con nombre y con tipo.</span><span class="sxs-lookup"><span data-stu-id="a2b59-107">A printer's configuration data consists of a set of named and typed values.</span></span> <span data-ttu-id="a2b59-108">La función **DeletePrinterData** elimina uno de estos valores, especificado por su nombre de valor.</span><span class="sxs-lookup"><span data-stu-id="a2b59-108">The **DeletePrinterData** function deletes one of these values, specified by its value name.</span></span>

<span data-ttu-id="a2b59-109">Llamar a **DeletePrinterData** es equivalente a llamar a la función [**DeletePrinterDataEx**](deleteprinterdataex.md) con el parámetro *pKeyName* establecido en "PrinterDriverData".</span><span class="sxs-lookup"><span data-stu-id="a2b59-109">Calling **DeletePrinterData** is equivalent to calling the [**DeletePrinterDataEx**](deleteprinterdataex.md) function with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b59-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2b59-110">Syntax</span></span>


```C++
DWORD DeletePrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName
);
```



## <a name="parameters"></a><span data-ttu-id="a2b59-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2b59-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2b59-112">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a2b59-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2b59-113">Identificador de la impresora cuyos datos de configuración se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="a2b59-113">A handle to the printer whose configuration data is to be deleted.</span></span> <span data-ttu-id="a2b59-114">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="a2b59-114">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="a2b59-115">*pValueName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a2b59-115">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2b59-116">Puntero al nombre terminado en NULL del valor de datos de configuración que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="a2b59-116">A pointer to the null-terminated name of the configuration data value to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2b59-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2b59-117">Return value</span></span>

<span data-ttu-id="a2b59-118">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a2b59-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a2b59-119">Si se produce un error en la función, el valor devuelto es un código de error del sistema.</span><span class="sxs-lookup"><span data-stu-id="a2b59-119">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2b59-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2b59-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a2b59-121">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="a2b59-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a2b59-122">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="a2b59-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a2b59-123">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="a2b59-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2b59-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2b59-124">Requirements</span></span>



| <span data-ttu-id="a2b59-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2b59-125">Requirement</span></span> | <span data-ttu-id="a2b59-126">Value</span><span class="sxs-lookup"><span data-stu-id="a2b59-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b59-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2b59-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a2b59-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a2b59-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a2b59-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2b59-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a2b59-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a2b59-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a2b59-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2b59-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2b59-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2b59-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a2b59-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2b59-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2b59-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2b59-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a2b59-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a2b59-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2b59-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="a2b59-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a2b59-137">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="a2b59-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a2b59-138">**DeletePrinterDataW** (Unicode) y **DeletePrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a2b59-138">**DeletePrinterDataW** (Unicode) and **DeletePrinterDataA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="a2b59-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2b59-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2b59-140">Impresión</span><span class="sxs-lookup"><span data-stu-id="a2b59-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a2b59-141">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="a2b59-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a2b59-142">**EnumPrinterData**</span><span class="sxs-lookup"><span data-stu-id="a2b59-142">**EnumPrinterData**</span></span>](enumprinterdata.md)
</dt> <dt>

[<span data-ttu-id="a2b59-143">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="a2b59-143">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="a2b59-144">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="a2b59-144">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="a2b59-145">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="a2b59-145">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="a2b59-146">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="a2b59-146">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> </dl>

 

 




