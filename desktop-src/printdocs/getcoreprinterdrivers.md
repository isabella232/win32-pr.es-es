---
description: Recupera el GUID, la versión y la fecha de los controladores de impresora principales especificados y la ruta de acceso a sus paquetes.
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
title: Función GetCorePrinterDrivers (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCorePrinterDrivers
- GetCorePrinterDriversA
- GetCorePrinterDriversW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5bdebc3f4b716a21c56c9ec756ff56c02765d1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360656"
---
# <a name="getcoreprinterdrivers-function"></a><span data-ttu-id="8f868-103">GetCorePrinterDrivers función)</span><span class="sxs-lookup"><span data-stu-id="8f868-103">GetCorePrinterDrivers function</span></span>

<span data-ttu-id="8f868-104">Recupera el GUID, la versión y la fecha de los controladores de impresora principales especificados y la ruta de acceso a sus paquetes.</span><span class="sxs-lookup"><span data-stu-id="8f868-104">Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f868-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f868-105">Syntax</span></span>


```C++
HRESULT GetCorePrinterDrivers(
  _In_  LPCTSTR              pszServer,
  _In_  LPCTSTR              pszEnvironment,
  _In_  LPCTSTR              pszzCoreDriverDependencies,
  _In_  DWORD                cCorePrinterDrivers,
  _Out_ PCORE_PRINTER_DRIVER pCorePrinterDrivers
);
```



## <a name="parameters"></a><span data-ttu-id="8f868-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f868-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f868-107">*pszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f868-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f868-108">Puntero a una cadena constante terminada en null que especifica el nombre del servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="8f868-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="8f868-109">Use **null** para el equipo local.</span><span class="sxs-lookup"><span data-stu-id="8f868-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="8f868-110">*pszEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f868-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f868-111">Puntero a una cadena constante terminada en null que especifica la arquitectura del procesador (por ejemplo, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="8f868-111">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="8f868-112">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="8f868-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8f868-113">*pszzCoreDriverDependencies* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f868-113">*pszzCoreDriverDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f868-114">Puntero a una cadena múltiple terminada en null que especifica los GUID de los controladores de impresora principales.</span><span class="sxs-lookup"><span data-stu-id="8f868-114">A pointer to a null-terminated multi-string that specifies the GUIDs of the core printer drivers.</span></span>

</dd> <dt>

<span data-ttu-id="8f868-115">*cCorePrinterDrivers* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f868-115">*cCorePrinterDrivers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f868-116">Número de cadenas de *pszzCoreDriverDependencies*.</span><span class="sxs-lookup"><span data-stu-id="8f868-116">The number of strings in *pszzCoreDriverDependencies*.</span></span>

</dd> <dt>

<span data-ttu-id="8f868-117">*pCorePrinterDrivers* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8f868-117">*pCorePrinterDrivers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f868-118">Puntero a una matriz de una o varias estructuras [**principales \_ del \_ controlador de impresora**](core-printer-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="8f868-118">A pointer to an array of one or more [**CORE\_PRINTER\_DRIVER**](core-printer-driver.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f868-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f868-119">Return value</span></span>

<span data-ttu-id="8f868-120">Si la operación se realiza correctamente, el valor devuelto es S \_ OK; de lo contrario, **HRESULT** contendrá un código de error.</span><span class="sxs-lookup"><span data-stu-id="8f868-120">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="8f868-121">Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="8f868-121">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8f868-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f868-122">Remarks</span></span>

<span data-ttu-id="8f868-123">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8f868-123">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8f868-124">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8f868-124">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8f868-125">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="8f868-125">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f868-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f868-126">Requirements</span></span>



| <span data-ttu-id="8f868-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f868-127">Requirement</span></span> | <span data-ttu-id="8f868-128">Value</span><span class="sxs-lookup"><span data-stu-id="8f868-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f868-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f868-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8f868-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8f868-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8f868-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f868-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8f868-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f868-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8f868-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f868-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f868-134"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f868-134"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8f868-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f868-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="8f868-136"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f868-136"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8f868-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8f868-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f868-138"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f868-138"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="8f868-139">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="8f868-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8f868-140">**GetCorePrinterDriversW** (Unicode) y **GetCorePrinterDriversA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8f868-140">**GetCorePrinterDriversW** (Unicode) and **GetCorePrinterDriversA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="8f868-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f868-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f868-142">Impresión</span><span class="sxs-lookup"><span data-stu-id="8f868-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8f868-143">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="8f868-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

