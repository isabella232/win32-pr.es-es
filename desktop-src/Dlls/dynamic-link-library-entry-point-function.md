---
description: Un archivo DLL puede especificar opcionalmente una función de punto de entrada.
ms.assetid: ec035fc6-0a6f-4e52-a4cc-8d7a25a94366
title: Dynamic-Link biblioteca Entry-Point función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62bff557bfa2aa792b420e8fe1856bbe0726921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811480"
---
# <a name="dynamic-link-library-entry-point-function"></a>Dynamic-Link biblioteca Entry-Point función

Un archivo DLL puede especificar opcionalmente una función de punto de entrada. Si está presente, el sistema llama a la función de punto de entrada cada vez que un proceso o subproceso carga o descarga el archivo DLL. Se puede usar para realizar tareas sencillas de inicialización y limpieza. Por ejemplo, puede configurar el almacenamiento local de subprocesos cuando se crea un nuevo subproceso y limpiarlo cuando se termina el subproceso.

Si va a vincular el archivo DLL con la biblioteca en tiempo de ejecución de C, puede proporcionar una función de punto de entrada y permitirle proporcionar una función de inicialización independiente. Consulte la documentación de la biblioteca en tiempo de ejecución para obtener más información.

Si proporciona su propio punto de entrada, vea la función [**DllMain**](dllmain.md) . El nombre **DllMain** es un marcador de posición para una función definida por el usuario. Debe especificar el nombre real que utilizará al compilar el archivo DLL. Para obtener más información, consulte la documentación que se incluye con las herramientas de desarrollo.

## <a name="calling-the-entry-point-function"></a>Llamar a la función Entry-Point

El sistema llama a la función de punto de entrada cuando se produce cualquiera de los siguientes eventos:

-   Un proceso carga el archivo DLL. Para los procesos que usan la vinculación dinámica en tiempo de carga, el archivo DLL se carga durante la inicialización del proceso. Para los procesos que usan la vinculación en tiempo de ejecución, el archivo DLL se carga antes de que se devuelva [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) .
-   Un proceso descarga el archivo DLL. El archivo DLL se descarga cuando finaliza el proceso o llama a la función [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) y el recuento de referencias se convierte en cero. Si el proceso finaliza como resultado de la función [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) o [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) , el sistema no llama a la función de punto de entrada del archivo dll.
-   Se crea un nuevo subproceso en un proceso que ha cargado el archivo DLL. Puede usar la función [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) para deshabilitar la notificación cuando se crean subprocesos.
-   Un subproceso de un proceso que ha cargado el archivo DLL finaliza con normalidad, sin usar [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) o [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Cuando un proceso descarga el archivo DLL, solo se llama una vez a la función de punto de entrada para todo el proceso, en lugar de una vez por cada subproceso existente del proceso. Puede usar [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) para deshabilitar la notificación cuando finalicen los subprocesos.

Solo un subproceso a la vez puede llamar a la función de punto de entrada.

El sistema llama a la función de punto de entrada en el contexto del proceso o subproceso que provocó la llamada a la función. Esto permite a un archivo DLL utilizar su función de punto de entrada para asignar memoria en el espacio de direcciones virtuales del proceso de llamada o para abrir identificadores accesibles para el proceso. La función de punto de entrada también puede asignar memoria que es privada para un nuevo subproceso mediante el almacenamiento local de subprocesos (TLS). Para obtener más información sobre el almacenamiento local de subprocesos, vea [almacenamiento local para el subproceso](/windows/desktop/ProcThread/thread-local-storage).

## <a name="entry-point-function-definition"></a>Definición de la función Entry-Point

La función de punto de entrada de DLL se debe declarar con la Convención de llamada de llamada estándar. Si el punto de entrada de DLL no se ha declarado correctamente, no se cargará el archivo DLL y el sistema mostrará un mensaje que indica que el punto de entrada de DLL debe declararse con WINAPI.

En el cuerpo de la función, puede controlar cualquier combinación de los siguientes escenarios en los que se ha llamado al punto de entrada de la DLL:

-   Un proceso carga el archivo DLL **( \_ \_ adjuntar el proceso dll**).
-   El proceso actual crea un nuevo subproceso **( \_ \_ Asociación de subprocesos dll**).
-   Un subproceso se cierra normalmente (la **\_ \_ desasociación de subprocesos dll**).
-   Un proceso descarga el archivo DLL (**\_ \_ desasociar el proceso dll**).

La función de punto de entrada debe realizar solo tareas de inicialización simples. No debe llamar a la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (o a una función que llama a estas funciones), ya que esto puede crear bucles de dependencia en el orden de carga de dll. Esto puede dar lugar a que se utilice un archivo DLL antes de que el sistema ejecute su código de inicialización. Del mismo modo, la función de punto de entrada no debe llamar a la función [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) (o una función que llame a **FreeLibrary**) durante la terminación del proceso, ya que esto puede dar lugar a que se use un archivo dll después de que el sistema haya ejecutado su código de finalización.

Dado que se garantiza la carga de Kernel32.dll en el espacio de direcciones de proceso cuando se llama a la función de punto de entrada, al llamar a funciones en Kernel32.dll no se usa el archivo DLL antes de que se haya ejecutado el código de inicialización. Por lo tanto, la función de punto de entrada puede crear [objetos de sincronización](/windows/desktop/Sync/synchronization-objects) , como secciones críticas y exclusiones mutuas, y usar TLS, ya que estas funciones se encuentran en Kernel32.dll. No es seguro llamar a las funciones del registro, por ejemplo, porque se encuentran en Advapi32.dll.

Llamar a otras funciones puede provocar problemas difíciles de diagnosticar. Por ejemplo, llamar a funciones de usuario, Shell y COM puede producir errores de infracción de acceso, ya que algunas funciones de sus archivos dll llaman a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar otros componentes del sistema. Por el contrario, llamar a esas funciones durante la terminación puede provocar errores de infracción de acceso porque es posible que el componente correspondiente ya se haya descargado o no inicializado.

En el ejemplo siguiente se muestra cómo estructurar la función de punto de entrada de DLL.

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

Cuando se llama a una función de punto de entrada de DLL porque se está cargando un proceso, la función devuelve **true** para indicar que la operación se ha realizado correctamente. En el caso de los procesos que usan la vinculación de tiempo de carga, un valor devuelto de **false** hace que se produzca un error en la inicialización del proceso y el proceso finalice. Para los procesos que usan la vinculación en tiempo de ejecución, un valor devuelto de FALSE hace que la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) devuelva **null**, lo que indica un error. (El sistema llama inmediatamente a la función de punto de entrada con la **\_ \_ desasociación del proceso de dll** y descarga el archivo dll). El valor devuelto de la función de punto de entrada no se tiene en cuenta cuando se llama a la función por cualquier otro motivo.

 

 
