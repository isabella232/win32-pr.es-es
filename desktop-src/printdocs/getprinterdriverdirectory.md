---
description: La función GetPrinterDriverDirectory recupera la ruta de acceso del directorio del controlador de impresora.
ms.assetid: 69c9cc87-d7e3-496a-b631-b3ae30cdb3fd
title: Función GetPrinterDriverDirectory (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverDirectory
- GetPrinterDriverDirectoryA
- GetPrinterDriverDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7acc68f99f9791ba4231bcfea2b1788cfb37011c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707230"
---
# <a name="getprinterdriverdirectory-function"></a><span data-ttu-id="f8e9f-103">GetPrinterDriverDirectory función)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-103">GetPrinterDriverDirectory function</span></span>

<span data-ttu-id="f8e9f-104">La función **GetPrinterDriverDirectory** recupera la ruta de acceso del directorio del controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-104">The **GetPrinterDriverDirectory** function retrieves the path of the printer-driver directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8e9f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8e9f-105">Syntax</span></span>


```C++
BOOL GetPrinterDriverDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverDirectory,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="f8e9f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8e9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8e9f-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8e9f-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8e9f-108">Puntero a una cadena terminada en null que especifica el nombre del servidor en el que reside el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-108">A pointer to a null-terminated string that specifies the name of the server on which the printer driver resides.</span></span> <span data-ttu-id="f8e9f-109">Si este parámetro es **null**, se recupera la ruta de acceso del directorio local del controlador.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-109">If this parameter is **NULL**, the local driver-directory path is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="f8e9f-110">*pEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8e9f-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8e9f-111">Un puntero a una cadena terminada en null que especifica el entorno (por ejemplo, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="f8e9f-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="f8e9f-112">Si este parámetro es **null**, se utiliza el entorno actual de la aplicación que realiza la llamada y el equipo cliente (no la aplicación de destino y el servidor de impresión).</span><span class="sxs-lookup"><span data-stu-id="f8e9f-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="f8e9f-113">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f8e9f-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8e9f-114">Nivel de estructura.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-114">The structure level.</span></span> <span data-ttu-id="f8e9f-115">Este valor debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="f8e9f-116">*pDriverDirectory* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f8e9f-116">*pDriverDirectory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8e9f-117">Un puntero a un búfer que recibe la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-117">A pointer to a buffer that receives the path.</span></span>

</dd> <dt>

<span data-ttu-id="f8e9f-118">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8e9f-118">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8e9f-119">Tamaño del búfer al que apunta *pDriverDirectory* .</span><span class="sxs-lookup"><span data-stu-id="f8e9f-119">The size of the buffer to which *pDriverDirectory* points.</span></span>

</dd> <dt>

<span data-ttu-id="f8e9f-120">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f8e9f-120">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8e9f-121">Un puntero a un valor que especifica el número de bytes copiados si la función se ejecuta correctamente, o el número de bytes necesarios si *cbBuf* es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-121">A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8e9f-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8e9f-122">Return value</span></span>

<span data-ttu-id="f8e9f-123">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f8e9f-124">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8e9f-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8e9f-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f8e9f-126">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f8e9f-127">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f8e9f-128">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f8e9f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8e9f-129">Requirements</span></span>



| <span data-ttu-id="f8e9f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8e9f-130">Requirement</span></span> | <span data-ttu-id="f8e9f-131">Value</span><span class="sxs-lookup"><span data-stu-id="f8e9f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8e9f-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8e9f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f8e9f-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f8e9f-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8e9f-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8e9f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f8e9f-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f8e9f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f8e9f-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8e9f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8e9f-137"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8e9f-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f8e9f-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8e9f-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8e9f-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8e9f-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f8e9f-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8e9f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8e9f-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f8e9f-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f8e9f-142">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f8e9f-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f8e9f-143">**GetPrinterDriverDirectoryW** (Unicode) y **GetPrinterDriverDirectoryA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-143">**GetPrinterDriverDirectoryW** (Unicode) and **GetPrinterDriverDirectoryA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f8e9f-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8e9f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8e9f-145">Impresión</span><span class="sxs-lookup"><span data-stu-id="f8e9f-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f8e9f-146">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="f8e9f-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f8e9f-147">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-147">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> </dl>

 

 




