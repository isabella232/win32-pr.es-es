---
description: La función EnumPrinterKey enumera las subclaves de una clave especificada para una impresora especificada.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: Función EnumPrinterKey (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterKey
- EnumPrinterKeyA
- EnumPrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d9af6a9ef26612385cee68eba9733c148cd36b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361098"
---
# <a name="enumprinterkey-function"></a><span data-ttu-id="1cf73-103">EnumPrinterKey función)</span><span class="sxs-lookup"><span data-stu-id="1cf73-103">EnumPrinterKey function</span></span>

<span data-ttu-id="1cf73-104">La función **EnumPrinterKey** enumera las subclaves de una clave especificada para una impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="1cf73-104">The **EnumPrinterKey** function enumerates the subkeys of a specified key for a specified printer.</span></span>

<span data-ttu-id="1cf73-105">Los datos de la impresora se almacenan en el registro.</span><span class="sxs-lookup"><span data-stu-id="1cf73-105">Printer data is stored in the registry.</span></span> <span data-ttu-id="1cf73-106">Al enumerar los datos de la impresora, no llame a las funciones del registro que podrían cambiar los datos.</span><span class="sxs-lookup"><span data-stu-id="1cf73-106">While enumerating printer data, do not call registry functions that might change the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf73-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cf73-107">Syntax</span></span>


```C++
DWORD EnumPrinterKey(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPTSTR  pSubkey,
  _In_  DWORD   cbSubkey,
  _Out_ LPDWORD pcbSubkey
);
```



## <a name="parameters"></a><span data-ttu-id="1cf73-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cf73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cf73-109">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cf73-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cf73-110">Identificador de la impresora para la que la función enumera las subclaves.</span><span class="sxs-lookup"><span data-stu-id="1cf73-110">A handle to the printer for which the function enumerates subkeys.</span></span> <span data-ttu-id="1cf73-111">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="1cf73-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="1cf73-112">*pKeyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cf73-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cf73-113">Puntero a una cadena terminada en null que especifica la clave que contiene las subclaves que se van a enumerar.</span><span class="sxs-lookup"><span data-stu-id="1cf73-113">A pointer to a null-terminated string that specifies the key containing the subkeys to enumerate.</span></span> <span data-ttu-id="1cf73-114">Use el carácter de barra diagonal inversa \\ como delimitador para especificar una ruta de acceso con una o más subclaves.</span><span class="sxs-lookup"><span data-stu-id="1cf73-114">Use the backslash '\\' character as a delimiter to specify a path with one or more subkeys.</span></span> <span data-ttu-id="1cf73-115">**EnumPrinterKey** enumera todas las subclaves de la clave, pero no enumera las subclaves de esas subclaves.</span><span class="sxs-lookup"><span data-stu-id="1cf73-115">**EnumPrinterKey** enumerates all subkeys of the key, but does not enumerate the subkeys of those subkeys.</span></span>

<span data-ttu-id="1cf73-116">Si *pKeyName* es una cadena vacía (""), **EnumPrinterKey** enumera la clave de nivel superior de la impresora.</span><span class="sxs-lookup"><span data-stu-id="1cf73-116">If *pKeyName* is an empty string (""), **EnumPrinterKey** enumerates the top-level key for the printer.</span></span> <span data-ttu-id="1cf73-117">Si *pKeyName* es **null**, **ENUMPRINTERKEY** devuelve un \_ parámetro de error no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="1cf73-117">If *pKeyName* is **NULL**, **EnumPrinterKey** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="1cf73-118">*pSubkey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1cf73-118">*pSubkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cf73-119">Puntero a un búfer que recibe una matriz de nombres de subclave terminados en NULL.</span><span class="sxs-lookup"><span data-stu-id="1cf73-119">A pointer to a buffer that receives an array of null-terminated subkey names.</span></span> <span data-ttu-id="1cf73-120">Dos caracteres nulos terminan la matriz.</span><span class="sxs-lookup"><span data-stu-id="1cf73-120">The array is terminated by two null characters.</span></span>

</dd> <dt>

<span data-ttu-id="1cf73-121">*cbSubkey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cf73-121">*cbSubkey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cf73-122">Tamaño, en bytes, del búfer al que apunta *pSubkey*.</span><span class="sxs-lookup"><span data-stu-id="1cf73-122">The size, in bytes, of the buffer pointed to by *pSubkey*.</span></span> <span data-ttu-id="1cf73-123">Si establece *cbSubkey* en cero, el parámetro *pcbSubkey* devuelve el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="1cf73-123">If you set *cbSubkey* to zero, the *pcbSubkey* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="1cf73-124">*pcbSubkey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1cf73-124">*pcbSubkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cf73-125">Puntero a una variable que recibe el número de bytes recuperados en el búfer de *pSubkey* .</span><span class="sxs-lookup"><span data-stu-id="1cf73-125">A pointer to a variable that receives the number of bytes retrieved in the *pSubkey* buffer.</span></span> <span data-ttu-id="1cf73-126">Si el tamaño de búfer especificado por *cbSubkey* es demasiado pequeño, la función devuelve un error \_ más \_ datos y *pcbSubkey* indica el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="1cf73-126">If the buffer size specified by *cbSubkey* is too small, the function returns ERROR\_MORE\_DATA and *pcbSubkey* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cf73-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cf73-127">Return value</span></span>

<span data-ttu-id="1cf73-128">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1cf73-128">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="1cf73-129">Si se produce un error en la función, el valor devuelto es un código de error del sistema.</span><span class="sxs-lookup"><span data-stu-id="1cf73-129">If the function fails, the return value is a system error code.</span></span> <span data-ttu-id="1cf73-130">Si *pKeyName* no existe, el valor devuelto es el \_ archivo de error \_ no \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="1cf73-130">If *pKeyName* does not exist, the return value is ERROR\_FILE\_NOT\_FOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cf73-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1cf73-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1cf73-132">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="1cf73-132">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="1cf73-133">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="1cf73-133">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="1cf73-134">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="1cf73-134">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1cf73-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cf73-135">Requirements</span></span>



| <span data-ttu-id="1cf73-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cf73-136">Requirement</span></span> | <span data-ttu-id="1cf73-137">Value</span><span class="sxs-lookup"><span data-stu-id="1cf73-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf73-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cf73-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1cf73-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1cf73-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1cf73-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cf73-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1cf73-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1cf73-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1cf73-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cf73-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cf73-143"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cf73-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1cf73-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1cf73-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="1cf73-145"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cf73-145"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1cf73-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1cf73-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cf73-147"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="1cf73-147"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="1cf73-148">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="1cf73-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1cf73-149">**EnumPrinterKeyW** (Unicode) y **EnumPrinterKeyA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1cf73-149">**EnumPrinterKeyW** (Unicode) and **EnumPrinterKeyA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="1cf73-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cf73-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cf73-151">Impresión</span><span class="sxs-lookup"><span data-stu-id="1cf73-151">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1cf73-152">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="1cf73-152">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1cf73-153">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="1cf73-153">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="1cf73-154">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="1cf73-154">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="1cf73-155">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="1cf73-155">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="1cf73-156">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="1cf73-156">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




