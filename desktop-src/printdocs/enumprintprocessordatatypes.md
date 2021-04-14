---
description: La función EnumPrintProcessorDatatypes enumera los tipos de datos que admite un procesador de impresión especificado.
ms.assetid: 27b6e074-d303-446b-9e5f-6cfa55c30d26
title: Función EnumPrintProcessorDatatypes (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessorDatatypes
- EnumPrintProcessorDatatypesA
- EnumPrintProcessorDatatypesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 39742aff1fce73b6dac138e77f2f8c794428ff3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545358"
---
# <a name="enumprintprocessordatatypes-function"></a><span data-ttu-id="32113-103">EnumPrintProcessorDatatypes función)</span><span class="sxs-lookup"><span data-stu-id="32113-103">EnumPrintProcessorDatatypes function</span></span>

<span data-ttu-id="32113-104">La función **EnumPrintProcessorDatatypes** enumera los tipos de datos que admite un procesador de impresión especificado.</span><span class="sxs-lookup"><span data-stu-id="32113-104">The **EnumPrintProcessorDatatypes** function enumerates the data types that a specified print processor supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="32113-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32113-105">Syntax</span></span>


```C++
BOOL EnumPrintProcessorDatatypes(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pPrintProcessorName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDatatypes,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="32113-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32113-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32113-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32113-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32113-108">Puntero a una cadena terminada en null que especifica el nombre del servidor en el que reside el procesador de impresión.</span><span class="sxs-lookup"><span data-stu-id="32113-108">A pointer to a null-terminated string that specifies the name of the server on which the print processor resides.</span></span> <span data-ttu-id="32113-109">Si este parámetro es **null**, se enumeran los tipos de datos del procesador de impresión local.</span><span class="sxs-lookup"><span data-stu-id="32113-109">If this parameter is **NULL**, the data types for the local print processor are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="32113-110">*pPrintProcessorName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32113-110">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32113-111">Puntero a una cadena terminada en null que especifica el nombre del procesador de impresión cuyos tipos de datos se enumeran.</span><span class="sxs-lookup"><span data-stu-id="32113-111">A pointer to a null-terminated string that specifies the name of the print processor whose data types are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="32113-112">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="32113-112">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32113-113">Tipo de información que se devuelve en el búfer de *pDatatypes* .</span><span class="sxs-lookup"><span data-stu-id="32113-113">The type of information returned in the *pDatatypes* buffer.</span></span> <span data-ttu-id="32113-114">Este parámetro debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="32113-114">This parameter must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="32113-115">*pDatatypes* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="32113-115">*pDatatypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32113-116">Puntero a un búfer que recibe una matriz de estructuras de [**información de tipos de \_ dato \_ 1**](datatypes-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="32113-116">A pointer to a buffer that receives an array of [**DATATYPES\_INFO\_1**](datatypes-info-1.md) structures.</span></span> <span data-ttu-id="32113-117">Cada estructura describe un tipo de datos disponible.</span><span class="sxs-lookup"><span data-stu-id="32113-117">Each structure describes an available data type.</span></span> <span data-ttu-id="32113-118">El búfer debe ser lo suficientemente grande como para recibir la matriz de estructuras y cualquier cadena u otros datos a los que apuntan los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="32113-118">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="32113-119">Para determinar el tamaño de búfer necesario, llame a **EnumPrintProcessorDatatypes** con *cbBuf* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="32113-119">To determine the required buffer size, call **EnumPrintProcessorDatatypes** with *cbBuf* set to zero.</span></span> <span data-ttu-id="32113-120">**EnumPrintProcessorDatatypes** produce un error, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error \_ \_ de búfer insuficiente y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.</span><span class="sxs-lookup"><span data-stu-id="32113-120">**EnumPrintProcessorDatatypes** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="32113-121">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32113-121">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32113-122">Tamaño, en bytes, del búfer al que apunta *pDatatypes*.</span><span class="sxs-lookup"><span data-stu-id="32113-122">The size, in bytes, of the buffer pointed to by *pDatatypes*.</span></span>

</dd> <dt>

<span data-ttu-id="32113-123">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="32113-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32113-124">Un puntero a una variable que recibe el número de bytes copiados en el búfer de *pDatatypes* si la función se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="32113-124">A pointer to a variable that receives the number of bytes copied to the *pDatatypes* buffer if the function succeeds.</span></span> <span data-ttu-id="32113-125">Si el búfer es demasiado pequeño, se produce un error en la función y la variable recibe el número de bytes necesarios.</span><span class="sxs-lookup"><span data-stu-id="32113-125">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="32113-126">*pcReturned* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="32113-126">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32113-127">Puntero a una variable que recibe el número de estructuras devueltas en el búfer de *pDatatypes* .</span><span class="sxs-lookup"><span data-stu-id="32113-127">A pointer to a variable that receives the number of structures returned in the *pDatatypes* buffer.</span></span> <span data-ttu-id="32113-128">Es el número de tipos de datos admitidos.</span><span class="sxs-lookup"><span data-stu-id="32113-128">This is the number of supported data types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32113-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32113-129">Return value</span></span>

<span data-ttu-id="32113-130">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="32113-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="32113-131">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="32113-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="32113-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32113-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="32113-133">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="32113-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="32113-134">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="32113-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="32113-135">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="32113-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="32113-136">v</span><span class="sxs-lookup"><span data-stu-id="32113-136">v</span></span>

<span data-ttu-id="32113-137">A partir de Windows Vista, la información del tipo de datos de los servidores de impresión remotos se recupera de una caché local.</span><span class="sxs-lookup"><span data-stu-id="32113-137">Starting with Windows Vista, the data type information from remote print servers is retrieved from a local cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="32113-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32113-138">Requirements</span></span>



| <span data-ttu-id="32113-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="32113-139">Requirement</span></span> | <span data-ttu-id="32113-140">Value</span><span class="sxs-lookup"><span data-stu-id="32113-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32113-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32113-141">Minimum supported client</span></span><br/> | <span data-ttu-id="32113-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="32113-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="32113-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32113-143">Minimum supported server</span></span><br/> | <span data-ttu-id="32113-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="32113-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="32113-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32113-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="32113-146"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32113-146"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="32113-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="32113-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="32113-148"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32113-148"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="32113-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32113-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32113-150"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="32113-150"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="32113-151">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="32113-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="32113-152">**EnumPrintProcessorDatatypesW** (Unicode) y **EnumPrintProcessorDatatypesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="32113-152">**EnumPrintProcessorDatatypesW** (Unicode) and **EnumPrintProcessorDatatypesA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="32113-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="32113-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32113-154">Impresión</span><span class="sxs-lookup"><span data-stu-id="32113-154">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="32113-155">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="32113-155">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="32113-156">**Información de tipos de \_ dato \_ 1**</span><span class="sxs-lookup"><span data-stu-id="32113-156">**DATATYPES\_INFO\_1**</span></span>](datatypes-info-1.md)
</dt> <dt>

[<span data-ttu-id="32113-157">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="32113-157">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> </dl>

 

