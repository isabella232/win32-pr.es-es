---
description: Un punto de entrada opcional en una biblioteca de vínculos dinámicos (DLL). Cuando el sistema inicia o finaliza un proceso o subproceso, llama a la función de punto de entrada para cada DLL cargada mediante el primer subproceso del proceso.
ms.assetid: 0c3e3083-9297-4626-b2a7-0062d1c2cf9e
title: Punto de entrada de DllMain (Process. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667634"
---
# <a name="dllmain-entry-point"></a>Punto de entrada de DllMain

Un punto de entrada opcional en una biblioteca de vínculos dinámicos (DLL). Cuando el sistema inicia o finaliza un proceso o subproceso, llama a la función de punto de entrada para cada DLL cargada mediante el primer subproceso del proceso. El sistema también llama a la función de punto de entrada de un archivo DLL cuando se carga o descarga mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) .

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
> Hay límites importantes sobre lo que se puede hacer de forma segura en un punto de entrada del archivo DLL. Vea las [prácticas recomendadas generales](dynamic-link-library-best-practices.md) para las API de Windows específicas que no se pueden llamar en DllMain. Si necesita algo más que la inicialización más sencilla, puede hacerlo en una función de inicialización para el archivo DLL. Puede requerir que las aplicaciones llamen a la función de inicialización después de que se haya ejecutado DllMain y antes de llamar a otras funciones del archivo DLL.

 

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

*hinstDLL* \[ de\]
</dt> <dd>

Identificador del módulo DLL. El valor es la dirección base del archivo DLL. El **hInstance** de un archivo dll es el mismo que el **HMODULE** del archivo dll, por lo que *hinstDLL* se puede usar en llamadas a funciones que requieren un identificador de módulo.

</dd> <dt>

*fdwReason* \[ de\]
</dt> <dd>

Código de motivo que indica por qué se llama a la función de punto de entrada del archivo DLL. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**Archivo dll \_ PROCESO de \_ Asociación**</dt> <dt>1</dt> </dl> | El archivo DLL se carga en el espacio de direcciones virtuales del proceso actual como resultado del inicio del proceso o como resultado de una llamada a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). Los archivos dll pueden utilizar esta oportunidad para inicializar los datos de una instancia o utilizar la función [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para asignar un índice de almacenamiento local de subprocesos (TLS).<br/> El parámetro *lpReserved* indica si el archivo dll se carga de forma estática o dinámica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**Archivo dll \_ \_Desasociar proceso**</dt> <dt>0</dt> </dl> | La DLL se está descargando del espacio de direcciones virtuales del proceso que realiza la llamada porque se cargó sin éxito o hasta que el recuento de referencias ha alcanzado cero (los procesos han terminado o llamado a [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) una vez por cada vez que llamó a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).<br/> El parámetro *lpReserved* indica si se está descargando el archivo dll como resultado de una llamada a [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) , un error de carga o la terminación del proceso.<br/> El archivo DLL puede utilizar esta oportunidad para llamar a la función [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) para liberar los índices TLS asignados mediante [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) y liberar los datos locales del subproceso.<br/> Tenga en cuenta que el subproceso que recibe la notificación de **\_ \_ desasociación del proceso dll** no es necesariamente el mismo subproceso que recibió la notificación de **\_ \_ Asociación del proceso dll** .<br/> |
| <span id="DLL_THREAD_ATTACH"></span><span id="dll_thread_attach"></span><dl> <dt>**Archivo dll \_ \_Conexión de subproceso**</dt> <dt>2</dt> </dl>    | El proceso actual está creando un nuevo subproceso. Cuando esto ocurre, el sistema llama a la función de punto de entrada de todos los archivos dll asociados actualmente al proceso. La llamada se realiza en el contexto del nuevo subproceso. Los archivos dll pueden utilizar esta oportunidad para inicializar una ranura TLS para el subproceso. Un subproceso que llama a la función de punto de entrada de DLL con la **\_ \_ Asociación de proceso de dll** no llama a la función de punto de entrada de dll con la **\_ \_ Asociación de subprocesos de dll**. <br/> Tenga en cuenta que el proceso de llama a la función de punto de entrada de un archivo DLL solo con este valor. Cuando se carga un archivo DLL mediante [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), los subprocesos existentes no llaman a la función de punto de entrada del archivo dll recién cargado.<br/>                                                                                                                                                                       |
| <span id="DLL_THREAD_DETACH"></span><span id="dll_thread_detach"></span><dl> <dt>**Archivo dll \_ \_Desasociación de SUBprocesos**</dt> <dt>3</dt> </dl>    | Un subproceso se está cerrando correctamente. Si el archivo DLL ha almacenado un puntero a la memoria asignada en una ranura TLS, debe utilizar esta oportunidad para liberar memoria. El sistema llama a la función de punto de entrada de todos los archivos dll cargados actualmente con este valor. La llamada se realiza en el contexto del subproceso de salida.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*lpvReserved* \[ de\]
</dt> <dd>

Si *fdwReason* es **un \_ proceso dll \_ Attach**, *lpvReserved* es **null** para cargas dinámicas y no NULL para cargas estáticas.

Si *fdwReason* es **una \_ \_ desasociación del proceso de dll**, *lpvReserved* es **null** si se ha llamado a [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) o si se ha producido un error en la carga de dll y no es **null** si el proceso está finalizando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cuando el sistema llama a la función **DllMain** con el valor **\_ \_ Attach del proceso dll** , la función devuelve **true** si se ejecuta correctamente o **false** si se produce un error de inicialización. Si el valor devuelto es **false** cuando se llama a **DllMain** porque el proceso utiliza la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , **LoadLibrary** devuelve NULL. (El sistema llama inmediatamente a la función de punto de entrada con la **\_ \_ desasociación del proceso de dll** y descarga el archivo dll). Si el valor devuelto es **false** cuando se llama a **DllMain** durante la inicialización del proceso, el proceso finaliza con un error. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Cuando el sistema llama a la función **DllMain** con cualquier valor distinto **de \_ \_ Attach del proceso dll**, se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

**DllMain** es un marcador de posición para el nombre de la función definida por la biblioteca. Debe especificar el nombre real que utilizará al compilar el archivo DLL. Para obtener más información, consulte la documentación que se incluye con las herramientas de desarrollo.

Durante el inicio del proceso inicial o después de una llamada a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), el sistema examina la lista de archivos dll cargados para el proceso. Para cada DLL que todavía no se ha llamado con el **valor \_ \_ Attach del proceso de dll** , el sistema llama a la función de punto de entrada del archivo dll. Esta llamada se realiza en el contexto del subproceso que provocó el cambio del espacio de direcciones de proceso, como el subproceso principal del proceso o el subproceso que llamó a **LoadLibrary**. El sistema serializa el acceso al punto de entrada en todo el proceso. Los subprocesos de *DllMain* mantienen el bloqueo del cargador, por lo que no se puede cargar ni inicializar de forma dinámica ningún dll adicional.

Si la función de punto de entrada del archivo DLL devuelve FALSE después de una notificación de **\_ \_ Asociación de proceso de dll** , recibe una notificación de **\_ \_ desasociación de proceso de dll** y la dll se descarga inmediatamente. Sin embargo, si el código para **\_ \_ adjuntar el proceso dll** produce una excepción, la función de punto de entrada no recibirá la notificación de **\_ \_ desasociación del proceso dll** .

Hay casos en los que se llama a la función de punto de entrada para un subproceso de terminación aunque la función de punto de entrada nunca se llamara con la **\_ \_ Asociación de subprocesos de dll** para el subproceso:

-   El subproceso era el subproceso inicial en el proceso, por lo que el sistema llamó a la función de punto de entrada con el valor **\_ \_ Attach del proceso de dll** .
-   El subproceso ya se estaba ejecutando cuando se realizó una llamada a la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , por lo que el sistema nunca llamó a la función de punto de entrada para él.

Cuando se descarga un archivo DLL de un proceso como resultado de una carga incorrecta del archivo DLL, la finalización del proceso o una llamada a [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary), el sistema no llama a la función de punto de entrada del archivo dll con el valor de **\_ \_ desasociación del subproceso dll** para los subprocesos individuales del proceso. Solo se envía una notificación de **\_ \_ desasociación de proceso de DLL** a la dll. Los archivos dll pueden tomar esta oportunidad para limpiar todos los recursos de todos los subprocesos que conoce el archivo DLL.

Al controlar **la \_ \_ desasociación de procesos DLL**, un archivo DLL debe liberar recursos como la memoria del montón solo si el archivo dll se descarga dinámicamente (el parámetro *lpReserved* es **null**). Si el proceso está finalizando (el parámetro *lpvReserved* no es **null**), todos los subprocesos del proceso, excepto el subproceso actual, ya han salido o se han terminado explícitamente mediante una llamada a la función [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) , lo que podría dejar algunos recursos de proceso, como los montones en un estado incoherente. En este caso, no es seguro que el archivo DLL Limpie los recursos. En su lugar, el archivo DLL debe permitir que el sistema operativo reclame la memoria.

Si finaliza un proceso mediante una llamada a [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) o [**TerminateJobObject**](/windows/desktop/api/jobapi2/nf-jobapi2-terminatejobobject), los archivos dll de ese proceso no reciben las notificaciones de **\_ \_ desasociación del proceso dll** . Si finaliza un subproceso llamando a [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread), los archivos dll de ese subproceso no recibirán notificaciones de **\_ \_ desasociación de subprocesos dll** .

La función de punto de entrada solo debe realizar tareas simples de inicialización o finalización. No debe llamar a la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (o a una función que llama a estas funciones), ya que esto puede crear bucles de dependencia en el orden de carga de dll. Esto puede dar lugar a que se utilice un archivo DLL antes de que el sistema ejecute su código de inicialización. Del mismo modo, la función de punto de entrada no debe llamar a la función [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) (o una función que llame a **FreeLibrary**) durante la terminación del proceso, ya que esto puede dar lugar a que se use un archivo dll después de que el sistema haya ejecutado su código de finalización.

Dado que se garantiza la carga de Kernel32.dll en el espacio de direcciones de proceso cuando se llama a la función de punto de entrada, al llamar a funciones en Kernel32.dll no se usa el archivo DLL antes de que se haya ejecutado el código de inicialización. Por consiguiente, la función de punto de entrada puede llamar a funciones de Kernel32.dll que no cargan otros archivos dll. Por ejemplo, *DllMain* puede crear [objetos de sincronización](/windows/desktop/Sync/synchronization-objects) , como secciones críticas y exclusiones mutuas, y usar TLS. Desafortunadamente, no hay una lista completa de funciones seguras en Kernel32.dll.

Llamar a funciones que requieren archivos dll distintos de Kernel32.dll puede producir problemas difíciles de diagnosticar. Por ejemplo, llamar a funciones de usuario, Shell y COM puede provocar errores de infracción de acceso, ya que algunas funciones cargan otros componentes del sistema. Por el contrario, llamar a funciones como estas durante la terminación puede provocar errores de infracción de acceso porque es posible que el componente correspondiente ya se haya descargado o no inicializado.

Dado que las notificaciones de DLL se serializan, las funciones de punto de entrada no deben intentar comunicarse con otros subprocesos o procesos. Como resultado, pueden producirse interbloqueos.

Para obtener información acerca de los procedimientos recomendados para escribir un archivo DLL, vea https://docs.microsoft.com/windows/win32/dlls/dynamic-link-library-best-practices .

Si el archivo DLL se vincula con la biblioteca en tiempo de ejecución de C (CRT), el punto de entrada proporcionado por CRT llama a los constructores y destructores para los objetos de C++ globales y estáticos. Por lo tanto, estas restricciones de *DllMain* también se aplican a los constructores y destructores y al código al que se llama desde ellos.

Considere la posibilidad de llamar a [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) al recibir la **\_ \_ Asociación del proceso dll**, a menos que el archivo dll esté vinculado con la biblioteca en tiempo de ejecución de C (CRT) estática.


## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Process. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Función Entry-Point de la biblioteca de vínculos dinámicos](dynamic-link-library-entry-point-function.md)
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
