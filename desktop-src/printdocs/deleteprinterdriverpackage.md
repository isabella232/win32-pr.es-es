---
description: Elimina un paquete de controladores de impresora del almacén de controladores.
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: Función DeletePrinterDriverPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverPackage
- DeletePrinterDriverPackageA
- DeletePrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 54d1cda53795f4feab60e397ce7e38402f22374f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706295"
---
# <a name="deleteprinterdriverpackage-function"></a><span data-ttu-id="80c93-103">DeletePrinterDriverPackage función)</span><span class="sxs-lookup"><span data-stu-id="80c93-103">DeletePrinterDriverPackage function</span></span>

<span data-ttu-id="80c93-104">Elimina un paquete de controladores de impresora del almacén de controladores.</span><span class="sxs-lookup"><span data-stu-id="80c93-104">Deletes a printer driver package from the driver store.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c93-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80c93-105">Syntax</span></span>


```C++
HRESULT DeletePrinterDriverPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszEnvironment
);
```



## <a name="parameters"></a><span data-ttu-id="80c93-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80c93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80c93-107">*pszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80c93-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c93-108">Puntero a una cadena constante terminada en null que especifica el nombre del servidor de impresión del que se va a eliminar el paquete de controladores.</span><span class="sxs-lookup"><span data-stu-id="80c93-108">A pointer to a constant, null-terminated string that specifies the name of the print server from which the driver package is being deleted.</span></span> <span data-ttu-id="80c93-109">Un valor de puntero **nulo** significa el equipo local.</span><span class="sxs-lookup"><span data-stu-id="80c93-109">A **NULL** pointer value means the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="80c93-110">*pszInfPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80c93-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c93-111">Puntero a una cadena constante terminada en null que especifica la ruta de acceso al \* archivo. inf del controlador.</span><span class="sxs-lookup"><span data-stu-id="80c93-111">A pointer to a constant, null-terminated string that specifies the path to the driver's \*.inf file.</span></span>

</dd> <dt>

<span data-ttu-id="80c93-112">*pszEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80c93-112">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c93-113">Puntero a una cadena constante terminada en null que especifica la arquitectura del procesador (por ejemplo, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="80c93-113">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="80c93-114">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="80c93-114">This can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80c93-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80c93-115">Return value</span></span>

<span data-ttu-id="80c93-116">S \_ correcto, si la operación se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="80c93-116">S\_OK, if the operation succeeds.</span></span>

<span data-ttu-id="80c93-117">E \_ ACCESSDENIED, si el paquete se incluyó con Windows.</span><span class="sxs-lookup"><span data-stu-id="80c93-117">E\_ACCESSDENIED, if the package was shipped with Windows.</span></span>

<span data-ttu-id="80c93-118">\_Código HRESULT (error \_ \_ \_ \_ de paquete de controlador de impresión en \_ uso), si se está usando el paquete.</span><span class="sxs-lookup"><span data-stu-id="80c93-118">HRESULT\_CODE(ERROR\_PRINT\_DRIVER\_PACKAGE\_IN\_USE), if the package is being used.</span></span>

<span data-ttu-id="80c93-119">De lo contrario, el **valor HRESULT** contendrá un código de error.</span><span class="sxs-lookup"><span data-stu-id="80c93-119">Otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="80c93-120">Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="80c93-120">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="80c93-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80c93-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="80c93-122">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="80c93-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="80c93-123">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="80c93-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="80c93-124">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="80c93-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="80c93-125">El almacén de controladores suele ser% WINDIR% \\ inf o% WINDIR% \\ system32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="80c93-125">The driver store is typically %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="80c93-126">No se puede quitar un paquete de controladores incluido con Windows con esta función.</span><span class="sxs-lookup"><span data-stu-id="80c93-126">A driver package that shipped with Windows cannot be removed with this function.</span></span>

<span data-ttu-id="80c93-127">El usuario debe tener privilegios de administración de impresora.</span><span class="sxs-lookup"><span data-stu-id="80c93-127">The user must have printer administration privileges.</span></span>

## <a name="requirements"></a><span data-ttu-id="80c93-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80c93-128">Requirements</span></span>



| <span data-ttu-id="80c93-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="80c93-129">Requirement</span></span> | <span data-ttu-id="80c93-130">Value</span><span class="sxs-lookup"><span data-stu-id="80c93-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80c93-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80c93-131">Minimum supported client</span></span><br/> | <span data-ttu-id="80c93-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="80c93-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="80c93-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80c93-133">Minimum supported server</span></span><br/> | <span data-ttu-id="80c93-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="80c93-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="80c93-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80c93-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="80c93-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80c93-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="80c93-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80c93-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="80c93-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80c93-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="80c93-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="80c93-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80c93-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80c93-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="80c93-141">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="80c93-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="80c93-142">**DeletePrinterDriverPackageW** (Unicode) y **DeletePrinterDriverPackageA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="80c93-142">**DeletePrinterDriverPackageW** (Unicode) and **DeletePrinterDriverPackageA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="80c93-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="80c93-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80c93-144">Impresión</span><span class="sxs-lookup"><span data-stu-id="80c93-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="80c93-145">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="80c93-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

