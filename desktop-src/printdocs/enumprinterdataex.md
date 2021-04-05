---
description: La función EnumPrinterDataEx enumera todos los nombres de valor y los datos de una impresora y una clave especificadas.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: Función EnumPrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDataEx
- EnumPrinterDataExA
- EnumPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 517d480d1c831627cadb289c41f99d24b1025ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815494"
---
# <a name="enumprinterdataex-function"></a><span data-ttu-id="cb265-103">EnumPrinterDataEx función)</span><span class="sxs-lookup"><span data-stu-id="cb265-103">EnumPrinterDataEx function</span></span>

<span data-ttu-id="cb265-104">La función **EnumPrinterDataEx** enumera todos los nombres de valor y los datos de una impresora y una clave especificadas.</span><span class="sxs-lookup"><span data-stu-id="cb265-104">The **EnumPrinterDataEx** function enumerates all value names and data for a specified printer and key.</span></span>

<span data-ttu-id="cb265-105">Los datos de la impresora se almacenan en el registro.</span><span class="sxs-lookup"><span data-stu-id="cb265-105">Printer data is stored in the registry.</span></span> <span data-ttu-id="cb265-106">Al enumerar los datos de la impresora, no llame a las funciones del registro que podrían cambiar los datos.</span><span class="sxs-lookup"><span data-stu-id="cb265-106">While enumerating printer data, do not call registry functions that might change the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb265-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb265-107">Syntax</span></span>


```C++
DWORD EnumPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPBYTE  pEnumValues,
  _In_  DWORD   cbEnumValues,
  _Out_ LPDWORD pcbEnumValues,
  _Out_ LPDWORD pnEnumValues
);
```



## <a name="parameters"></a><span data-ttu-id="cb265-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb265-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb265-109">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb265-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb265-110">Identificador de la impresora para la que la función recupera datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="cb265-110">A handle to the printer for which the function retrieves configuration data.</span></span> <span data-ttu-id="cb265-111">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="cb265-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="cb265-112">*pKeyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb265-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb265-113">Puntero a una cadena terminada en null que especifica la clave que contiene los valores que se van a enumerar.</span><span class="sxs-lookup"><span data-stu-id="cb265-113">A pointer to a null-terminated string that specifies the key containing the values to enumerate.</span></span> <span data-ttu-id="cb265-114">Use el carácter de barra diagonal inversa ( \\ ) como delimitador para especificar una ruta de acceso con una o más subclaves.</span><span class="sxs-lookup"><span data-stu-id="cb265-114">Use the backslash ( \\ ) character as a delimiter to specify a path with one or more subkeys.</span></span> <span data-ttu-id="cb265-115">**EnumPrinterDataEx** enumera todos los valores de la clave, pero no enumera los valores de las subclaves de la clave especificada.</span><span class="sxs-lookup"><span data-stu-id="cb265-115">**EnumPrinterDataEx** enumerates all values of the key, but does not enumerate values of subkeys of the specified key.</span></span> <span data-ttu-id="cb265-116">Utilice la función [**EnumPrinterKey**](enumprinterkey.md) para enumerar las subclaves.</span><span class="sxs-lookup"><span data-stu-id="cb265-116">Use the [**EnumPrinterKey**](enumprinterkey.md) function to enumerate subkeys.</span></span>

<span data-ttu-id="cb265-117">Si *pKeyName* es **null** o una cadena vacía, **EnumPrinterDataEx** devuelve un \_ parámetro no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="cb265-117">If *pKeyName* is **NULL** or an empty string, **EnumPrinterDataEx** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="cb265-118">*pEnumValues* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cb265-118">*pEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb265-119">Un puntero a un búfer que recibe una matriz de estructuras de [**\_ \_ valores de enumeración de impresora**](printer-enum-values.md) .</span><span class="sxs-lookup"><span data-stu-id="cb265-119">A pointer to a buffer that receives an array of [**PRINTER\_ENUM\_VALUES**](printer-enum-values.md) structures.</span></span> <span data-ttu-id="cb265-120">Cada estructura contiene el nombre del valor, el tipo, los datos y los tamaños de un valor bajo la clave.</span><span class="sxs-lookup"><span data-stu-id="cb265-120">Each structure contains the value name, type, data, and sizes of a value under the key.</span></span>

</dd> <dt>

<span data-ttu-id="cb265-121">*cbEnumValues* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb265-121">*cbEnumValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb265-122">Tamaño, en bytes, del búfer al que apunta *pcbEnumValues*.</span><span class="sxs-lookup"><span data-stu-id="cb265-122">The size, in bytes, of the buffer pointed to by *pcbEnumValues*.</span></span> <span data-ttu-id="cb265-123">Si establece *cbEnumValues* en cero, el parámetro *pcbEnumValues* devuelve el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="cb265-123">If you set *cbEnumValues* to zero, the *pcbEnumValues* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="cb265-124">*pcbEnumValues* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cb265-124">*pcbEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb265-125">Puntero a una variable que recibe el tamaño, en bytes, de los datos de configuración recuperados.</span><span class="sxs-lookup"><span data-stu-id="cb265-125">A pointer to a variable that receives the size, in bytes, of the retrieved configuration data.</span></span> <span data-ttu-id="cb265-126">Si el tamaño de búfer especificado por *cbEnumValues* es demasiado pequeño, la función devuelve un error \_ más \_ datos y *pcbEnumValues* indica el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="cb265-126">If the buffer size specified by *cbEnumValues* is too small, the function returns ERROR\_MORE\_DATA and *pcbEnumValues* indicates the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="cb265-127">*pnEnumValues* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cb265-127">*pnEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb265-128">Puntero a una variable que recibe el número de estructuras [**de \_ \_ valores de enumeración de impresora**](printer-enum-values.md) devueltas en *pEnumValues*.</span><span class="sxs-lookup"><span data-stu-id="cb265-128">A pointer to a variable that receives the number of [**PRINTER\_ENUM\_VALUES**](printer-enum-values.md) structures returned in *pEnumValues*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb265-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb265-129">Return value</span></span>

<span data-ttu-id="cb265-130">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="cb265-130">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="cb265-131">Si se produce un error en la función, el valor devuelto es un código de error del sistema.</span><span class="sxs-lookup"><span data-stu-id="cb265-131">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb265-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb265-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cb265-133">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="cb265-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="cb265-134">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="cb265-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="cb265-135">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="cb265-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="cb265-136">**EnumPrinterDataEx** recupera los datos de configuración de la impresora establecidos por las funciones [**SetPrinterDataEx**](setprinterdataex.md) y [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="cb265-136">**EnumPrinterDataEx** retrieves printer configuration data set by the [**SetPrinterDataEx**](setprinterdataex.md) and [**SetPrinterData**](setprinterdata.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb265-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb265-137">Requirements</span></span>



| <span data-ttu-id="cb265-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb265-138">Requirement</span></span> | <span data-ttu-id="cb265-139">Value</span><span class="sxs-lookup"><span data-stu-id="cb265-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb265-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb265-140">Minimum supported client</span></span><br/> | <span data-ttu-id="cb265-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cb265-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cb265-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb265-142">Minimum supported server</span></span><br/> | <span data-ttu-id="cb265-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cb265-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cb265-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb265-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb265-145"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb265-145"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cb265-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb265-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb265-147"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb265-147"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="cb265-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb265-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb265-149"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="cb265-149"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="cb265-150">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="cb265-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cb265-151">**EnumPrinterDataExW** (Unicode) y **EnumPrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cb265-151">**EnumPrinterDataExW** (Unicode) and **EnumPrinterDataExA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="cb265-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb265-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb265-153">Impresión</span><span class="sxs-lookup"><span data-stu-id="cb265-153">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cb265-154">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="cb265-154">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="cb265-155">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="cb265-155">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="cb265-156">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="cb265-156">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="cb265-157">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="cb265-157">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="cb265-158">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="cb265-158">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="cb265-159">**\_valores de enumeración de impresora \_**</span><span class="sxs-lookup"><span data-stu-id="cb265-159">**PRINTER\_ENUM\_VALUES**</span></span>](printer-enum-values.md)
</dt> <dt>

[<span data-ttu-id="cb265-160">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="cb265-160">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> <dt>

[<span data-ttu-id="cb265-161">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="cb265-161">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




