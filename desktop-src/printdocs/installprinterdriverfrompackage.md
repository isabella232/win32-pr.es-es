---
description: Instala un controlador de impresora desde un paquete de controladores que se encuentra en el almacén de controladores del servidor de impresión.
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: Función InstallPrinterDriverFromPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallPrinterDriverFromPackage
- InstallPrinterDriverFromPackageA
- InstallPrinterDriverFromPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f817f5e73537f6a71d8236ad9532acdf02a53552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279026"
---
# <a name="installprinterdriverfrompackage-function"></a><span data-ttu-id="930c6-103">InstallPrinterDriverFromPackage función)</span><span class="sxs-lookup"><span data-stu-id="930c6-103">InstallPrinterDriverFromPackage function</span></span>

<span data-ttu-id="930c6-104">Instala un controlador de impresora desde un paquete de controladores que se encuentra en el almacén de controladores del servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="930c6-104">Installs a printer driver from a driver package that is in the print server's driver store.</span></span>

## <a name="syntax"></a><span data-ttu-id="930c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="930c6-105">Syntax</span></span>


```C++
HRESULT InstallPrinterDriverFromPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszDriverName,
  _In_ LPCTSTR pszEnvironment,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="930c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="930c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="930c6-107">*pszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="930c6-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930c6-108">Puntero a una cadena constante terminada en null que especifica el nombre del servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="930c6-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="930c6-109">**Null** significa el equipo local.</span><span class="sxs-lookup"><span data-stu-id="930c6-109">**NULL** means the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="930c6-110">*pszInfPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="930c6-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930c6-111">Puntero a una cadena constante terminada en null que especifica la ruta de acceso del almacén de controladores al archivo. inf del controlador de impresión.</span><span class="sxs-lookup"><span data-stu-id="930c6-111">A pointer to a constant, null-terminated string that specifies the driver store path to the print driver's .inf file.</span></span> <span data-ttu-id="930c6-112">**Null** significa que el controlador está en un archivo INF que se incluye con Windows.</span><span class="sxs-lookup"><span data-stu-id="930c6-112">**NULL** means the driver is in an inf file that shipped with Windows.</span></span>

</dd> <dt>

<span data-ttu-id="930c6-113">*pszDriverName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="930c6-113">*pszDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930c6-114">Puntero a una cadena constante terminada en null que especifica el nombre del controlador.</span><span class="sxs-lookup"><span data-stu-id="930c6-114">A pointer to a constant, null-terminated string that specifies the name of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="930c6-115">*pszEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="930c6-115">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930c6-116">Puntero a una cadena constante terminada en null que especifica la arquitectura del procesador (por ejemplo, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="930c6-116">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="930c6-117">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="930c6-117">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="930c6-118">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="930c6-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930c6-119">Solo puede ser 0 o IPDFP \_ copiar \_ todos los \_ archivos.</span><span class="sxs-lookup"><span data-stu-id="930c6-119">This can only be 0 or IPDFP\_COPY\_ALL\_FILES.</span></span> <span data-ttu-id="930c6-120">Un valor de 0 significa que el controlador de impresora debe agregarse y se deben copiar todos los archivos del directorio de controladores de impresora que sean más recientes que los archivos correspondientes actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="930c6-120">A value of 0 means that the printer driver must be added and any files in the printer driver directory that are newer than corresponding files currently in use must be copied.</span></span> <span data-ttu-id="930c6-121">Un valor de IPDFP \_ copiar \_ todos \_ los archivos significa que se debe agregar el controlador de impresora y todos los archivos del directorio de controladores de impresora.</span><span class="sxs-lookup"><span data-stu-id="930c6-121">A value of IPDFP\_COPY\_ALL\_FILES means the printer driver and all the files in the printer driver directory must be added.</span></span> <span data-ttu-id="930c6-122">Las marcas de tiempo de archivo se omiten cuando *dwFlags* tiene un valor de IPDFP \_ copiar \_ todos \_ los archivos.</span><span class="sxs-lookup"><span data-stu-id="930c6-122">The file time stamps are ignored when *dwFlags* has a value of IPDFP\_COPY\_ALL\_FILES.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="930c6-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="930c6-123">Return value</span></span>

<span data-ttu-id="930c6-124">Si la operación se realiza correctamente, el valor devuelto es S \_ OK; de lo contrario, **HRESULT** contendrá un código de error.</span><span class="sxs-lookup"><span data-stu-id="930c6-124">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="930c6-125">Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="930c6-125">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="930c6-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="930c6-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="930c6-127">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="930c6-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="930c6-128">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="930c6-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="930c6-129">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="930c6-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="930c6-130">El almacén de controladores suele ser% WINDIR% \\ inf o% WINDIR% \\ system32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="930c6-130">The driver store is typically either %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="930c6-131">**InstallPrinterDriverFromPackage** también instala otros archivos en el paquete, como perfiles de color y procesadores de impresión.</span><span class="sxs-lookup"><span data-stu-id="930c6-131">**InstallPrinterDriverFromPackage** also installs other files in the package, such as color profiles and print processors.</span></span>

<span data-ttu-id="930c6-132">Los usuarios deben tener derechos de administración de impresoras para instalar en un equipo remoto o en el equipo local cuando el usuario inicia sesión con Terminal Services.</span><span class="sxs-lookup"><span data-stu-id="930c6-132">Users must have printer administration rights to install either on a remote computer or on the local computer when the user is logged in with Terminal Services.</span></span>

<span data-ttu-id="930c6-133">Solo los paquetes firmados se pueden instalar en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="930c6-133">Only signed packages can be installed on a remote computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="930c6-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="930c6-134">Requirements</span></span>



| <span data-ttu-id="930c6-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="930c6-135">Requirement</span></span> | <span data-ttu-id="930c6-136">Value</span><span class="sxs-lookup"><span data-stu-id="930c6-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="930c6-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="930c6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="930c6-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="930c6-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="930c6-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="930c6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="930c6-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="930c6-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="930c6-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="930c6-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="930c6-142"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="930c6-142"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="930c6-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="930c6-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="930c6-144"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="930c6-144"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="930c6-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="930c6-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="930c6-146"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="930c6-146"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="930c6-147">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="930c6-147">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="930c6-148">**InstallPrinterDriverFromPackageW** (Unicode) y **InstallPrinterDriverFromPackageA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="930c6-148">**InstallPrinterDriverFromPackageW** (Unicode) and **InstallPrinterDriverFromPackageA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="930c6-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="930c6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="930c6-150">Impresión</span><span class="sxs-lookup"><span data-stu-id="930c6-150">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="930c6-151">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="930c6-151">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

