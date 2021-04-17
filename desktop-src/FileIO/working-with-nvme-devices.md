---
description: Obtenga información sobre cómo trabajar con dispositivos de NVMe de alta velocidad desde la aplicación Windows.
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: Trabajar con unidades de NVMe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be94adf8355940bd93de137d122d91e468c2173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666818"
---
# <a name="working-with-nvme-drives"></a><span data-ttu-id="c8aae-103">Trabajar con unidades de NVMe</span><span class="sxs-lookup"><span data-stu-id="c8aae-103">Working with NVMe drives</span></span>

<span data-ttu-id="c8aae-104">**Se aplica a:**</span><span class="sxs-lookup"><span data-stu-id="c8aae-104">**Applies to:**</span></span>

-   <span data-ttu-id="c8aae-105">Windows 10</span><span class="sxs-lookup"><span data-stu-id="c8aae-105">Windows 10</span></span>
-   <span data-ttu-id="c8aae-106">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c8aae-106">Windows Server 2016</span></span>

<span data-ttu-id="c8aae-107">Obtenga información sobre cómo trabajar con dispositivos de NVMe de alta velocidad desde la aplicación Windows.</span><span class="sxs-lookup"><span data-stu-id="c8aae-107">Learn how to work with high-speed NVMe devices from your Windows application.</span></span> <span data-ttu-id="c8aae-108">El acceso al dispositivo se habilita a través de **StorNVMe.sys**, el controlador incluido por primera vez en Windows Server 2012 R2 y Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="c8aae-108">Device access is enabled via **StorNVMe.sys**, the in-box driver first introduced in Windows Server 2012 R2 and Windows 8.1.</span></span> <span data-ttu-id="c8aae-109">También está disponible para los dispositivos de Windows 7 a través de una corrección urgente de KB.</span><span class="sxs-lookup"><span data-stu-id="c8aae-109">It's also available to Windows 7 devices through a KB hot fix.</span></span> <span data-ttu-id="c8aae-110">En Windows 10, se introdujeron varias características nuevas, incluido un mecanismo de paso a través para comandos de NVMe específicos del proveedor y actualizaciones de los ioctl existentes.</span><span class="sxs-lookup"><span data-stu-id="c8aae-110">In Windows 10, several new features were introduced, including a pass-through mechanism for vendor-specific NVMe commands and updates to existing IOCTLs.</span></span>

<span data-ttu-id="c8aae-111">En este tema se proporciona información general sobre las API de uso general que puede usar para tener acceso a las unidades de NVMe en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c8aae-111">This topic provides an overview of general-use APIs that you can use to access NVMe drives in Windows 10.</span></span> <span data-ttu-id="c8aae-112">También se describe:</span><span class="sxs-lookup"><span data-stu-id="c8aae-112">It also describes:</span></span>

-   <span data-ttu-id="c8aae-113">Cómo enviar un comando de NVMe específico del proveedor con [paso a través](#pass-through-mechanism)</span><span class="sxs-lookup"><span data-stu-id="c8aae-113">How to send a vendor-specific NVMe command with [pass-through](#pass-through-mechanism)</span></span>
-   <span data-ttu-id="c8aae-114">Cómo [Enviar un comando de identificación, obtener características u obtener páginas de registro](#protocol-specific-queries) a la unidad de NVMe</span><span class="sxs-lookup"><span data-stu-id="c8aae-114">How to [send an Identify, Get Features, or Get Log Pages command](#protocol-specific-queries) to the NVMe drive</span></span>
-   <span data-ttu-id="c8aae-115">Obtención de [información de temperatura](#temperature-queries) de una unidad de NVMe</span><span class="sxs-lookup"><span data-stu-id="c8aae-115">How to [obtain temperature information](#temperature-queries) from an NVMe drive</span></span>
-   <span data-ttu-id="c8aae-116">Realización de comandos de cambio de comportamiento, como el [establecimiento de umbrales de temperatura](#behavior-changing-commands)</span><span class="sxs-lookup"><span data-stu-id="c8aae-116">How to perform behavior changing commands, such as [setting temperature thresholds](#behavior-changing-commands)</span></span>

## <a name="apis-for-working-with-nvme-drives"></a><span data-ttu-id="c8aae-117">API para trabajar con unidades de NVMe</span><span class="sxs-lookup"><span data-stu-id="c8aae-117">APIs for working with NVMe drives</span></span>

<span data-ttu-id="c8aae-118">Puede usar las siguientes API de uso general para acceder a las unidades de NVMe en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c8aae-118">You can use the following general-use APIs to access NVMe drives in Windows 10.</span></span> <span data-ttu-id="c8aae-119">Estas API se pueden encontrar en **winioctl. h** para las aplicaciones en modo de usuario y **ntddstor. h** para los controladores en modo kernel.</span><span class="sxs-lookup"><span data-stu-id="c8aae-119">These APIs can be found in **winioctl.h** for user mode applications, and **ntddstor.h** for kernel mode drivers.</span></span> <span data-ttu-id="c8aae-120">Para obtener más información acerca de los archivos de encabezado, consulte [archivos de encabezado](#header-files).</span><span class="sxs-lookup"><span data-stu-id="c8aae-120">For more information about header files, see [Header files](#header-files).</span></span>

-   <span data-ttu-id="c8aae-121">[**Ioctl \_ \_ \_ Comando de protocolo de almacenamiento**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : Use este ioctl con la estructura de **\_ \_ comandos del Protocolo de almacenamiento** para emitir comandos de NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-121">[**IOCTL\_STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : Use this IOCTL with the **STORAGE\_PROTOCOL\_COMMAND** structure to issue NVMe commands.</span></span> <span data-ttu-id="c8aae-122">Este IOCTL permite el paso a través de NVMe y admite el registro de efectos de comando en NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-122">This IOCTL enables NVMe pass-through and supports the Command Effects log in NVMe.</span></span> <span data-ttu-id="c8aae-123">Puede usarlo con comandos específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c8aae-123">You can use it with vendor-specific commands.</span></span> <span data-ttu-id="c8aae-124">Para obtener más información, vea [mecanismo de paso a través](#pass-through-mechanism).</span><span class="sxs-lookup"><span data-stu-id="c8aae-124">For more info, see [Pass-through mechanism](#pass-through-mechanism).</span></span>

-   <span data-ttu-id="c8aae-125">[**Almacenamiento \_ de \_Comando de protocolo**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : esta estructura de búfer de entrada incluye un campo **ReturnStatus** que se puede usar para notificar los siguientes valores de estado.</span><span class="sxs-lookup"><span data-stu-id="c8aae-125">[**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : This input-buffer structure includes a **ReturnStatus** field that can be used report the following status values.</span></span>
    -   <span data-ttu-id="c8aae-126">**Estado del Protocolo de almacenamiento \_ \_ \_ pendiente**</span><span class="sxs-lookup"><span data-stu-id="c8aae-126">**STORAGE\_PROTOCOL\_STATUS\_PENDING**</span></span>
    -   <span data-ttu-id="c8aae-127">**Estado del Protocolo de almacenamiento \_ \_ \_ correcta**</span><span class="sxs-lookup"><span data-stu-id="c8aae-127">**STORAGE\_PROTOCOL\_STATUS\_SUCCESS**</span></span>
    -   <span data-ttu-id="c8aae-128">**\_error de \_ Estado del Protocolo de almacenamiento \_**</span><span class="sxs-lookup"><span data-stu-id="c8aae-128">**STORAGE\_PROTOCOL\_STATUS\_ERROR**</span></span>
    -   <span data-ttu-id="c8aae-129">**Estado del Protocolo de almacenamiento \_ \_ \_ solicitud no válida \_**</span><span class="sxs-lookup"><span data-stu-id="c8aae-129">**STORAGE\_PROTOCOL\_STATUS\_INVALID\_REQUEST**</span></span>
    -   <span data-ttu-id="c8aae-130">**Estado del Protocolo de almacenamiento \_ \_ \_ sin \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="c8aae-130">**STORAGE\_PROTOCOL\_STATUS\_NO\_DEVICE**</span></span>
    -   <span data-ttu-id="c8aae-131">**Estado de protocolo de almacenamiento \_ \_ \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="c8aae-131">**STORAGE\_PROTOCOL\_STATUS\_BUSY**</span></span>
    -   <span data-ttu-id="c8aae-132">**\_saturación de \_ datos de estado del Protocolo de almacenamiento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c8aae-132">**STORAGE\_PROTOCOL\_STATUS\_DATA\_OVERRUN**</span></span>
    -   <span data-ttu-id="c8aae-133">**\_ \_ \_ faltan recursos en el estado del Protocolo de almacenamiento \_**</span><span class="sxs-lookup"><span data-stu-id="c8aae-133">**STORAGE\_PROTOCOL\_STATUS\_INSUFFICIENT\_RESOURCES**</span></span>
    -   <span data-ttu-id="c8aae-134">**Estado del Protocolo de almacenamiento \_ \_ \_ no \_ admitido**</span><span class="sxs-lookup"><span data-stu-id="c8aae-134">**STORAGE\_PROTOCOL\_STATUS\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="c8aae-135">[**Ioctl \_ \_ \_ Propiedad de consulta de almacenamiento**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : Use este ioctl con la estructura de la **\_ \_ consulta de propiedades de almacenamiento** para recuperar la información del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8aae-135">[**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : Use this IOCTL with the **STORAGE\_PROPERTY\_QUERY** structure to retrieve device information.</span></span> <span data-ttu-id="c8aae-136">Para obtener más información, consulte consultas [específicas del protocolo](#protocol-specific-queries) y [consultas de temperatura](#temperature-queries).</span><span class="sxs-lookup"><span data-stu-id="c8aae-136">For more info, see [Protocol-specific queries](#protocol-specific-queries) and [Temperature queries](#temperature-queries).</span></span>

-   <span data-ttu-id="c8aae-137">[**Almacenamiento \_ de \_Consulta de propiedad**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : esta estructura incluye los campos **PropertyId** y **AdditionalParameters** para especificar los datos que se van a consultar.</span><span class="sxs-lookup"><span data-stu-id="c8aae-137">[**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : This structure includes the **PropertyId** and **AdditionalParameters** fields to specify the data to be queried.</span></span> <span data-ttu-id="c8aae-138">En **PropertyId** , utilice la enumeración **\_ \_ ID** . de propiedad de almacenamiento para especificar el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c8aae-138">In the **PropertyId** filed, use the **STORAGE\_PROPERTY\_ID** enumeration to specify the type of data.</span></span> <span data-ttu-id="c8aae-139">Use el campo **AdditionalParameters** para especificar más detalles, dependiendo del tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c8aae-139">Use the **AdditionalParameters** field to specify more details, depending on the type of data.</span></span> <span data-ttu-id="c8aae-140">En el caso de los datos específicos del Protocolo, use la estructura de **\_ \_ \_ datos específica del Protocolo de almacenamiento** en el campo **AdditionalParameters** .</span><span class="sxs-lookup"><span data-stu-id="c8aae-140">For protocol-specific data, use the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** structure in the **AdditionalParameters** field.</span></span> <span data-ttu-id="c8aae-141">Para los datos de temperatura, use la estructura de **\_ \_ información de temperatura de almacenamiento** en el campo **AdditionalParameters** .</span><span class="sxs-lookup"><span data-stu-id="c8aae-141">For temperature data, use the **STORAGE\_TEMPERATURE\_INFO** structure in the **AdditionalParameters** field.</span></span>
-   <span data-ttu-id="c8aae-142">[**Almacenamiento \_ de \_ID. de propiedad**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : esta enumeración incluye nuevos valores que permiten que la **\_ \_ \_ propiedad de consulta de almacenamiento ioctl** recupere información específica del protocolo y de la temperatura.</span><span class="sxs-lookup"><span data-stu-id="c8aae-142">[**STORAGE\_PROPERTY\_ID**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : This enumeration includes new values that allow **IOCTL\_STORAGE\_QUERY\_PROPERTY** to retrieve protocol-specific and temperature information.</span></span>

    -   <span data-ttu-id="c8aae-143">**StorageAdapterProtocolSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="c8aae-143">**StorageAdapterProtocolSpecificProperty**</span></span>
    -   <span data-ttu-id="c8aae-144">**StorageDeviceProtocolSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="c8aae-144">**StorageDeviceProtocolSpecificProperty**</span></span>

    <span data-ttu-id="c8aae-145">Use uno de estos identificadores de propiedad específicos del protocolo en combinación con **\_ \_ \_ datos específicos del Protocolo de almacenamiento** para recuperar datos específicos del protocolo en la estructura de [**\_ \_ \_ descriptor de datos del Protocolo de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="c8aae-145">Use one of these protocol-specific property IDs in combination with **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** to retrieve protocol-specific data in the [**STORAGE\_PROTOCOL\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) structure.</span></span>

    -   <span data-ttu-id="c8aae-146">**StorageAdapterTemperatureProperty**</span><span class="sxs-lookup"><span data-stu-id="c8aae-146">**StorageAdapterTemperatureProperty**</span></span>
    -   <span data-ttu-id="c8aae-147">**StorageDeviceTemperatureProperty**</span><span class="sxs-lookup"><span data-stu-id="c8aae-147">**StorageDeviceTemperatureProperty**</span></span>

    <span data-ttu-id="c8aae-148">Use uno de estos identificadores de propiedad de temperatura para recuperar los datos de temperatura en la estructura de [**\_ \_ \_ descriptor de datos de temperatura de almacenamiento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="c8aae-148">Use one of these temperature property IDs to retrieve temperature data in the [**STORAGE\_TEMPERATURE\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) structure.</span></span>

-   <span data-ttu-id="c8aae-149">[**Almacenamiento \_ de \_ \_ Datos específicos del protocolo**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : Recupere datos específicos de NVMe cuando esta estructura se usa para el campo **AdditionalParameters** de la consulta de **\_ propiedades \_ de almacenamiento** y se especifica un valor de enumeración de [**tipo de datos de nVMe del Protocolo de almacenamiento \_ \_ \_ \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) .</span><span class="sxs-lookup"><span data-stu-id="c8aae-149">[**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : Retrieve NVMe-specific data when this structure is used for the **AdditionalParameters** field of **STORAGE\_PROPERTY\_QUERY** and a [**STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) enum value is specified.</span></span> <span data-ttu-id="c8aae-150">Use uno de los siguientes valores de **tipo de datos de protocolo de almacenamiento \_ \_ NVME \_ \_** en el campo **DataType** de la estructura de **\_ \_ \_ datos específica del Protocolo de almacenamiento** :</span><span class="sxs-lookup"><span data-stu-id="c8aae-150">Use one of the following **STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE** values in the **DataType** field of the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** structure:</span></span>

    -   <span data-ttu-id="c8aae-151">Use **NVMeDataTypeIdentify** para obtener los datos del controlador de identificación o identificar los datos del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="c8aae-151">Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.</span></span>
    -   <span data-ttu-id="c8aae-152">Use **NVMeDataTypeLogPage** para obtener páginas de registro (incluidos los datos de estado o inteligentes).</span><span class="sxs-lookup"><span data-stu-id="c8aae-152">Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).</span></span>
    -   <span data-ttu-id="c8aae-153">Use **NVMeDataTypeFeature** para obtener características de la unidad de NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-153">Use **NVMeDataTypeFeature** to get features of the NVMe drive.</span></span>

-   <span data-ttu-id="c8aae-154">[**Almacenamiento \_ de \_Información de temperatura**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : esta estructura se usa para almacenar datos de temperatura concretos.</span><span class="sxs-lookup"><span data-stu-id="c8aae-154">[**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : This structure is used to hold specific temperature data.</span></span> <span data-ttu-id="c8aae-155">Se usa en el **\_ \_ \_ descriptor de datos TEMERATURE de almacenamiento** para devolver los resultados de una consulta de temperatura.</span><span class="sxs-lookup"><span data-stu-id="c8aae-155">It's used in the **STORAGE\_TEMERATURE\_DATA\_DESCRIPTOR** to return the results of a temperature query.</span></span>

-   <span data-ttu-id="c8aae-156">[**Ioctl \_ \_Umbral de \_ temperatura \_ del conjunto de almacenamiento**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Use este ioctl con la estructura del **\_ \_ umbral de temperatura de almacenamiento** para establecer los umbrales de temperatura.</span><span class="sxs-lookup"><span data-stu-id="c8aae-156">[**IOCTL\_STORAGE\_SET\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Use this IOCTL with the **STORAGE\_TEMPERATURE\_THRESHOLD** structure to set temperature thresholds.</span></span> <span data-ttu-id="c8aae-157">Para obtener más información, consulte [Behavior Changing Commands](#behavior-changing-commands).</span><span class="sxs-lookup"><span data-stu-id="c8aae-157">For more info, see [Behavior changing commands](#behavior-changing-commands).</span></span>

-   <span data-ttu-id="c8aae-158">[**Almacenamiento \_ de \_Umbral de temperatura**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : esta estructura se usa como búfer de entrada para especificar el umbral de temperatura.</span><span class="sxs-lookup"><span data-stu-id="c8aae-158">[**STORAGE\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : This structure is used as an input buffer to specify the temperature threshold.</span></span> <span data-ttu-id="c8aae-159">El campo de **sobreumbral** (booleano) especifica si el campo de **umbral** es el valor de umbral superior o no (de lo contrario, es el valor de umbral inferior).</span><span class="sxs-lookup"><span data-stu-id="c8aae-159">The **OverThreshold** field (boolean) specifies if the **Threshold** field is the over threshold value or not (otherwise, it's the under threshold value).</span></span>

## <a name="pass-through-mechanism"></a><span data-ttu-id="c8aae-160">Mecanismo de paso a través</span><span class="sxs-lookup"><span data-stu-id="c8aae-160">Pass-through mechanism</span></span>

<span data-ttu-id="c8aae-161">Los comandos que no están definidos en la especificación de NVMe son los más difíciles de controlar para el SO del host: el host no tiene información sobre los efectos que pueden tener los comandos en el dispositivo de destino, la infraestructura expuesta (tamaños de espacios de nombres y bloques) y su comportamiento.</span><span class="sxs-lookup"><span data-stu-id="c8aae-161">Commands which are not defined in the NVMe specification are the most difficult for the host OS to handle – the host has no insight into the effects that the commands may have on the target device, the exposed infrastructure (namespaces/block sizes), and its behavior.</span></span>

<span data-ttu-id="c8aae-162">Para realizar mejor los comandos específicos de este dispositivo a través de la pila de almacenamiento de Windows, un nuevo mecanismo de paso permite canalizar comandos específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c8aae-162">To better carry such device specific commands through the Windows storage stack, a new pass-through mechanism allows vendor-specific commands to be piped through.</span></span> <span data-ttu-id="c8aae-163">Esta canalización de paso a través también ayudará en el desarrollo de herramientas de administración y pruebas.</span><span class="sxs-lookup"><span data-stu-id="c8aae-163">This pass-through pipe will also aid in development of management and testing tools.</span></span> <span data-ttu-id="c8aae-164">Sin embargo, este mecanismo de paso a través requiere el uso del registro de efectos de comando.</span><span class="sxs-lookup"><span data-stu-id="c8aae-164">However, this pass-through mechanism requires use of the Command Effects Log.</span></span> <span data-ttu-id="c8aae-165">Además, StoreNVMe.sys requiere que todos los comandos, no solo los comandos de paso a través, se describirán en el registro de efectos de comando.</span><span class="sxs-lookup"><span data-stu-id="c8aae-165">Moreover, StoreNVMe.sys requires all commands, not just pass-through commands, to be described in the Command Effects Log.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8aae-166">StorNVMe.sys y Storport.sys bloquearán cualquier comando en un dispositivo si no se describe en el registro de efectos de comandos.</span><span class="sxs-lookup"><span data-stu-id="c8aae-166">StorNVMe.sys and Storport.sys will block any command to a device if it is not described in the Command Effects Log.</span></span>

 

### <a name="supporting-the-command-effects-log"></a><span data-ttu-id="c8aae-167">Compatibilidad con el registro de efectos de comando</span><span class="sxs-lookup"><span data-stu-id="c8aae-167">Supporting the Command Effects Log</span></span>

<span data-ttu-id="c8aae-168">El registro de efectos de comando (como se describe en comandos compatibles y efectos, sección 5.10.1.5 de la [especificación de NVMe 1,2](https://nvmexpress.org/specifications)) permite la descripción de los efectos de los comandos específicos del proveedor junto con los comandos definidos por la especificación.</span><span class="sxs-lookup"><span data-stu-id="c8aae-168">The Command Effects Log (as described in Commands Supported and Effects, section 5.10.1.5 of [NVMe Specification 1.2](https://nvmexpress.org/specifications)) allows the description of the effects of vendor-specific commands together with specification-defined commands.</span></span> <span data-ttu-id="c8aae-169">Esto facilita la validación de la compatibilidad de comandos, así como la optimización del comportamiento del comando y, por lo tanto, debe implementarse para todo el conjunto de comandos que admite el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8aae-169">This facilitates both command support validation as well as command behavior optimization, and therefore should be implemented for the entire set of commands that the device supports.</span></span> <span data-ttu-id="c8aae-170">Las siguientes condiciones describen el resultado de cómo se envía el comando en función de su entrada de registro de efectos de comando.</span><span class="sxs-lookup"><span data-stu-id="c8aae-170">The following conditions describe the result on how the command is sent based on its Command Effects Log entry.</span></span>

<span data-ttu-id="c8aae-171">Para cualquier comando específico descrito en el registro de efectos de comandos...</span><span class="sxs-lookup"><span data-stu-id="c8aae-171">For any specific command described in the Command Effects Log...</span></span>

<span data-ttu-id="c8aae-172">**While**:</span><span class="sxs-lookup"><span data-stu-id="c8aae-172">**While**:</span></span>

-   <span data-ttu-id="c8aae-173">El comando compatible (CSUPP) se establece en ' 1 ', lo que significa que el comando es compatible con el controlador (bit 01)</span><span class="sxs-lookup"><span data-stu-id="c8aae-173">Command Supported (CSUPP) is set to ‘1’ signifying that the command is supported by the controller (Bit 01)</span></span>

    > [!Note]  
    > <span data-ttu-id="c8aae-174">Cuando CSUPP se establece en "0" (lo que significa que no se admite el comando), se bloqueará el comando.</span><span class="sxs-lookup"><span data-stu-id="c8aae-174">When CSUPP is set to ‘0’ (signifying that the command is not supported) the command will be blocked</span></span>

     

<span data-ttu-id="c8aae-175">**Y si** se establece alguna de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="c8aae-175">**And if** any of the following is set:</span></span>

-   <span data-ttu-id="c8aae-176">El cambio de capacidad del controlador (CCC) se establece en ' 1 ', lo que significa que el comando puede cambiar las capacidades del controlador (bit 04)</span><span class="sxs-lookup"><span data-stu-id="c8aae-176">Controller Capability Change (CCC) is set to ‘1’ signifying that the command may change controller capabilities (Bit 04)</span></span>

-   <span data-ttu-id="c8aae-177">El cambio de inventario de espacios de nombres (NIC) se establece en ' 1 ', lo que significa que el comando puede cambiar el número o capacidades para varios espacios de nombres (bit 03)</span><span class="sxs-lookup"><span data-stu-id="c8aae-177">Namespace Inventory Change (NIC) is set to ‘1’ signifying that the command may change the number, or capabilities for multiple namespaces (Bit 03)</span></span>

-   <span data-ttu-id="c8aae-178">El cambio de capacidad de espacio de nombres (NCC) se establece en ' 1 ', lo que significa que el comando puede cambiar las capacidades de un solo espacio de nombres (bit 02)</span><span class="sxs-lookup"><span data-stu-id="c8aae-178">Namespace Capability Change (NCC) is set to ‘1’ signifying that the command may change the capabilities of a single namespace (Bit 02)</span></span>

-   <span data-ttu-id="c8aae-179">El envío y la ejecución de comandos (CSE) se establece en 001B o 010B, lo que significa que el comando se puede enviar cuando no hay ningún otro comando pendiente al mismo espacio de nombres o a cualquier otro comando, y que no se debe enviar otro comando al mismo espacio de nombres o a cualquier otro espacio de nombres hasta que se complete este comando (bits 18:16)</span><span class="sxs-lookup"><span data-stu-id="c8aae-179">Command Submission and Execution (CSE) is set to 001b or 010b, signifying that the command may be submitted when there is no other outstanding command to the same or any namespace, and that another command should not be submitted to the same or any namespace until this command is complete (Bits 18:16)</span></span>

<span data-ttu-id="c8aae-180">**A continuación,** el comando se enviará como el único comando pendiente del adaptador.</span><span class="sxs-lookup"><span data-stu-id="c8aae-180">**Then** the command will be sent as the only command outstanding to the adapter.</span></span>

<span data-ttu-id="c8aae-181">De lo **contrario, si**:</span><span class="sxs-lookup"><span data-stu-id="c8aae-181">**Else if**:</span></span>

-   <span data-ttu-id="c8aae-182">El envío y la ejecución de comandos (CSE) se establecen en 001B, lo que significa que el comando se puede enviar cuando no hay ningún otro comando pendiente al mismo espacio de nombres y que no se debe enviar otro comando al mismo espacio de nombres hasta que se complete este comando (bits 18:16)</span><span class="sxs-lookup"><span data-stu-id="c8aae-182">Command Submission and Execution (CSE) is set to 001b, signifying that the command may be submitted when there is no other outstanding command to the same namespace, and that another command should not be submitted to the same namespace until this command is complete (Bits 18:16)</span></span>

<span data-ttu-id="c8aae-183">**A continuación,** el comando se enviará como el único comando pendiente al objeto de número de unidad lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="c8aae-183">**Then** the command will be sent as the only command outstanding to the Logical Unit Number object (LUN).</span></span>

<span data-ttu-id="c8aae-184">De **lo contrario**, el comando se envía con otros comandos pendientes sin inhibición.</span><span class="sxs-lookup"><span data-stu-id="c8aae-184">**Otherwise**, the command is sent with other commands outstanding without inhibition.</span></span> <span data-ttu-id="c8aae-185">Por ejemplo, si se envía un comando específico del proveedor al dispositivo para recuperar información estadística no definida por la especificación, no debería haber ningún riesgo de cambiar el comportamiento del dispositivo o la capacidad de ejecutar comandos de e/s.</span><span class="sxs-lookup"><span data-stu-id="c8aae-185">For example, if a vendor-specific command is sent to the device to retrieve statistical information that is not spec-defined, there should be no risk to changing the device’s behavior or capability to execute I/O commands.</span></span> <span data-ttu-id="c8aae-186">Estas solicitudes se pueden atender en paralelo a e/s y no sería necesario pausar PAUSE-resume.</span><span class="sxs-lookup"><span data-stu-id="c8aae-186">Such requests could be serviced in parallel to I/O and no pause-resume would be necessary.</span></span>

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a><span data-ttu-id="c8aae-187">Uso del \_ \_ \_ comando de protocolo de almacenamiento ioctl para enviar comandos</span><span class="sxs-lookup"><span data-stu-id="c8aae-187">Using IOCTL\_STORAGE\_PROTOCOL\_COMMAND to send commands</span></span>

<span data-ttu-id="c8aae-188">El paso a través se puede realizar mediante [**el \_ \_ \_ comando de protocolo de almacenamiento ioctl**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introducido en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c8aae-188">Pass-through can be conducted using the [**IOCTL\_STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introduced in Windows 10.</span></span> <span data-ttu-id="c8aae-189">Este IOCTL se diseñó para tener un comportamiento similar al de los ioctl de paso a través de SCSI y ATA existentes, a fin de enviar un comando incrustado al dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="c8aae-189">This IOCTL was designed to have a similar behavior as the existing SCSI and ATA pass-through IOCTLs, to send an embedded command to the target device.</span></span> <span data-ttu-id="c8aae-190">A través de este IOCTL, el paso a través se puede enviar a un dispositivo de almacenamiento, incluida una unidad de NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-190">Via this IOCTL, pass-through can be sent to a storage device, including an NVMe drive.</span></span>

<span data-ttu-id="c8aae-191">Por ejemplo, en NVMe, IOCTL permitirá el envío de los siguientes códigos de comando.</span><span class="sxs-lookup"><span data-stu-id="c8aae-191">For example, in NVMe, the IOCTL will allow the sending down of the following command codes.</span></span>

-   <span data-ttu-id="c8aae-192">Comandos de administración específicos del proveedor (C0h – FFh)</span><span class="sxs-lookup"><span data-stu-id="c8aae-192">Vendor Specific Admin Commands (C0h – FFh)</span></span>
-   <span data-ttu-id="c8aae-193">Comandos de NVMe específicos del proveedor (80h – FFh)</span><span class="sxs-lookup"><span data-stu-id="c8aae-193">Vendor Specific NVMe Commands (80h – FFh)</span></span>

<span data-ttu-id="c8aae-194">Como con todos los demás ioctl, use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar el ioctl de paso a través.</span><span class="sxs-lookup"><span data-stu-id="c8aae-194">As with all other IOCTLs, Use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) to send the pass-through IOCTL down.</span></span> <span data-ttu-id="c8aae-195">El IOCTL se rellena mediante la estructura de búfer de entrada del [**\_ \_ comando del Protocolo de almacenamiento**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) que se encuentra en **ntddstor. h**.</span><span class="sxs-lookup"><span data-stu-id="c8aae-195">The IOCTL is populated using the [**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) input-buffer structure found in **ntddstor.h**.</span></span> <span data-ttu-id="c8aae-196">Rellene el campo **comando** con el comando específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c8aae-196">Populate the **Command** field with the vendor-specific command.</span></span>


```C++
typedef struct _STORAGE_PROTOCOL_COMMAND {

    ULONG   Version;                        // STORAGE_PROTOCOL_STRUCTURE_VERSION
    ULONG   Length;                         // sizeof(STORAGE_PROTOCOL_COMMAND)

    STORAGE_PROTOCOL_TYPE  ProtocolType;
    ULONG   Flags;                          // Flags for the request

    ULONG   ReturnStatus;                   // return value
    ULONG   ErrorCode;                      // return value, optional

    ULONG   CommandLength;                  // non-zero value should be set by caller
    ULONG   ErrorInfoLength;                // optional, can be zero
    ULONG   DataToDeviceTransferLength;     // optional, can be zero. Used by WRITE type of request.
    ULONG   DataFromDeviceTransferLength;   // optional, can be zero. Used by READ type of request.

    ULONG   TimeOutValue;                   // in unit of seconds

    ULONG   ErrorInfoOffset;                // offsets need to be pointer aligned
    ULONG   DataToDeviceBufferOffset;       // offsets need to be pointer aligned
    ULONG   DataFromDeviceBufferOffset;     // offsets need to be pointer aligned

    ULONG   CommandSpecific;                // optional information passed along with Command.
    ULONG   Reserved0;

    ULONG   FixedProtocolReturnData;        // return data, optional. Some protocol, such as NVMe, may return a small amount data (DWORD0 from completion queue entry) without the need of separate device data transfer.
    ULONG   Reserved1[3];

    _Field_size_bytes_full_(CommandLength) UCHAR Command[ANYSIZE_ARRAY];

} STORAGE_PROTOCOL_COMMAND, *PSTORAGE_PROTOCOL_COMMAND;
```



<span data-ttu-id="c8aae-197">El comando específico del proveedor que se desea enviar se debe rellenar en el campo resaltado anterior.</span><span class="sxs-lookup"><span data-stu-id="c8aae-197">The vendor specific command desired to be sent should be populated in the highlighted field above.</span></span> <span data-ttu-id="c8aae-198">Vuelva a tener en cuenta que el registro de efectos de comando debe implementarse para los comandos de paso a través.</span><span class="sxs-lookup"><span data-stu-id="c8aae-198">Note again that the Command Effects Log must be implemented for pass-through commands.</span></span> <span data-ttu-id="c8aae-199">En concreto, estos comandos deben aparecer como compatibles en el registro de efectos de comando (consulte la sección anterior para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="c8aae-199">In particular, these commands need to be reported as supported in the Command Effects Log (see previous section for more information).</span></span> <span data-ttu-id="c8aae-200">Tenga en cuenta también que los campos PRP son específicos del controlador, por lo que las aplicaciones que envían comandos pueden dejarlos como 0.</span><span class="sxs-lookup"><span data-stu-id="c8aae-200">Also note that PRP fields are driver specific thus applications sending commands can leave them as 0.</span></span>

<span data-ttu-id="c8aae-201">Por último, este IOCTL de paso a través está pensado para enviar comandos específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c8aae-201">Finally, this pass-through IOCTL is intended for sending vendor-specific commands.</span></span> <span data-ttu-id="c8aae-202">No se debe usar este IOCTL de paso a través para enviar otros comandos de NVMe específicos de administrador o no de proveedor, como la identificación.</span><span class="sxs-lookup"><span data-stu-id="c8aae-202">To send other admin or non-vendor specific NVMe commands such as Identify, this pass-through IOCTL should not be used.</span></span> <span data-ttu-id="c8aae-203">Por ejemplo, **la \_ \_ \_ propiedad consulta de almacenamiento ioctl** debe usarse para identificar o obtener páginas de registro.</span><span class="sxs-lookup"><span data-stu-id="c8aae-203">For example, **IOCTL\_STORAGE\_QUERY\_PROPERTY** should be used for Identify or Get Log Pages.</span></span> <span data-ttu-id="c8aae-204">Para obtener más información, vea la sección siguiente, [consultas específicas del protocolo](/windows).</span><span class="sxs-lookup"><span data-stu-id="c8aae-204">For more info, see the next section, [Protocol-specific queries](/windows).</span></span>

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a><span data-ttu-id="c8aae-205">No actualice el firmware a través del mecanismo de paso a través</span><span class="sxs-lookup"><span data-stu-id="c8aae-205">Don't update firmware through the pass-through mechanism</span></span>

<span data-ttu-id="c8aae-206">Los comandos de descarga y activación del firmware no se deben enviar mediante el paso a través.</span><span class="sxs-lookup"><span data-stu-id="c8aae-206">Firmware download and activation commands should not be sent using pass-through.</span></span> <span data-ttu-id="c8aae-207">**Ioctl \_ El \_ \_ comando de protocolo de almacenamiento** solo se debe usar para comandos específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c8aae-207">**IOCTL\_STORAGE\_PROTOCOL\_COMMAND** should only be used for vendor-specific commands.</span></span>

<span data-ttu-id="c8aae-208">En su lugar, use los siguientes ioctl de almacenamiento general (introducidos en Windows 10) para evitar que las aplicaciones usen directamente la \_ versión de MINIPUERTO SCSI del ioctl de firmware.</span><span class="sxs-lookup"><span data-stu-id="c8aae-208">Instead, use the following general storage IOCTLs (introduced in Windows 10) to avoid applications directly using the SCSI\_miniport version of the Firmware IOCTL.</span></span> <span data-ttu-id="c8aae-209">Los controladores de almacenamiento traducirán el IOCTL a un comando SCSI o a la \_ versión del MINIPUERTO SCSI del ioctl en el minipuerto.</span><span class="sxs-lookup"><span data-stu-id="c8aae-209">Storage drivers will translate the IOCTL to either a SCSI command or the SCSI\_miniport version of the IOCTL to the miniport.</span></span>

<span data-ttu-id="c8aae-210">Estos ioctl se recomiendan para desarrollar herramientas de actualización de firmware en Windows 10 y Windows Server 2016:</span><span class="sxs-lookup"><span data-stu-id="c8aae-210">These IOCTLs are recommended for developing firmware upgrade tools in Windows 10 and Windows Server 2016:</span></span>

-   [<span data-ttu-id="c8aae-211">**\_ \_ \_ obtener información de firmware de almacenamiento de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="c8aae-211">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [<span data-ttu-id="c8aae-212">**\_descarga de \_ firmware de almacenamiento de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="c8aae-212">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [<span data-ttu-id="c8aae-213">**\_ \_ Activar firmware de almacenamiento de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="c8aae-213">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

<span data-ttu-id="c8aae-214">Para obtener información de almacenamiento y actualizar el firmware, Windows también admite cmdlets de PowerShell para hacerlo rápidamente:</span><span class="sxs-lookup"><span data-stu-id="c8aae-214">For getting storage information and updating firmware, Windows also supports PowerShell cmdlets for doing this quickly:</span></span>

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> <span data-ttu-id="c8aae-215">Para actualizar el firmware en NVMe en Windows 8.1, use \_ el \_ firmware del minipuerto SCSI de ioctl \_ .</span><span class="sxs-lookup"><span data-stu-id="c8aae-215">To update firmware on NVMe in Windows 8.1, use IOCTL\_SCSI\_MINIPORT\_FIRMWARE.</span></span> <span data-ttu-id="c8aae-216">Este IOCTL no se ha trasladado a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c8aae-216">This IOCTL was not backported to Windows 7.</span></span> <span data-ttu-id="c8aae-217">Para obtener más información, consulte [actualización del firmware de un dispositivo de NVMe en Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).</span><span class="sxs-lookup"><span data-stu-id="c8aae-217">For more information, see [Upgrading Firmware for an NVMe Device in Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).</span></span>

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a><span data-ttu-id="c8aae-218">Devolver errores a través del mecanismo de paso a través</span><span class="sxs-lookup"><span data-stu-id="c8aae-218">Returning errors through the pass-through mechanism</span></span>

<span data-ttu-id="c8aae-219">Similar a los ioctl de paso a través de SCSI y ATA, cuando se envía un comando o una solicitud al minipuerto o dispositivo, el IOCTL devuelve si es correcto o no.</span><span class="sxs-lookup"><span data-stu-id="c8aae-219">Similar to SCSI and ATA pass-through IOCTLs, when a command/request is sent to the miniport or device, the IOCTL returns if it was successful or not.</span></span> <span data-ttu-id="c8aae-220">En la estructura de [**\_ \_ comandos del Protocolo de almacenamiento**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) , el ioctl devuelve el estado a través del campo **ReturnStatus** .</span><span class="sxs-lookup"><span data-stu-id="c8aae-220">In the [**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) structure, the IOCTL returns the status through the **ReturnStatus** field.</span></span>

### <a name="example-sending-a-vendor-specific-command"></a><span data-ttu-id="c8aae-221">Ejemplo: enviar un comando específico del proveedor</span><span class="sxs-lookup"><span data-stu-id="c8aae-221">Example: sending a vendor-specific command</span></span>

<span data-ttu-id="c8aae-222">En este ejemplo, se envía un comando específico del proveedor (0xFF) arbitrario a través de un paso a una unidad de NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-222">In this example, an arbitrary vendor-specific command (0xFF) is sent via pass-through to an NVMe drive.</span></span> <span data-ttu-id="c8aae-223">El código siguiente asigna un búfer, Inicializa una consulta y, a continuación, envía el comando al dispositivo a través de DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="c8aae-223">The following code allocates a buffer, initializes a query, and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    ZeroMemory(buffer, bufferLength);  
    protocolCommand = (PSTORAGE_PROTOCOL_COMMAND)buffer;  

    protocolCommand->Version = STORAGE_PROTOCOL_STRUCTURE_VERSION;  
    protocolCommand->Length = sizeof(STORAGE_PROTOCOL_COMMAND);  
    protocolCommand->ProtocolType = ProtocolTypeNvme;  
    protocolCommand->Flags = STORAGE_PROTOCOL_COMMAND_FLAG_ADAPTER_REQUEST;  
    protocolCommand->CommandLength = STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->ErrorInfoLength = sizeof(NVME_ERROR_INFO_LOG);  
    protocolCommand->DataFromDeviceTransferLength = 4096;  
    protocolCommand->TimeOutValue = 10;  
    protocolCommand->ErrorInfoOffset = FIELD_OFFSET(STORAGE_PROTOCOL_COMMAND, Command) + STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->DataFromDeviceBufferOffset = protocolCommand->ErrorInfoOffset + protocolCommand->ErrorInfoLength;  
    protocolCommand->CommandSpecific = STORAGE_PROTOCOL_SPECIFIC_NVME_ADMIN_COMMAND;  

    command = (PNVME_COMMAND)protocolCommand->Command;  

    command->CDW0.OPC = 0xFF;  
    command->u.GENERAL.CDW10 = 0xto_fill_in;  
    command->u.GENERAL.CDW12 = 0xto_fill_in;  
    command->u.GENERAL.CDW13 = 0xto_fill_in;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_PROTOCOL_COMMAND,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL 
                             );  
```



<span data-ttu-id="c8aae-224">En este ejemplo, se espera `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` que el comando se haya ejecutado correctamente en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8aae-224">In this example, we expect `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` if the command succeeded to the device.</span></span>

## <a name="protocol-specific-queries"></a><span data-ttu-id="c8aae-225">Consultas específicas del Protocolo</span><span class="sxs-lookup"><span data-stu-id="c8aae-225">Protocol-specific queries</span></span>

<span data-ttu-id="c8aae-226">Windows 8.1 ha introducido la [**\_ propiedad de \_ consulta \_ de almacenamiento ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) para la recuperación de datos.</span><span class="sxs-lookup"><span data-stu-id="c8aae-226">Windows 8.1 introduced [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) for data retrieval.</span></span> <span data-ttu-id="c8aae-227">En Windows 10, el IOCTL se mejoró para admitir las características de NVMe solicitadas comúnmente, como **obtener páginas de registro**, **obtener características** e **identificar**.</span><span class="sxs-lookup"><span data-stu-id="c8aae-227">In Windows 10, the IOCTL was enhanced to support commonly requested NVMe features such as **Get Log Pages**, **Get Features**, and **Identify**.</span></span> <span data-ttu-id="c8aae-228">Esto permite la recuperación de información específica de NVMe para fines de supervisión e inventario.</span><span class="sxs-lookup"><span data-stu-id="c8aae-228">This allows for the retrieval of NVMe specific information for monitoring and inventory purposes.</span></span>

<span data-ttu-id="c8aae-229">Aquí se muestra el búfer de entrada de IOCTL, la [**\_ \_ consulta de propiedades de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (desde Windows 10).</span><span class="sxs-lookup"><span data-stu-id="c8aae-229">The input buffer for the IOCTL, [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



<span data-ttu-id="c8aae-230">Al utilizar [**la \_ \_ \_ propiedad de consulta de almacenamiento ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) para recuperar información específica del Protocolo de NVMe en el [**\_ \_ \_ descriptor de datos del Protocolo de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configure la estructura de [**\_ \_ consulta de propiedades de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c8aae-230">When using [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) to retrieve NVMe protocol-specific information in the [**STORAGE\_PROTOCOL\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configure the [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure as follows:</span></span>

-   <span data-ttu-id="c8aae-231">Asigna un búfer que puede contener una [**consulta de \_ propiedades \_ de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) y una estructura de [**\_ \_ \_ datos específica del Protocolo de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) .</span><span class="sxs-lookup"><span data-stu-id="c8aae-231">Allocate a buffer that can contains both a [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) and a [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure.</span></span>

-   <span data-ttu-id="c8aae-232">Establezca el campo **PropertyID** en **StorageAdapterProtocolSpecificProperty** o **StorageDeviceProtocolSpecificProperty** para una solicitud de controlador o dispositivo/espacio de nombres, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c8aae-232">Set the **PropertyID** field to **StorageAdapterProtocolSpecificProperty** or **StorageDeviceProtocolSpecificProperty** for a controller or device/namespace request, respectively.</span></span>

-   <span data-ttu-id="c8aae-233">Establezca el campo **QueryType** en **PropertyStandardQuery**.</span><span class="sxs-lookup"><span data-stu-id="c8aae-233">Set the **QueryType** field to **PropertyStandardQuery**.</span></span>

-   <span data-ttu-id="c8aae-234">Rellene la estructura de [**\_ \_ \_ datos específica del Protocolo de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) con los valores deseados.</span><span class="sxs-lookup"><span data-stu-id="c8aae-234">Fill the [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure with the desired values.</span></span> <span data-ttu-id="c8aae-235">El inicio de los **\_ \_ \_ datos específicos del Protocolo de almacenamiento** es el campo **AdditionalParameters** de la consulta de la [**\_ propiedad \_ Storage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).</span><span class="sxs-lookup"><span data-stu-id="c8aae-235">The start of the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** is the **AdditionalParameters** field of [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).</span></span>

<span data-ttu-id="c8aae-236">Aquí se muestra la estructura de [**\_ \_ \_ datos específica del Protocolo de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) (de Windows 10).</span><span class="sxs-lookup"><span data-stu-id="c8aae-236">The [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                 

    ULONG   ProtocolDataRequestValue;
    ULONG   ProtocolDataRequestSubValue;

    ULONG   ProtocolDataOffset;         
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;   
    ULONG   Reserved[3];

} STORAGE_PROTOCOL_SPECIFIC_DATA, *PSTORAGE_PROTOCOL_SPECIFIC_DATA;
```



<span data-ttu-id="c8aae-237">Para especificar un tipo de información específica del Protocolo de NVMe, configure la estructura de [**\_ \_ \_ datos específica del Protocolo de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c8aae-237">To specify a type of NVMe protocol-specific information, configure the [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure as follows:</span></span>

-   <span data-ttu-id="c8aae-238">Establezca el campo **protocolType** en **ProtocolTypeNVMe**.</span><span class="sxs-lookup"><span data-stu-id="c8aae-238">Set the **ProtocolType** field to **ProtocolTypeNVMe**.</span></span>

-   <span data-ttu-id="c8aae-239">Establezca el campo **DataType** en un valor de enumeración definido por el tipo de [**datos de protocolo de almacenamiento \_ \_ NVME \_ \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):</span><span class="sxs-lookup"><span data-stu-id="c8aae-239">Set the **DataType** field to an enumeration value defined by [**STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):</span></span>

    -   <span data-ttu-id="c8aae-240">Use **NVMeDataTypeIdentify** para obtener los datos del controlador de identificación o identificar los datos del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="c8aae-240">Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.</span></span>
    -   <span data-ttu-id="c8aae-241">Use **NVMeDataTypeLogPage** para obtener páginas de registro (incluidos los datos de estado o inteligentes).</span><span class="sxs-lookup"><span data-stu-id="c8aae-241">Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).</span></span>
    -   <span data-ttu-id="c8aae-242">Use **NVMeDataTypeFeature** para obtener características de la unidad de NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-242">Use **NVMeDataTypeFeature** to get features of the NVMe drive.</span></span>

<span data-ttu-id="c8aae-243">Cuando se usa **ProtocolTypeNVMe** como **protocolType**, las consultas de información específica del Protocolo se pueden recuperar en paralelo con otras e/s en la unidad de NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-243">When **ProtocolTypeNVMe** is used as the **ProtocolType**, queries for protocol-specific information can be retrieved in parallel with other I/O on the NVMe drive.</span></span>

<span data-ttu-id="c8aae-244">En los siguientes ejemplos se muestran las consultas específicas del protocolo NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-244">The following examples demonstrate NVMe protocol-specific queries.</span></span>

### <a name="example-nvme-identify-query"></a><span data-ttu-id="c8aae-245">Ejemplo: la consulta de identificación de NVMe</span><span class="sxs-lookup"><span data-stu-id="c8aae-245">Example: NVMe Identify query</span></span>

<span data-ttu-id="c8aae-246">En este ejemplo, la solicitud de **identificación** se envía a una unidad de NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-246">In this example, the **Identify** request is sent to an NVMe drive.</span></span> <span data-ttu-id="c8aae-247">El código siguiente inicializa la estructura de datos de consulta y, a continuación, envía el comando al dispositivo a través de DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="c8aae-247">The following code initializes the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    BOOL    result;
    PVOID   buffer = NULL;
    ULONG   bufferLength = 0;
    ULONG   returnedLength = 0;

    PSTORAGE_PROPERTY_QUERY query = NULL;
    PSTORAGE_PROTOCOL_SPECIFIC_DATA protocolData = NULL;
    PSTORAGE_PROTOCOL_DATA_DESCRIPTOR protocolDataDescr = NULL;

    //
    // Allocate buffer for use.
    //
    bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_QUERY, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA) + NVME_MAX_LOG_SIZE;
    buffer = malloc(bufferLength);

    if (buffer == NULL) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: allocate buffer failed, exit.\n"));
        goto exit;
    }

    //
    // Initialize query data structure to get Identify Controller Data.
    //
    ZeroMemory(buffer, bufferLength);

    query = (PSTORAGE_PROPERTY_QUERY)buffer;
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;

    query->PropertyId = StorageAdapterProtocolSpecificProperty;
    query->QueryType = PropertyStandardQuery;

    protocolData->ProtocolType = ProtocolTypeNvme;
    protocolData->DataType = NVMeDataTypeIdentify;
    protocolData->ProtocolDataRequestValue = NVME_IDENTIFY_CNS_CONTROLLER;
    protocolData->ProtocolDataRequestSubValue = 0;
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);
    protocolData->ProtocolDataLength = NVME_MAX_LOG_SIZE;

    //
    // Send request down.
    //
    result = DeviceIoControl(DeviceList[Index].Handle,
                             IOCTL_STORAGE_QUERY_PROPERTY,
                             buffer,
                             bufferLength,
                             buffer,
                             bufferLength,
                             &returnedLength,
                             NULL
                             );

    ZeroMemory(buffer, bufferLength);
    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < NVME_MAX_LOG_SIZE)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // Identify Controller Data 
    //
    {
        PNVME_IDENTIFY_CONTROLLER_DATA identifyControllerData = (PNVME_IDENTIFY_CONTROLLER_DATA)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        if ((identifyControllerData->VID == 0) ||
            (identifyControllerData->NN == 0)) {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Identify Controller Data not valid.\n"));
            goto exit;
        } else {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Identify Controller Data succeeded_*_.\n"));
        }
    }

  
```



<span data-ttu-id="c8aae-248">Tenga en cuenta que el autor de la llamada debe asignar un único búfer que contiene \_ \_ la consulta de propiedades de almacenamiento y el tamaño de los \_ datos específicos del Protocolo de almacenamiento \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c8aae-248">Note that the caller needs to allocate a single buffer containing STORAGE\_PROPERTY\_QUERY and the size of STORAGE\_PROTOCOL\_SPECIFIC\_DATA.</span></span> <span data-ttu-id="c8aae-249">En este ejemplo, se usa el mismo búfer para la entrada y la salida de la consulta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c8aae-249">In this example, it’s using the same buffer for input and output from the property query.</span></span> <span data-ttu-id="c8aae-250">Esta es la razón por la que el búfer asignado tiene un tamaño de "desplazamiento de campo \_ ( \_ consulta de propiedad \_ de almacenamiento, AdditionalParameters) + sizeof ( \_ \_ datos específicos del Protocolo de almacenamiento \_ ) + NVME ( \_ tamaño máximo de registro) \_ \_ ".</span><span class="sxs-lookup"><span data-stu-id="c8aae-250">That’s why the buffer that was allocated has a size of “FIELD\_OFFSET(STORAGE\_PROPERTY\_QUERY, AdditionalParameters) + sizeof(STORAGE\_PROTOCOL\_SPECIFIC\_DATA) + NVME\_MAX\_LOG\_SIZE”.</span></span> <span data-ttu-id="c8aae-251">Aunque se podrían asignar búferes independientes para la entrada y la salida, se recomienda usar un solo búfer para consultar información relacionada con NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-251">Although separate buffers could be allocated for both input and output, we recommend using a single buffer to query NVMe related-information.</span></span>

### <a name="example-nvme-get-log-pages-query"></a><span data-ttu-id="c8aae-252">Ejemplo: consulta de las páginas de registro de NVMe</span><span class="sxs-lookup"><span data-stu-id="c8aae-252">Example: NVMe Get Log Pages query</span></span>

<span data-ttu-id="c8aae-253">En este ejemplo, basado en el anterior, la solicitud _ *Get log pages*\* se envía a una unidad de NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-253">In this example, based off of the previous one, the _ *Get Log Pages*\* request is sent to an NVMe drive.</span></span> <span data-ttu-id="c8aae-254">En el código siguiente se prepara la estructura de datos de consulta y, a continuación, se envía el comando al dispositivo a través de DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="c8aae-254">The following code prepares the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    ZeroMemory(buffer, bufferLength);  

    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  // This will be passed as the lower 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue2 = 0; // This will be passed as the higher 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue3 = 0; // This will be passed as Log Specific Identifier in CDW11.
    protocolData->ProtocolDataRequestSubValue4 = 0; // This will map to STORAGE_PROTOCOL_DATA_SUBVALUE_GET_LOG_PAGE definition, then user can pass Retain Asynchronous Event, Log Specific Field.

    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log failed. Error Code %d.\n"), GetLastError());
        goto exit;
    }

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < sizeof(NVME_HEALTH_INFO_LOG))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // SMART/Health Information Log Data 
    //
    {
        PNVME_HEALTH_INFO_LOG smartInfo = (PNVME_HEALTH_INFO_LOG)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log Data - Temperature %d.\n"), ((ULONG)smartInfo->Temperature[1] << 8 | smartInfo->Temperature[0]) - 273);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_SMART/Health Information Log succeeded_*_.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a><span data-ttu-id="c8aae-255">Ejemplo: consulta de funciones de búsqueda de NVMe</span><span class="sxs-lookup"><span data-stu-id="c8aae-255">Example: NVMe Get Features query</span></span>

<span data-ttu-id="c8aae-256">En este ejemplo, basado en el anterior, la solicitud _ *Get Features*\* se envía a una unidad de NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-256">In this example, based off of the previous one, the _ *Get Features*\* request is sent to an NVMe drive.</span></span> <span data-ttu-id="c8aae-257">En el código siguiente se prepara la estructura de datos de consulta y, a continuación, se envía el comando al dispositivo a través de DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="c8aae-257">The following code prepares the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    //  
    // Initialize query data structure to Volatile Cache feature.  
    //  

    ZeroMemory(buffer, bufferLength);  


    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeFeature;  
    protocolData->ProtocolDataRequestValue = NVME_FEATURE_VOLATILE_WRITE_CACHE;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = 0;  
    protocolData->ProtocolDataLength = 0;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache failed. Error Code %d.\n"), GetLastError());  
        goto exit;  
    }  

    //  
    // Validate the returned data.  
    //  

    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||  
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache  - data descriptor header not valid.\n"));  
        return;                                           
    }  

    //
    // Volatile Cache 
    //
    {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache - %x.\n"), protocolDataDescr->ProtocolSpecificData.FixedProtocolReturnData);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Get Feature - Volatile Cache succeeded_*_.\n"));
    }
```
## <a name="protocol-specific-set"></a><span data-ttu-id="c8aae-258">Conjunto específico del Protocolo</span><span class="sxs-lookup"><span data-stu-id="c8aae-258">Protocol-specific set</span></span>

<span data-ttu-id="c8aae-259">En Windows 10 19H1, el IOCTL_STORAGE_SET_PROPERTY se mejoró para admitir las características del conjunto de NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-259">From Windows 10 19H1, the IOCTL_STORAGE_SET_PROPERTY was enhanced to support NVMe Set Features.</span></span>

<span data-ttu-id="c8aae-260">El búfer de entrada del IOCTL_STORAGE_SET_PROPERTY se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="c8aae-260">The input buffer for the IOCTL_STORAGE_SET_PROPERTY is shown here:</span></span>

```C++
typedef struct _STORAGE_PROPERTY_SET {

    //
    // ID of the property being retrieved
    //

    STORAGE_PROPERTY_ID PropertyId;

    //
    // Flags indicating the type of set property being performed
    //

    STORAGE_SET_TYPE SetType;

    //
    // Space for additional parameters if necessary
    //

    UCHAR AdditionalParameters[1];

} STORAGE_PROPERTY_SET, _PSTORAGE_PROPERTY_SET;
```

<span data-ttu-id="c8aae-261">Al usar IOCTL_STORAGE_SET_PROPERTY para establecer la característica de NVMe, configure la estructura de STORAGE_PROPERTY_SET como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="c8aae-261">When using IOCTL_STORAGE_SET_PROPERTY to set NVMe feature, configure the STORAGE_PROPERTY_SET structure as follows:</span></span>

-   <span data-ttu-id="c8aae-262">Asigna un búfer que puede contener un STORAGE_PROPERTY_SET y una estructura de STORAGE_PROTOCOL_SPECIFIC_DATA_EXT;</span><span class="sxs-lookup"><span data-stu-id="c8aae-262">Allocate a buffer that can contains both a STORAGE_PROPERTY_SET and a STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure;</span></span>
-   <span data-ttu-id="c8aae-263">Establezca el campo PropertyID en StorageAdapterProtocolSpecificProperty o StorageDeviceProtocolSpecificProperty para una solicitud de controlador o dispositivo/espacio de nombres, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c8aae-263">Set the PropertyID field to StorageAdapterProtocolSpecificProperty or StorageDeviceProtocolSpecificProperty for a controller or device/namespace request, respectively.</span></span>
-   <span data-ttu-id="c8aae-264">Rellene la estructura de STORAGE_PROTOCOL_SPECIFIC_DATA_EXT con los valores deseados.</span><span class="sxs-lookup"><span data-stu-id="c8aae-264">Fill the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure with the desired values.</span></span> <span data-ttu-id="c8aae-265">El inicio del STORAGE_PROTOCOL_SPECIFIC_DATA_EXT es el campo AdditionalParameters de STORAGE_PROPERTY_SET.</span><span class="sxs-lookup"><span data-stu-id="c8aae-265">The start of the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT is the AdditionalParameters field of STORAGE_PROPERTY_SET.</span></span>

<span data-ttu-id="c8aae-266">Aquí se muestra la estructura de STORAGE_PROTOCOL_SPECIFIC_DATA_EXT.</span><span class="sxs-lookup"><span data-stu-id="c8aae-266">The STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure is shown here.</span></span>

```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA_EXT {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                   // The value will be protocol specific, as defined in STORAGE_PROTOCOL_NVME_DATA_TYPE or STORAGE_PROTOCOL_ATA_DATA_TYPE.

    ULONG   ProtocolDataValue;
    ULONG   ProtocolDataSubValue;      // Data sub request value

    ULONG   ProtocolDataOffset;         // The offset of data buffer is from beginning of this data structure.
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;
    ULONG   ProtocolDataSubValue2;     // First additional data sub request value

    ULONG   ProtocolDataSubValue3;     // Second additional data sub request value
    ULONG   ProtocolDataSubValue4;     // Third additional data sub request value

    ULONG   ProtocolDataSubValue5;     // Fourth additional data sub request value
    ULONG   Reserved[5];
} STORAGE_PROTOCOL_SPECIFIC_DATA_EXT, *PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
```

<span data-ttu-id="c8aae-267">Para especificar un tipo de característica de NVMe que se va a establecer, configure la STORAGE_PROTOCOL_SPECIFIC_DATA_EXT estructura de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c8aae-267">To specify a type of NVMe feature to set, configure the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure as follows:</span></span>
-   <span data-ttu-id="c8aae-268">Establezca el campo ProtocolType en ProtocolTypeNvme;</span><span class="sxs-lookup"><span data-stu-id="c8aae-268">Set the ProtocolType field to ProtocolTypeNvme;</span></span>
-   <span data-ttu-id="c8aae-269">Establezca el campo DataType en el valor de enumeración NVMeDataTypeFeature definido por STORAGE_PROTOCOL_NVME_DATA_TYPE;</span><span class="sxs-lookup"><span data-stu-id="c8aae-269">Set the DataType field to the enumeration value NVMeDataTypeFeature defined by STORAGE_PROTOCOL_NVME_DATA_TYPE;</span></span>

<span data-ttu-id="c8aae-270">En los siguientes ejemplos se muestra el conjunto de características de NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-270">The following examples demonstrate NVMe feature set.</span></span>

### <a name="example-nvme-set-features"></a><span data-ttu-id="c8aae-271">Ejemplo: características del conjunto de NVMe</span><span class="sxs-lookup"><span data-stu-id="c8aae-271">Example: NVMe Set Features</span></span>

<span data-ttu-id="c8aae-272">En este ejemplo, la solicitud Set Features se envía a una unidad de NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-272">In this example, the Set Features request is sent to an NVMe drive.</span></span> <span data-ttu-id="c8aae-273">En el código siguiente se prepara la estructura de datos establecida y, a continuación, se envía el comando al dispositivo a través de DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="c8aae-273">The following code prepares the set data structure and then sends the command down to the device via DeviceIoControl.</span></span>

```C++
            PSTORAGE_PROPERTY_SET                   setProperty = NULL;
            PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT     protocolData = NULL;
            PSTORAGE_PROTOCOL_DATA_DESCRIPTOR_EXT   protocolDataDescr = NULL;

            //
            // Allocate buffer for use.
            //
            bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_SET, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA_EXT);
            bufferLength += NVME_MAX_LOG_SIZE;

            buffer = new UCHAR[bufferLength];

            //
            // Initialize query data structure to get the desired log page.
            //
            ZeroMemory(buffer, bufferLength);

            setProperty = (PSTORAGE_PROPERTY_SET)buffer;

            setProperty->PropertyId = StorageAdapterProtocolSpecificProperty;
            setProperty->SetType = PropertyStandardSet;

            protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT)setProperty->AdditionalParameters;

            protocolData->ProtocolType = ProtocolTypeNvme;
            protocolData->DataType = NVMeDataTypeFeature;
            protocolData->ProtocolDataValue = NVME_FEATURE_HOST_CONTROLLED_THERMAL_MANAGEMENT;

            protocolData->ProtocolDataSubValue = 0; // This will pass to CDW11.
            protocolData->ProtocolDataSubValue2 = 0; // This will pass to CDW12.
            protocolData->ProtocolDataSubValue3 = 0; // This will pass to CDW13.
            protocolData->ProtocolDataSubValue4 = 0; // This will pass to CDW14.
            protocolData->ProtocolDataSubValue5 = 0; // This will pass to CDW15.

            protocolData->ProtocolDataOffset = 0;
            protocolData->ProtocolDataLength = 0;

            //
            // Send request down.
            //
            result = DeviceIoControl(m_deviceHandle,
                                     IOCTL_STORAGE_SET_PROPERTY,
                                     buffer,
                                     bufferLength,
                                     buffer,
                                     bufferLength,
                                     &returnedLength,
                                     NULL
            );
```

## <a name="temperature-queries"></a><span data-ttu-id="c8aae-274">Consultas de temperatura</span><span class="sxs-lookup"><span data-stu-id="c8aae-274">Temperature queries</span></span>

<span data-ttu-id="c8aae-275">En Windows 10, [**la \_ \_ \_ propiedad consulta de almacenamiento de ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) también se puede usar para consultar datos de temperatura de los dispositivos NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-275">In Windows 10, [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) can also be used to query temperature data from NVMe devices.</span></span>

<span data-ttu-id="c8aae-276">Para recuperar información de temperatura de una unidad de NVMe en el [**\_ \_ \_ descriptor de datos de temperatura de almacenamiento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configure la estructura de [**\_ \_ consulta de propiedades de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c8aae-276">To retrieve temperature information from an NVMe drive in the [**STORAGE\_TEMPERATURE\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configure the [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure as follows:</span></span>

-   <span data-ttu-id="c8aae-277">Asigna un búfer que puede contener una estructura de [**\_ \_ consulta de propiedades de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) .</span><span class="sxs-lookup"><span data-stu-id="c8aae-277">Allocate a buffer that can contains a [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure.</span></span>

-   <span data-ttu-id="c8aae-278">Establezca el campo **PropertyID** en **StorageAdapterTemperatureProperty** o **StorageDeviceTemperatureProperty** para una solicitud de controlador o dispositivo/espacio de nombres, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c8aae-278">Set the **PropertyID** field to **StorageAdapterTemperatureProperty** or **StorageDeviceTemperatureProperty** for a controller or device/namespace request, respectively.</span></span>

-   <span data-ttu-id="c8aae-279">Establezca el campo **QueryType** en **PropertyStandardQuery**.</span><span class="sxs-lookup"><span data-stu-id="c8aae-279">Set the **QueryType** field to **PropertyStandardQuery**.</span></span>

<span data-ttu-id="c8aae-280">Aquí se muestra la estructura de [**\_ \_ información de temperatura de almacenamiento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (desde Windows 10).</span><span class="sxs-lookup"><span data-stu-id="c8aae-280">The [**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) structure (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_TEMPERATURE_INFO {

    USHORT  Index;                      // Starts from 0. Index 0 may indicate a composite value.
    SHORT   Temperature;                // Signed value; in Celsius.
    SHORT   OverThreshold;              // Signed value; in Celsius.
    SHORT   UnderThreshold;             // Signed value; in Celsius.

    BOOLEAN OverThresholdChangable;     // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN UnderThresholdChangable;    // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN EventGenerated;             // Indicates that notification will be generated when temperature cross threshold.
    UCHAR   Reserved0;
    ULONG   Reserved1;

} STORAGE_TEMPERATURE_INFO, *PSTORAGE_TEMPERATURE_INFO;
```



## <a name="behavior-changing-commands"></a><span data-ttu-id="c8aae-281">Comandos de cambio de comportamiento</span><span class="sxs-lookup"><span data-stu-id="c8aae-281">Behavior changing commands</span></span>

<span data-ttu-id="c8aae-282">Los comandos que manipulan atributos de dispositivo o que pueden afectar al comportamiento del dispositivo son más difíciles de tratar con el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c8aae-282">Commands that manipulate device attributes or potentially impact device behavior are more difficult for the operating system to deal with.</span></span> <span data-ttu-id="c8aae-283">Si los atributos del dispositivo cambian en tiempo de ejecución mientras se procesan las operaciones de e/s, pueden surgir problemas de integridad de datos o de sincronización si no se administran correctamente.</span><span class="sxs-lookup"><span data-stu-id="c8aae-283">If device attributes change at run-time while I/O is being processed, synchronization or data integrity issues can arise if not properly handled.</span></span>

<span data-ttu-id="c8aae-284">El comando **set-Features** de NVMe es un buen ejemplo de un comando de cambio de comportamiento.</span><span class="sxs-lookup"><span data-stu-id="c8aae-284">The NVMe **Set-Features** command is a good example of a behavior changing command.</span></span> <span data-ttu-id="c8aae-285">Permite cambiar el mecanismo de arbitraje y la configuración de umbrales de temperatura.</span><span class="sxs-lookup"><span data-stu-id="c8aae-285">It allows for the changing of the arbitration mechanism and the setting of temperature thresholds.</span></span> <span data-ttu-id="c8aae-286">Para asegurarse de que los datos en vuelo no estén en riesgo cuando se envíen los comandos SET que afectan al comportamiento, Windows pausará todas las e/s en el dispositivo de NVMe, las colas de purga y los búferes de vaciado.</span><span class="sxs-lookup"><span data-stu-id="c8aae-286">To ensure that in-flight data is not at risk when behavior-affecting set commands are sent down, Windows will pause all I/O to the NVMe device, drain queues, and flush buffers.</span></span> <span data-ttu-id="c8aae-287">Una vez que el comando set se ha ejecutado correctamente, se reanuda la e/s (si es posible).</span><span class="sxs-lookup"><span data-stu-id="c8aae-287">Once the set command has executed successfully, I/O is resumed (if possible).</span></span> <span data-ttu-id="c8aae-288">Si no se puede reanudar la e/s, puede que sea necesario restablecer el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8aae-288">If I/O cannot be resumed, a device reset may be required.</span></span>

### <a name="setting-temperature-thresholds"></a><span data-ttu-id="c8aae-289">Configuración de umbrales de temperatura</span><span class="sxs-lookup"><span data-stu-id="c8aae-289">Setting temperature thresholds</span></span>

<span data-ttu-id="c8aae-290">Windows 10 presentó [**el \_ \_ umbral de \_ temperatura \_ del conjunto de almacenamiento ioctl**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), un ioctl para obtener y establecer umbrales de temperatura.</span><span class="sxs-lookup"><span data-stu-id="c8aae-290">Windows 10 introduced [**IOCTL\_STORAGE\_SET\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), an IOCTL for getting and setting temperature thresholds.</span></span> <span data-ttu-id="c8aae-291">También puede usarlo para obtener la temperatura actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8aae-291">You can also use it to get the current temperature of the device.</span></span> <span data-ttu-id="c8aae-292">El búfer de entrada y salida para este IOCTL es la estructura de [**\_ \_ información de temperatura de almacenamiento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) , de la sección de código anterior.</span><span class="sxs-lookup"><span data-stu-id="c8aae-292">The input/output buffer for this IOCTL is the [**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) structure, from the previous code section.</span></span>

### <a name="example-setting-over-threshold-temperature"></a><span data-ttu-id="c8aae-293">Ejemplo: establecer la temperatura supera el umbral</span><span class="sxs-lookup"><span data-stu-id="c8aae-293">Example: Setting over-threshold temperature</span></span>

<span data-ttu-id="c8aae-294">En este ejemplo, se establece la temperatura super del umbral de la unidad de NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-294">In this example, an NVMe drive's over-threshold temperature is set.</span></span> <span data-ttu-id="c8aae-295">El código siguiente prepara el comando y, a continuación, lo envía al dispositivo a través de DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="c8aae-295">The following code prepares the command and then sends it down to the device via DeviceIoControl.</span></span>


```C++
    BOOL    result;  
    ULONG   returnedLength = 0;  
    
    STORAGE_TEMPERATURE_THRESHOLD setThreshold = {0};  

    setThreshold.Version = sizeof(STORAGE_TEMPERATURE_THRESHOLD); 
    setThreshold.Size = sizeof(STORAGE_TEMPERATURE_THRESHOLD);  
    setThreshold.Flags = STORAGE_TEMPERATURE_THRESHOLD_FLAG_ADAPTER_REQUEST;  
    setThreshold.Index = SensorIndex;  
    setThreshold.Threshold = Threshold;  
    setThreshold.OverThreshold = UpdateOverThreshold; 

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD,  
                             &setThreshold,  
                             sizeof(STORAGE_TEMPERATURE_THRESHOLD),  
                             NULL,  
                             0,  
                             &returnedLength,  
                             NULL  
                             ); 

```



### <a name="setting-vendor-specific-features"></a><span data-ttu-id="c8aae-296">Configuración de características específicas del proveedor</span><span class="sxs-lookup"><span data-stu-id="c8aae-296">Setting vendor-specific features</span></span>

<span data-ttu-id="c8aae-297">Sin el registro de efectos de comando, el controlador no tiene conocimiento de las ramificaciones del comando.</span><span class="sxs-lookup"><span data-stu-id="c8aae-297">Without the Command Effects Log, the driver has no knowledge of the ramifications of the command.</span></span> <span data-ttu-id="c8aae-298">Este es el motivo por el que se requiere el registro de efectos de comando.</span><span class="sxs-lookup"><span data-stu-id="c8aae-298">This is why the Command Effects Log is required.</span></span> <span data-ttu-id="c8aae-299">Ayuda al sistema operativo a determinar si un comando tiene un gran impacto y si se puede enviar en paralelo con otros comandos a la unidad.</span><span class="sxs-lookup"><span data-stu-id="c8aae-299">It helps the operating system determine if a command is high impact and if it can be sent in parallel with other commands to the drive.</span></span>

<span data-ttu-id="c8aae-300">El registro de efectos de comando todavía no es suficientemente granular para abarcar los comandos **set-Features** específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c8aae-300">The Command Effects Log is not yet granular enough to encompass vendor-specific **Set-Features** commands.</span></span> <span data-ttu-id="c8aae-301">Por esta razón, todavía no es posible enviar comandos **set-Features** específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c8aae-301">For this reason, it is not yet possible to send vendor-specific **Set-Features** commands.</span></span> <span data-ttu-id="c8aae-302">Sin embargo, es posible usar el mecanismo de paso a través, descrito anteriormente, para enviar comandos específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c8aae-302">However, it is possible to use the pass-through mechanism, discussed earlier, to send vendor-specific commands.</span></span> <span data-ttu-id="c8aae-303">Para obtener más información, vea [mecanismo de paso a través](#pass-through-mechanism).</span><span class="sxs-lookup"><span data-stu-id="c8aae-303">For more info, see [Pass-through mechanism](#pass-through-mechanism).</span></span>

## <a name="header-files"></a><span data-ttu-id="c8aae-304">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c8aae-304">Header files</span></span>

<span data-ttu-id="c8aae-305">Los siguientes archivos son relevantes para el desarrollo de NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-305">The following files are relevant to NVMe development.</span></span> <span data-ttu-id="c8aae-306">Estos archivos se incluyen en el [Kit de desarrollo de software (SDK) de Microsoft Windows](https://developer.microsoft.com/windows/downloads).</span><span class="sxs-lookup"><span data-stu-id="c8aae-306">These files are included with the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads).</span></span>



| <span data-ttu-id="c8aae-307">Archivo de encabezado</span><span class="sxs-lookup"><span data-stu-id="c8aae-307">Header file</span></span>    | <span data-ttu-id="c8aae-308">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8aae-308">Description</span></span>                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8aae-309">**ntddstor. h**</span><span class="sxs-lookup"><span data-stu-id="c8aae-309">**ntddstor.h**</span></span> | <span data-ttu-id="c8aae-310">Define constantes y tipos para tener acceso a los controladores de clase de almacenamiento desde el modo kernel.</span><span class="sxs-lookup"><span data-stu-id="c8aae-310">Defines constants and types for accessing the storage class drivers from kernel mode.</span></span>   |
| <span data-ttu-id="c8aae-311">**nVMe. h**</span><span class="sxs-lookup"><span data-stu-id="c8aae-311">**nvme.h**</span></span>     | <span data-ttu-id="c8aae-312">Para otras estructuras de datos relacionadas con NVMe.</span><span class="sxs-lookup"><span data-stu-id="c8aae-312">For other NVMe-related data-structures.</span></span>                                                 |
| <span data-ttu-id="c8aae-313">**winioctl. h**</span><span class="sxs-lookup"><span data-stu-id="c8aae-313">**winioctl.h**</span></span> | <span data-ttu-id="c8aae-314">Para las definiciones de IOCTL de Win32 generales, incluidas las API de almacenamiento para aplicaciones de modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="c8aae-314">For overall Win32 IOCTL definitions, including storage APIs for user mode applications.</span></span> |



 

 

 
