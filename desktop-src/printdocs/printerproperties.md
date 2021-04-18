---
description: La función PrinterProperties muestra una hoja de propiedades de las propiedades de la impresora especificada.
ms.assetid: 1d4c961b-178b-47af-b983-5b7327919f93
title: Función PrinterProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrinterProperties
api_type:
- DllExport
api_location:
- plotui.dll
- winspool.drv
ms.openlocfilehash: e7e2c8586c06b2cb64a0e499bd05a6b6016de0a6
ms.sourcegitcommit: c77ed4d933c9f30af0ca0e095a75ad2bdd4d8bf8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "106011185"
---
# <a name="printerproperties-function"></a><span data-ttu-id="fd711-103">PrinterProperties función)</span><span class="sxs-lookup"><span data-stu-id="fd711-103">PrinterProperties function</span></span>

<span data-ttu-id="fd711-104">La función **PrinterProperties** muestra una hoja de propiedades de las propiedades de la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="fd711-104">The **PrinterProperties** function displays a printer-properties property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd711-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd711-105">Syntax</span></span>


```C++
BOOL PrinterProperties(
  _In_ HWND   hWnd,
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="fd711-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd711-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd711-107">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fd711-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd711-108">Identificador de la ventana primaria de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="fd711-108">A handle to the parent window of the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="fd711-109">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fd711-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd711-110">Identificador de un objeto de impresora.</span><span class="sxs-lookup"><span data-stu-id="fd711-110">A handle to a printer object.</span></span> <span data-ttu-id="fd711-111">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="fd711-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd711-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd711-112">Return value</span></span>

<span data-ttu-id="fd711-113">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="fd711-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="fd711-114">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="fd711-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd711-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd711-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fd711-116">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="fd711-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="fd711-117">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="fd711-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="fd711-118">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="fd711-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fd711-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd711-119">Requirements</span></span>



| <span data-ttu-id="fd711-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd711-120">Requirement</span></span> | <span data-ttu-id="fd711-121">Value</span><span class="sxs-lookup"><span data-stu-id="fd711-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd711-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd711-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fd711-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fd711-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fd711-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd711-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fd711-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd711-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fd711-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd711-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd711-127"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd711-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fd711-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd711-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd711-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd711-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="fd711-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fd711-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd711-131"><dt>winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="fd711-131"><dt>winspool.drv</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fd711-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fd711-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd711-133">Impresión</span><span class="sxs-lookup"><span data-stu-id="fd711-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fd711-134">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="fd711-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="fd711-135">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="fd711-135">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="fd711-136">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="fd711-136">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




