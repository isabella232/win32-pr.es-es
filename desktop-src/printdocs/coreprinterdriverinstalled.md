---
description: La función CorePrinterDriverInstalled notifica si está instalado un controlador de impresora principal con un GUID, una fecha y una versión especificados.
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: Función CorePrinterDriverInstalled (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2e4f7033e5ca15a892a208621049c2f500873d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083024"
---
# <a name="coreprinterdriverinstalled-function"></a><span data-ttu-id="91357-103">CorePrinterDriverInstalled función)</span><span class="sxs-lookup"><span data-stu-id="91357-103">CorePrinterDriverInstalled function</span></span>

<span data-ttu-id="91357-104">La función **CorePrinterDriverInstalled** notifica si está instalado un controlador de impresora principal con un GUID, una fecha y una versión especificados.</span><span class="sxs-lookup"><span data-stu-id="91357-104">The **CorePrinterDriverInstalled** function reports whether a core printer driver with a specified GUID, date, and version is installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="91357-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91357-105">Syntax</span></span>


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
);
```



## <a name="parameters"></a><span data-ttu-id="91357-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91357-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91357-107">*pszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91357-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91357-108">Puntero a una cadena constante y terminada en null que especifica el nombre del servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="91357-108">Pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="91357-109">Use **null** para el equipo local.</span><span class="sxs-lookup"><span data-stu-id="91357-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="91357-110">*pszEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91357-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91357-111">Puntero a una cadena constante, terminada en null que especifica la arquitectura del procesador (por ejemplo, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="91357-111">Pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="91357-112">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="91357-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="91357-113">*CoreDriverGUID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91357-113">*CoreDriverGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91357-114">GUID del controlador de impresora principal.</span><span class="sxs-lookup"><span data-stu-id="91357-114">The GUID of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="91357-115">*ftDriverDate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91357-115">*ftDriverDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91357-116">La fecha del controlador de impresora principal.</span><span class="sxs-lookup"><span data-stu-id="91357-116">The date of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="91357-117">*dwlDriverVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91357-117">*dwlDriverVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91357-118">Versión del controlador de impresora principal.</span><span class="sxs-lookup"><span data-stu-id="91357-118">The version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="91357-119">*pbDriverInstalled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="91357-119">*pbDriverInstalled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91357-120">Un puntero a **true** si se instala el controlador, o una versión más reciente, **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="91357-120">A pointer to **TRUE** if the driver, or a newer version, is installed, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91357-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91357-121">Return value</span></span>

<span data-ttu-id="91357-122">Si la operación se realiza correctamente, el valor devuelto es S \_ OK; de lo contrario, **HRESULT** contendrá un código de error.</span><span class="sxs-lookup"><span data-stu-id="91357-122">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="91357-123">Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="91357-123">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="91357-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91357-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="91357-125">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="91357-125">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="91357-126">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="91357-126">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="91357-127">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="91357-127">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="91357-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91357-128">Requirements</span></span>



| <span data-ttu-id="91357-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="91357-129">Requirement</span></span> | <span data-ttu-id="91357-130">Value</span><span class="sxs-lookup"><span data-stu-id="91357-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91357-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91357-131">Minimum supported client</span></span><br/> | <span data-ttu-id="91357-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="91357-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="91357-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91357-133">Minimum supported server</span></span><br/> | <span data-ttu-id="91357-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="91357-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="91357-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91357-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="91357-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91357-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="91357-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="91357-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="91357-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91357-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="91357-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="91357-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91357-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91357-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="91357-141">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="91357-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="91357-142">**CorePrinterDriverInstalledW** (Unicode) y **CorePrinterDriverInstalledA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="91357-142">**CorePrinterDriverInstalledW** (Unicode) and **CorePrinterDriverInstalledA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="91357-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="91357-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91357-144">Impresión</span><span class="sxs-lookup"><span data-stu-id="91357-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="91357-145">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="91357-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

