---
description: La función EnumPorts enumera los puertos que están disponibles para imprimir en un servidor especificado.
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
title: Función EnumPorts (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPorts
- EnumPortsA
- EnumPortsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 2f4cceb6b6915f92139d8919b74f62ba4392381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648511"
---
# <a name="enumports-function"></a><span data-ttu-id="b6666-103">EnumPorts función)</span><span class="sxs-lookup"><span data-stu-id="b6666-103">EnumPorts function</span></span>

<span data-ttu-id="b6666-104">La función **EnumPorts** enumera los puertos que están disponibles para imprimir en un servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="b6666-104">The **EnumPorts** function enumerates the ports that are available for printing on a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6666-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6666-105">Syntax</span></span>


```C++
BOOL EnumPorts(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPorts,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="b6666-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6666-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6666-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b6666-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6666-108">Puntero a una cadena terminada en null que especifica el nombre del servidor cuyos puertos de impresora se desea enumerar.</span><span class="sxs-lookup"><span data-stu-id="b6666-108">A pointer to a null-terminated string that specifies the name of the server whose printer ports you want to enumerate.</span></span>

<span data-ttu-id="b6666-109">Si *pName* es **null**, la función enumera los puertos de impresora del equipo local.</span><span class="sxs-lookup"><span data-stu-id="b6666-109">If *pName* is **NULL**, the function enumerates the local machine's printer ports.</span></span>

</dd> <dt>

<span data-ttu-id="b6666-110">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b6666-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6666-111">Tipo de información que se devuelve en el búfer de *pPorts* .</span><span class="sxs-lookup"><span data-stu-id="b6666-111">The type of information returned in the *pPorts* buffer.</span></span> <span data-ttu-id="b6666-112">Si el *nivel* es 1, *pPorts* recibe una matriz de estructuras de [**información de puerto \_ \_ 1**](port-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="b6666-112">If *Level* is 1, *pPorts* receives an array of [**PORT\_INFO\_1**](port-info-1.md) structures.</span></span> <span data-ttu-id="b6666-113">Si *LEVEL* es 2, *pPorts* recibe una matriz de estructuras [**Port \_ info \_ 2**](port-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="b6666-113">If *Level* is 2, *pPorts* receives an array of [**PORT\_INFO\_2**](port-info-2.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="b6666-114">*pPorts* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b6666-114">*pPorts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6666-115">Un puntero a un búfer que recibe una matriz de estructuras de la [**información de puerto \_ \_ 1**](port-info-1.md) o de la [**información de puerto \_ \_ 2**](port-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="b6666-115">A pointer to a buffer that receives an array of [**PORT\_INFO\_1**](port-info-1.md) or [**PORT\_INFO\_2**](port-info-2.md) structures.</span></span> <span data-ttu-id="b6666-116">Cada estructura contiene datos que describen un puerto de impresora disponible.</span><span class="sxs-lookup"><span data-stu-id="b6666-116">Each structure contains data that describes an available printer port.</span></span> <span data-ttu-id="b6666-117">El búfer debe ser lo suficientemente grande como para almacenar las cadenas a las que apuntan los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="b6666-117">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="b6666-118">Para determinar el tamaño de búfer necesario, llame a **EnumPorts** con *cbBuf* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="b6666-118">To determine the required buffer size, call **EnumPorts** with *cbBuf* set to zero.</span></span> <span data-ttu-id="b6666-119">**EnumPorts** produce un error, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error \_ \_ de búfer insuficiente y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.</span><span class="sxs-lookup"><span data-stu-id="b6666-119">**EnumPorts** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="b6666-120">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b6666-120">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6666-121">Tamaño, en bytes, del búfer al que apunta *pPorts*.</span><span class="sxs-lookup"><span data-stu-id="b6666-121">The size, in bytes, of the buffer pointed to by *pPorts*.</span></span>

</dd> <dt>

<span data-ttu-id="b6666-122">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b6666-122">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6666-123">Puntero a una variable que recibe el número de bytes copiados en el búfer de *pPorts* .</span><span class="sxs-lookup"><span data-stu-id="b6666-123">A pointer to a variable that receives the number of bytes copied to the *pPorts* buffer.</span></span> <span data-ttu-id="b6666-124">Si el búfer es demasiado pequeño, se produce un error en la función y la variable recibe el número de bytes necesarios.</span><span class="sxs-lookup"><span data-stu-id="b6666-124">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="b6666-125">*pcReturned* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b6666-125">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6666-126">Un puntero a una variable que recibe el número de estructuras de [**información de puerto \_ \_ 1**](port-info-1.md) o de la [**información de puerto \_ \_ 2**](port-info-2.md) devueltas en el búfer de *pPorts* .</span><span class="sxs-lookup"><span data-stu-id="b6666-126">A pointer to a variable that receives the number of [**PORT\_INFO\_1**](port-info-1.md) or [**PORT\_INFO\_2**](port-info-2.md) structures returned in the *pPorts* buffer.</span></span> <span data-ttu-id="b6666-127">Es el número de puertos de impresora que están disponibles en el servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="b6666-127">This is the number of printer ports that are available on the specified server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6666-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6666-128">Return value</span></span>

<span data-ttu-id="b6666-129">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b6666-129">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b6666-130">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="b6666-130">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6666-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6666-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b6666-132">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b6666-132">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b6666-133">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b6666-133">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b6666-134">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="b6666-134">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b6666-135">La función **EnumPorts** puede tener éxito incluso si el servidor especificado por *pName* no tiene una impresora definida.</span><span class="sxs-lookup"><span data-stu-id="b6666-135">The **EnumPorts** function can succeed even if the server specified by *pName* does not have a printer defined.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6666-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6666-136">Requirements</span></span>



| <span data-ttu-id="b6666-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6666-137">Requirement</span></span> | <span data-ttu-id="b6666-138">Value</span><span class="sxs-lookup"><span data-stu-id="b6666-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6666-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6666-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b6666-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b6666-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b6666-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6666-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b6666-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b6666-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b6666-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6666-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6666-144"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6666-144"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b6666-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6666-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6666-146"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6666-146"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b6666-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b6666-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6666-148"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b6666-148"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b6666-149">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="b6666-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b6666-150">**EnumPortsW** (Unicode) y **EnumPortsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b6666-150">**EnumPortsW** (Unicode) and **EnumPortsA** (ANSI)</span></span><br/>                                             |



## <a name="see-also"></a><span data-ttu-id="b6666-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6666-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6666-152">Impresión</span><span class="sxs-lookup"><span data-stu-id="b6666-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b6666-153">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="b6666-153">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b6666-154">**AddPort**</span><span class="sxs-lookup"><span data-stu-id="b6666-154">**AddPort**</span></span>](addport.md)
</dt> <dt>

[<span data-ttu-id="b6666-155">**DeletePort**</span><span class="sxs-lookup"><span data-stu-id="b6666-155">**DeletePort**</span></span>](deleteport.md)
</dt> <dt>

[<span data-ttu-id="b6666-156">**Información de puerto \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="b6666-156">**PORT\_INFO\_1**</span></span>](port-info-1.md)
</dt> <dt>

[<span data-ttu-id="b6666-157">**INFO. de puerto \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b6666-157">**PORT\_INFO\_2**</span></span>](port-info-2.md)
</dt> </dl>

 

