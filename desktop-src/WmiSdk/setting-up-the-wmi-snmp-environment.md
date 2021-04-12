---
description: La comunicación con un dispositivo de red mediante la interfaz SNMP de WMI requiere la configuración del dispositivo, SNMP y los servicios WMI. La información de este tema explica cómo configurar el entorno de WMI SNMP.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Configuración del entorno SNMP de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeed470b1e38bf853bd6b023fa0f07b01c5df47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361444"
---
# <a name="setting-up-the-wmi-snmp-environment"></a><span data-ttu-id="a9035-104">Configuración del entorno SNMP de WMI</span><span class="sxs-lookup"><span data-stu-id="a9035-104">Setting up the WMI SNMP Environment</span></span>

<span data-ttu-id="a9035-105">La comunicación con un dispositivo de red mediante la interfaz SNMP de WMI requiere la configuración del dispositivo, SNMP y los servicios WMI.</span><span class="sxs-lookup"><span data-stu-id="a9035-105">Communicating with a network device using the WMI SNMP interface requires the configuration of the device, SNMP, and WMI services.</span></span> <span data-ttu-id="a9035-106">La información de este tema explica cómo configurar el entorno de WMI SNMP.</span><span class="sxs-lookup"><span data-stu-id="a9035-106">The information in this topic explains how to set up the WMI SNMP environment.</span></span>

<span data-ttu-id="a9035-107">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="a9035-107">The following sections are discussed in this topic:</span></span>

## <a name="installing-the-snmp-provider"></a><span data-ttu-id="a9035-108">Instalación del proveedor SNMP</span><span class="sxs-lookup"><span data-stu-id="a9035-108">Installing the SNMP Provider</span></span>

<span data-ttu-id="a9035-109">El servicio SNMP no está habilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a9035-109">The SNMP service is not enabled by default.</span></span> <span data-ttu-id="a9035-110">Puede habilitar el servicio SNMP y el proveedor SNMP de WMI a través del panel de control.</span><span class="sxs-lookup"><span data-stu-id="a9035-110">You can enable the SNMP service and the WMI SNMP Provider through the Control Panel.</span></span> <span data-ttu-id="a9035-111">Tenga en cuenta que el servicio SNMP debe estar habilitado y en ejecución para que el proveedor SNMP de WMI funcione.</span><span class="sxs-lookup"><span data-stu-id="a9035-111">Be aware that the SNMP service must be enabled and running for the WMI SNMP provider to work.</span></span>

<span data-ttu-id="a9035-112">A partir de Windows Vista, use el siguiente procedimiento para instalar el proveedor SNMP.</span><span class="sxs-lookup"><span data-stu-id="a9035-112">Starting with Windows Vista, use the following procedure to install the SNMP provider.</span></span>

<span data-ttu-id="a9035-113">**Para instalar el proveedor SNMP**</span><span class="sxs-lookup"><span data-stu-id="a9035-113">**To install the SNMP Provider**</span></span>

1.  <span data-ttu-id="a9035-114">En el **Panel de control**, seleccione **programas**.</span><span class="sxs-lookup"><span data-stu-id="a9035-114">From the **Control Panel**, select **Programs**.</span></span>
2.  <span data-ttu-id="a9035-115">En **programas y características**, seleccione **activar o desactivar las características de Windows**.</span><span class="sxs-lookup"><span data-stu-id="a9035-115">Under **Programs and Features**, select **Turn Windows features on or off**.</span></span>
3.  <span data-ttu-id="a9035-116">En la lista características de Windows, desplácese hacia abajo hasta la **característica SNMP** y expanda la lista para que pueda ver el **proveedor SNMP de WMI**.</span><span class="sxs-lookup"><span data-stu-id="a9035-116">In the Windows features list, scroll down to **SNMP feature** and expand the list so that you can see **WMI SNMP Provider**.</span></span>
4.  <span data-ttu-id="a9035-117">Active la casilla correspondiente al **proveedor SNMP de WMI**.</span><span class="sxs-lookup"><span data-stu-id="a9035-117">Select the check box for **WMI SNMP Provider**.</span></span> <span data-ttu-id="a9035-118">La casilla de la **característica SNMP** se selecciona automáticamente porque el proveedor requiere SNMP.</span><span class="sxs-lookup"><span data-stu-id="a9035-118">The check box for **SNMP feature** is selected automatically because the provider requires SNMP.</span></span>
5.  <span data-ttu-id="a9035-119">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9035-119">Click **OK**.</span></span>
6.  <span data-ttu-id="a9035-120">En un símbolo del sistema o en el menú **Inicio** , ejecute Services. msc y asegúrese de que se ha iniciado el servicio SNMP.</span><span class="sxs-lookup"><span data-stu-id="a9035-120">From a command prompt or the **Start** menu, run Services.msc and ensure that the SNMP service is started.</span></span>

## <a name="creating-an-snmp-namespace"></a><span data-ttu-id="a9035-121">Crear un espacio de nombres SNMP</span><span class="sxs-lookup"><span data-stu-id="a9035-121">Creating an SNMP Namespace</span></span>

<span data-ttu-id="a9035-122">Un espacio de nombres SNMP define una vista de un dispositivo de red.</span><span class="sxs-lookup"><span data-stu-id="a9035-122">An SNMP namespace defines a view of a network device.</span></span>

> [!Note]  
> <span data-ttu-id="a9035-123">Para obtener más información acerca de la compatibilidad y la instalación de este componente en un sistema operativo específico, consulte [disponibilidad del sistema operativo de los componentes de WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="a9035-123">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

<span data-ttu-id="a9035-124">En el procedimiento siguiente se describe cómo crear un [*espacio de nombres*](gloss-n.md)WMI de SNMP.</span><span class="sxs-lookup"><span data-stu-id="a9035-124">The following procedure describes how to create an SNMP WMI [*namespace*](gloss-n.md).</span></span>

<span data-ttu-id="a9035-125">**Para crear un espacio de nombres SNMP**</span><span class="sxs-lookup"><span data-stu-id="a9035-125">**To create an SNMP namespace**</span></span>

1.  <span data-ttu-id="a9035-126">Cree una instancia de la clase de sistema de [**\_ \_ espacio de nombres**](--namespace.md) mediante la compilación de un archivo [*Managed Object Format*](gloss-m.md) . mof o mediante la [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a9035-126">Create an instance of the [**\_\_Namespace**](--namespace.md) system class either by compiling a [*Managed Object Format*](gloss-m.md) .mof file or by using the [COM API for WMI](com-api-for-wmi.md).</span></span>

    <span data-ttu-id="a9035-127">Para obtener más información, vea [Crear jerarquías en WMI](creating-hierarchies-within-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a9035-127">For more information, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

2.  <span data-ttu-id="a9035-128">Asocie los [*calificadores*](gloss-q.md) de proveedor SNMP con la definición de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="a9035-128">Associate SNMP provider [*qualifiers*](gloss-q.md) with the namespace definition.</span></span>

    <span data-ttu-id="a9035-129">Los calificadores de proveedor SNMP contienen información de contexto específica de la implementación y propiedades de transporte que definen cómo el proveedor SNMP obtiene acceso a un dispositivo SNMP.</span><span class="sxs-lookup"><span data-stu-id="a9035-129">The SNMP provider qualifiers contain implementation-specific context information and transport properties that define how the SNMP provider accesses an SNMP device.</span></span> <span data-ttu-id="a9035-130">Para obtener más información, consulte [**calificadores específicos del proveedor SNMP**](qualifiers-specific-to-the-snmp-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a9035-130">For more information, see [**Qualifiers Specific to the SNMP Provider**](qualifiers-specific-to-the-snmp-provider.md).</span></span>

3.  <span data-ttu-id="a9035-131">Use la herramienta de línea de comandos [MOFCOMP](mofcomp.md) para cargar el código MOF en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="a9035-131">Use the [mofcomp](mofcomp.md) command line tool to load the MOF code into the WMI repository.</span></span>

    <span data-ttu-id="a9035-132">Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="a9035-132">For more information, see [Compiling MOF files](compiling-mof-files.md).</span></span>

<span data-ttu-id="a9035-133">En el siguiente ejemplo de código MOF \\ se define el espacio de nombres SNMP con un subconjunto de los calificadores que se pueden asociar a un espacio de nombres SNMP.</span><span class="sxs-lookup"><span data-stu-id="a9035-133">The following MOF code example defines the \\snmp namespace with a subset of the qualifiers that can be associated with an SNMP namespace.</span></span>

``` syntax
// Load classes and instances into <\\.\root> namespace

#pragma namespace("\\\\.\\root")               

[ 
  AgentAddress( "localhost" ), 
  AgentReadCommunityName( "public"), 
  AgentWriteCommunityName( "private"), 
  AgentRetryCount( 1 ), 
  AgentRetryTimeout( 500 ), 
  AgentVarBindsPerPdu( 10 ),
  AgentFlowControlWindowSize ( 3 ) 
]

  instance of __Namespace
  {
      Name = "snmp" ;
  };
```

## <a name="inserting-snmp-mib-data-into-wmi"></a><span data-ttu-id="a9035-134">Inserción de datos MIB SNMP en WMI</span><span class="sxs-lookup"><span data-stu-id="a9035-134">Inserting SNMP MIB Data into WMI</span></span>

<span data-ttu-id="a9035-135">Como proveedor, el proveedor SNMP actúa como un puente entre los datos SNMP y las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="a9035-135">As a provider, the SNMP provider acts as a bridge between SNMP data and WMI classes.</span></span> <span data-ttu-id="a9035-136">Por lo tanto, debe tener clases en WMI que representen distintos aspectos de un dispositivo habilitado para SNMP.</span><span class="sxs-lookup"><span data-stu-id="a9035-136">Therefore, you must have classes in WMI that represent different aspects of an SNMP-enabled device.</span></span> <span data-ttu-id="a9035-137">Para ello, debe usar el compilador de módulos de información SNMP ([smi2smir](smi2smir.md)) para compilar la información de administración de SNMP desde el formato SNMP en las definiciones de esquema CIM equivalentes.</span><span class="sxs-lookup"><span data-stu-id="a9035-137">To do so, you must use the SNMP information module compiler ([smi2smir](smi2smir.md)) to compile SNMP management information from the SNMP format into the equivalent CIM schema definitions.</span></span> <span data-ttu-id="a9035-138">A continuación, puede dirigir la salida del compilador de información a una base de datos de esquema SNMP denominada "repositorio de información de módulos SNMP (SMIR)" o a varios tipos diferentes de archivos MOF.</span><span class="sxs-lookup"><span data-stu-id="a9035-138">You can then direct the output of the information compiler into an SNMP schema database called the "SNMP Module Information Repository (SMIR)" or to several different kinds of MOF files.</span></span>

<span data-ttu-id="a9035-139">El compilador se ejecuta en el modo de línea de comandos, utilizando un archivo MIB como entrada.</span><span class="sxs-lookup"><span data-stu-id="a9035-139">The compiler runs in the command-line mode, using one MIB file as input.</span></span> <span data-ttu-id="a9035-140">El siguiente comando carga el archivo MIB especificado en SMIR.</span><span class="sxs-lookup"><span data-stu-id="a9035-140">The following command loads the specified MIB file into the SMIR.</span></span>

<span data-ttu-id="a9035-141">\**smi2smir/a\*\*\*<MIB file>*</span><span class="sxs-lookup"><span data-stu-id="a9035-141">**smi2smir /a** *<MIB file>*</span></span>

## <a name="setting-up-snmp-communities"></a><span data-ttu-id="a9035-142">Configuración de comunidades SNMP</span><span class="sxs-lookup"><span data-stu-id="a9035-142">Setting Up SNMP Communities</span></span>

<span data-ttu-id="a9035-143">Como medida de seguridad, la comunidad SNMP "pública" no se crea de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a9035-143">As a security measure, the SNMP "public" community is not created by default.</span></span> <span data-ttu-id="a9035-144">Puede crear la comunidad como se describe en [configuración del registro de comunidades](/previous-versions/windows/embedded/ms907028(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="a9035-144">You can create the community as described in [Communities Registry Settings](/previous-versions/windows/embedded/ms907028(v=msdn.10)).</span></span> <span data-ttu-id="a9035-145">Si no tiene ninguna comunidad, cree la comunidad "pública" para tener acceso al proveedor SNMP.</span><span class="sxs-lookup"><span data-stu-id="a9035-145">If you do not have any community, then create the "public" community to access the SNMP provider.</span></span>

## <a name="generating-mof-files-from-mib-files"></a><span data-ttu-id="a9035-146">Generación de archivos MOF a partir de archivos MIB</span><span class="sxs-lookup"><span data-stu-id="a9035-146">Generating MOF Files from MIB Files</span></span>

<span data-ttu-id="a9035-147">Los siguientes comandos son un ejemplo de cómo generar archivos MOF a partir de los archivos MIB que se instalan cuando se instala el proveedor SNMP.</span><span class="sxs-lookup"><span data-stu-id="a9035-147">The following commands are an example of how to generate MOF files from the MIB files that are installed when the SNMP provider is installed.</span></span>

<span data-ttu-id="a9035-148">**CD** *% WINDIR% \\ system32 \\ WBEM \\ SNMP*</span><span class="sxs-lookup"><span data-stu-id="a9035-148">**cd** *%windir%\\system32\\wbem\\SNMP*</span></span>

<span data-ttu-id="a9035-149">**Smi2smir/g** *... \\ . \\ hostmib. MIB* **>** *hostmib. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-149">**Smi2smir /g** *..\\..\\hostmib.mib* **>** *hostmib.mof*</span></span>

<span data-ttu-id="a9035-150">**Smi2smir/g** *... \\ . \\ ipforwd. MIB* **>** *ipforwd. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-150">**Smi2smir /g** *..\\..\\ipforwd.mib* **>** *ipforwd.mof*</span></span>

<span data-ttu-id="a9035-151">**Smi2smir/g** *... \\ . \\ NIPX. MIB* **>** *NIPX. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-151">**Smi2smir /g** *..\\..\\nipx.mib* **>** *nipx.mof*</span></span>

<span data-ttu-id="a9035-152">**Smi2smir/g** *... \\ . \\ MIB \_ II. MIB* II. **>** *\_ MOF*</span><span class="sxs-lookup"><span data-stu-id="a9035-152">**Smi2smir /g** *..\\..\\mib\_ii.mib* **>** *mib\_ii.mof*</span></span>

<span data-ttu-id="a9035-153">**Smi2smir/g** *... \\ . \\ lmmib2. MIB* **>** *lmmib2. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-153">**Smi2smir /g** *..\\..\\lmmib2.mib* **>** *lmmib2.mof*</span></span>

<span data-ttu-id="a9035-154">**Smi2smir/g** *... \\ . \\ mcastmib. MIB* **>** *mcastmib. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-154">**Smi2smir /g** *..\\..\\mcastmib.mib* **>** *mcastmib.mof*</span></span>

<span data-ttu-id="a9035-155">**Smi2smir/g** *... \\ . \\ rfc2571. MIB* **>** *rfc2571. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-155">**Smi2smir /g** *..\\..\\rfc2571.mib* **>** *rfc2571.mof*</span></span>

<span data-ttu-id="a9035-156">**Smi2smir/g** *... \\ . \\ wfospf. MIB* **>** *wfospf. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-156">**Smi2smir /g** *..\\..\\wfospf.mib* **>** *wfospf.mof*</span></span>

<span data-ttu-id="a9035-157">**Smi2smir/g** *... \\ . \\ DHCP. MIB \\ . \\ ... msft. MIB* **>** *DHCP. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-157">**Smi2smir /g** *..\\..\\dhcp.mib..\\..\\msft.mib* **>** *dhcp.mof*</span></span>

<span data-ttu-id="a9035-158">**Smi2smir/g** *... \\ . \\ WINS. MIB \\ .. \\ .. msft. MIB* **>** *gana. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-158">**Smi2smir /g** *..\\..\\wins.mib..\\..\\msft.mib* **>** *wins.mof*</span></span>

<span data-ttu-id="a9035-159">**Smi2smir/g** *... \\ . \\ mipx. MIB \\ .. \\ .. msft. MIB* **>** *mipx. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-159">**Smi2smir /g** *..\\..\\mipx.mib..\\..\\msft.mib* **>** *mipx.mof*</span></span>

<span data-ttu-id="a9035-160">**Smi2smir/g** *... \\ . \\ mripsap. MIB \\ .. \\ .. msft. MIB* **>** *mripsap. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-160">**Smi2smir /g** *..\\..\\mripsap.mib..\\..\\msft.mib* **>** *mripsap.mof*</span></span>

<span data-ttu-id="a9035-161">**Smi2smir/g** *... \\ . \\ msipbtp. MIB \\ .. \\ .. msft. MIB* **>** *msipbtp. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-161">**Smi2smir /g** *..\\..\\msipbtp.mib..\\..\\msft.mib* **>** *msipbtp.mof*</span></span>

<span data-ttu-id="a9035-162">**Smi2smir/g** *... \\ . \\ msiprip2. MIB \\ .. \\ .. msft. MIB* **>** *msiprip2. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-162">**Smi2smir /g** *..\\..\\msiprip2.mib..\\..\\msft.mib* **>** *msiprip2.mof*</span></span>

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a><span data-ttu-id="a9035-163">Agregar archivos MOF de SNMP al repositorio WMI</span><span class="sxs-lookup"><span data-stu-id="a9035-163">Adding SNMP MOF Files to the WMI Repository</span></span>

<span data-ttu-id="a9035-164">Los siguientes comandos son un ejemplo de cómo agregar los archivos MOF que se generan desde los archivos MIB al repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="a9035-164">The following commands are an example of how to add the MOF files that are generated from the MIB files to the WMI repository.</span></span> <span data-ttu-id="a9035-165">Si desea agregar los archivos MOF a la lista de archivos que se van a restaurar automáticamente en una recuperación del [*repositorio WMI*](gloss-w.md) , agregue el marcador **-Autorrecuperación** al final de cada comando.</span><span class="sxs-lookup"><span data-stu-id="a9035-165">If you want to add the MOF files to the list of files to be automatically restored in a [*WMI repository*](gloss-w.md) recovery, add the **-AUTORECOVER** flag to the end of each command.</span></span> <span data-ttu-id="a9035-166">Para obtener más información acerca de la herramienta de línea de comandos de WMI Mofcomp.exe, consulte [**MOFCOMP**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="a9035-166">For more information about the WMI Mofcomp.exe command-line tool, see [**mofcomp**](mofcomp.md).</span></span>

<span data-ttu-id="a9035-167">**MOFCOMP** *hostmib. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-167">**mofcomp** *hostmib.mof*</span></span>

<span data-ttu-id="a9035-168">**MOFCOMP** *ipforwd. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-168">**mofcomp** *ipforwd.mof*</span></span>

<span data-ttu-id="a9035-169">**MOFCOMP** *NIPX. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-169">**mofcomp** *nipx.mof*</span></span>

<span data-ttu-id="a9035-170"> *MIB \_ II. mof* de MOFCOMP</span><span class="sxs-lookup"><span data-stu-id="a9035-170">**mofcomp** *mib\_ii.mof*</span></span>

<span data-ttu-id="a9035-171">**MOFCOMP** *lmmib2. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-171">**mofcomp** *lmmib2.mof*</span></span>

<span data-ttu-id="a9035-172">**MOFCOMP** *mcastmib. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-172">**mofcomp** *mcastmib.mof*</span></span>

<span data-ttu-id="a9035-173">**MOFCOMP** *rfc2571. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-173">**mofcomp** *rfc2571.mof*</span></span>

<span data-ttu-id="a9035-174">**MOFCOMP** *wfospf. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-174">**mofcomp** *wfospf.mof*</span></span>

<span data-ttu-id="a9035-175">**MOFCOMP** *DHCP. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-175">**mofcomp** *dhcp.mof*</span></span>

<span data-ttu-id="a9035-176">**MOFCOMP** *mipx. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-176">**mofcomp** *mipx.mof*</span></span>

<span data-ttu-id="a9035-177">**MOFCOMP** *mripsap. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-177">**mofcomp** *mripsap.mof*</span></span>

<span data-ttu-id="a9035-178">**MOFCOMP** *msipbtp. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-178">**mofcomp** *msipbtp.mof*</span></span>

<span data-ttu-id="a9035-179">**MOFCOMP** *msiprip2. mof*</span><span class="sxs-lookup"><span data-stu-id="a9035-179">**mofcomp** *msiprip2.mof*</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9035-180">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9035-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9035-181">Acceso a dispositivos SNMP</span><span class="sxs-lookup"><span data-stu-id="a9035-181">Accessing SNMP Devices</span></span>](accessing-snmp-devices.md)
</dt> </dl>

 

 
