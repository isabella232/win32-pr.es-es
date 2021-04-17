---
description: Muestra cómo usar las interfaces VSS para crear un proveedor de hardware VSS.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Herramienta y ejemplo de VssSampleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fceaa65b851e5469a3e82323da92d8bde0651a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696444"
---
# <a name="vsssampleprovider-tool-and-sample"></a><span data-ttu-id="4b48a-103">Herramienta y ejemplo de VssSampleProvider</span><span class="sxs-lookup"><span data-stu-id="4b48a-103">VssSampleProvider Tool and Sample</span></span>

<span data-ttu-id="4b48a-104">Muestra cómo usar las [interfaces](volume-shadow-copy-api-interfaces.md) VSS para crear un proveedor de hardware VSS.</span><span class="sxs-lookup"><span data-stu-id="4b48a-104">Shows how to use the VSS [interfaces](volume-shadow-copy-api-interfaces.md) to create a VSS hardware provider.</span></span>

> [!Note]  
> <span data-ttu-id="4b48a-105">La herramienta VssSampleProvider y el ejemplo se incluyen en el kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4b48a-105">The VssSampleProvider tool and sample are included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4b48a-106">Puede descargar el Windows SDK desde el [Kit de desarrollo de software (SDK) de Windows para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).</span><span class="sxs-lookup"><span data-stu-id="4b48a-106">You can download the Windows SDK from [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).</span></span>

 

<span data-ttu-id="4b48a-107">En la instalación de Windows SDK, la herramienta VssSampleProvider se puede encontrar en `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para Windows de 64 bits) y `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (para windows de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="4b48a-107">In the Windows SDK installation, the VssSampleProvider tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

> [!Note]  
> <span data-ttu-id="4b48a-108">Los proveedores de hardware solo se admiten en sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4b48a-108">Hardware providers are only supported on Windows Server operating systems.</span></span> <span data-ttu-id="4b48a-109">En un sistema operativo de cliente de Windows, puede compilar el ejemplo VssSampleProvider, pero no puede registrarlo como proveedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="4b48a-109">On a Windows Client operating system, you can compile the VssSampleProvider sample, but you can't register it as a hardware provider.</span></span>

 

<span data-ttu-id="4b48a-110">La herramienta VssSampleProvider consta de los siguientes archivos:</span><span class="sxs-lookup"><span data-stu-id="4b48a-110">The VssSampleProvider tool consists of the following files:</span></span>

-   <span data-ttu-id="4b48a-111">Virtualstorage.sys</span><span class="sxs-lookup"><span data-stu-id="4b48a-111">Virtualstorage.sys</span></span>
-   <span data-ttu-id="4b48a-112">Vstorcontrol.exe</span><span class="sxs-lookup"><span data-stu-id="4b48a-112">Vstorcontrol.exe</span></span>
-   <span data-ttu-id="4b48a-113">Vssampleprovider.dll</span><span class="sxs-lookup"><span data-stu-id="4b48a-113">Vssampleprovider.dll</span></span>
-   <span data-ttu-id="4b48a-114">Vstorinterface.dll</span><span class="sxs-lookup"><span data-stu-id="4b48a-114">Vstorinterface.dll</span></span>

<span data-ttu-id="4b48a-115">El ejemplo VssSampleProvider incluye los siguientes scripts de instalación y desinstalación:</span><span class="sxs-lookup"><span data-stu-id="4b48a-115">The VssSampleProvider sample includes the following installation and uninstallation scripts:</span></span>

-   <span data-ttu-id="4b48a-116">Install-sampleprovider. cmd</span><span class="sxs-lookup"><span data-stu-id="4b48a-116">Install-sampleprovider.cmd</span></span>
-   <span data-ttu-id="4b48a-117">Uninstall-sampleprovider. cmd</span><span class="sxs-lookup"><span data-stu-id="4b48a-117">Uninstall-sampleprovider.cmd</span></span>
-   <span data-ttu-id="4b48a-118">Registrar \_app.vbs</span><span class="sxs-lookup"><span data-stu-id="4b48a-118">Register\_app.vbs</span></span>

<span data-ttu-id="4b48a-119">**Para instalar y usar el ejemplo VssSampleProvider**</span><span class="sxs-lookup"><span data-stu-id="4b48a-119">**To install and use the VssSampleProvider sample**</span></span>

1.  <span data-ttu-id="4b48a-120">Vaya al directorio `Program Files (x86)\Windows Kits\8.0\bin\`.</span><span class="sxs-lookup"><span data-stu-id="4b48a-120">Navigate to the `Program Files (x86)\Windows Kits\8.0\bin\` directory.</span></span> <span data-ttu-id="4b48a-121">Este directorio contiene virtualstoragevss.sys y vstorcontrol.exe.</span><span class="sxs-lookup"><span data-stu-id="4b48a-121">This directory contains virtualstoragevss.sys and vstorcontrol.exe.</span></span>
2.  <span data-ttu-id="4b48a-122">Abra una ventana del símbolo del sistema en el directorio especificado.</span><span class="sxs-lookup"><span data-stu-id="4b48a-122">Open a command prompt window in the specified directory.</span></span>
3.  <span data-ttu-id="4b48a-123">Para instalar el controlador de almacenamiento virtual, en la ventana del símbolo del sistema, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="4b48a-123">To install the virtual storage driver, in the command prompt window, type the following command:</span></span>

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  <span data-ttu-id="4b48a-124">Para instalar el proveedor de ejemplo de VSS, en la ventana del símbolo del sistema, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="4b48a-124">To install the VSS sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  <span data-ttu-id="4b48a-125">Para crear un LUN virtual, haga lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="4b48a-125">To create a virtual LUN, do the following.</span></span>

    1.  <span data-ttu-id="4b48a-126">En la ventana del símbolo del sistema, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="4b48a-126">In the command prompt window, type the following command:</span></span>

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        <span data-ttu-id="4b48a-127">Este comando crea un LUN virtual cuyo identificador de almacenamiento es **proveedor de HW de ejemplo de VSS**.</span><span class="sxs-lookup"><span data-stu-id="4b48a-127">This command creates a virtual LUN whose storage identifier is **VSS Sample HW Provider**.</span></span> <span data-ttu-id="4b48a-128">Para crear LUN virtuales adicionales, repita este paso.</span><span class="sxs-lookup"><span data-stu-id="4b48a-128">To create additional virtual LUNs, repeat this step.</span></span>

        <span data-ttu-id="4b48a-129">El proveedor de ejemplo de VSS reconoce un LUN solo si el **proveedor de HW de ejemplo de VSS** forma parte del identificador de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="4b48a-129">The VSS sample provider recognizes a LUN only if **VSS Sample HW Provider** is a part of the storage identifier.</span></span> <span data-ttu-id="4b48a-130">Para obtener más información sobre el identificador de almacenamiento, consulte la siguiente entrada de blog.</span><span class="sxs-lookup"><span data-stu-id="4b48a-130">For more information about the storage identifier, see the following blog post.</span></span>

        [<span data-ttu-id="4b48a-131">LUN: resincronización con DiskShadow y almacenamiento virtual</span><span class="sxs-lookup"><span data-stu-id="4b48a-131">LUN - Resync with Diskshadow and Virtual Storage</span></span>](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  <span data-ttu-id="4b48a-132">En la ventana del símbolo del sistema, use diskpart.exe para formatear el disco virtual y asignarle una letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="4b48a-132">In the command prompt window, use diskpart.exe to format the virtual disk and assign a drive letter to it.</span></span>

        <span data-ttu-id="4b48a-133">Este es un script de ejemplo para ejecutar en el símbolo del sistema de Diskpart.</span><span class="sxs-lookup"><span data-stu-id="4b48a-133">Here is a sample script to run at the diskpart command prompt.</span></span>

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  <span data-ttu-id="4b48a-134">Para ejecutar el proveedor de ejemplo, en la ventana del símbolo del sistema, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="4b48a-134">To run the sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    <span data-ttu-id="4b48a-135">*<drive>* representa la letra de unidad del LUN virtual.</span><span class="sxs-lookup"><span data-stu-id="4b48a-135">*<drive>* represents the drive letter of the virtual LUN.</span></span>

7.  <span data-ttu-id="4b48a-136">Para desinstalar el proveedor de ejemplo de VSS, en la ventana del símbolo del sistema, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="4b48a-136">To uninstall the VSS sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  <span data-ttu-id="4b48a-137">Para desinstalar el controlador de almacenamiento virtual, en la ventana del símbolo del sistema, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="4b48a-137">To uninstall the virtual storage driver, in the command prompt window, type the following command:</span></span>

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



