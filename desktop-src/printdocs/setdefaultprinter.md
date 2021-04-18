---
description: La función SetDefaultPrinter establece el nombre de la impresora predeterminada para el usuario actual en el equipo local.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: Función SetDefaultPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDefaultPrinter
- SetDefaultPrinterA
- SetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 346d356aea3d806284823541aa219699e51c2187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716482"
---
# <a name="setdefaultprinter-function"></a><span data-ttu-id="bf0f8-103">SetDefaultPrinter función)</span><span class="sxs-lookup"><span data-stu-id="bf0f8-103">SetDefaultPrinter function</span></span>

<span data-ttu-id="bf0f8-104">La función **SetDefaultPrinter** establece el nombre de la impresora predeterminada para el usuario actual en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="bf0f8-104">The **SetDefaultPrinter** function sets the printer name of the default printer for the current user on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf0f8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf0f8-105">Syntax</span></span>


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="bf0f8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf0f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf0f8-107">*pszPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bf0f8-107">*pszPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0f8-108">Puntero a una cadena terminada en null que contiene el nombre de impresora predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bf0f8-108">A pointer to a null-terminated string containing the default printer name.</span></span> <span data-ttu-id="bf0f8-109">Para una conexión de impresora remota, el formato de nombre es nombredeimpresora de **\\\\** _servidor_ *_\\_* .</span><span class="sxs-lookup"><span data-stu-id="bf0f8-109">For a remote printer connection, the name format is **\\\\**_server_*_\\_*_printername_.</span></span> <span data-ttu-id="bf0f8-110">En el caso de una impresora local, el formato de nombre es *nombreimpresora*.</span><span class="sxs-lookup"><span data-stu-id="bf0f8-110">For a local printer, the name format is *printername*.</span></span>

<span data-ttu-id="bf0f8-111">Si este parámetro es **null** o una cadena vacía, es decir, "", **SetDefaultPrinter** seleccionará una impresora predeterminada de una de las impresoras instaladas.</span><span class="sxs-lookup"><span data-stu-id="bf0f8-111">If this parameter is **NULL** or an empty string, that is, "", **SetDefaultPrinter** will select a default printer from one of the installed printers.</span></span> <span data-ttu-id="bf0f8-112">Si ya existe una impresora predeterminada, la llamada a **SetDefaultPrinter** con un **valor null** o una cadena vacía en este parámetro podría cambiar la impresora predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bf0f8-112">If a default printer already exists, calling **SetDefaultPrinter** with a **NULL** or an empty string in this parameter might change the default printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf0f8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf0f8-113">Return value</span></span>

<span data-ttu-id="bf0f8-114">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="bf0f8-114">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="bf0f8-115">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="bf0f8-115">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf0f8-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf0f8-116">Remarks</span></span>

<span data-ttu-id="bf0f8-117">Al utilizar este método, debe especificar una impresora, un controlador y un puerto válidos.</span><span class="sxs-lookup"><span data-stu-id="bf0f8-117">When using this method, you must specify a valid printer, driver, and port.</span></span> <span data-ttu-id="bf0f8-118">Si no son válidas, no se produce ningún error en las API, pero no se define el resultado.</span><span class="sxs-lookup"><span data-stu-id="bf0f8-118">If they are invalid, the APIs do not fail but the result is not defined.</span></span> <span data-ttu-id="bf0f8-119">Esto puede hacer que otros programas vuelvan a establecer la impresora en la impresora válida anterior.</span><span class="sxs-lookup"><span data-stu-id="bf0f8-119">This could cause other programs to set the printer back to the previous valid printer.</span></span> <span data-ttu-id="bf0f8-120">Puede usar [**EnumPrinters**](enumprinters.md) para recuperar el nombre de la impresora, el nombre del controlador y el nombre del puerto de todas las impresoras disponibles.</span><span class="sxs-lookup"><span data-stu-id="bf0f8-120">You can use [**EnumPrinters**](enumprinters.md) to retrieve the printer name, driver name, and port name of all available printers.</span></span>

> [!Note]  
> <span data-ttu-id="bf0f8-121">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="bf0f8-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="bf0f8-122">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="bf0f8-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="bf0f8-123">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="bf0f8-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf0f8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf0f8-124">Requirements</span></span>



| <span data-ttu-id="bf0f8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf0f8-125">Requirement</span></span> | <span data-ttu-id="bf0f8-126">Value</span><span class="sxs-lookup"><span data-stu-id="bf0f8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf0f8-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf0f8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bf0f8-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bf0f8-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bf0f8-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf0f8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bf0f8-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bf0f8-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bf0f8-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf0f8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf0f8-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf0f8-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bf0f8-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf0f8-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf0f8-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf0f8-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="bf0f8-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf0f8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf0f8-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="bf0f8-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="bf0f8-137">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="bf0f8-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bf0f8-138">**SetDefaultPrinterW** (Unicode) y **SetDefaultPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bf0f8-138">**SetDefaultPrinterW** (Unicode) and **SetDefaultPrinterA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="bf0f8-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf0f8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf0f8-140">Impresión</span><span class="sxs-lookup"><span data-stu-id="bf0f8-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bf0f8-141">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="bf0f8-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="bf0f8-142">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="bf0f8-142">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="bf0f8-143">**GetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="bf0f8-143">**GetDefaultPrinter**</span></span>](getdefaultprinter.md)
</dt> </dl>

 

 




