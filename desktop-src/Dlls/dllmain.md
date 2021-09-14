---
description: Punto de entrada opcional en una biblioteca de vínculos dinámicos (DLL). Cuando el sistema inicia o finaliza un proceso o subproceso, llama a la función de punto de entrada para cada archivo DLL cargado mediante el primer subproceso del proceso.
ms.assetid: 0c3e3083-9297-4626-b2a7-0062d1c2cf9e
title: Punto de entrada de DllMain (Process.h)
ms.topic: reference
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: ee182fd54f11909e54e98f827904f1da5e46f557
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063172"
---
# <a name="dllmain-entry-point"></a>Punto de entrada de DllMain

Punto de entrada opcional en una biblioteca de vínculos dinámicos (DLL). Cuando el sistema inicia o finaliza un proceso o subproceso, llama a la función de punto de entrada para cada archivo DLL cargado mediante el primer subproceso del proceso. El sistema también llama a la función de punto de entrada para un archivo DLL cuando se carga o descarga mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y FreeLibrary.**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)

## <a name="example"></a>Ejemplo

```cpp
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

Este es un ejemplo de la [biblioteca de vínculos dinámicos Entry-Point función](dynamic-link-library-entry-point-function.md).


> [!WARNING]
> Hay límites importantes sobre lo que se puede hacer de forma segura en un punto de entrada del archivo DLL. Consulte [Procedimientos recomendados generales](dynamic-link-library-best-practices.md) para obtener Windows API específicas que no son seguras para llamar a en DllMain. Si necesita algo más que la inicialización más sencilla, puede hacerlo en una función de inicialización para el archivo DLL. Puede requerir que las aplicaciones llamen a la función de inicialización después de ejecutar DllMain y antes de que llamen a cualquier otra función del archivo DLL.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI DllMain(
  _In_ HINSTANCE hinstDLL,
  _In_ DWORD     fdwReason,
  _In_ LPVOID    lpvReserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*prendstDLL* \[ En\]
</dt> <dd>

Identificador del módulo DLL. El valor es la dirección base del archivo DLL. El **HINSTANCE** de un archivo DLL es el mismo que el **HMODULE** del archivo DLL, por lo que se puede usar *en* llamadas a funciones que requieren un identificador de módulo.

</dd> <dt>

*fdwReason* \[ En\]
</dt> <dd>

Código de motivo que indica por qué se llama a la función de punto de entrada dll. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**DLL \_ ASOCIACIÓN \_ DE PROCESOS**</dt> <dt>1</dt> </dl> | El archivo DLL se carga en el espacio de direcciones virtuales del proceso actual como resultado del inicio del proceso o como resultado de una llamada a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). Los archivos DLL pueden usar esta oportunidad para inicializar cualquier dato de instancia o para usar la [**función TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para asignar un índice de almacenamiento local de subprocesos (TLS).<br/> El *parámetro lpReserved* indica si el archivo DLL se carga estática o dinámicamente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**DLL \_ PROCESS \_ DETACH**</dt> <dt>0</dt> </dl> | El archivo DLL se está descargando del espacio de direcciones virtuales del proceso de llamada porque se cargó incorrectamente o el recuento de referencias ha alcanzado cero (los procesos han finalizado o llamado a [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) una vez por cada vez que llamó [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).<br/> El *parámetro lpReserved* indica si el archivo DLL se está descargando como resultado de una llamada [**a FreeLibrary,**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) un error de carga o la terminación del proceso.<br/> El archivo DLL puede usar esta oportunidad para llamar a la función [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) a fin de liberar los índices TLS asignados mediante [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) y liberar los datos locales de cualquier subproceso.<br/> Tenga en cuenta que el subproceso que recibe la notificación **\_ DLL PROCESS \_ DETACH** no es necesariamente el mismo subproceso que recibió la notificación **DLL PROCESS \_ \_ ATTACH.**<br/> |
| <span id="DLL_THREAD_ATTACH"></span><span id="dll_thread_attach"></span><dl> <dt>**DLL \_ ASOCIACIÓN \_ DE SUBPROCESOS**</dt> <dt>2</dt> </dl>    | El proceso actual está creando un nuevo subproceso. Cuando esto sucede, el sistema llama a la función de punto de entrada de todos los archivos DLL asociados actualmente al proceso. La llamada se realiza en el contexto del nuevo subproceso. Los archivos DLL pueden usar esta oportunidad para inicializar una ranura TLS para el subproceso. Un subproceso que llama a la función de punto de entrada dll con **DLL \_ PROCESS \_ ATTACH** no llama a la función de punto de entrada dll **con DLL THREAD \_ \_ ATTACH**. <br/> Tenga en cuenta que solo los subprocesos creados después de cargar el archivo DLL cargan la función de punto de entrada de un archivo DLL con este valor. Cuando se carga un archivo DLL mediante [**LoadLibrary,**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)los subprocesos existentes no llaman a la función de punto de entrada del archivo DLL recién cargado.<br/>                                                                                                                                                                       |
| <span id="DLL_THREAD_DETACH"></span><span id="dll_thread_detach"></span><dl> <dt>**DLL \_ \_DESASOCIÓN DE SUBPROCESOS**</dt> <dt>3</dt> </dl>    | Un subproceso se cierra sin problemas. Si el archivo DLL ha almacenado un puntero a la memoria asignada en una ranura TLS, debe usar esta oportunidad para liberar la memoria. El sistema llama a la función de punto de entrada de todos los archivos DLL cargados actualmente con este valor. La llamada se realiza en el contexto del subproceso de salida.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*lpvReserved* \[ En\]
</dt> <dd>

Si *fdwReason es* **DLL PROCESS \_ \_ ATTACH,** *lpvReserved* es **NULL** para cargas dinámicas y no NULL para cargas estáticas.

Si *fdwReason* es **DLL PROCESS \_ \_ DETACH,** *lpvReserved* es **NULL** si se ha llamado a [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) o se ha realizado un error en la carga del archivo DLL y no es **NULL** si el proceso está finalizando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cuando el sistema llama a la **función DllMain** con el valor **DLL PROCESS \_ \_ ATTACH,** la función devuelve **TRUE** si se realiza correctamente o **FALSE** si se produce un error en la inicialización. Si el valor devuelto es **FALSE cuando** se llama **a DllMain** porque el proceso usa la [**función LoadLibrary,**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) **LoadLibrary** devuelve NULL. (El sistema llama inmediatamente a la función de punto de entrada con **DLL \_ PROCESS \_ DETACH** y descarga el archivo DLL). Si el valor devuelto es **FALSE cuando** se llama **a DllMain** durante la inicialización del proceso, el proceso finaliza con un error. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Cuando el sistema llama a **la función DllMain** con cualquier valor distinto de **DLL PROCESS \_ \_ ATTACH**, se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

**DllMain es** un marcador de posición para el nombre de la función definida por la biblioteca. Debe especificar el nombre real que usa al compilar el archivo DLL. Para más información, consulte la documentación incluida con las herramientas de desarrollo.

Durante el inicio del proceso inicial o después de una llamada a [**LoadLibrary,**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)el sistema examina la lista de archivos DLL cargados para el proceso. Para cada archivo DLL que aún no se haya llamado con el valor **\_ DLL PROCESS \_ ATTACH,** el sistema llama a la función de punto de entrada del archivo DLL. Esta llamada se realiza en el contexto del subproceso que hizo que el espacio de direcciones del proceso cambiara, como el subproceso principal del proceso o el subproceso que llamó **a LoadLibrary**. El sistema serializa el acceso al punto de entrada en todo el proceso. Los subprocesos *de DllMain* mantienen el bloqueo del cargador para que no se puedan cargar ni inicializar archivos DLL adicionales de forma dinámica.

Si la función de punto de entrada del archivo DLL devuelve FALSE después de una notificación **DLL \_ PROCESS \_ ATTACH,** recibe una notificación **DLL PROCESS \_ \_ DETACH** y el archivo DLL se descarga inmediatamente. Sin embargo, si el código **\_ DLL PROCESS \_ ATTACH** produce una excepción, la función de punto de entrada no recibirá la notificación **DLL PROCESS \_ \_ DETACH.**

Hay casos en los que se llama a la función de punto de entrada para un subproceso de terminación incluso si nunca se llamó a la función de punto de entrada con **DLL \_ THREAD \_ ATTACH** para el subproceso:

-   El subproceso era el subproceso inicial del proceso, por lo que el sistema llamó a la función de punto de entrada con el **valor \_ DLL PROCESS \_ ATTACH.**
-   El subproceso ya se estaba ejecutando cuando se realizó una llamada a la función [**LoadLibrary,**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) por lo que el sistema nunca llamó a la función de punto de entrada para ella.

Cuando se descarga un archivo DLL de un proceso como resultado de una carga incorrecta del archivo DLL, la finalización del proceso o una llamada a [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary), el sistema no llama a la función de punto de entrada del archivo DLL con el valor **\_ \_ DETACH DE** DLL THREAD para los subprocesos individuales del proceso. El archivo DLL solo se envía una **notificación DLL \_ PROCESS \_ DETACH.** Los archivos DLL pueden aprovechar esta oportunidad para limpiar todos los recursos de todos los subprocesos conocidos por el archivo DLL.

Al controlar **DLL \_ PROCESS \_ DETACH,** un archivo DLL debe liberar recursos como la memoria del montón solo si el archivo DLL se descarga dinámicamente (el *parámetro lpReserved* es **NULL).** Si el proceso está finalizando (el parámetro *lpvReserved* no es **NULL),** todos los subprocesos del proceso excepto el subproceso actual ya han terminado o se han terminado explícitamente mediante una llamada a la función [**ExitProcess,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) lo que podría dejar algunos recursos de proceso como montones en un estado incoherente. En este caso, no es seguro que el archivo DLL limpie los recursos. En su lugar, el archivo DLL debe permitir que el sistema operativo reclame la memoria.

Si finaliza un proceso mediante una llamada a [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) o [**TerminateJobObject**](/windows/desktop/api/jobapi2/nf-jobapi2-terminatejobobject), los archivos DLL de ese proceso no reciben notificaciones **\_ \_ DETACH de DLL** PROCESS. Si finaliza un subproceso mediante una llamada a [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread), los archivos DLL de ese subproceso no reciben notificaciones **DLL THREAD \_ \_ DETACH.**

La función de punto de entrada solo debe realizar tareas simples de inicialización o finalización. No debe llamar a las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (o a una función que llama a estas funciones), ya que esto puede crear bucles de dependencia en el orden de carga de dll. Esto puede dar lugar a que se utilice un archivo DLL antes de que el sistema haya ejecutado su código de inicialización. De forma similar, la función de punto de entrada no debe llamar a la función [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) (o a una función que llama a **FreeLibrary)** durante la finalización del proceso, ya que esto puede dar lugar a que se utilice un archivo DLL después de que el sistema haya ejecutado su código de finalización.

Dado Kernel32.dll se garantiza que se cargue en el espacio de direcciones del proceso cuando se llama a la función de punto de entrada, la llamada a funciones de Kernel32.dll no da lugar a que el archivo DLL se utilice antes de que se haya ejecutado su código de inicialización. Por lo tanto, la función de punto de entrada puede llamar a funciones Kernel32.dll que no cargan otros archivos DLL. Por ejemplo, *DllMain puede* crear objetos [de sincronización,](/windows/desktop/Sync/synchronization-objects) como secciones críticas y exclusiones mutuas, y usar TLS. Desafortunadamente, no hay una lista completa de funciones seguras en Kernel32.dll.

Llamar a funciones que requieren archivos DLL que no Kernel32.dll pueden dar lugar a problemas difíciles de diagnosticar. Por ejemplo, llamar a las funciones User, Shell y COM puede provocar errores de infracción de acceso, porque algunas funciones cargan otros componentes del sistema. Por el contrario, llamar a funciones como estas durante la finalización puede provocar errores de infracción de acceso porque es posible que el componente correspondiente ya se haya descargado o no inicializado.

Dado que las notificaciones DLL se serializan, las funciones de punto de entrada no deben intentar comunicarse con otros subprocesos o procesos. Como resultado, pueden producirse interbloqueos.

Para obtener información sobre los procedimientos recomendados al escribir un archivo DLL, vea https://docs.microsoft.com/windows/win32/dlls/dynamic-link-library-best-practices .

Si el archivo DLL está vinculado a la biblioteca en tiempo de ejecución de C (CRT), el punto de entrada proporcionado por CRT llama a los constructores y destructores de objetos de C++ globales y estáticos. Por lo tanto, estas restricciones *para DllMain* también se aplican a constructores y destructores, así como a cualquier código al que se llame desde ellos.

Considere la posibilidad de llamar a [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) al recibir **DLL PROCESS \_ \_ ATTACH**, a menos que el archivo DLL esté vinculado a la biblioteca estática en tiempo de ejecución de C (CRT).


## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Process.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Función de biblioteca de vínculos Entry-Point dinámica](dynamic-link-library-entry-point-function.md)
</dt> <dt>

[Funciones de la biblioteca de vínculos dinámicos](dynamic-link-library-functions.md)
</dt> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> <dt>

[**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc)
</dt> <dt>

[**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree)
</dt> <dt>

[**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls)





</dt> </dl>
