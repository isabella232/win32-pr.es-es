---
description: Windows 8 y Windows Server 2012 presentan la posibilidad de que el software que se ejecuta en una máquina virtual detecte que se puede haber producido un evento de cambio de hora.
ms.assetid: 0793E46B-8464-425E-8C5B-77C14DA90004
title: Identificador de generación de máquina virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df6ecbb600dbc7ae2efe14d36cb17cc75816444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688353"
---
# <a name="virtual-machine-generation-identifier"></a><span data-ttu-id="780c0-103">Identificador de generación de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="780c0-103">Virtual machine generation identifier</span></span>

<span data-ttu-id="780c0-104">Windows 8 y Windows Server 2012 presentan la posibilidad de que el software que se ejecuta en una máquina virtual detecte que se puede haber producido un evento de cambio de hora.</span><span class="sxs-lookup"><span data-stu-id="780c0-104">Windows 8 and Windows Server 2012 introduce the ability for software that is running on a virtual machine to detect that a time shift event may have occurred.</span></span> <span data-ttu-id="780c0-105">Los eventos de cambio de hora pueden producirse como resultado de una aplicación de una instantánea de máquina virtual o de la restauración de una copia de seguridad de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="780c0-105">Time shift events can occur as a result of an application of a virtual machine snapshot or the restoration of a virtual machine backup.</span></span> <span data-ttu-id="780c0-106">Para obtener más información acerca de esta funcionalidad, consulte las notas del producto sobre el [identificador de generación de máquinas virtuales](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).</span><span class="sxs-lookup"><span data-stu-id="780c0-106">For more information about this functionality, see the [Virtual Machine Generation ID white paper](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="780c0-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="780c0-107">Prerequisites</span></span>

<span data-ttu-id="780c0-108">Para usar el identificador de generación de la máquina virtual desde dentro de una máquina virtual, la máquina virtual debe cumplir con lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="780c0-108">To use the virtual machine generation identifier from inside a virtual machine your virtual machine must conform to the following.</span></span>

-   <span data-ttu-id="780c0-109">La máquina virtual debe ejecutarse en un hipervisor que implementa la compatibilidad con los identificadores de generación de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="780c0-109">The virtual machine must be running on a hypervisor that implements support for virtual machine generation identifiers.</span></span> <span data-ttu-id="780c0-110">Actualmente, son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="780c0-110">Currently, these are the following:</span></span>
    -   <span data-ttu-id="780c0-111">Windows 8</span><span class="sxs-lookup"><span data-stu-id="780c0-111">Windows 8</span></span>
    -   <span data-ttu-id="780c0-112">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="780c0-112">Windows Server 2012</span></span>
    -   <span data-ttu-id="780c0-113">Microsoft Hyper-V Server 2012</span><span class="sxs-lookup"><span data-stu-id="780c0-113">Microsoft Hyper-V Server 2012</span></span>
-   <span data-ttu-id="780c0-114">La máquina virtual debe ejecutar un sistema operativo invitado que sea compatible con el identificador de generación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="780c0-114">The virtual machine must be running a guest operating system that has support for the virtual machine generation identifier.</span></span> <span data-ttu-id="780c0-115">Actualmente, son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="780c0-115">Currently, these are the following.</span></span>

    <span data-ttu-id="780c0-116">Los sistemas operativos siguientes tienen compatibilidad nativa con el identificador de generación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="780c0-116">The following operating systems have native support for the virtual machine generation identifier.</span></span>

    -   <span data-ttu-id="780c0-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="780c0-117">Windows 8</span></span>
    -   <span data-ttu-id="780c0-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="780c0-118">Windows Server 2012</span></span>
    -   

    <span data-ttu-id="780c0-119">Se puede usar el siguiente funcionamiento como sistema operativo invitado si están instalados los servicios de integración de Hyper-V de Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="780c0-119">The following operating can be used as the guest operating system if the Hyper-V integration services from Windows 8 or Windows Server 2012 are installed.</span></span>

    -   <span data-ttu-id="780c0-120">Windows Server 2008 R2 con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="780c0-120">Windows Server 2008 R2 with Service Pack 1 (SP1)</span></span>
    -   <span data-ttu-id="780c0-121">Windows 7 con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="780c0-121">Windows 7 with Service Pack 1 (SP1)</span></span>
    -   <span data-ttu-id="780c0-122">Windows Server 2008 con Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="780c0-122">Windows Server 2008 with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="780c0-123">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="780c0-123">Windows Server 2003 R2</span></span>
    -   <span data-ttu-id="780c0-124">Windows Server 2003 con Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="780c0-124">Windows Server 2003 with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="780c0-125">Windows Vista con Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="780c0-125">Windows Vista with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="780c0-126">Windows XP con Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="780c0-126">Windows XP with Service Pack 3 (SP3)</span></span>

## <a name="obtaining-the-virtual-machine-generation-identifier"></a><span data-ttu-id="780c0-127">Obtención del identificador de generación de la máquina virtual</span><span class="sxs-lookup"><span data-stu-id="780c0-127">Obtaining the virtual machine generation identifier</span></span>

<span data-ttu-id="780c0-128">Para obtener el identificador de generación de la máquina virtual mediante programación, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="780c0-128">To programmatically obtain the virtual machine generation identifier, perform the following steps.</span></span>

> [!Note]  
> <span data-ttu-id="780c0-129">Para que funcione correctamente, se debe ejecutar lo siguiente con privilegios de administrador o sistema.</span><span class="sxs-lookup"><span data-stu-id="780c0-129">The following must be run with administrator or system privileges to function correctly.</span></span>

 

1.  <span data-ttu-id="780c0-130">Incluya el archivo de encabezado "vmgenerationcounter. h" en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="780c0-130">Include header file "vmgenerationcounter.h" in your app.</span></span> <span data-ttu-id="780c0-131">El archivo de encabezado contiene estas definiciones:</span><span class="sxs-lookup"><span data-stu-id="780c0-131">The header file contains these definitions:</span></span>
    ```C++
    DEFINE_GUID(
        GUID_DEVINTERFACE_VM_GENCOUNTER,
        0x3ff2c92b, 
        0x6598, 
        0x4e60, 
        0x8e, 
        0x1c, 
        0x0c, 
        0xcf, 
        0x49, 
        0x27, 
        0xe3, 
        0x19);

    #define VM_GENCOUNTER_SYMBOLIC_LINK_NAME L"VmGenerationCounter"

    #define IOCTL_VMGENCOUNTER_READ CTL_CODE( \
        FILE_DEVICE_ACPI, \
        0x1, METHOD_BUFFERED, \
        FILE_READ_ACCESS | FILE_WRITE_ACCESS)

    typedef struct _VM_GENCOUNTER
    {
        ULONGLONG GenerationCount;
        ULONGLONG GenerationCountHigh;
    } VM_GENCOUNTER, *PVM_GENCOUNTER;
    ```

    

2.  <span data-ttu-id="780c0-132">Abra un identificador para el " \\ \\ . \\ VmGenerationCounter "dispositivo con la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="780c0-132">Open a handle to the "\\\\.\\VmGenerationCounter" device using the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="780c0-133">Como alternativa, puede usar el administrador de PnP para consumir el GUID de la interfaz de dispositivo **\_ DEVINTERFACE \_ VM \_ GENCOUNTER** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}).</span><span class="sxs-lookup"><span data-stu-id="780c0-133">Alternatively, you can use the PnP manager to consume the device interface **GUID\_DEVINTERFACE\_VM\_GENCOUNTER** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}).</span></span> <span data-ttu-id="780c0-134">Estos objetos no estarán presentes si la aplicación no se está ejecutando en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="780c0-134">These objects will not be present if the app is not running in a virtual machine.</span></span>
3.  <span data-ttu-id="780c0-135">Envíe el [**ioctl \_ VMGENCOUNTER \_ Read**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL al controlador para recuperar el identificador de generación.</span><span class="sxs-lookup"><span data-stu-id="780c0-135">Send the [**IOCTL\_VMGENCOUNTER\_READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL to the driver to retrieve the generation identifier.</span></span>

    <span data-ttu-id="780c0-136">Ioctl [**\_ VMGENCOUNTER \_ Read**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) ioctl funciona en uno de dos modos, *sondeo* e *impulsado por eventos*.</span><span class="sxs-lookup"><span data-stu-id="780c0-136">The [**IOCTL\_VMGENCOUNTER\_READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL operates in one of two modes, *polling*, and *event driven*.</span></span>

    <span data-ttu-id="780c0-137">Para emitir IOCTL en modo de sondeo, envíe el IOCTL con un búfer de entrada de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="780c0-137">To issue the IOCTL in polling mode, you submit the IOCTL with an input buffer of zero length.</span></span> <span data-ttu-id="780c0-138">En respuesta a esto, el controlador recupera el identificador de generación actual, lo escribe en el búfer de salida y completa el IOCTL.</span><span class="sxs-lookup"><span data-stu-id="780c0-138">In response to this, the driver retrieves the current generation identifier, writes it to the output buffer, and completes the IOCTL.</span></span>

    <span data-ttu-id="780c0-139">Para emitir IOCTL en modo basado en eventos, envíe el IOCTL con un búfer de entrada que contenga un identificador de generación existente.</span><span class="sxs-lookup"><span data-stu-id="780c0-139">To issue the IOCTL in event driven mode, submit the IOCTL with an input buffer that contains an existing generation identifier.</span></span> <span data-ttu-id="780c0-140">En respuesta a esto, el controlador espera hasta que el identificador de generación actual sea diferente del identificador de generación que se pasó.</span><span class="sxs-lookup"><span data-stu-id="780c0-140">In response to this, the driver waits until the current generation identifier becomes different from the generation identifier that was passed in.</span></span> <span data-ttu-id="780c0-141">Cuando cambia el identificador de generación, el controlador escribe el identificador de generación actual en el búfer de salida y completa el IOCTL.</span><span class="sxs-lookup"><span data-stu-id="780c0-141">When the generation identifier changes, the driver writes the current generation identifier to the output buffer and completes the IOCTL.</span></span>

    <span data-ttu-id="780c0-142">En ambos modos, el formato y la longitud del búfer de salida están dictados por la estructura [**\_ GENCOUNTER de la máquina virtual**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) .</span><span class="sxs-lookup"><span data-stu-id="780c0-142">In both modes, the format and length of the output buffer is dictated by the [**VM\_GENCOUNTER**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) structure.</span></span>

    <span data-ttu-id="780c0-143">El modo de sondeo es compatible con todos los sistemas operativos invitados enumerados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="780c0-143">Polling mode is supported on all of the guest operating systems listed above.</span></span> <span data-ttu-id="780c0-144">El modo basado en eventos solo se admite en Windows Vista con SP2, Windows Server 2008 con SP2 y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="780c0-144">Event driven mode is supported only on Windows Vista with SP2, Windows Server 2008 with SP2, and later operating systems.</span></span> <span data-ttu-id="780c0-145">En los sistemas operativos anteriores, se producirá **un error en el código \_ de \_** error cuando se emita en modo basado en eventos.</span><span class="sxs-lookup"><span data-stu-id="780c0-145">On earlier operating systems, the IOCTL will fail with the error code **ERROR\_NOT\_SUPPORTED** when issued in event driven mode.</span></span>

    <span data-ttu-id="780c0-146">Es posible que el identificador de generación cambie entre el momento en que lo recupera el controlador y el momento en que se completa el IOCTL.</span><span class="sxs-lookup"><span data-stu-id="780c0-146">It is possible for the generation identifier to change between the time that it is retrieved by the driver and the time the IOCTL is completed.</span></span> <span data-ttu-id="780c0-147">Esto puede dar lugar a que la aplicación cliente reciba datos obsoletos.</span><span class="sxs-lookup"><span data-stu-id="780c0-147">This can result in the client app receiving stale data.</span></span> <span data-ttu-id="780c0-148">Para evitar esto, la aplicación cliente puede usar el modo orientado a eventos para asegurarse de que obtendrá más información sobre las actualizaciones del identificador de generación.</span><span class="sxs-lookup"><span data-stu-id="780c0-148">To avoid this, the client app can use event driven mode to ensure that it will eventually learn about any updates to the generation identifier.</span></span> <span data-ttu-id="780c0-149">Tomando el identificador actual de la aplicación cliente como entrada, el modo basado en eventos evita posibles condiciones de carrera que harían que el autor de la llamada no pudiera recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="780c0-149">By taking the client app's current identifier as input, event driven mode avoids potential race conditions that would cause the caller to miss notifications.</span></span>

<span data-ttu-id="780c0-150">En el ejemplo de código siguiente se muestra cómo realizar las acciones anteriores para obtener el identificador de generación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="780c0-150">The following code example shows how to perform the above actions to obtain the virtual machine generation identifier.</span></span>

> [!Note]  
> <span data-ttu-id="780c0-151">El código siguiente se debe ejecutar con privilegios de administrador o sistema para que funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="780c0-151">The following code must be run with administrator or system privileges to function correctly.</span></span>

 


```C++
HRESULT GetVmCounter(bool fWaitForChange)
{
    BOOL success = FALSE;
    DWORD error = ERROR_SUCCESS;
    VM_GENCOUNTER vmCounterOutput = {0};
    DWORD size = 0;
    HANDLE handle = INVALID_HANDLE_VALUE;
    HRESULT hr = S_OK;

    handle = CreateFile(
        L"\\\\.\\" VM_GENCOUNTER_SYMBOLIC_LINK_NAME,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_EXISTING,
        0,
        NULL);

    if (handle == INVALID_HANDLE_VALUE)
    {
        error = GetLastError();

        wprintf(
            L"Unable to open device %s. Error code = %d.", 
            VM_GENCOUNTER_SYMBOLIC_LINK_NAME, 
            error);

        hr = HRESULT_FROM_WIN32(error);

        goto Cleanup;
    }

    /*
    Call into the driver. 

    Because the 4th parameter to DeviceIoControl (nInBufferSize) is zero, this 
    is a polling request rather than an event-driven request.
    */
    success = DeviceIoControl(
        handle,
        IOCTL_VMGENCOUNTER_READ,
        NULL,
        0,
        &vmCounterOutput,
        sizeof(vmCounterOutput),
        &size,
        NULL);

    if (!success)
    {
        error = GetLastError();

        wprintf(L"Call IOCTL_VMGENCOUNTER_READ failed with %d.", error);

        hr = HRESULT_FROM_WIN32(error);

        goto Cleanup;
    }

    wprintf(
        L"VmCounterValue: %I64x:%I64x",
        vmCounterOutput.GenerationCount,
        vmCounterOutput.GenerationCountHigh);

    if (fWaitForChange)
    {
        /*
        Call into the driver again in event-driven mode. DeviceIoControl won't 
        return until the generation identifier has changed.
        */
        success = DeviceIoControl(
            handle,
            IOCTL_VMGENCOUNTER_READ,
            &vmCounterOutput,
            sizeof(vmCounterOutput),
            &vmCounterOutput,
            sizeof(vmCounterOutput),
            &size,
            NULL);

        if (!success)
        {
            error = GetLastError();

            wprintf(L"Call IOCTL_VMGENCOUNTER_READ failed with %d.", error);

            hr = HRESULT_FROM_WIN32(error);

            goto Cleanup;
        }

        wprintf(
            L"VmCounterValue changed to: %I64x:%I64x",
            vmCounterOutput.GenerationCount,
            vmCounterOutput.GenerationCountHigh);
    }

Cleanup:

    if (handle != INVALID_HANDLE_VALUE)
    {
        CloseHandle(handle);
    }

    return hr;
};
```



## <a name="determining-if-a-time-shift-event-has-occurred"></a><span data-ttu-id="780c0-152">Determinar si se ha producido un evento de cambio de hora</span><span class="sxs-lookup"><span data-stu-id="780c0-152">Determining if a time shift event has occurred</span></span>

<span data-ttu-id="780c0-153">Después de obtener el identificador de generación de la máquina virtual, debe almacenarlo para su uso futuro.</span><span class="sxs-lookup"><span data-stu-id="780c0-153">After you have obtained the virtual machine generation identifier, you should store it for future use.</span></span> <span data-ttu-id="780c0-154">Antes de que la aplicación realice una operación dependiente del tiempo, como confirmar en una base de datos, debe volver a obtener el identificador de generación y compararlo con el valor almacenado.</span><span class="sxs-lookup"><span data-stu-id="780c0-154">Before your app performs a time-sensitive operation, such as committing to a database, you should re-obtain the generation identifier and compare it to the stored value.</span></span> <span data-ttu-id="780c0-155">Si el identificador ha cambiado, significa que se ha producido un evento de cambio de hora y que la aplicación debe actuar adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="780c0-155">If the identifier has changed, that means that a time shift event has occurred, and your app must act appropriately.</span></span>

 

 
