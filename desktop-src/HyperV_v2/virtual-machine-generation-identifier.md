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
# <a name="virtual-machine-generation-identifier"></a>Identificador de generación de máquina virtual

Windows 8 y Windows Server 2012 presentan la posibilidad de que el software que se ejecuta en una máquina virtual detecte que se puede haber producido un evento de cambio de hora. Los eventos de cambio de hora pueden producirse como resultado de una aplicación de una instantánea de máquina virtual o de la restauración de una copia de seguridad de una máquina virtual. Para obtener más información acerca de esta funcionalidad, consulte las notas del producto sobre el [identificador de generación de máquinas virtuales](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).

## <a name="prerequisites"></a>Requisitos previos

Para usar el identificador de generación de la máquina virtual desde dentro de una máquina virtual, la máquina virtual debe cumplir con lo siguiente.

-   La máquina virtual debe ejecutarse en un hipervisor que implementa la compatibilidad con los identificadores de generación de máquinas virtuales. Actualmente, son los siguientes:
    -   Windows 8
    -   Windows Server 2012
    -   Microsoft Hyper-V Server 2012
-   La máquina virtual debe ejecutar un sistema operativo invitado que sea compatible con el identificador de generación de la máquina virtual. Actualmente, son los siguientes.

    Los sistemas operativos siguientes tienen compatibilidad nativa con el identificador de generación de la máquina virtual.

    -   Windows 8
    -   Windows Server 2012
    -   

    Se puede usar el siguiente funcionamiento como sistema operativo invitado si están instalados los servicios de integración de Hyper-V de Windows 8 o Windows Server 2012.

    -   Windows Server 2008 R2 con Service Pack 1 (SP1)
    -   Windows 7 con Service Pack 1 (SP1)
    -   Windows Server 2008 con Service Pack 2 (SP2)
    -   Windows Server 2003 R2
    -   Windows Server 2003 con Service Pack 2 (SP2)
    -   Windows Vista con Service Pack 2 (SP2)
    -   Windows XP con Service Pack 3 (SP3)

## <a name="obtaining-the-virtual-machine-generation-identifier"></a>Obtención del identificador de generación de la máquina virtual

Para obtener el identificador de generación de la máquina virtual mediante programación, realice los pasos siguientes.

> [!Note]  
> Para que funcione correctamente, se debe ejecutar lo siguiente con privilegios de administrador o sistema.

 

1.  Incluya el archivo de encabezado "vmgenerationcounter. h" en la aplicación. El archivo de encabezado contiene estas definiciones:
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

    

2.  Abra un identificador para el " \\ \\ . \\ VmGenerationCounter "dispositivo con la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) . Como alternativa, puede usar el administrador de PnP para consumir el GUID de la interfaz de dispositivo **\_ DEVINTERFACE \_ VM \_ GENCOUNTER** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}). Estos objetos no estarán presentes si la aplicación no se está ejecutando en una máquina virtual.
3.  Envíe el [**ioctl \_ VMGENCOUNTER \_ Read**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL al controlador para recuperar el identificador de generación.

    Ioctl [**\_ VMGENCOUNTER \_ Read**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) ioctl funciona en uno de dos modos, *sondeo* e *impulsado por eventos*.

    Para emitir IOCTL en modo de sondeo, envíe el IOCTL con un búfer de entrada de longitud cero. En respuesta a esto, el controlador recupera el identificador de generación actual, lo escribe en el búfer de salida y completa el IOCTL.

    Para emitir IOCTL en modo basado en eventos, envíe el IOCTL con un búfer de entrada que contenga un identificador de generación existente. En respuesta a esto, el controlador espera hasta que el identificador de generación actual sea diferente del identificador de generación que se pasó. Cuando cambia el identificador de generación, el controlador escribe el identificador de generación actual en el búfer de salida y completa el IOCTL.

    En ambos modos, el formato y la longitud del búfer de salida están dictados por la estructura [**\_ GENCOUNTER de la máquina virtual**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) .

    El modo de sondeo es compatible con todos los sistemas operativos invitados enumerados anteriormente. El modo basado en eventos solo se admite en Windows Vista con SP2, Windows Server 2008 con SP2 y sistemas operativos posteriores. En los sistemas operativos anteriores, se producirá **un error en el código \_ de \_** error cuando se emita en modo basado en eventos.

    Es posible que el identificador de generación cambie entre el momento en que lo recupera el controlador y el momento en que se completa el IOCTL. Esto puede dar lugar a que la aplicación cliente reciba datos obsoletos. Para evitar esto, la aplicación cliente puede usar el modo orientado a eventos para asegurarse de que obtendrá más información sobre las actualizaciones del identificador de generación. Tomando el identificador actual de la aplicación cliente como entrada, el modo basado en eventos evita posibles condiciones de carrera que harían que el autor de la llamada no pudiera recibir notificaciones.

En el ejemplo de código siguiente se muestra cómo realizar las acciones anteriores para obtener el identificador de generación de la máquina virtual.

> [!Note]  
> El código siguiente se debe ejecutar con privilegios de administrador o sistema para que funcione correctamente.

 


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

Después de obtener el identificador de generación de la máquina virtual, debe almacenarlo para su uso futuro. Antes de que la aplicación realice una operación dependiente del tiempo, como confirmar en una base de datos, debe volver a obtener el identificador de generación y compararlo con el valor almacenado. Si el identificador ha cambiado, significa que se ha producido un evento de cambio de hora y que la aplicación debe actuar adecuadamente.

 

 
