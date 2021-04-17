---
description: El método EnableLog del objeto de instalador habilita el registro del tipo de mensaje seleccionado para todas las sesiones de instalación posteriores en el espacio de proceso actual.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Instalador. EnableLog (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.EnableLog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 573b56dda0479f58595b0849f6443fd8a2e67e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653355"
---
# <a name="installerenablelog-method"></a><span data-ttu-id="61502-103">Instalador. EnableLog (método)</span><span class="sxs-lookup"><span data-stu-id="61502-103">Installer.EnableLog method</span></span>

<span data-ttu-id="61502-104">El método **EnableLog** del objeto de [**instalador**](installer-object.md) habilita el registro del tipo de mensaje seleccionado para todas las sesiones de instalación posteriores en el espacio de proceso actual.</span><span class="sxs-lookup"><span data-stu-id="61502-104">The **EnableLog** method of the [**Installer**](installer-object.md) object enables logging of the selected message type for all subsequent installation sessions in the current process space.</span></span>

## <a name="syntax"></a><span data-ttu-id="61502-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61502-105">Syntax</span></span>


```JScript
Installer.EnableLog(
  logMode,
  logFile
)
```



## <a name="parameters"></a><span data-ttu-id="61502-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61502-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61502-107">*logMode*</span><span class="sxs-lookup"><span data-stu-id="61502-107">*logMode*</span></span> 
</dt> <dd>

<span data-ttu-id="61502-108">Cadena requerida que contiene letras que representan los tipos de mensaje que se van a registrar.</span><span class="sxs-lookup"><span data-stu-id="61502-108">A required string that contains letters representing the message types to log.</span></span> <span data-ttu-id="61502-109">La cadena puede ser una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="61502-109">The string can be a combination of the following values.</span></span>



| <span data-ttu-id="61502-110">Value</span><span class="sxs-lookup"><span data-stu-id="61502-110">Value</span></span> | <span data-ttu-id="61502-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="61502-111">Description</span></span>                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61502-112">I</span><span class="sxs-lookup"><span data-stu-id="61502-112">I</span></span>     | <span data-ttu-id="61502-113">Mensajes de solo información.</span><span class="sxs-lookup"><span data-stu-id="61502-113">Information-only messages.</span></span>                                                                             |
| <span data-ttu-id="61502-114">w</span><span class="sxs-lookup"><span data-stu-id="61502-114">w</span></span>     | <span data-ttu-id="61502-115">Mensajes de advertencia no graves.</span><span class="sxs-lookup"><span data-stu-id="61502-115">Non-fatal warning messages.</span></span>                                                                            |
| <span data-ttu-id="61502-116">h</span><span class="sxs-lookup"><span data-stu-id="61502-116">e</span></span>     | <span data-ttu-id="61502-117">Mensajes de error que pueden ser errores irrecuperables.</span><span class="sxs-lookup"><span data-stu-id="61502-117">Error messages that may be fatal errors.</span></span>                                                               |
| <span data-ttu-id="61502-118">f</span><span class="sxs-lookup"><span data-stu-id="61502-118">f</span></span>     | <span data-ttu-id="61502-119">Lista de archivos en uso que se deben reemplazar.</span><span class="sxs-lookup"><span data-stu-id="61502-119">List of files in use that need to be replaced.</span></span>                                                         |
| <span data-ttu-id="61502-120">a</span><span class="sxs-lookup"><span data-stu-id="61502-120">a</span></span>     | <span data-ttu-id="61502-121">Inicio de la notificación de acción.</span><span class="sxs-lookup"><span data-stu-id="61502-121">Start of action notification.</span></span>                                                                          |
| <span data-ttu-id="61502-122">r</span><span class="sxs-lookup"><span data-stu-id="61502-122">r</span></span>     | <span data-ttu-id="61502-123">Registro de datos de acción que contiene contenido específico de la acción.</span><span class="sxs-lookup"><span data-stu-id="61502-123">Action data record containing content specific to action.</span></span>                                              |
| <span data-ttu-id="61502-124">u</span><span class="sxs-lookup"><span data-stu-id="61502-124">u</span></span>     | <span data-ttu-id="61502-125">Mensajes de solicitud de usuario.</span><span class="sxs-lookup"><span data-stu-id="61502-125">User request messages.</span></span>                                                                                 |
| <span data-ttu-id="61502-126">c</span><span class="sxs-lookup"><span data-stu-id="61502-126">c</span></span>     | <span data-ttu-id="61502-127">Parámetros de inicialización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="61502-127">UI initialization parameters.</span></span>                                                                          |
| <span data-ttu-id="61502-128">m</span><span class="sxs-lookup"><span data-stu-id="61502-128">m</span></span>     | <span data-ttu-id="61502-129">Mensaje de memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="61502-129">Out-of-memory message.</span></span>                                                                                 |
| <span data-ttu-id="61502-130">v</span><span class="sxs-lookup"><span data-stu-id="61502-130">v</span></span>     | <span data-ttu-id="61502-131">Envía grandes cantidades de información al archivo de registro que no suele ser útil para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="61502-131">Sends large amounts of information to log file not generally useful to users.</span></span> <span data-ttu-id="61502-132">Se puede usar para la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="61502-132">May be used for support.</span></span> |
| <span data-ttu-id="61502-133">p</span><span class="sxs-lookup"><span data-stu-id="61502-133">p</span></span>     | <span data-ttu-id="61502-134">Tabla de propiedades dump; "propiedad = valor" al finalizar el motor</span><span class="sxs-lookup"><span data-stu-id="61502-134">Dump property table; "property = value" at engine termination</span></span>                                          |
| \+    | <span data-ttu-id="61502-135">Anexar al archivo de registro existente.</span><span class="sxs-lookup"><span data-stu-id="61502-135">Append to existing log file.</span></span>                                                                           |
| <span data-ttu-id="61502-136">!</span><span class="sxs-lookup"><span data-stu-id="61502-136">!</span></span>     | <span data-ttu-id="61502-137">Vacíe cada línea en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="61502-137">Flush each line to the log file.</span></span>                                                                       |
| <span data-ttu-id="61502-138">x</span><span class="sxs-lookup"><span data-stu-id="61502-138">x</span></span>     | <span data-ttu-id="61502-139">Información de depuración adicional.</span><span class="sxs-lookup"><span data-stu-id="61502-139">Extra debugging information.</span></span> <span data-ttu-id="61502-140">Esta opción solo está disponible en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="61502-140">This option only available with Windows Server 2003.</span></span>                      |
| <span data-ttu-id="61502-141">o</span><span class="sxs-lookup"><span data-stu-id="61502-141">o</span></span>     | <span data-ttu-id="61502-142">Mensajes de espacio insuficiente en disco.</span><span class="sxs-lookup"><span data-stu-id="61502-142">Out-of-disk-space messages.</span></span>                                                                            |



 

</dd> <dt>

<span data-ttu-id="61502-143">*MSDTC*</span><span class="sxs-lookup"><span data-stu-id="61502-143">*logFile*</span></span> 
</dt> <dd>

<span data-ttu-id="61502-144">Cadena requerida que contiene la ruta de acceso al archivo de registro que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="61502-144">Required string containing the path to the log file to be created.</span></span> <span data-ttu-id="61502-145">Use una cadena vacía ("") para desactivar el registro.</span><span class="sxs-lookup"><span data-stu-id="61502-145">Use an empty string ("") to turn off logging.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61502-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61502-146">Return value</span></span>

<span data-ttu-id="61502-147">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="61502-147">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61502-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61502-148">Remarks</span></span>

<span data-ttu-id="61502-149">La ruta de acceso a la ubicación del archivo de registro ya debe existir al utilizar este método.</span><span class="sxs-lookup"><span data-stu-id="61502-149">The path to the logfile location must already exist when using this method.</span></span> <span data-ttu-id="61502-150">El instalador no crea la estructura de directorios para el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="61502-150">The Installer does not create the directory structure for the logfile.</span></span>

<span data-ttu-id="61502-151">Las opciones de registro establecidas mediante **EnableLog** invalidan cualquier configuración existente de la Directiva de registro de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="61502-151">The logging options set using **EnableLog** override any existing Windows Installer logging policy settings.</span></span>

<span data-ttu-id="61502-152">De forma predeterminada, el registro sobrescribe un archivo de registro existente.</span><span class="sxs-lookup"><span data-stu-id="61502-152">Logging overwrites an existing log file by default.</span></span> <span data-ttu-id="61502-153">Debe usar la letra ' + ' en el modo de registro para anexar a un archivo de registro existente.</span><span class="sxs-lookup"><span data-stu-id="61502-153">You must use the '+' letter in the logging mode to append to an existing log file.</span></span>

<span data-ttu-id="61502-154">No se recomienda la opción '! ' porque puede ralentizar considerablemente la instalación.</span><span class="sxs-lookup"><span data-stu-id="61502-154">The '!' option is not recommended because it can significantly slow installation.</span></span> <span data-ttu-id="61502-155">Esta opción puede ser útil al depurar una instalación de.</span><span class="sxs-lookup"><span data-stu-id="61502-155">This option may be useful when debugging an installation.</span></span>

<span data-ttu-id="61502-156">El siguiente script de ejemplo activa el registro detallado para una instalación de.</span><span class="sxs-lookup"><span data-stu-id="61502-156">The following sample script turns on verbose logging for an installation.</span></span> <span data-ttu-id="61502-157">Al final de la instalación, el archivo de registro generado estará en c: \\ temp \\ install. log.</span><span class="sxs-lookup"><span data-stu-id="61502-157">At the end of the installation, the generated log file will be at c:\\temp\\install.log.</span></span>


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a><span data-ttu-id="61502-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61502-158">Requirements</span></span>



| <span data-ttu-id="61502-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="61502-159">Requirement</span></span> | <span data-ttu-id="61502-160">Value</span><span class="sxs-lookup"><span data-stu-id="61502-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61502-161">Versión</span><span class="sxs-lookup"><span data-stu-id="61502-161">Version</span></span><br/> | <span data-ttu-id="61502-162">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="61502-162">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="61502-163">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="61502-163">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="61502-164">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="61502-164">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="61502-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="61502-165">DLL</span></span><br/>     | <dl> <span data-ttu-id="61502-166"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61502-166"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="61502-167">IID</span><span class="sxs-lookup"><span data-stu-id="61502-167">IID</span></span><br/>     | <span data-ttu-id="61502-168">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="61502-168">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="61502-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="61502-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61502-170">Registro de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="61502-170">Windows Installer Logging</span></span>](windows-installer-logging.md)
</dt> </dl>

 

 




