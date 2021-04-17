---
description: La propiedad MsiLogging establece el modo de registro predeterminado para el paquete de Windows Installer.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: Propiedad MsiLogging
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e53df57723157f7184a904e512aac9035a9f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681044"
---
# <a name="msilogging-property"></a><span data-ttu-id="81e14-103">Propiedad MsiLogging</span><span class="sxs-lookup"><span data-stu-id="81e14-103">MsiLogging property</span></span>

<span data-ttu-id="81e14-104">La propiedad **MsiLogging** establece el modo de registro predeterminado para el paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="81e14-104">The **MsiLogging** property sets the default logging mode for the Windows Installer package.</span></span> <span data-ttu-id="81e14-105">Si esta propiedad opcional está presente en la [tabla de propiedades](property-table.md), el instalador genera un archivo de registro denominado MSI \* . Inicia.</span><span class="sxs-lookup"><span data-stu-id="81e14-105">If this optional property is present in the [Property table](property-table.md), the installer generates a log file named MSI\*.LOG.</span></span> <span data-ttu-id="81e14-106">La ruta de acceso completa al archivo de registro se proporciona mediante el valor de la propiedad [**MsiLogFileLocation**](msilogfilelocation.md) .</span><span class="sxs-lookup"><span data-stu-id="81e14-106">The full path to the log file is given by the value of the [**MsiLogFileLocation**](msilogfilelocation.md) property.</span></span>

## <a name="value"></a><span data-ttu-id="81e14-107">Value</span><span class="sxs-lookup"><span data-stu-id="81e14-107">Value</span></span>

<span data-ttu-id="81e14-108">El valor de esta propiedad debe ser una cadena de los siguientes caracteres que especifican el modo de registro predeterminado.</span><span class="sxs-lookup"><span data-stu-id="81e14-108">The value of this property should be a string of the following characters that specify the default logging mode.</span></span>



| <span data-ttu-id="81e14-109">Value</span><span class="sxs-lookup"><span data-stu-id="81e14-109">Value</span></span>                                                                        | <span data-ttu-id="81e14-110">Significado</span><span class="sxs-lookup"><span data-stu-id="81e14-110">Meaning</span></span>                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81e14-111"><dt>I</dt></span><span class="sxs-lookup"><span data-stu-id="81e14-111"><dt>I</dt></span></span> </dl> | <span data-ttu-id="81e14-112">Mensajes de estado.</span><span class="sxs-lookup"><span data-stu-id="81e14-112">Status messages.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="81e14-113"><dt>w</dt></span><span class="sxs-lookup"><span data-stu-id="81e14-113"><dt>w</dt></span></span> </dl> | <span data-ttu-id="81e14-114">Advertencias no graves.</span><span class="sxs-lookup"><span data-stu-id="81e14-114">Nonfatal warnings.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="81e14-115"><dt>e</dt></span><span class="sxs-lookup"><span data-stu-id="81e14-115"><dt>e</dt></span></span> </dl> | <span data-ttu-id="81e14-116">Todos los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="81e14-116">All error messages.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="81e14-117"><dt>un</dt></span><span class="sxs-lookup"><span data-stu-id="81e14-117"><dt>a</dt></span></span> </dl> | <span data-ttu-id="81e14-118">Inicio de acciones.</span><span class="sxs-lookup"><span data-stu-id="81e14-118">Start up of actions.</span></span><br/>                                                |
| <dl> <span data-ttu-id="81e14-119"><dt>r</dt></span><span class="sxs-lookup"><span data-stu-id="81e14-119"><dt>r</dt></span></span> </dl> | <span data-ttu-id="81e14-120">Registros específicos de la acción.</span><span class="sxs-lookup"><span data-stu-id="81e14-120">Action-specific records.</span></span><br/>                                            |
| <dl> <span data-ttu-id="81e14-121"><dt>u</dt></span><span class="sxs-lookup"><span data-stu-id="81e14-121"><dt>u</dt></span></span> </dl> | <span data-ttu-id="81e14-122">Solicitudes de usuario.</span><span class="sxs-lookup"><span data-stu-id="81e14-122">User requests.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="81e14-123"><dt>c</dt></span><span class="sxs-lookup"><span data-stu-id="81e14-123"><dt>c</dt></span></span> </dl> | <span data-ttu-id="81e14-124">Parámetros iniciales de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="81e14-124">Initial UI parameters.</span></span><br/>                                              |
| <dl> <span data-ttu-id="81e14-125"><dt>m</dt></span><span class="sxs-lookup"><span data-stu-id="81e14-125"><dt>m</dt></span></span> </dl> | <span data-ttu-id="81e14-126">Memoria insuficiente o información de salida irrecuperable.</span><span class="sxs-lookup"><span data-stu-id="81e14-126">Out-of-memory or fatal exit information.</span></span><br/>                            |
| <dl> <span data-ttu-id="81e14-127"><dt>o</dt></span><span class="sxs-lookup"><span data-stu-id="81e14-127"><dt>o</dt></span></span> </dl> | <span data-ttu-id="81e14-128">Mensajes de espacio insuficiente en disco.</span><span class="sxs-lookup"><span data-stu-id="81e14-128">Out-of-disk-space messages.</span></span><br/>                                         |
| <dl> <span data-ttu-id="81e14-129"><dt>m</dt></span><span class="sxs-lookup"><span data-stu-id="81e14-129"><dt>p</dt></span></span> </dl> | <span data-ttu-id="81e14-130">Propiedades de terminal.</span><span class="sxs-lookup"><span data-stu-id="81e14-130">Terminal properties.</span></span><br/>                                                |
| <dl> <span data-ttu-id="81e14-131"><dt>v</dt></span><span class="sxs-lookup"><span data-stu-id="81e14-131"><dt>v</dt></span></span> </dl> | <span data-ttu-id="81e14-132">Salida detallada.</span><span class="sxs-lookup"><span data-stu-id="81e14-132">Verbose output.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="81e14-133"><dt>x</dt></span><span class="sxs-lookup"><span data-stu-id="81e14-133"><dt>x</dt></span></span> </dl> | <span data-ttu-id="81e14-134">Información de depuración adicional.</span><span class="sxs-lookup"><span data-stu-id="81e14-134">Extra debugging information.</span></span> <span data-ttu-id="81e14-135">Solo disponible en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="81e14-135">Only available on Windows Server 2003.</span></span><br/> |
| <dl> <span data-ttu-id="81e14-136"><dt>!</dt></span><span class="sxs-lookup"><span data-stu-id="81e14-136"><dt>!</dt></span></span> </dl> | <span data-ttu-id="81e14-137">Vacíe cada línea en el registro.</span><span class="sxs-lookup"><span data-stu-id="81e14-137">Flush each line to the log.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="81e14-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81e14-138">Remarks</span></span>

<span data-ttu-id="81e14-139">Esta propiedad está disponible a partir de Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="81e14-139">This property is available starting with Windows Installer 4.0.</span></span>

<span data-ttu-id="81e14-140">No se pueden usar los valores "+" y " \* " de la opción/l en el valor de la propiedad **MsiLogging** .</span><span class="sxs-lookup"><span data-stu-id="81e14-140">You cannot use the "+" and "\*" values of the /L option in the value of the **MsiLogging** property.</span></span>

<span data-ttu-id="81e14-141">El modo de registro se puede establecer mediante una directiva, una opción de línea de comandos o mediante programación.</span><span class="sxs-lookup"><span data-stu-id="81e14-141">The logging mode can be set using policy, a command-line option, or programmatically.</span></span> <span data-ttu-id="81e14-142">Esto invalida el modo de registro predeterminado.</span><span class="sxs-lookup"><span data-stu-id="81e14-142">This overrides the default logging mode.</span></span> <span data-ttu-id="81e14-143">Para obtener más información acerca de todos los métodos que están disponibles para establecer el modo de registro, consulte el [registro normal](normal-logging.md) en la sección [registro de Windows Installer](windows-installer-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="81e14-143">For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.</span></span>

<span data-ttu-id="81e14-144">Si la propiedad **MsiLogging** está presente en la [tabla de propiedades](property-table.md), el modo de registro predeterminado del paquete se puede modificar cambiando el valor de esta propiedad mediante una [transformación de base de datos](database-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="81e14-144">If the **MsiLogging** property is present in the [Property table](property-table.md), the default logging mode of the package can be modified by changing the value of this property using a [database transform](database-transforms.md).</span></span> <span data-ttu-id="81e14-145">El modo de registro predeterminado no se puede cambiar mediante un [paquete de revisión](patch-packages.md) (un archivo. msp).</span><span class="sxs-lookup"><span data-stu-id="81e14-145">The default logging mode cannot be changed using a [Patch Package](patch-packages.md) (a .msp file.)</span></span>

<span data-ttu-id="81e14-146">Si se ha establecido la propiedad **MsiLogging** en la [tabla de propiedades](property-table.md), se puede especificar el modo de registro predeterminado para todos los usuarios del equipo mediante el establecimiento de la Directiva de [DisableLoggingFromPackage](disableloggingfrompackage.md) y la Directiva de [registro](logging.md) .</span><span class="sxs-lookup"><span data-stu-id="81e14-146">If the **MsiLogging** property has been set in the [Property table](property-table.md), the default logging mode for all users of the computer can be specified by setting both the [DisableLoggingFromPackage](disableloggingfrompackage.md) policy and [Logging](logging.md) policy.</span></span> <span data-ttu-id="81e14-147">El establecimiento de la Directiva DisableLoggingFromPackage y de la Directiva de registro reemplazará la propiedad **MsiLogging** de todos los paquetes.</span><span class="sxs-lookup"><span data-stu-id="81e14-147">Setting both the DisableLoggingFromPackage policy and Logging policy will override the **MsiLogging** property for all packages.</span></span>

## <a name="requirements"></a><span data-ttu-id="81e14-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81e14-148">Requirements</span></span>



| <span data-ttu-id="81e14-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="81e14-149">Requirement</span></span> | <span data-ttu-id="81e14-150">Value</span><span class="sxs-lookup"><span data-stu-id="81e14-150">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81e14-151">Versión</span><span class="sxs-lookup"><span data-stu-id="81e14-151">Version</span></span><br/> | <span data-ttu-id="81e14-152">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="81e14-152">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="81e14-153">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="81e14-153">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="81e14-154">Windows Installer 4,5 en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="81e14-154">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="81e14-155">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="81e14-155">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="81e14-156">Consulte también</span><span class="sxs-lookup"><span data-stu-id="81e14-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81e14-157">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81e14-157">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="81e14-158">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="81e14-158">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




