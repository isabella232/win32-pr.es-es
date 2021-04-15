---
title: Cómo llamar a un método WMI
description: El propósito principal de WMI es proporcionar acceso a las clases e instancias que representan los objetos de la red.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892561785280e78ecf29da1030883994990fc822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546099"
---
# <a name="how-to-call-a-wmi-method"></a><span data-ttu-id="9b482-103">Cómo llamar a un método WMI</span><span class="sxs-lookup"><span data-stu-id="9b482-103">How to call a WMI method</span></span>

<span data-ttu-id="9b482-104">El propósito principal de WMI es proporcionar acceso a las clases e instancias que representan los objetos de la red.</span><span class="sxs-lookup"><span data-stu-id="9b482-104">The main purpose of WMI is to provide access to classes and instances that represent objects on your network.</span></span> <span data-ttu-id="9b482-105">Los proveedores admiten estas clases e instancias.</span><span class="sxs-lookup"><span data-stu-id="9b482-105">These classes and instances are supported by providers.</span></span> <span data-ttu-id="9b482-106">Por ejemplo, todas las instancias de que representan dispositivos de hardware estándar en su empresa, como [**Win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) o [**la \_ impresora Win32**](/windows/desktop/CIMWin32Prov/win32-printer), son compatibles con el proveedor de Win32.</span><span class="sxs-lookup"><span data-stu-id="9b482-106">For example, all of the instances that represent standard hardware devices on your enterprise, such as [**Win32\_PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) or [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer), are supported by the Win32 provider.</span></span> <span data-ttu-id="9b482-107">Del mismo modo, puede tener acceso al registro de eventos a través del proveedor de registro de eventos y el registro a través del proveedor del registro.</span><span class="sxs-lookup"><span data-stu-id="9b482-107">Similarly, you can access the event log through the Event Log provider, and the registry through the Registry provider.</span></span>

<span data-ttu-id="9b482-108">Los métodos que WMI implementa en interfaces como [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) o objetos de scripting, como [**SWbemServices**](swbemservices.md), son principalmente para obtener y manipular de forma genérica los datos suministrados por cualquier proveedor.</span><span class="sxs-lookup"><span data-stu-id="9b482-108">The methods that WMI implements in interfaces such as [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) or scripting objects such as [**SWbemServices**](swbemservices.md), are primarily for generically obtaining and manipulating data supplied by any provider.</span></span> <span data-ttu-id="9b482-109">Por ejemplo, use [**SWbemServices. instances**](swbemservices-instancesof.md) para obtener todas las instancias [**del \_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) en un subconjunto de equipos empresariales.</span><span class="sxs-lookup"><span data-stu-id="9b482-109">For example, use [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) to obtain all the instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) in a subset of enterprise computers.</span></span> <span data-ttu-id="9b482-110">Después, puede llamar al método de proveedor de Win32 [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) en cada objeto de **\_ proceso de Win32** .</span><span class="sxs-lookup"><span data-stu-id="9b482-110">You can then call the Win32 provider method [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) on each **Win32\_Process** object.</span></span>

<span data-ttu-id="9b482-111">En el ejemplo siguiente, se llama al método [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) como método de automatización en el objeto de proceso.</span><span class="sxs-lookup"><span data-stu-id="9b482-111">In the following example, the [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) method is called as an automation method on the Process object.</span></span> <span data-ttu-id="9b482-112">También se podría llamar a un método WMI, como el método [**\_ path**](swbemobject-path-.md) definido para [**SWbemObject**](swbemobject.md) en el objeto **Process** .</span><span class="sxs-lookup"><span data-stu-id="9b482-112">A WMI method, such as the [**Path\_**](swbemobject-path-.md) method defined for [**SWbemObject**](swbemobject.md) could also be called on the **Process** object.</span></span>


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



<span data-ttu-id="9b482-113">El proceso real de usar los métodos de WMI es idéntico al uso de cualquier otra interfaz de automatización o COM de Windows.</span><span class="sxs-lookup"><span data-stu-id="9b482-113">The actual process of using the WMI methods is identical to using any other Windows COM or automation interface.</span></span> <span data-ttu-id="9b482-114">Para obtener más información, consulte [com](../cossdk/component-services-portal.md) y [crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="9b482-114">For more information, see [COM](../cossdk/component-services-portal.md) and [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span> <span data-ttu-id="9b482-115">Para obtener más información acerca de las interfaces que admite WMI, vea [API de com para WMI](com-api-for-wmi.md) y [API de scripting para WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="9b482-115">For more information about the interfaces that WMI supports, see [COM API for WMI](com-api-for-wmi.md) and [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

<span data-ttu-id="9b482-116">Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="9b482-116">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b482-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b482-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b482-118">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="9b482-118">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
