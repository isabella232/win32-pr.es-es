---
description: La función DeletePrinterDataEx elimina un valor especificado de los datos de configuración de una impresora.
ms.assetid: bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55
title: Función DeletePrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDataEx
- DeletePrinterDataExA
- DeletePrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 07cf6262db0a1e3a3c4c098ee26e03b3fdad4002
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814875"
---
# <a name="deleteprinterdataex-function"></a><span data-ttu-id="49e8f-103">DeletePrinterDataEx función)</span><span class="sxs-lookup"><span data-stu-id="49e8f-103">DeletePrinterDataEx function</span></span>

<span data-ttu-id="49e8f-104">La función **DeletePrinterDataEx** elimina un valor especificado de los datos de configuración de una impresora.</span><span class="sxs-lookup"><span data-stu-id="49e8f-104">The **DeletePrinterDataEx** function deletes a specified value from the configuration data for a printer.</span></span> <span data-ttu-id="49e8f-105">Los datos de configuración de una impresora se componen de un conjunto de valores con nombre y con tipo que se almacenan en una jerarquía de claves del registro.</span><span class="sxs-lookup"><span data-stu-id="49e8f-105">A printer's configuration data consists of a set of named and typed values stored in a hierarchy of registry keys.</span></span> <span data-ttu-id="49e8f-106">La función elimina un valor especificado en una clave especificada.</span><span class="sxs-lookup"><span data-stu-id="49e8f-106">The function deletes a specified value under a specified key.</span></span>

<span data-ttu-id="49e8f-107">Al igual que la función [**DeletePrinterData**](deleteprinterdata.md) , **DeletePrinterDataEx** puede eliminar valores almacenados por la función [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="49e8f-107">Like the [**DeletePrinterData**](deleteprinterdata.md) function, **DeletePrinterDataEx** can delete values stored by the [**SetPrinterData**](setprinterdata.md) function.</span></span> <span data-ttu-id="49e8f-108">Además, **DeletePrinterDataEx** puede eliminar valores almacenados en una clave especificada por la función [**SetPrinterDataEx**](setprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="49e8f-108">In addition, **DeletePrinterDataEx** can delete values stored under a specified key by the [**SetPrinterDataEx**](setprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="49e8f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49e8f-109">Syntax</span></span>


```C++
DWORD DeletePrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName
);
```



## <a name="parameters"></a><span data-ttu-id="49e8f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49e8f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49e8f-111">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49e8f-111">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e8f-112">Identificador de la impresora para la que la función elimina un valor.</span><span class="sxs-lookup"><span data-stu-id="49e8f-112">A handle to the printer for which the function deletes a value.</span></span> <span data-ttu-id="49e8f-113">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="49e8f-113">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="49e8f-114">*pKeyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49e8f-114">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e8f-115">Puntero a una cadena terminada en null que especifica la clave que contiene el valor que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="49e8f-115">A pointer to a null-terminated string that specifies the key containing the value to delete.</span></span> <span data-ttu-id="49e8f-116">Use el carácter de barra diagonal inversa ( \\ ) como delimitador para especificar una ruta de acceso que tenga una o más subclaves.</span><span class="sxs-lookup"><span data-stu-id="49e8f-116">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="49e8f-117">Si *pKeyName* es **null** o una cadena vacía, **DeletePrinterDataEx** devuelve un \_ parámetro no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="49e8f-117">If *pKeyName* is **NULL** or an empty string, **DeletePrinterDataEx** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="49e8f-118">*pValueName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49e8f-118">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e8f-119">Puntero a una cadena terminada en null que especifica el nombre del valor que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="49e8f-119">A pointer to a null-terminated string that specifies the name of the value to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49e8f-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49e8f-120">Return value</span></span>

<span data-ttu-id="49e8f-121">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="49e8f-121">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="49e8f-122">Si se produce un error en la función, el valor devuelto es un código de error del sistema.</span><span class="sxs-lookup"><span data-stu-id="49e8f-122">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="49e8f-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49e8f-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="49e8f-124">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="49e8f-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="49e8f-125">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="49e8f-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="49e8f-126">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="49e8f-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49e8f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49e8f-127">Requirements</span></span>



| <span data-ttu-id="49e8f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="49e8f-128">Requirement</span></span> | <span data-ttu-id="49e8f-129">Value</span><span class="sxs-lookup"><span data-stu-id="49e8f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49e8f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49e8f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="49e8f-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="49e8f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="49e8f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49e8f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="49e8f-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="49e8f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="49e8f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49e8f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="49e8f-135"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49e8f-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="49e8f-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49e8f-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="49e8f-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49e8f-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="49e8f-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49e8f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49e8f-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="49e8f-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="49e8f-140">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="49e8f-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="49e8f-141">**DeletePrinterDataExW** (Unicode) y **DeletePrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="49e8f-141">**DeletePrinterDataExW** (Unicode) and **DeletePrinterDataExA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="49e8f-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="49e8f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e8f-143">Impresión</span><span class="sxs-lookup"><span data-stu-id="49e8f-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="49e8f-144">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="49e8f-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="49e8f-145">**DeletePrinterKey**</span><span class="sxs-lookup"><span data-stu-id="49e8f-145">**DeletePrinterKey**</span></span>](deleteprinterkey.md)
</dt> <dt>

[<span data-ttu-id="49e8f-146">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="49e8f-146">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="49e8f-147">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="49e8f-147">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="49e8f-148">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="49e8f-148">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="49e8f-149">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="49e8f-149">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="49e8f-150">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="49e8f-150">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




