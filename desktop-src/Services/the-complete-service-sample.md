---
description: 'Más información sobre: el ejemplo de servicio completo'
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: El ejemplo de servicio completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb87ebfef3f964eacee66be94a4b5291c335d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668183"
---
# <a name="the-complete-service-sample"></a><span data-ttu-id="86fc6-103">El ejemplo de servicio completo</span><span class="sxs-lookup"><span data-stu-id="86fc6-103">The Complete Service Sample</span></span>

<span data-ttu-id="86fc6-104">Los temas de esta sección forman un ejemplo de servicio completo:</span><span class="sxs-lookup"><span data-stu-id="86fc6-104">The topics in this section form a complete service sample:</span></span>

-   <span data-ttu-id="86fc6-105">[Sample.MC](sample-mc.md) (contiene mensajes de error)</span><span class="sxs-lookup"><span data-stu-id="86fc6-105">[Sample.mc](sample-mc.md) (contains error messages)</span></span>
-   <span data-ttu-id="86fc6-106">[SVC. cpp](svc-cpp.md) (contiene el código de servicio)</span><span class="sxs-lookup"><span data-stu-id="86fc6-106">[Svc.cpp](svc-cpp.md) (contains the service code)</span></span>
-   <span data-ttu-id="86fc6-107">[SvcConfig. cpp](svcconfig-cpp.md) (contiene código de configuración de servicio)</span><span class="sxs-lookup"><span data-stu-id="86fc6-107">[SvcConfig.cpp](svcconfig-cpp.md) (contains service configuration code)</span></span>
-   <span data-ttu-id="86fc6-108">[SvcControl. cpp](svccontrol-cpp.md) (contiene el código de control de servicio)</span><span class="sxs-lookup"><span data-stu-id="86fc6-108">[SvcControl.cpp](svccontrol-cpp.md) (contains service control code)</span></span>

## <a name="building-the-service"></a><span data-ttu-id="86fc6-109">Compilar el servicio</span><span class="sxs-lookup"><span data-stu-id="86fc6-109">Building the Service</span></span>

<span data-ttu-id="86fc6-110">En el procedimiento siguiente se describe cómo crear el servicio y registrar el archivo DLL del mensaje de evento.</span><span class="sxs-lookup"><span data-stu-id="86fc6-110">The following procedure describes how to build the service and register the event message DLL.</span></span>

<span data-ttu-id="86fc6-111">**Para generar el servicio y registrar el archivo DLL del mensaje de evento**</span><span class="sxs-lookup"><span data-stu-id="86fc6-111">**To build the service and register the event message DLL**</span></span>

1.  <span data-ttu-id="86fc6-112">Cree el archivo DLL de mensajes desde Sample.mc mediante los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="86fc6-112">Build the message DLL from Sample.mc using the following steps:</span></span>
    1.  <span data-ttu-id="86fc6-113">**MC-U sample.mc**</span><span class="sxs-lookup"><span data-stu-id="86fc6-113">**mc -U sample.mc**</span></span>
    2.  <span data-ttu-id="86fc6-114">**RC-r sample. RC**</span><span class="sxs-lookup"><span data-stu-id="86fc6-114">**rc -r sample.rc**</span></span>
    3.  <span data-ttu-id="86fc6-115">**Link-dll-NOENTRY -out:sample.dll sample. res**</span><span class="sxs-lookup"><span data-stu-id="86fc6-115">**link -dll -noentry -out:sample.dll sample.res**</span></span>
2.  <span data-ttu-id="86fc6-116">Cree Svc.exe, SvcConfig.exe y SvcControl.exe de SVC. cpp, SvcConfig. cpp y SvcControl. cpp, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="86fc6-116">Build Svc.exe, SvcConfig.exe, and SvcControl.exe from Svc.cpp, SvcConfig.cpp, and SvcControl.cpp, respectively.</span></span>
3.  <span data-ttu-id="86fc6-117">Cree la clave del registro **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ EventLog \\ Application \\ SvcName** y agregue los siguientes valores del registro a esta clave.</span><span class="sxs-lookup"><span data-stu-id="86fc6-117">Create the registry key **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\EventLog\\Application\\SvcName** and add the following registry values to this key.</span></span>

    | <span data-ttu-id="86fc6-118">Value</span><span class="sxs-lookup"><span data-stu-id="86fc6-118">Value</span></span>                              | <span data-ttu-id="86fc6-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="86fc6-119">Type</span></span>       | <span data-ttu-id="86fc6-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="86fc6-120">Description</span></span>                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="86fc6-121">**EventMessageFile**  =  *\_ ruta de acceso de dll*</span><span class="sxs-lookup"><span data-stu-id="86fc6-121">**EventMessageFile** = *dll\_path*</span></span> | <span data-ttu-id="86fc6-122">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="86fc6-122">REG\_SZ</span></span>    | <span data-ttu-id="86fc6-123">La ruta de acceso al archivo DLL de solo recurso que contiene cadenas que el servicio puede escribir en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="86fc6-123">The path to the resource-only DLL that contains strings that the service can write to the event log.</span></span>               |
    | <span data-ttu-id="86fc6-124">**TypesSupported** = 0x00000007</span><span class="sxs-lookup"><span data-stu-id="86fc6-124">**TypesSupported** = 0x00000007</span></span>    | <span data-ttu-id="86fc6-125">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="86fc6-125">REG\_DWORD</span></span> | <span data-ttu-id="86fc6-126">Máscara de bits que especifica los tipos de evento admitidos.</span><span class="sxs-lookup"><span data-stu-id="86fc6-126">A bit mask that specifies the supported event types.</span></span> <span data-ttu-id="86fc6-127">El valor 0x000000007 indica que se admiten todos los tipos.</span><span class="sxs-lookup"><span data-stu-id="86fc6-127">The value 0x000000007 indicates that all types are supported.</span></span> |

    

     

## <a name="testing-the-service"></a><span data-ttu-id="86fc6-128">Probar el servicio</span><span class="sxs-lookup"><span data-stu-id="86fc6-128">Testing the Service</span></span>

<span data-ttu-id="86fc6-129">En el procedimiento siguiente se describe cómo probar el servicio.</span><span class="sxs-lookup"><span data-stu-id="86fc6-129">The following procedure describes how to test the service.</span></span>

<span data-ttu-id="86fc6-130">**Para probar el servicio**</span><span class="sxs-lookup"><span data-stu-id="86fc6-130">**To test the service**</span></span>

1.  <span data-ttu-id="86fc6-131">En el panel de control, inicie la aplicación **servicios** .</span><span class="sxs-lookup"><span data-stu-id="86fc6-131">In Control Panel, start the **Services** application.</span></span> <span data-ttu-id="86fc6-132">(En los pasos siguientes, use la tecla F5 para actualizar la pantalla después de ejecutar un comando que modifique la información en la aplicación **servicios** ).</span><span class="sxs-lookup"><span data-stu-id="86fc6-132">(In the following steps, use the F5 key to refresh the display after executing a command that modifies the information in the **Services** application.)</span></span>
2.  <span data-ttu-id="86fc6-133">Ejecute el siguiente comando para instalar el servicio:</span><span class="sxs-lookup"><span data-stu-id="86fc6-133">Run the following command to install the service:</span></span>

    <span data-ttu-id="86fc6-134">**instalación de SVC**</span><span class="sxs-lookup"><span data-stu-id="86fc6-134">**svc install**</span></span>

    <span data-ttu-id="86fc6-135">El servicio escribe "el servicio se instaló correctamente" en la consola si la operación se realiza correctamente, o bien un mensaje de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="86fc6-135">The service writes "Service installed successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="86fc6-136">Si la instalación del servicio se realiza correctamente, el servicio se muestra en la aplicación **servicios** .</span><span class="sxs-lookup"><span data-stu-id="86fc6-136">If the service installation succeeds, the service is displayed in the **Services** application.</span></span> <span data-ttu-id="86fc6-137">Tenga en cuenta que name se establece en "SvcName", la **Descripción** y el **Estado** están en blanco y **el** **tipo de inicio** se establece en "manual".</span><span class="sxs-lookup"><span data-stu-id="86fc6-137">Note that **Name** is set to "SvcName", **Description** and **Status** are blank, and **Startup Type** is set to "Manual".</span></span>

3.  <span data-ttu-id="86fc6-138">Ejecute el siguiente comando para iniciar el servicio:</span><span class="sxs-lookup"><span data-stu-id="86fc6-138">Run the following command to start the service:</span></span>

    <span data-ttu-id="86fc6-139">**svccontrol Start SvcName**</span><span class="sxs-lookup"><span data-stu-id="86fc6-139">**svccontrol start SvcName**</span></span>

    <span data-ttu-id="86fc6-140">Si la operación se realiza correctamente, el programa de control de servicio escribe "el inicio del servicio está pendiente..." y, a continuación, "el servicio se inició correctamente" en la consola.</span><span class="sxs-lookup"><span data-stu-id="86fc6-140">If the operation succeeds, the service control program writes "Service start pending..." and then "Service started successfully" to the console.</span></span> <span data-ttu-id="86fc6-141">De lo contrario, el programa escribe un mensaje de error en la consola.</span><span class="sxs-lookup"><span data-stu-id="86fc6-141">Otherwise, the program writes an error message to the console.</span></span>

    <span data-ttu-id="86fc6-142">Si el servicio se inicia correctamente, el **Estado** se establece en "iniciado".</span><span class="sxs-lookup"><span data-stu-id="86fc6-142">If the service starts successfully, **Status** is set to "Started".</span></span> <span data-ttu-id="86fc6-143">El código de la función [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) lo ejecuta el SCM.</span><span class="sxs-lookup"><span data-stu-id="86fc6-143">The code in the [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function is executed by the SCM.</span></span> <span data-ttu-id="86fc6-144">Si se produce un error, el servicio escribirá un mensaje de error en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="86fc6-144">If an error occurs, the service will write an error message to the event log.</span></span> <span data-ttu-id="86fc6-145">Este mensaje incluye el nombre de la función que produjo un error y el código de error que se devolvió en caso de error.</span><span class="sxs-lookup"><span data-stu-id="86fc6-145">This message includes the name of the function that failed and the error code that was returned on failure.</span></span>

4.  <span data-ttu-id="86fc6-146">Ejecute el siguiente comando para actualizar la descripción del servicio:</span><span class="sxs-lookup"><span data-stu-id="86fc6-146">Run the following command to update the service description:</span></span>

    <span data-ttu-id="86fc6-147">**svcconfig describir SvcName**</span><span class="sxs-lookup"><span data-stu-id="86fc6-147">**svcconfig describe SvcName**</span></span>

    <span data-ttu-id="86fc6-148">El programa de configuración de servicio escribe "Descripción del servicio actualizada correctamente" en la consola si la operación se realiza correctamente, o bien un mensaje de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="86fc6-148">The service configuration program writes "Service description updated successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="86fc6-149">Si la actualización se realiza correctamente, la **Descripción** se establece en "esta es una descripción de la prueba".</span><span class="sxs-lookup"><span data-stu-id="86fc6-149">If the update succeeds, **Description** is set to "This is a test description".</span></span>

5.  <span data-ttu-id="86fc6-150">Ejecute el siguiente comando para consultar la configuración del servicio:</span><span class="sxs-lookup"><span data-stu-id="86fc6-150">Run the following command to query the service configuration:</span></span>

    <span data-ttu-id="86fc6-151">**SvcName consulta svcconfig**</span><span class="sxs-lookup"><span data-stu-id="86fc6-151">**svcconfig query SvcName**</span></span>

    <span data-ttu-id="86fc6-152">El programa de configuración del servicio escribe la información de configuración del servicio en la consola si la operación se realiza correctamente, o bien un mensaje de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="86fc6-152">The service configuration program writes the service configuration information to the console if the operation succeeds or an error message otherwise.</span></span>

6.  <span data-ttu-id="86fc6-153">Ejecute el siguiente comando para cambiar la DACL de servicio:</span><span class="sxs-lookup"><span data-stu-id="86fc6-153">Run the following command to change the service DACL:</span></span>

    <span data-ttu-id="86fc6-154">**svccontrol DACL SvcName**</span><span class="sxs-lookup"><span data-stu-id="86fc6-154">**svccontrol dacl SvcName**</span></span>

    <span data-ttu-id="86fc6-155">El programa de configuración del servicio escribe "DACL del servicio se actualizó correctamente" en la consola si la operación se realiza correctamente, o bien un mensaje de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="86fc6-155">The service configuration program writes "Service DACL updated successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

7.  <span data-ttu-id="86fc6-156">Ejecute el siguiente comando para deshabilitar el servicio:</span><span class="sxs-lookup"><span data-stu-id="86fc6-156">Run the following command to disable the service:</span></span>

    <span data-ttu-id="86fc6-157">**svcconfig deshabilitar SvcName**</span><span class="sxs-lookup"><span data-stu-id="86fc6-157">**svcconfig disable SvcName**</span></span>

    <span data-ttu-id="86fc6-158">El programa de configuración del servicio escribe "servicio deshabilitado correctamente" en la consola si la operación se realiza correctamente, o bien un mensaje de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="86fc6-158">The service configuration program writes "Service disabled successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="86fc6-159">Si el servicio se deshabilita correctamente, el **tipo de inicio** se establece en "deshabilitado".</span><span class="sxs-lookup"><span data-stu-id="86fc6-159">If the service is disabled successfully, **Startup Type** is set to "Disabled".</span></span>

8.  <span data-ttu-id="86fc6-160">Ejecute el siguiente comando para habilitar el servicio:</span><span class="sxs-lookup"><span data-stu-id="86fc6-160">Run the following command to enable the service:</span></span>

    <span data-ttu-id="86fc6-161">**svcconfig habilitar SvcName**</span><span class="sxs-lookup"><span data-stu-id="86fc6-161">**svcconfig enable SvcName**</span></span>

    <span data-ttu-id="86fc6-162">El programa de configuración del servicio escribe "servicio habilitado correctamente" en la consola si la operación se realiza correctamente, o bien un mensaje de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="86fc6-162">The service configuration program writes "Service enabled successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="86fc6-163">Si el servicio se habilita correctamente, el **tipo de inicio** se establece en "manual".</span><span class="sxs-lookup"><span data-stu-id="86fc6-163">If the service is enabled successfully, **Startup Type** is set to "Manual".</span></span>

9.  <span data-ttu-id="86fc6-164">Ejecute el siguiente comando para detener el servicio:</span><span class="sxs-lookup"><span data-stu-id="86fc6-164">Run the following command to stop the service:</span></span>

    <span data-ttu-id="86fc6-165">**svccontrol detener SvcName**</span><span class="sxs-lookup"><span data-stu-id="86fc6-165">**svccontrol stop SvcName**</span></span>

    <span data-ttu-id="86fc6-166">Si la operación se realiza correctamente, el programa de control de servicio escribe "servicio detenido pendiente..." y, a continuación, "el servicio se detuvo correctamente" en la consola.</span><span class="sxs-lookup"><span data-stu-id="86fc6-166">If the operation succeeds, the service control program writes "Service stop pending..." and then "Service stopped successfully" to the console.</span></span> <span data-ttu-id="86fc6-167">De lo contrario, el programa escribe un mensaje de error en la consola.</span><span class="sxs-lookup"><span data-stu-id="86fc6-167">Otherwise, the program writes an error message to the console.</span></span>

    <span data-ttu-id="86fc6-168">Si el servicio se detiene correctamente, el **Estado** es en blanco.</span><span class="sxs-lookup"><span data-stu-id="86fc6-168">If the service stops successfully, **Status** is blank.</span></span>

    <span data-ttu-id="86fc6-169">Si no se puede detener el servicio, el programa de control de servicio escribe un mensaje de error en el registro de eventos que incluye el nombre de la función en la que se produjo el error y el código de error devuelto en caso de error.</span><span class="sxs-lookup"><span data-stu-id="86fc6-169">If the service fails to stop, the service control program writes an error message to the event log that includes the name of the function that failed and the error code that was returned on failure.</span></span>

10. <span data-ttu-id="86fc6-170">Ejecute el siguiente comando para eliminar el servicio:</span><span class="sxs-lookup"><span data-stu-id="86fc6-170">Run the following command to delete the service:</span></span>

    <span data-ttu-id="86fc6-171">**svcconfig eliminar SvcName**</span><span class="sxs-lookup"><span data-stu-id="86fc6-171">**svcconfig delete SvcName**</span></span>

    <span data-ttu-id="86fc6-172">El programa de configuración de servicio escribe "el servicio se eliminó correctamente" en la consola si la operación se realiza correctamente, o bien un mensaje de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="86fc6-172">The service configuration program writes "Service deleted successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="86fc6-173">Si el servicio se elimina correctamente, ya no se muestra en la aplicación **servicios** .</span><span class="sxs-lookup"><span data-stu-id="86fc6-173">If the service is deleted successfully, it is no longer displayed in the **Services** application.</span></span> <span data-ttu-id="86fc6-174">(Tenga en cuenta que si intenta eliminar un servicio que no está detenido, la operación se realiza correctamente, pero el **tipo de inicio** se establece en "deshabilitado" y la entrada del servicio se eliminará al reiniciar el sistema o cuando el servicio finalice con el administrador de tareas.)</span><span class="sxs-lookup"><span data-stu-id="86fc6-174">(Note that if you attempt to delete a service that is not stopped, the operation succeeds but **Startup Type** is set to "Disabled" and the service entry will be deleted at system restart or when the service is terminated using Task Manager.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="86fc6-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86fc6-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86fc6-176">Uso de servicios</span><span class="sxs-lookup"><span data-stu-id="86fc6-176">Using Services</span></span>](using-services.md)
</dt> </dl>

 

 
