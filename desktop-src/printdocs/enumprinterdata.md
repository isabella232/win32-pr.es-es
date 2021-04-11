---
description: La función EnumPrinterData enumera los datos de configuración de una impresora especificada.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: Función EnumPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterData
- EnumPrinterDataA
- EnumPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d7c175b0c90853a592e0ff979095d41432c16b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276661"
---
# <a name="enumprinterdata-function"></a><span data-ttu-id="ce051-103">EnumPrinterData función)</span><span class="sxs-lookup"><span data-stu-id="ce051-103">EnumPrinterData function</span></span>

<span data-ttu-id="ce051-104">La función **EnumPrinterData** enumera los datos de configuración de una impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="ce051-104">The **EnumPrinterData** function enumerates configuration data for a specified printer.</span></span>

<span data-ttu-id="ce051-105">Para recuperar los datos de configuración en una sola llamada, utilice la función [**EnumPrinterDataEx**](enumprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="ce051-105">To retrieve the configuration data in a single call, use the [**EnumPrinterDataEx**](enumprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce051-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce051-106">Syntax</span></span>


```C++
DWORD EnumPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   dwIndex,
  _Out_ LPTSTR  pValueName,
  _In_  DWORD   cbValueName,
  _Out_ LPDWORD pcbValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbData,
  _Out_ LPDWORD pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="ce051-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce051-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce051-108">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ce051-108">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce051-109">Identificador de la impresora cuyos datos de configuración se van a obtener.</span><span class="sxs-lookup"><span data-stu-id="ce051-109">A handle to the printer whose configuration data is to be obtained.</span></span> <span data-ttu-id="ce051-110">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="ce051-110">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="ce051-111">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ce051-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce051-112">Valor de índice que especifica el valor de los datos de configuración que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="ce051-112">An index value that specifies the configuration data value to retrieve.</span></span>

<span data-ttu-id="ce051-113">Establezca este parámetro en cero para la primera llamada a **EnumPrinterData** para un identificador de impresora especificado.</span><span class="sxs-lookup"><span data-stu-id="ce051-113">Set this parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="ce051-114">A continuación, incremente el parámetro en uno para las llamadas posteriores que impliquen la misma impresora, hasta que la función devuelva el ERROR \_ no \_ más \_ elementos.</span><span class="sxs-lookup"><span data-stu-id="ce051-114">Then increment the parameter by one for subsequent calls involving the same printer, until the function returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="ce051-115">Vea la siguiente sección de comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="ce051-115">See the following Remarks section for further information.</span></span>

<span data-ttu-id="ce051-116">Si usa la técnica mencionada en las descripciones de los parámetros *cbValueName* y *cbData* para obtener los valores de tamaño de búfer adecuados, al establecer ambos parámetros en cero en una primera llamada a **EnumPrinterData** para un identificador de impresora especificado, el valor de *dwIndex* no es relevante para esa llamada.</span><span class="sxs-lookup"><span data-stu-id="ce051-116">If you use the technique mentioned in the descriptions of the *cbValueName* and *cbData* parameters to obtain adequate buffer size values, setting both those parameters to zero in a first call to **EnumPrinterData** for a specified printer handle, the value of *dwIndex* does not matter for that call.</span></span> <span data-ttu-id="ce051-117">Establezca *dwIndex* en cero en la siguiente llamada a **EnumPrinterData** para iniciar el proceso de enumeración real.</span><span class="sxs-lookup"><span data-stu-id="ce051-117">Set *dwIndex* to zero in the next call to **EnumPrinterData** to start the actual enumeration process.</span></span>

<span data-ttu-id="ce051-118">Los valores de los datos de configuración no están ordenados.</span><span class="sxs-lookup"><span data-stu-id="ce051-118">Configuration data values are not ordered.</span></span> <span data-ttu-id="ce051-119">Los valores nuevos tendrán un índice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ce051-119">New values will have an arbitrary index.</span></span> <span data-ttu-id="ce051-120">Esto significa que la función **EnumPrinterData** puede devolver valores en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="ce051-120">This means that the **EnumPrinterData** function may return values in any order.</span></span>

</dd> <dt>

<span data-ttu-id="ce051-121">*pValueName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ce051-121">*pValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce051-122">Un puntero a un búfer que recibe el nombre del valor de los datos de configuración, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="ce051-122">A pointer to a buffer that receives the name of the configuration data value, including a terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="ce051-123">*cbValueName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ce051-123">*cbValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce051-124">Tamaño, en bytes, del búfer al que apunta *pValueName*.</span><span class="sxs-lookup"><span data-stu-id="ce051-124">The size, in bytes, of the buffer pointed to by *pValueName*.</span></span>

<span data-ttu-id="ce051-125">Si desea que el sistema operativo proporcione un tamaño de búfer adecuado, establezca este parámetro y el parámetro *cbData* en cero para la primera llamada a **EnumPrinterData** para un identificador de impresora especificado.</span><span class="sxs-lookup"><span data-stu-id="ce051-125">If you want to have the operating system supply an adequate buffer size, set both this parameter and the *cbData* parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="ce051-126">Cuando la función devuelve, la variable a la que apunta *pcbValueName* contendrá un tamaño de búfer que es lo suficientemente grande como para enumerar correctamente todos los nombres de los valores de los datos de configuración de la impresora.</span><span class="sxs-lookup"><span data-stu-id="ce051-126">When the function returns, the variable pointed to by *pcbValueName* will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.</span></span>

</dd> <dt>

<span data-ttu-id="ce051-127">*pcbValueName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ce051-127">*pcbValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce051-128">Puntero a una variable que recibe el número de bytes almacenados en el búfer al que apunta *pValueName*.</span><span class="sxs-lookup"><span data-stu-id="ce051-128">A pointer to a variable that receives the number of bytes stored into the buffer pointed to by *pValueName*.</span></span>

</dd> <dt>

<span data-ttu-id="ce051-129">*pType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ce051-129">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce051-130">Puntero a una variable que recibe un código que indica el tipo de datos almacenados en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="ce051-130">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="ce051-131">Para obtener una lista de los códigos de tipo posibles, vea [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="ce051-131">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span> <span data-ttu-id="ce051-132">El parámetro *pType* puede ser **null** si no se requiere el código de tipo.</span><span class="sxs-lookup"><span data-stu-id="ce051-132">The *pType* parameter can be **NULL** if the type code is not required.</span></span>

</dd> <dt>

<span data-ttu-id="ce051-133">*pdata* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ce051-133">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce051-134">Un puntero a un búfer que recibe el valor de los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="ce051-134">A pointer to a buffer that receives the configuration data value.</span></span>

<span data-ttu-id="ce051-135">Este parámetro puede ser **null** si el valor de los datos de configuración no es necesario.</span><span class="sxs-lookup"><span data-stu-id="ce051-135">This parameter can be **NULL** if the configuration data value is not required.</span></span>

</dd> <dt>

<span data-ttu-id="ce051-136">*cbData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ce051-136">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce051-137">Tamaño, en bytes, del búfer al que apunta *pdata*.</span><span class="sxs-lookup"><span data-stu-id="ce051-137">The size, in bytes, of the buffer pointed to by *pData*.</span></span>

<span data-ttu-id="ce051-138">Si desea que el sistema operativo proporcione un tamaño de búfer adecuado, establezca este parámetro y el parámetro *cbValueName* en cero para la primera llamada a **EnumPrinterData** para un identificador de impresora especificado.</span><span class="sxs-lookup"><span data-stu-id="ce051-138">If you want to have the operating system supply an adequate buffer size, set both this parameter and the *cbValueName* parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="ce051-139">Cuando la función devuelve, la variable a la que apunta *pcbData* contendrá un tamaño de búfer que es lo suficientemente grande como para enumerar correctamente todos los nombres de los valores de los datos de configuración de la impresora.</span><span class="sxs-lookup"><span data-stu-id="ce051-139">When the function returns, the variable pointed to by *pcbData* will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.</span></span>

</dd> <dt>

<span data-ttu-id="ce051-140">*pcbData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ce051-140">*pcbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce051-141">Puntero a una variable que recibe el número de bytes almacenados en el búfer al que apunta *pdata*.</span><span class="sxs-lookup"><span data-stu-id="ce051-141">A pointer to a variable that receives the number of bytes stored into the buffer pointed to by *pData*.</span></span>

<span data-ttu-id="ce051-142">Este parámetro puede ser **null** si *pdata* es **null**.</span><span class="sxs-lookup"><span data-stu-id="ce051-142">This parameter can be **NULL** if *pData* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce051-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce051-143">Return value</span></span>

<span data-ttu-id="ce051-144">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ce051-144">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="ce051-145">Si se produce un error en la función, el valor devuelto es un código de error del sistema.</span><span class="sxs-lookup"><span data-stu-id="ce051-145">If the function fails, the return value is a system error code.</span></span>

<span data-ttu-id="ce051-146">La función devuelve el ERROR \_ no hay \_ más \_ elementos cuando no hay más valores de datos de configuración para recuperar en un identificador de impresora especificado.</span><span class="sxs-lookup"><span data-stu-id="ce051-146">The function returns ERROR\_NO\_MORE\_ITEMS when there are no more configuration data values to retrieve for a specified printer handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce051-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce051-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ce051-148">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="ce051-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ce051-149">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="ce051-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ce051-150">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="ce051-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ce051-151">**EnumPrinterData** recupera los datos de configuración de la impresora establecidos por la función [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="ce051-151">**EnumPrinterData** retrieves printer configuration data set by the [**SetPrinterData**](setprinterdata.md) function.</span></span> <span data-ttu-id="ce051-152">Los datos de configuración de una impresora se componen de un conjunto de valores con nombre y con tipo.</span><span class="sxs-lookup"><span data-stu-id="ce051-152">A printer's configuration data consists of a set of named and typed values.</span></span> <span data-ttu-id="ce051-153">La función **EnumPrinterData** obtiene uno de estos valores, y su nombre y código de tipo, cada vez que lo llame.</span><span class="sxs-lookup"><span data-stu-id="ce051-153">The **EnumPrinterData** function obtains one of these values, and its name and a type code, each time you call it.</span></span> <span data-ttu-id="ce051-154">Llame a la función **EnumPrinterData** varias veces consecutivas para obtener todos los valores de datos de configuración de una impresora.</span><span class="sxs-lookup"><span data-stu-id="ce051-154">Call the **EnumPrinterData** function several times in succession to obtain all of a printer's configuration data values.</span></span>

<span data-ttu-id="ce051-155">Los datos de configuración de la impresora se almacenan en el registro.</span><span class="sxs-lookup"><span data-stu-id="ce051-155">Printer configuration data is stored in the registry.</span></span> <span data-ttu-id="ce051-156">Al enumerar los datos de configuración de la impresora, debe evitar llamar a las funciones del registro que podrían cambiar los datos.</span><span class="sxs-lookup"><span data-stu-id="ce051-156">While enumerating printer configuration data, you should avoid calling registry functions that might change that data.</span></span>

<span data-ttu-id="ce051-157">Si desea que el sistema operativo proporcione un tamaño de búfer adecuado, llame primero a **EnumPrinterData** con los parámetros *cbValueName* y *cbData* establecidos en cero, como se indicó anteriormente en la sección de parámetros.</span><span class="sxs-lookup"><span data-stu-id="ce051-157">If you want to have the operating system supply an adequate buffer size, first call **EnumPrinterData** with both the *cbValueName* and *cbData* parameters set to zero, as noted earlier in the Parameters section.</span></span> <span data-ttu-id="ce051-158">El valor de *dwIndex* no es relevante para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="ce051-158">The value of *dwIndex* does not matter for this call.</span></span> <span data-ttu-id="ce051-159">Cuando la función devuelve, \* *pcbValueName* y \* *pcbData* contendrán tamaños de búfer lo suficientemente grandes como para enumerar todos los valores y nombres de los datos de configuración de la impresora.</span><span class="sxs-lookup"><span data-stu-id="ce051-159">When the function returns, \**pcbValueName* and \**pcbData* will contain buffer sizes that are large enough to enumerate all of the printer's configuration data value names and values.</span></span> <span data-ttu-id="ce051-160">En la siguiente llamada, asigne el nombre de valor y los búferes de datos, establezca *cbValueName* y *cbData* en los tamaños en bytes de los búferes asignados y establezca *dwIndex* en cero.</span><span class="sxs-lookup"><span data-stu-id="ce051-160">On the next call, allocate value name and data buffers, set *cbValueName* and *cbData* to the sizes in bytes of the allocated buffers, and set *dwIndex* to zero.</span></span> <span data-ttu-id="ce051-161">Después, continúe llamando a la función **EnumPrinterData** , incrementando *dwIndex* en uno cada vez, hasta que la función devuelva el error \_ no \_ más \_ elementos.</span><span class="sxs-lookup"><span data-stu-id="ce051-161">Thereafter, continue to call the **EnumPrinterData** function, incrementing *dwIndex* by one each time, until the function returns ERROR\_NO\_MORE\_ITEMS.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce051-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce051-162">Requirements</span></span>



| <span data-ttu-id="ce051-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce051-163">Requirement</span></span> | <span data-ttu-id="ce051-164">Value</span><span class="sxs-lookup"><span data-stu-id="ce051-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce051-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce051-165">Minimum supported client</span></span><br/> | <span data-ttu-id="ce051-166">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ce051-166">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ce051-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce051-167">Minimum supported server</span></span><br/> | <span data-ttu-id="ce051-168">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ce051-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ce051-169">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce051-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce051-170"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce051-170"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ce051-171">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce051-171">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce051-172"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce051-172"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ce051-173">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ce051-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce051-174"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ce051-174"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ce051-175">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ce051-175">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ce051-176">**EnumPrinterDataW** (Unicode) y **EnumPrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ce051-176">**EnumPrinterDataW** (Unicode) and **EnumPrinterDataA** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="ce051-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce051-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce051-178">Impresión</span><span class="sxs-lookup"><span data-stu-id="ce051-178">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ce051-179">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="ce051-179">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ce051-180">**DeletePrinterData**</span><span class="sxs-lookup"><span data-stu-id="ce051-180">**DeletePrinterData**</span></span>](deleteprinterdata.md)
</dt> <dt>

[<span data-ttu-id="ce051-181">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="ce051-181">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="ce051-182">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="ce051-182">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="ce051-183">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="ce051-183">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="ce051-184">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="ce051-184">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="ce051-185">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="ce051-185">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> </dl>

 

