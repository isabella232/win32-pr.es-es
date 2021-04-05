---
description: La función EnumPrintProcessors enumera los procesadores de impresión instalados en el servidor especificado.
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
title: Función EnumPrintProcessors (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessors
- EnumPrintProcessorsA
- EnumPrintProcessorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0c446c39cdfc37ae7c578f5123afe57d61519704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002303"
---
# <a name="enumprintprocessors-function"></a><span data-ttu-id="40fb2-103">EnumPrintProcessors función)</span><span class="sxs-lookup"><span data-stu-id="40fb2-103">EnumPrintProcessors function</span></span>

<span data-ttu-id="40fb2-104">La función **EnumPrintProcessors** enumera los procesadores de impresión instalados en el servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="40fb2-104">The **EnumPrintProcessors** function enumerates the print processors installed on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="40fb2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40fb2-105">Syntax</span></span>


```C++
BOOL EnumPrintProcessors(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="40fb2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40fb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40fb2-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="40fb2-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40fb2-108">Puntero a una cadena terminada en null que especifica el nombre del servidor en el que residen los procesadores de impresión.</span><span class="sxs-lookup"><span data-stu-id="40fb2-108">A pointer to a null-terminated string that specifies the name of the server on which the print processors reside.</span></span> <span data-ttu-id="40fb2-109">Si este parámetro es **null**, se enumeran los procesadores de impresión locales.</span><span class="sxs-lookup"><span data-stu-id="40fb2-109">If this parameter is **NULL**, the local print processors are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="40fb2-110">*pEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="40fb2-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40fb2-111">Un puntero a una cadena terminada en null que especifica el entorno (por ejemplo, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="40fb2-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="40fb2-112">Si este parámetro es **null**, se utiliza el entorno actual de la aplicación que realiza la llamada y el equipo cliente (no la aplicación de destino y el servidor de impresión).</span><span class="sxs-lookup"><span data-stu-id="40fb2-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="40fb2-113">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="40fb2-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40fb2-114">Tipo de información que se devuelve en el búfer de *pPrintProcessorInfo* .</span><span class="sxs-lookup"><span data-stu-id="40fb2-114">The type of information returned in the *pPrintProcessorInfo* buffer.</span></span> <span data-ttu-id="40fb2-115">Este parámetro debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="40fb2-115">This parameter must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="40fb2-116">*pPrintProcessorInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="40fb2-116">*pPrintProcessorInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40fb2-117">Un puntero a un búfer que recibe una matriz de estructuras [**PRINTPROCESSOR \_ info \_ 1**](printprocessor-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="40fb2-117">A pointer to a buffer that receives an array of [**PRINTPROCESSOR\_INFO\_1**](printprocessor-info-1.md) structures.</span></span> <span data-ttu-id="40fb2-118">Cada estructura describe un procesador de impresión disponible.</span><span class="sxs-lookup"><span data-stu-id="40fb2-118">Each structure describes an available print processor.</span></span> <span data-ttu-id="40fb2-119">El búfer debe ser lo suficientemente grande como para recibir la matriz de estructuras y las cadenas a las que apuntan los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="40fb2-119">The buffer must be large enough to receive the array of structures and any strings to which the structure members point.</span></span>

<span data-ttu-id="40fb2-120">Para determinar el tamaño de búfer necesario, llame a **EnumPrintProcessors** con *cbBuf* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="40fb2-120">To determine the required buffer size, call **EnumPrintProcessors** with *cbBuf* set to zero.</span></span> <span data-ttu-id="40fb2-121">**EnumPrintProcessors** produce un error, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error \_ \_ de búfer insuficiente y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.</span><span class="sxs-lookup"><span data-stu-id="40fb2-121">**EnumPrintProcessors** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="40fb2-122">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="40fb2-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40fb2-123">Tamaño, en bytes, del búfer al que apunta *pPrintProcessorInfo*.</span><span class="sxs-lookup"><span data-stu-id="40fb2-123">The size, in bytes, of the buffer pointed to by *pPrintProcessorInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="40fb2-124">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="40fb2-124">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40fb2-125">Un puntero a una variable que recibe el número de bytes copiados en el búfer de *pPrintProcessorInfo* si la función se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="40fb2-125">A pointer to a variable that receives the number of bytes copied to the *pPrintProcessorInfo* buffer if the function succeeds.</span></span> <span data-ttu-id="40fb2-126">Si el búfer es demasiado pequeño, se produce un error en la función y la variable recibe el número de bytes necesarios.</span><span class="sxs-lookup"><span data-stu-id="40fb2-126">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="40fb2-127">*pcReturned* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="40fb2-127">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40fb2-128">Puntero a una variable que recibe el número de estructuras devueltas en el búfer de *pPrintProcessorInfo* .</span><span class="sxs-lookup"><span data-stu-id="40fb2-128">A pointer to a variable that receives the number of structures returned in the *pPrintProcessorInfo* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40fb2-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40fb2-129">Return value</span></span>

<span data-ttu-id="40fb2-130">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="40fb2-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="40fb2-131">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="40fb2-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="40fb2-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40fb2-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="40fb2-133">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="40fb2-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="40fb2-134">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="40fb2-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="40fb2-135">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="40fb2-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="40fb2-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40fb2-136">Requirements</span></span>



| <span data-ttu-id="40fb2-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="40fb2-137">Requirement</span></span> | <span data-ttu-id="40fb2-138">Value</span><span class="sxs-lookup"><span data-stu-id="40fb2-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40fb2-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40fb2-139">Minimum supported client</span></span><br/> | <span data-ttu-id="40fb2-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="40fb2-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="40fb2-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40fb2-141">Minimum supported server</span></span><br/> | <span data-ttu-id="40fb2-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="40fb2-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="40fb2-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40fb2-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="40fb2-144"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40fb2-144"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="40fb2-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40fb2-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="40fb2-146"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40fb2-146"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="40fb2-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="40fb2-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40fb2-148"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="40fb2-148"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="40fb2-149">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="40fb2-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="40fb2-150">**EnumPrintProcessorsW** (Unicode) y **EnumPrintProcessorsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="40fb2-150">**EnumPrintProcessorsW** (Unicode) and **EnumPrintProcessorsA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="40fb2-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="40fb2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40fb2-152">Impresión</span><span class="sxs-lookup"><span data-stu-id="40fb2-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="40fb2-153">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="40fb2-153">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="40fb2-154">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="40fb2-154">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> <dt>

[<span data-ttu-id="40fb2-155">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="40fb2-155">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> <dt>

[<span data-ttu-id="40fb2-156">**PRINTPROCESSOR \_ info \_ 1**</span><span class="sxs-lookup"><span data-stu-id="40fb2-156">**PRINTPROCESSOR\_INFO\_1**</span></span>](printprocessor-info-1.md)
</dt> </dl>

 

