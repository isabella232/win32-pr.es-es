---
description: La función EnumMonitors recupera información acerca de los monitores de Puerto instalados en el servidor especificado.
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
title: Función EnumMonitors (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMonitors
- EnumMonitorsA
- EnumMonitorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 1154cae0864b9d034ff356657d689cd3a768186f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813558"
---
# <a name="enummonitors-function"></a><span data-ttu-id="59c42-103">EnumMonitors función)</span><span class="sxs-lookup"><span data-stu-id="59c42-103">EnumMonitors function</span></span>

<span data-ttu-id="59c42-104">La función **EnumMonitors** recupera información acerca de los monitores de Puerto instalados en el servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="59c42-104">The **EnumMonitors** function retrieves information about the port monitors installed on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="59c42-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59c42-105">Syntax</span></span>


```C++
BOOL EnumMonitors(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pMonitors,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="59c42-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59c42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59c42-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59c42-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c42-108">Puntero a una cadena terminada en null que especifica el nombre del servidor en el que residen los monitores.</span><span class="sxs-lookup"><span data-stu-id="59c42-108">A pointer to a null-terminated string that specifies the name of the server on which the monitors reside.</span></span> <span data-ttu-id="59c42-109">Si este parámetro es **null**, se enumeran los monitores locales.</span><span class="sxs-lookup"><span data-stu-id="59c42-109">If this parameter is **NULL**, the local monitors are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="59c42-110">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="59c42-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c42-111">Versión de la estructura a la que apunta *pMonitors*.</span><span class="sxs-lookup"><span data-stu-id="59c42-111">The version of the structure pointed to by *pMonitors*.</span></span>

<span data-ttu-id="59c42-112">Este valor puede ser 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="59c42-112">This value can be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="59c42-113">*pMonitors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="59c42-113">*pMonitors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59c42-114">Puntero a un búfer que recibe una matriz de estructuras.</span><span class="sxs-lookup"><span data-stu-id="59c42-114">A pointer to a buffer that receives an array of structures.</span></span> <span data-ttu-id="59c42-115">El búfer debe ser lo suficientemente grande como para almacenar las cadenas a las que hacen referencia los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="59c42-115">The buffer must be large enough to store the strings referenced by the structure members.</span></span>

<span data-ttu-id="59c42-116">Para determinar el tamaño de búfer necesario, llame a **EnumMonitors** con *cbBuf* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="59c42-116">To determine the required buffer size, call **EnumMonitors** with *cbBuf* set to zero.</span></span> <span data-ttu-id="59c42-117">**EnumMonitors** produce un error, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error \_ \_ de búfer insuficiente y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.</span><span class="sxs-lookup"><span data-stu-id="59c42-117">**EnumMonitors** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

<span data-ttu-id="59c42-118">El búfer recibe una matriz de estructuras de supervisión de la [**\_ información \_ 1**](monitor-info-1.md) si el *nivel* es 1 o estructuras de [**supervisión de \_ información \_ 2**](monitor-info-2.md) si el *nivel* es 2.</span><span class="sxs-lookup"><span data-stu-id="59c42-118">The buffer receives an array of [**MONITOR\_INFO\_1**](monitor-info-1.md) structures if *Level* is 1, or [**MONITOR\_INFO\_2**](monitor-info-2.md) structures if *Level* is 2.</span></span>

</dd> <dt>

<span data-ttu-id="59c42-119">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59c42-119">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c42-120">Tamaño, en bytes, del búfer al que apunta *pMonitors*.</span><span class="sxs-lookup"><span data-stu-id="59c42-120">The size, in bytes, of the buffer pointed to by *pMonitors*.</span></span>

</dd> <dt>

<span data-ttu-id="59c42-121">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="59c42-121">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59c42-122">Puntero a una variable que recibe el número de bytes copiados si la función se ejecuta correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="59c42-122">A pointer to a variable that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> <dt>

<span data-ttu-id="59c42-123">*pcReturned* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="59c42-123">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59c42-124">Puntero a una variable que recibe el número de estructuras que se devolvieron en el búfer al que apunta *pMonitors*.</span><span class="sxs-lookup"><span data-stu-id="59c42-124">A pointer to a variable that receives the number of structures that were returned in the buffer pointed to by *pMonitors*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59c42-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59c42-125">Return value</span></span>

<span data-ttu-id="59c42-126">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="59c42-126">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="59c42-127">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="59c42-127">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="59c42-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59c42-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="59c42-129">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="59c42-129">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="59c42-130">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="59c42-130">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="59c42-131">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="59c42-131">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="59c42-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59c42-132">Requirements</span></span>



| <span data-ttu-id="59c42-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="59c42-133">Requirement</span></span> | <span data-ttu-id="59c42-134">Value</span><span class="sxs-lookup"><span data-stu-id="59c42-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59c42-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59c42-135">Minimum supported client</span></span><br/> | <span data-ttu-id="59c42-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="59c42-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="59c42-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59c42-137">Minimum supported server</span></span><br/> | <span data-ttu-id="59c42-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="59c42-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="59c42-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59c42-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="59c42-140"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59c42-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="59c42-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59c42-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="59c42-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59c42-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="59c42-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="59c42-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59c42-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="59c42-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="59c42-145">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="59c42-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="59c42-146">**EnumMonitorsW** (Unicode) y **EnumMonitorsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="59c42-146">**EnumMonitorsW** (Unicode) and **EnumMonitorsA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="59c42-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="59c42-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c42-148">Impresión</span><span class="sxs-lookup"><span data-stu-id="59c42-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="59c42-149">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="59c42-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="59c42-150">**Información de supervisión \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="59c42-150">**MONITOR\_INFO\_1**</span></span>](monitor-info-1.md)
</dt> <dt>

[<span data-ttu-id="59c42-151">**Información de supervisión \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="59c42-151">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

