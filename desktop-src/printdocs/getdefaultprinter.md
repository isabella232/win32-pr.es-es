---
description: La función GetDefaultPrinter recupera el nombre de la impresora predeterminada del usuario actual en el equipo local.
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: Función GetDefaultPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDefaultPrinter
- GetDefaultPrinterA
- GetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8db5b2aef859ea5d8247fc203611af74c8daddd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697155"
---
# <a name="getdefaultprinter-function"></a><span data-ttu-id="eebcc-103">GetDefaultPrinter función)</span><span class="sxs-lookup"><span data-stu-id="eebcc-103">GetDefaultPrinter function</span></span>

<span data-ttu-id="eebcc-104">La función **GetDefaultPrinter** recupera el nombre de la impresora predeterminada del usuario actual en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="eebcc-104">The **GetDefaultPrinter** function retrieves the printer name of the default printer for the current user on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="eebcc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eebcc-105">Syntax</span></span>


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="eebcc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eebcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eebcc-107">*pszBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eebcc-107">*pszBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eebcc-108">Un puntero a un búfer que recibe una cadena de caracteres terminada en null que contiene el nombre de impresora predeterminado.</span><span class="sxs-lookup"><span data-stu-id="eebcc-108">A pointer to a buffer that receives a null-terminated character string containing the default printer name.</span></span> <span data-ttu-id="eebcc-109">Si este parámetro es **null**, se produce un error en la función y la variable a la que apunta *pcchBuffer* devuelve el tamaño de búfer necesario, en caracteres.</span><span class="sxs-lookup"><span data-stu-id="eebcc-109">If this parameter is **NULL**, the function fails and the variable pointed to by *pcchBuffer* returns the required buffer size, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="eebcc-110">*pcchBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eebcc-110">*pcchBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eebcc-111">En la entrada, especifica el tamaño, en caracteres, del búfer de *pszBuffer* .</span><span class="sxs-lookup"><span data-stu-id="eebcc-111">On input, specifies the size, in characters, of the *pszBuffer* buffer.</span></span> <span data-ttu-id="eebcc-112">En la salida, recibe el tamaño, en caracteres, de la cadena del nombre de la impresora, incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="eebcc-112">On output, receives the size, in characters, of the printer name string, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eebcc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eebcc-113">Return value</span></span>

<span data-ttu-id="eebcc-114">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero y la variable a la que apunta *pcchBuffer* contiene el número de caracteres copiados en el búfer *pszBuffer* , incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="eebcc-114">If the function succeeds, the return value is a nonzero value and the variable pointed to by *pcchBuffer* contains the number of characters copied to the *pszBuffer* buffer, including the terminating null character.</span></span>

<span data-ttu-id="eebcc-115">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="eebcc-115">If the function fails, the return value is zero.</span></span>



| <span data-ttu-id="eebcc-116">Value</span><span class="sxs-lookup"><span data-stu-id="eebcc-116">Value</span></span>                       | <span data-ttu-id="eebcc-117">Significado</span><span class="sxs-lookup"><span data-stu-id="eebcc-117">Meaning</span></span>                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eebcc-118">ERROR \_ de \_ búfer insuficiente</span><span class="sxs-lookup"><span data-stu-id="eebcc-118">ERROR\_INSUFFICIENT\_BUFFER</span></span> | <span data-ttu-id="eebcc-119">El búfer de *pszBuffer* es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="eebcc-119">The *pszBuffer* buffer is too small.</span></span> <span data-ttu-id="eebcc-120">La variable a la que apunta *pcchBuffer* contiene el tamaño de búfer necesario, en caracteres.</span><span class="sxs-lookup"><span data-stu-id="eebcc-120">The variable pointed to by *pcchBuffer* contains the required buffer size, in characters.</span></span> |
| <span data-ttu-id="eebcc-121">\_ \_ no \_ se encontró el archivo de error</span><span class="sxs-lookup"><span data-stu-id="eebcc-121">ERROR\_FILE\_NOT\_FOUND</span></span>     | <span data-ttu-id="eebcc-122">No hay ninguna impresora predeterminada.</span><span class="sxs-lookup"><span data-stu-id="eebcc-122">There is no default printer.</span></span>                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="eebcc-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eebcc-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eebcc-124">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="eebcc-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="eebcc-125">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="eebcc-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="eebcc-126">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="eebcc-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eebcc-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eebcc-127">Requirements</span></span>



| <span data-ttu-id="eebcc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="eebcc-128">Requirement</span></span> | <span data-ttu-id="eebcc-129">Value</span><span class="sxs-lookup"><span data-stu-id="eebcc-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eebcc-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eebcc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="eebcc-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eebcc-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="eebcc-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eebcc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="eebcc-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eebcc-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="eebcc-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eebcc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="eebcc-135"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eebcc-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="eebcc-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eebcc-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="eebcc-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eebcc-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="eebcc-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eebcc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eebcc-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="eebcc-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="eebcc-140">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="eebcc-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="eebcc-141">**GetDefaultPrinterW** (Unicode) y **GetDefaultPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="eebcc-141">**GetDefaultPrinterW** (Unicode) and **GetDefaultPrinterA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="eebcc-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="eebcc-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eebcc-143">Impresión</span><span class="sxs-lookup"><span data-stu-id="eebcc-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="eebcc-144">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="eebcc-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="eebcc-145">**SetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="eebcc-145">**SetDefaultPrinter**</span></span>](setdefaultprinter.md)
</dt> </dl>

 

 




