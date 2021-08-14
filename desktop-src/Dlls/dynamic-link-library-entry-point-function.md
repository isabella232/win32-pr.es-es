---
description: Opcionalmente, un archivo DLL puede especificar una función de punto de entrada.
ms.assetid: ec035fc6-0a6f-4e52-a4cc-8d7a25a94366
title: Dynamic-Link library Entry-Point Function
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6289f705a11dad58eca8b047ba469ee07320dedef762024cbfa04046a0677f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815843"
---
# <a name="dynamic-link-library-entry-point-function"></a>Dynamic-Link library Entry-Point Function

Opcionalmente, un archivo DLL puede especificar una función de punto de entrada. Si está presente, el sistema llama a la función de punto de entrada cada vez que un proceso o subproceso carga o descarga el archivo DLL. Se puede usar para realizar tareas sencillas de inicialización y limpieza. Por ejemplo, puede configurar el almacenamiento local de subprocesos cuando se crea un subproceso nuevo y limpiarlo cuando se termina el subproceso.

Si va a vincular el archivo DLL con la biblioteca en tiempo de ejecución de C, puede proporcionar una función de punto de entrada y permitirle proporcionar una función de inicialización independiente. Consulte la documentación de la biblioteca en tiempo de ejecución para obtener más información.

Si va a proporcionar su propio punto de entrada, consulte la [**función DllMain.**](dllmain.md) El nombre **DllMain es** un marcador de posición para una función definida por el usuario. Debe especificar el nombre real que usa al compilar el archivo DLL. Para más información, consulte la documentación incluida con las herramientas de desarrollo.

## <a name="calling-the-entry-point-function"></a>Llamar a la Entry-Point función

El sistema llama a la función de punto de entrada cada vez que se produce cualquiera de los siguientes eventos:

-   Un proceso carga el archivo DLL. Para los procesos que usan la vinculación dinámica en tiempo de carga, el archivo DLL se carga durante la inicialización del proceso. Para los procesos que usan la vinculación en tiempo de ejecución, el archivo DLL se carga antes de que [**se devuelva LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**o LoadLibraryEx.**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   Un proceso descarga el archivo DLL. El archivo DLL se descarga cuando el proceso finaliza o llama a la función [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) y el recuento de referencias se convierte en cero. Si el proceso finaliza como resultado de las funciones [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) o [**TerminateThread,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) el sistema no llama a la función de punto de entrada dll.
-   Se crea un nuevo subproceso en un proceso que ha cargado el archivo DLL. Puede usar la función [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) para deshabilitar la notificación cuando se crean subprocesos.
-   Un subproceso de un proceso que ha cargado el archivo DLL finaliza normalmente, sin usar [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) o [**TerminateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) Cuando un proceso descarga el archivo DLL, se llama a la función de punto de entrada solo una vez para todo el proceso, en lugar de una vez para cada subproceso existente del proceso. Puede usar [**DisableThreadLibraryCalls para deshabilitar**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) la notificación cuando finalizan los subprocesos.

Solo un subproceso a la vez puede llamar a la función de punto de entrada.

El sistema llama a la función de punto de entrada en el contexto del proceso o subproceso que hizo que se llamara a la función. Esto permite que un archivo DLL use su función de punto de entrada para asignar memoria en el espacio de direcciones virtuales del proceso de llamada o para abrir los identificadores accesibles para el proceso. La función de punto de entrada también puede asignar memoria privada a un subproceso nuevo mediante el almacenamiento local de subprocesos (TLS). Para obtener más información sobre el almacenamiento local de subprocesos, vea [Thread Local Storage](/windows/desktop/ProcThread/thread-local-storage).

## <a name="entry-point-function-definition"></a>definición Entry-Point función

La función de punto de entrada dll debe declararse con la convención de llamada estándar. Si el punto de entrada dll no se declara correctamente, el archivo DLL no se carga y el sistema muestra un mensaje que indica que el punto de entrada de DLL debe declararse con WINAPI.

En el cuerpo de la función, puede controlar cualquier combinación de los siguientes escenarios en los que se ha llamado al punto de entrada del archivo DLL:

-   Un proceso carga el archivo DLL **(DLL \_ PROCESS \_ ATTACH**).
-   El proceso actual crea un nuevo subproceso **(DLL \_ THREAD \_ ATTACH**).
-   Un subproceso se cierra normalmente **(DLL \_ THREAD \_ DETACH**).
-   Un proceso descarga el archivo DLL **(DLL \_ PROCESS \_ DETACH**).

La función de punto de entrada solo debe realizar tareas de inicialización sencillas. No debe llamar a las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (o a una función que llama a estas funciones), ya que esto puede crear bucles de dependencia en el orden de carga de dll. Esto puede dar lugar a que se utilice un archivo DLL antes de que el sistema haya ejecutado su código de inicialización. De forma similar, la función de punto de entrada no debe llamar a la función [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) (o a una función que llama a **FreeLibrary)** durante la finalización del proceso, ya que esto puede dar lugar a que se utilice un archivo DLL después de que el sistema haya ejecutado su código de finalización.

Dado Kernel32.dll se garantiza que se cargue en el espacio de direcciones del proceso cuando se llama a la función de punto de entrada, la llamada a funciones de Kernel32.dll no da lugar a que el archivo DLL se utilice antes de que se haya ejecutado su código de inicialización. Por lo tanto, la [](/windows/desktop/Sync/synchronization-objects) función de punto de entrada puede crear objetos de sincronización, como secciones críticas y exclusiones mutuas, y usar TLS, ya que estas funciones se encuentran en Kernel32.dll. No es seguro llamar a las funciones del Registro, por ejemplo, porque se encuentran en Advapi32.dll.

Llamar a otras funciones puede dar lugar a problemas difíciles de diagnosticar. Por ejemplo, llamar a las funciones User, Shell y COM puede provocar errores de infracción de acceso, ya que algunas funciones de sus archivos DLL llaman a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar otros componentes del sistema. Por el contrario, llamar a esas funciones durante la finalización puede provocar errores de infracción de acceso porque es posible que el componente correspondiente ya se haya descargado o no inicializado.

En el ejemplo siguiente se muestra cómo estructurar la función de punto de entrada dll.

``` syntax
BOOL WINAPI DllMain(
    HINSTANCE hinstDLL,  // handle to DLL module
    DWORD fdwReason,     // reason for calling function
    LPVOID lpReserved )  // reserved
{
    // Perform actions based on the reason for calling.
    switch( fdwReason ) 
    { 
        case DLL_PROCESS_ATTACH:
         // Initialize once for each new process.
         // Return FALSE to fail DLL load.
            break;

        case DLL_THREAD_ATTACH:
         // Do thread-specific initialization.
            break;

        case DLL_THREAD_DETACH:
         // Do thread-specific cleanup.
            break;

        case DLL_PROCESS_DETACH:
         // Perform any necessary cleanup.
            break;
    }
    return TRUE;  // Successful DLL_PROCESS_ATTACH.
}
```

## <a name="entry-point-function-return-value"></a>Entry-Point valor devuelto de la función

Cuando se llama a una función de punto de entrada dll porque se está cargando un proceso, la función devuelve **TRUE** para indicar que se ha hecho correctamente. Para los procesos que usan la vinculación en tiempo de carga, un valor devuelto **de FALSE** hace que se produce un error en la inicialización del proceso y el proceso finaliza. Para los procesos que usan la vinculación en tiempo de ejecución, un valor devuelto de FALSE hace que las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) **devuelvan NULL,** lo que indica un error. (El sistema llama inmediatamente a la función de punto de entrada con **DLL \_ PROCESS \_ DETACH** y descarga el archivo DLL). El valor devuelto de la función de punto de entrada se ignora cuando se llama a la función por cualquier otro motivo.

 

 
