---
description: La función GetPrintProcessorDirectory recupera la ruta de acceso al directorio del procesador de impresión en el servidor especificado.
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: Función GetPrintProcessorDirectory (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintProcessorDirectory
- GetPrintProcessorDirectoryA
- GetPrintProcessorDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a105025ba22c7e188b8dd20df67f5e8ad28fce01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913154"
---
# <a name="getprintprocessordirectory-function"></a><span data-ttu-id="a12c9-103">GetPrintProcessorDirectory función)</span><span class="sxs-lookup"><span data-stu-id="a12c9-103">GetPrintProcessorDirectory function</span></span>

<span data-ttu-id="a12c9-104">La función **GetPrintProcessorDirectory** recupera la ruta de acceso al directorio del procesador de impresión en el servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="a12c9-104">The **GetPrintProcessorDirectory** function retrieves the path to the print processor directory on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a12c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a12c9-105">Syntax</span></span>


```C++
BOOL GetPrintProcessorDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="a12c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a12c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a12c9-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a12c9-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a12c9-108">Puntero a una cadena terminada en null que especifica el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="a12c9-108">A pointer to a null-terminated string that specifies the name of the server.</span></span> <span data-ttu-id="a12c9-109">Si este parámetro es **null**, se devuelve una ruta de acceso local.</span><span class="sxs-lookup"><span data-stu-id="a12c9-109">If this parameter is **NULL**, a local path is returned.</span></span>

</dd> <dt>

<span data-ttu-id="a12c9-110">*pEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a12c9-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a12c9-111">Un puntero a una cadena terminada en null que especifica el entorno (por ejemplo, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="a12c9-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="a12c9-112">Si este parámetro es **null**, se utiliza el entorno actual de la aplicación que realiza la llamada y el equipo cliente (no la aplicación de destino y el servidor de impresión).</span><span class="sxs-lookup"><span data-stu-id="a12c9-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="a12c9-113">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a12c9-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a12c9-114">Nivel de estructura.</span><span class="sxs-lookup"><span data-stu-id="a12c9-114">The structure level.</span></span> <span data-ttu-id="a12c9-115">Este valor debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="a12c9-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="a12c9-116">*pPrintProcessorInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a12c9-116">*pPrintProcessorInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a12c9-117">Un puntero a un búfer que recibe la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a12c9-117">A pointer to a buffer that receives the path.</span></span> <span data-ttu-id="a12c9-118">Tenga en cuenta que, para los sistemas operativos anteriores a Windows Server 2003 SP 1, la ruta de acceso está en el formato local del servidor, no en el formato remoto real.</span><span class="sxs-lookup"><span data-stu-id="a12c9-118">Note that, for operating systems prior to Windows Server 2003 SP 1, the path is in the local format for the server, not the true remote format.</span></span> <span data-ttu-id="a12c9-119">Por ejemplo, la ruta de acceso se proporciona como "% WINDIR% \\ system32 \\ spool \\ Prtprocs \\ % Environment%" en lugar de " \\ \\ ServerName \\ Print $ \\ Prtprocs \\ % Environment%", incluso cuando se llama para un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="a12c9-119">For example, the path is given as "%Windir%\\System32\\Spool\\Prtprocs\\%Environment%" instead of "\\\\ServerName\\Print$\\Prtprocs\\%Environment%", even when called for a remote server.</span></span> <span data-ttu-id="a12c9-120">En el caso de los sistemas operativos Windows Server 2003 SP 1 y versiones posteriores, se devuelve la ruta de acceso remota verdadera.</span><span class="sxs-lookup"><span data-stu-id="a12c9-120">For the operating systems Windows Server 2003 SP 1 and later, the true remote path is returned.</span></span>

</dd> <dt>

<span data-ttu-id="a12c9-121">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a12c9-121">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a12c9-122">Tamaño del búfer al que apunta *pPrintProcessorInfo*.</span><span class="sxs-lookup"><span data-stu-id="a12c9-122">The size of the buffer pointed to by *pPrintProcessorInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="a12c9-123">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a12c9-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a12c9-124">Un puntero a un valor que especifica el número de bytes copiados si la función se ejecuta correctamente, o el número de bytes necesarios si *cbBuf* es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="a12c9-124">A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a12c9-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a12c9-125">Return value</span></span>

<span data-ttu-id="a12c9-126">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="a12c9-126">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a12c9-127">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="a12c9-127">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a12c9-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a12c9-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a12c9-129">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="a12c9-129">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a12c9-130">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="a12c9-130">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a12c9-131">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="a12c9-131">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a12c9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a12c9-132">Requirements</span></span>



| <span data-ttu-id="a12c9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a12c9-133">Requirement</span></span> | <span data-ttu-id="a12c9-134">Value</span><span class="sxs-lookup"><span data-stu-id="a12c9-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a12c9-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a12c9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a12c9-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a12c9-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a12c9-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a12c9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a12c9-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a12c9-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a12c9-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a12c9-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a12c9-140"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a12c9-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a12c9-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a12c9-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="a12c9-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a12c9-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a12c9-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a12c9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a12c9-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="a12c9-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a12c9-145">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="a12c9-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a12c9-146">**GetPrintProcessorDirectoryW** (Unicode) y **GetPrintProcessorDirectoryA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a12c9-146">**GetPrintProcessorDirectoryW** (Unicode) and **GetPrintProcessorDirectoryA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="a12c9-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="a12c9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a12c9-148">Impresión</span><span class="sxs-lookup"><span data-stu-id="a12c9-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a12c9-149">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="a12c9-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a12c9-150">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="a12c9-150">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> </dl>

 

 




