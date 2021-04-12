---
title: Servicios de Escritorio remoto clases de configuración
description: El proveedor WMI de configuración de Servicios de Escritorio remoto proporciona las siguientes clases. A continuación se muestra una ilustración.
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc9c58be85b8b4efc35495f35902ab67b35ad153
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420759"
---
# <a name="remote-desktop-services-configuration-classes"></a><span data-ttu-id="84435-104">Servicios de Escritorio remoto clases de configuración</span><span class="sxs-lookup"><span data-stu-id="84435-104">Remote Desktop Services Configuration classes</span></span>

<span data-ttu-id="84435-105">El proveedor WMI de configuración de Servicios de Escritorio remoto proporciona las siguientes clases.</span><span class="sxs-lookup"><span data-stu-id="84435-105">The Remote Desktop Services Configuration WMI provider provides the following classes.</span></span> <span data-ttu-id="84435-106">A continuación se muestra una ilustración.</span><span class="sxs-lookup"><span data-stu-id="84435-106">An illustration follows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="84435-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="84435-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="84435-108">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="84435-108">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dd>

<span data-ttu-id="84435-109">Representa la asociación entre los elementos del sistema administrados y la clase de configuración definida para ellos.</span><span class="sxs-lookup"><span data-stu-id="84435-109">Represents the association between managed system elements and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-110">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="84435-110">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dd>

<span data-ttu-id="84435-111">La clase base para todos los componentes del sistema que representan componentes del sistema abstractos, como perfiles, procesos o capacidades del sistema, en forma de dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="84435-111">The base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-112">**ManagedSystemElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84435-112">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dd>

<span data-ttu-id="84435-113">La clase base para la jerarquía de elementos del sistema.</span><span class="sxs-lookup"><span data-stu-id="84435-113">The base class for the system element hierarchy.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-114">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84435-114">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dd>

<span data-ttu-id="84435-115">Representa los parámetros operativos y relacionados con la configuración de uno o más elementos del sistema administrados.</span><span class="sxs-lookup"><span data-stu-id="84435-115">Represents configuration-related and operational parameters for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-116">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="84435-116">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dd>

<span data-ttu-id="84435-117">representa un terminal.</span><span class="sxs-lookup"><span data-stu-id="84435-117">represents a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-118">**Win32 \_ TerminalError**</span><span class="sxs-lookup"><span data-stu-id="84435-118">**Win32\_TerminalError**</span></span>](win32-terminalerror.md)
</dt> <dd>

<span data-ttu-id="84435-119">Representa un error de terminal.</span><span class="sxs-lookup"><span data-stu-id="84435-119">Represents a terminal error.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-120">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="84435-120">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dd>

<span data-ttu-id="84435-121">una subclase de la clase de [**\_ servicio de Win32**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="84435-121">a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class.</span></span> <span data-ttu-id="84435-122">[**Win32 \_ TerminalService**](win32-terminalservice.md) representa la propiedad de **elemento** de la Asociación [**\_ TerminalServiceToSetting de Win32**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="84435-122">[**Win32\_TerminalService**](win32-terminalservice.md) represents the **Element** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-123">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="84435-123">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dd>

<span data-ttu-id="84435-124">representa la configuración de un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="84435-124">represents the configuration for a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-125">**Win32 \_ TerminalServiceToSetting**</span><span class="sxs-lookup"><span data-stu-id="84435-125">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dd>

<span data-ttu-id="84435-126">representa la asociación entre una instancia de la clase [**Win32 \_ TerminalService**](win32-terminalservice.md) y el valor de una propiedad [**\_ TerminalServiceSetting de Win32**](win32-terminalservicesetting.md) determinada.</span><span class="sxs-lookup"><span data-stu-id="84435-126">represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and the setting of a particular [**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) property.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-127">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="84435-127">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dd>

<span data-ttu-id="84435-128">representa la configuración que se puede aplicar a un terminal.</span><span class="sxs-lookup"><span data-stu-id="84435-128">represents the settings that can be applied to a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-129">**Win32 \_ TerminalTerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="84435-129">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> <dd>

<span data-ttu-id="84435-130">representa la asociación entre un terminal y sus valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="84435-130">represents the association between a terminal and its configuration settings.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-131">**Win32 \_ TSAccount**</span><span class="sxs-lookup"><span data-stu-id="84435-131">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> <dd>

<span data-ttu-id="84435-132">permite la eliminación de una cuenta que existe en [**el \_ terminal Win32**](win32-terminal.md) y la modificación de los permisos existentes.</span><span class="sxs-lookup"><span data-stu-id="84435-132">allows deletion of an account that exists on the [**Win32\_Terminal**](win32-terminal.md) and modification of existing permissions.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-133">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="84435-133">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> <dd>

<span data-ttu-id="84435-134">define la configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) relacionada con la Directiva de conexión.</span><span class="sxs-lookup"><span data-stu-id="84435-134">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to connection policy.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-135">**Win32 \_ TSDiscoveredLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="84435-135">**Win32\_TSDiscoveredLicenseServer**</span></span>](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

<span data-ttu-id="84435-136">Proporciona detalles sobre el servidor de licencias Escritorio remoto detectado.</span><span class="sxs-lookup"><span data-stu-id="84435-136">Provides details about the discovered Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-137">**Win32 \_ TSEnvironmentSetting**</span><span class="sxs-lookup"><span data-stu-id="84435-137">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> <dd>

<span data-ttu-id="84435-138">define los valores de configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) , incluida la Directiva de programa inicial.</span><span class="sxs-lookup"><span data-stu-id="84435-138">defines the configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including initial program policy.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-139">**Win32 \_ TSGeneralSetting**</span><span class="sxs-lookup"><span data-stu-id="84435-139">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> <dd>

<span data-ttu-id="84435-140">representa la configuración general del terminal como el nivel de cifrado y el protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="84435-140">represents general settings of the terminal such as the encryption level and transport protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-141">**Win32 \_ TSLogonSetting**</span><span class="sxs-lookup"><span data-stu-id="84435-141">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> <dd>

<span data-ttu-id="84435-142">define la configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) relacionada con el inicio de sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="84435-142">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to client logon.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-143">**Win32 \_ TSNetworkAdapterListSetting**</span><span class="sxs-lookup"><span data-stu-id="84435-143">**Win32\_TSNetworkAdapterListSetting**</span></span>](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

<span data-ttu-id="84435-144">enumera la lista de adaptadores de red que se pueden configurar para un [**\_ terminal Win32**](win32-terminal.md), según el protocolo de terminal y el método de transporte especificados.</span><span class="sxs-lookup"><span data-stu-id="84435-144">enumerates the list of network adapters that can be configured for a [**Win32\_Terminal**](win32-terminal.md), based on the specified terminal protocol and transport method.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-145">**Win32 \_ TSNetworkAdapterSetting**</span><span class="sxs-lookup"><span data-stu-id="84435-145">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> <dd>

<span data-ttu-id="84435-146">define diversos valores de configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) , incluidas las propiedades relacionadas con el adaptador de red y el número máximo de conexiones permitidas.</span><span class="sxs-lookup"><span data-stu-id="84435-146">defines various configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including properties related to the network adapter and the maximum number of connections allowed.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-147">**Win32 \_ TSPermissionsSetting**</span><span class="sxs-lookup"><span data-stu-id="84435-147">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> <dd>

<span data-ttu-id="84435-148">incluye un método para agregar cuentas nuevas al terminal y un método para restaurar los permisos predeterminados en un terminal.</span><span class="sxs-lookup"><span data-stu-id="84435-148">includes a method to add new accounts to the terminal and a method to restore the default permissions to a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-149">**Win32 \_ TSRemoteControlSetting**</span><span class="sxs-lookup"><span data-stu-id="84435-149">**Win32\_TSRemoteControlSetting**</span></span>](win32-tsremotecontrolsetting.md)
</dt> <dd>

<span data-ttu-id="84435-150">define la configuración de control remoto para la clase de [**\_ terminal Win32**](win32-terminal.md) .</span><span class="sxs-lookup"><span data-stu-id="84435-150">defines the remote control configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-151">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="84435-151">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> <dd>

<span data-ttu-id="84435-152">Define los valores de configuración del agente de Conexión a Escritorio remoto (agente de conexión a escritorio remoto) para la clase [**\_ TSSessionDirectorySetting de Win32**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="84435-152">Defines the Remote Desktop Connection Broker (RD Connection Broker) configuration settings for the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-153">**Win32 \_ TSSessionDirectorySetting**</span><span class="sxs-lookup"><span data-stu-id="84435-153">**Win32\_TSSessionDirectorySetting**</span></span>](win32-tssessiondirectorysetting.md)
</dt> <dd>

<span data-ttu-id="84435-154">Representa la asociación entre una instancia de la clase [**Win32 \_ TerminalService**](win32-terminalservice.md) y una instancia de la clase [**\_ TSSessionDirectory de Win32**](win32-tssessiondirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="84435-154">Represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and an instance of the [**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-155">**Win32 \_ TSSessionSetting**</span><span class="sxs-lookup"><span data-stu-id="84435-155">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> <dd>

<span data-ttu-id="84435-156">define los valores de configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) , como los límites de tiempo, y las acciones de desconexión y reconexión.</span><span class="sxs-lookup"><span data-stu-id="84435-156">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class such as time-limits, and disconnection and reconnection actions.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-157">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="84435-157">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> <dd>

<span data-ttu-id="84435-158">Define la configuración de virtualización del Protocolo de Internet (IP) para un servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="84435-158">Defines Internet protocol (IP) virtualization settings for a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="84435-159">**Win32 \_ TSVirtualIPSetting**</span><span class="sxs-lookup"><span data-stu-id="84435-159">**Win32\_TSVirtualIPSetting**</span></span>](win32-tsvirtualipsetting.md)
</dt> <dd>

<span data-ttu-id="84435-160">Representa la asociación entre una clase de elemento de [**Win32 \_ TerminalService**](win32-terminalservice.md) y una clase de configuración [**\_ TSVirtualIP de Win32**](win32-tsvirtualip.md) .</span><span class="sxs-lookup"><span data-stu-id="84435-160">Represents the association between a [**Win32\_TerminalService**](win32-terminalservice.md) element class and a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) setting class.</span></span>

</dd> </dl>

<span data-ttu-id="84435-161">En la ilustración siguiente se muestran las relaciones entre estas clases.</span><span class="sxs-lookup"><span data-stu-id="84435-161">The following illustration shows the relationships between these classes.</span></span>

![las relaciones entre las clases admitidas](images/tswmi.png)

 

 