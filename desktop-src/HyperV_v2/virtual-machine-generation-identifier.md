---
description: Windows 8 y Windows Server 2012 la capacidad de software que se ejecuta en una máquina virtual para detectar que se puede haber producido un evento de cambio de hora.
ms.assetid: 0793E46B-8464-425E-8C5B-77C14DA90004
title: Identificador de generación de máquinas virtuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d810a1a65e95f4dde0ccf9779b1e955f2630623e362ffbf94ab8ca36d51d116e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899015"
---
# <a name="virtual-machine-generation-identifier"></a>Identificador de generación de máquinas virtuales

Windows 8 y Windows Server 2012 la capacidad de software que se ejecuta en una máquina virtual para detectar que se puede haber producido un evento de cambio de hora. Los eventos de cambio de hora pueden producirse como resultado de una aplicación de una instantánea de máquina virtual o de la restauración de una copia de seguridad de máquina virtual. Para obtener más información sobre esta funcionalidad, consulte las white paper del identificador de [generación de máquinas virtuales](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).

## <a name="prerequisites"></a>Prerrequisitos

Para usar el identificador de generación de máquinas virtuales desde dentro de una máquina virtual, la máquina virtual debe ajustarse a lo siguiente.

-   La máquina virtual debe ejecutarse en un hipervisor que implemente la compatibilidad con identificadores de generación de máquinas virtuales. Actualmente, estos son los siguientes:
    -   Windows 8
    -   Windows Server 2012
    -   Microsoft Hyper-V Server 2012
-   La máquina virtual debe ejecutar un sistema operativo invitado que admita el identificador de generación de máquinas virtuales. Actualmente, estos son los siguientes.

    Los siguientes sistemas operativos tienen compatibilidad nativa con el identificador de generación de máquinas virtuales.

    -   Windows 8
    -   Windows Server 2012
    -   

    El siguiente funcionamiento se puede usar como sistema operativo invitado si los servicios de integración de Hyper-V Windows 8 o Windows Server 2012 están instalados.

    -   Windows Server 2008 R2 con Service Pack 1 (SP1)
    -   Windows 7 con Service Pack 1 (SP1)
    -   Windows Server 2008 con Service Pack 2 (SP2)
    -   Windows Server 2003 R2
    -   Windows Server 2003 con Service Pack 2 (SP2)
    -   Windows Vista con Service Pack 2 (SP2)
    -   Windows XP con Service Pack 3 (SP3)

## <a name="obtaining-the-virtual-machine-generation-identifier"></a>Obtención del identificador de generación de máquinas virtuales

Para obtener mediante programación el identificador de generación de máquinas virtuales, realice los pasos siguientes.

> [!Note]  
> Lo siguiente debe ejecutarse con privilegios de administrador o del sistema para funcionar correctamente.

 

1.  Incluya el archivo de encabezado "vmgenerationcounter.h" en la aplicación. El archivo de encabezado contiene estas definiciones:
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

    

2.  Abra un identificador para " \\ \\ . \\ VmGenerationCounter" mediante la [**función CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Como alternativa, puede usar el administrador de PnP para consumir la interfaz de dispositivo **GUID \_ DEVINTERFACE \_ VM \_ GENCOUNTER** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}). Estos objetos no estarán presentes si la aplicación no se ejecuta en una máquina virtual.
3.  Envíe [**ioCTL \_ VMGENCOUNTER \_ READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL al controlador para recuperar el identificador de generación.

    [**IOCTL \_ VMGENCOUNTER \_ READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL funciona en uno de los dos modos: *sondear* y *controlado por eventos.*

    Para emitir la IOCTL en modo de sondeo, envíe la IOCTL con un búfer de entrada de longitud cero. En respuesta a esto, el controlador recupera el identificador de generación actual, lo escribe en el búfer de salida y completa la IOCTL.

    Para emitir la IOCTL en modo controlado por eventos, envíe la IOCTL con un búfer de entrada que contenga un identificador de generación existente. En respuesta a esto, el controlador espera hasta que el identificador de generación actual sea diferente del identificador de generación que se pasó. Cuando cambia el identificador de generación, el controlador escribe el identificador de generación actual en el búfer de salida y completa la IOCTL.

    En ambos modos, el formato y la longitud del búfer de salida viene determinado por la estructura [**\_ GENCOUNTER de**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) la máquina virtual.

    El modo de sondeo se admite en todos los sistemas operativos invitados enumerados anteriormente. El modo controlado por eventos solo se admite en Windows Vista con SP2, Windows Server 2008 con SP2 y sistemas operativos posteriores. En sistemas operativos anteriores, la IOCTL producirá un error con el código de error **ERROR \_ NOT \_ SUPPORTED** cuando se emita en modo controlado por eventos.

    Es posible que el identificador de generación cambie entre el momento en que el controlador lo recupera y el momento en que se completa la IOCTL. Esto puede dar lugar a que la aplicación cliente reciba datos obsoletos. Para evitarlo, la aplicación cliente puede usar el modo controlado por eventos para asegurarse de que finalmente aprenderá sobre las actualizaciones del identificador de generación. Al tomar el identificador actual de la aplicación cliente como entrada, el modo controlado por eventos evita posibles condiciones de carrera que harían que el autor de la llamada pierda las notificaciones.

En el ejemplo de código siguiente se muestra cómo realizar las acciones anteriores para obtener el identificador de generación de máquinas virtuales.

> [!Note]  
> El código siguiente debe ejecutarse con privilegios de administrador o del sistema para funcionar correctamente.

 


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



## <a name="determining-if-a-time-shift-event-has-occurred"></a>Determinar si se ha producido un evento de cambio de hora

Una vez que haya obtenido el identificador de generación de máquinas virtuales, debe almacenarlo para su uso futuro. Antes de que la aplicación realice una operación de tiempo, como confirmar en una base de datos, debe volver a obtener el identificador de generación y compararlo con el valor almacenado. Si el identificador ha cambiado, significa que se ha producido un evento de cambio de hora y la aplicación debe actuar correctamente.

 

 
