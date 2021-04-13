---
description: Se puede tener acceso a los dispositivos SNMP mediante la lectura o la escritura en su instancia de clase correspondiente en el SMIR de WMI (repositorio de información del módulo SNMP).
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: Leer y escribir en dispositivos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc25f384d499e16e19c5e909f7d091ea34f9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544830"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a><span data-ttu-id="6b36a-103">Leer y escribir en dispositivos SNMP</span><span class="sxs-lookup"><span data-stu-id="6b36a-103">Reading from and Writing to SNMP Devices</span></span>

<span data-ttu-id="6b36a-104">Se puede tener acceso a los dispositivos SNMP mediante la lectura o la escritura en su instancia de clase correspondiente en el SMIR de WMI (repositorio de información del módulo SNMP).</span><span class="sxs-lookup"><span data-stu-id="6b36a-104">SNMP devices can be accessed by reading from or writing to their corresponding class instance in the WMI SMIR (SNMP Module Information Repository).</span></span> <span data-ttu-id="6b36a-105">Cuando trabaje con varios dispositivos del mismo tipo, para mayor eficacia, cargue las MIB para un tipo de dispositivo SNMP en el SMIR.</span><span class="sxs-lookup"><span data-stu-id="6b36a-105">When you are working with multiple devices of the same type, for efficiency, load the MIBs for one SNMP device type into the SMIR.</span></span>

> [!Note]  
> <span data-ttu-id="6b36a-106">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="6b36a-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="6b36a-107">Seleccione una de las siguientes opciones para leer o escribir en cada tipo de dispositivo SNMP actualizando la información de contexto de la instancia antes de comunicarse con cada una de ellas.</span><span class="sxs-lookup"><span data-stu-id="6b36a-107">Select one of the following options to read to or write from each SNMP device type by updating the context information of the instance before communicating with each one.</span></span>

-   <span data-ttu-id="6b36a-108">Use un nombre DNS en lugar de la dirección IP al hacer referencia a un dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="6b36a-108">Use a DNS name instead of the IP address when referencing a specific device.</span></span>

    <span data-ttu-id="6b36a-109">En el ejemplo siguiente se muestra cómo usar el nombre DNS para un dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="6b36a-109">The following example shows how to use the DNS name for a specific device.</span></span>

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   <span data-ttu-id="6b36a-110">Cree un espacio de nombres independiente y asocie una dirección de dispositivo al objeto de espacio de nombres mediante el calificador de instancia de AgentAddress para que el espacio de nombres esté enlazado permanentemente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b36a-110">Create a separate namespace and associate a device address to the namespace object using the AgentAddress instance qualifier so that the namespace is permanently bound to the device.</span></span> <span data-ttu-id="6b36a-111">En este caso, no es necesario especificar la información del objeto de contexto.</span><span class="sxs-lookup"><span data-stu-id="6b36a-111">In this case, you need not specify the context object information.</span></span>
-   <span data-ttu-id="6b36a-112">Leer desde un dispositivo SNMP.</span><span class="sxs-lookup"><span data-stu-id="6b36a-112">Read from an SNMP device.</span></span>

    <span data-ttu-id="6b36a-113">En el ejemplo siguiente se realiza una operación get en una clase de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b36a-113">The following example performs a Get operation on a device class.</span></span>

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set objSet = objServices.ExecQuery _
        ("SELECT * FROM SNMP_NET_DEVICE_123 WHERE hdwr_idx>1",, _
          wbemFlagReturnWhenComplete)
    for each obj in objset 
      'do whatever 
    next
    ```

    

-   <span data-ttu-id="6b36a-114">Escribir en un dispositivo SNMP.</span><span class="sxs-lookup"><span data-stu-id="6b36a-114">Write to an SNMP device.</span></span>

    <span data-ttu-id="6b36a-115">En el siguiente ejemplo se realiza una operación SET en una clase Device.</span><span class="sxs-lookup"><span data-stu-id="6b36a-115">The following example performs a Set operation on a device class.</span></span>

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

<span data-ttu-id="6b36a-116">Las clases correlacionadas son aquellas a las que se sabe que un determinado dispositivo SNMP es compatible cuando se produce la enumeración.</span><span class="sxs-lookup"><span data-stu-id="6b36a-116">Correlated classes are those that a given SNMP device is known to support when enumeration occurs.</span></span> <span data-ttu-id="6b36a-117">La correlación afecta al conjunto de clases devueltas desde SMIR.</span><span class="sxs-lookup"><span data-stu-id="6b36a-117">Correlation affects the set of classes returned from the SMIR.</span></span> <span data-ttu-id="6b36a-118">La enumeración no correlacionada devuelve todas las clases presentes en el SMIR, independientemente de si el dispositivo las admite.</span><span class="sxs-lookup"><span data-stu-id="6b36a-118">Noncorrelated enumeration returns all classes present within the SMIR, regardless of whether the device supports them.</span></span> <span data-ttu-id="6b36a-119">Para obtener más información sobre el uso de técnicas de correlación de WMI, vea [correlación de clases SNMP de WMI](wmi-snmp-class-correlation.md).</span><span class="sxs-lookup"><span data-stu-id="6b36a-119">For more information about using WMI correlation techniques, see [WMI SNMP Class Correlation](wmi-snmp-class-correlation.md).</span></span>

 

 



