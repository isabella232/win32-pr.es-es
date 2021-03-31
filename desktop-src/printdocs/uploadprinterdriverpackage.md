---
description: Carga un controlador de impresora en el almacén de controladores de los servidores de impresión para que se pueda instalar llamando a InstallPrinterDriverFromPackage.
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: Función UploadPrinterDriverPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UploadPrinterDriverPackage
- UploadPrinterDriverPackageA
- UploadPrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f616c4f731d3a416806f499a513f48466263f441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278643"
---
# <a name="uploadprinterdriverpackage-function"></a><span data-ttu-id="8482a-103">UploadPrinterDriverPackage función)</span><span class="sxs-lookup"><span data-stu-id="8482a-103">UploadPrinterDriverPackage function</span></span>

<span data-ttu-id="8482a-104">Carga un controlador de impresora en el almacén de controladores del servidor de impresión para que se pueda instalar llamando a [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).</span><span class="sxs-lookup"><span data-stu-id="8482a-104">Uploads a printer driver to the print server's driver store so that it can be installed by calling [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8482a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8482a-105">Syntax</span></span>


```C++
HRESULT UploadPrinterDriverPackage(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszInfPath,
  _In_    LPCTSTR pszEnvironment,
  _In_    DWORD   dwFlags,
  _In_    HWND    hwnd,
  _Out_   LPTSTR  pszDestInfPath,
  _Inout_ PULONG  pcchDestInfPath
);
```



## <a name="parameters"></a><span data-ttu-id="8482a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8482a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8482a-107">*pszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8482a-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8482a-108">Puntero a una cadena constante terminada en null que especifica el nombre del servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="8482a-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="8482a-109">Use **null** si el servidor es el equipo local.</span><span class="sxs-lookup"><span data-stu-id="8482a-109">Use **NULL** if the server is the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-110">*pszInfPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8482a-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8482a-111">Puntero a una cadena constante terminada en null que especifica la ruta de acceso de origen al archivo. inf del controlador.</span><span class="sxs-lookup"><span data-stu-id="8482a-111">A pointer to a constant ,null-terminated string that specifies the source path to the driver's .inf file.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-112">*pszEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8482a-112">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8482a-113">Puntero a una cadena constante terminada en null que especifica la arquitectura de procesador del servidor (por ejemplo, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="8482a-113">A pointer to a constant, null-terminated string that specifies the server's processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="8482a-114">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="8482a-114">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-115">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8482a-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8482a-116">Puede ser cualquiera de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="8482a-116">This can be any of the following values:</span></span>



| <span data-ttu-id="8482a-117">Value</span><span class="sxs-lookup"><span data-stu-id="8482a-117">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="8482a-118">Significado</span><span class="sxs-lookup"><span data-stu-id="8482a-118">Meaning</span></span>                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <span data-ttu-id="8482a-119"><dt>**UPDP_SILENT_UPLOAD**</dt></span><span class="sxs-lookup"><span data-stu-id="8482a-119"><dt>**UPDP_SILENT_UPLOAD**</dt></span></span> </dl>             | <span data-ttu-id="8482a-120">La interfaz de usuario no se mostrará durante la carga.</span><span class="sxs-lookup"><span data-stu-id="8482a-120">The UI will not be shown during the upload.</span></span><br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <span data-ttu-id="8482a-121"><dt>**UPDP_UPLOAD_ALWAYS**</dt></span><span class="sxs-lookup"><span data-stu-id="8482a-121"><dt>**UPDP_UPLOAD_ALWAYS**</dt></span></span> </dl>             | <span data-ttu-id="8482a-122">Los archivos se cargarán incluso si el paquete ya está en el almacén de controladores del servidor.</span><span class="sxs-lookup"><span data-stu-id="8482a-122">The files will be uploaded even if the package is already in the server's driver store.</span></span><br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <span data-ttu-id="8482a-123"><dt>**UPDP_CHECK_DRIVERSTORE**</dt></span><span class="sxs-lookup"><span data-stu-id="8482a-123"><dt>**UPDP_CHECK_DRIVERSTORE**</dt></span></span> </dl> | <span data-ttu-id="8482a-124">El almacén de controladores del servidor se comprobará antes de la carga para ver si el paquete ya está allí.</span><span class="sxs-lookup"><span data-stu-id="8482a-124">The server's driver store will be checked before upload to see if the package is already there.</span></span> <span data-ttu-id="8482a-125">Este valor se omite si se establece UPDP_UPLOAD_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="8482a-125">This setting is ignored if UPDP_UPLOAD_ALWAYS is set.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8482a-126">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8482a-126">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8482a-127">Identificador de la interfaz de usuario que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="8482a-127">A handle to the copying user interface.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-128">*pszDestInfPath* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8482a-128">*pszDestInfPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8482a-129">Un puntero a la ruta de acceso de destino, en el almacén de controladores, donde se copió el archivo. inf del controlador.</span><span class="sxs-lookup"><span data-stu-id="8482a-129">A pointer to the destination path, in the driver store, to which the driver's .inf file was copied.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-130">*pcchDestInfPath* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8482a-130">*pcchDestInfPath* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8482a-131">En la entrada, especifica el tamaño, en caracteres, del búfer de *pszDestInfPath* .</span><span class="sxs-lookup"><span data-stu-id="8482a-131">On input, specifies the size, in characters, of the *pszDestInfPath* buffer.</span></span> <span data-ttu-id="8482a-132">En la salida, recibe el tamaño, en caracteres, de la cadena de ruta de acceso, incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="8482a-132">On output, receives the size, in characters, of the path string, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8482a-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8482a-133">Return value</span></span>

<span data-ttu-id="8482a-134">Si la operación se realiza correctamente, el valor devuelto es S_OK; de lo contrario, **HRESULT** contendrá un código de error.</span><span class="sxs-lookup"><span data-stu-id="8482a-134">If the operation succeeds, the return value is S_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="8482a-135">Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="8482a-135">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8482a-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8482a-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8482a-137">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8482a-137">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8482a-138">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8482a-138">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8482a-139">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="8482a-139">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8482a-140">El almacén de controladores suele ser% WINDIR% \\ inf o% WINDIR% \\ system32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="8482a-140">The driver store is typically either %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="8482a-141">Solo se puede cargar un paquete a la vez.</span><span class="sxs-lookup"><span data-stu-id="8482a-141">Only one package at a time can be uploaded.</span></span> <span data-ttu-id="8482a-142">Si un paquete depende de otros, debe cargarse por separado.</span><span class="sxs-lookup"><span data-stu-id="8482a-142">If a package is dependent on others, they must be uploaded separately.</span></span>

<span data-ttu-id="8482a-143">Solo se pueden cargar paquetes de controladores firmados.</span><span class="sxs-lookup"><span data-stu-id="8482a-143">Only signed driver packages can be uploaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="8482a-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8482a-144">Requirements</span></span>



| <span data-ttu-id="8482a-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="8482a-145">Requirement</span></span> | <span data-ttu-id="8482a-146">Value</span><span class="sxs-lookup"><span data-stu-id="8482a-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8482a-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8482a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="8482a-148">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8482a-148">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8482a-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8482a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="8482a-150">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8482a-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8482a-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8482a-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="8482a-152"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8482a-152"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8482a-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8482a-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="8482a-154"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8482a-154"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8482a-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8482a-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8482a-156"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8482a-156"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="8482a-157">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="8482a-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8482a-158">**UploadPrinterDriverPackageW** (Unicode) y **UploadPrinterDriverPackageA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8482a-158">**UploadPrinterDriverPackageW** (Unicode) and **UploadPrinterDriverPackageA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="8482a-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="8482a-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8482a-160">Impresión</span><span class="sxs-lookup"><span data-stu-id="8482a-160">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8482a-161">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="8482a-161">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

