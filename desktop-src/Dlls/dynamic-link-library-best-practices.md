---
description: La creación de archivos dll presenta una serie de desafíos para los desarrolladores.
ms.assetid: 44EFC4B5-7A2F-43A6-914E-D4EB7446AC35
title: Procedimientos recomendados de la biblioteca Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88aba0999f3d0825c6d2f4df3afe09d766a82232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669707"
---
# <a name="dynamic-link-library-best-practices"></a>Procedimientos recomendados de la biblioteca Dynamic-Link

* * Actualizado: * *

-   17 de mayo de 2006

**API importantes**

-   [**DllMain**](dllmain.md)
-   [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

La creación de archivos dll presenta una serie de desafíos para los desarrolladores. Los archivos dll no tienen control de versiones aplicado por el sistema. Cuando existen varias versiones de un archivo DLL en un sistema, la facilidad de sobrescribirse junto con la falta de un esquema de control de versiones crea conflictos de dependencias y API. La complejidad en el entorno de desarrollo, la implementación del cargador y las dependencias de DLL han creado fragilidad en el orden de carga y el comportamiento de la aplicación. Por último, muchas aplicaciones se basan en archivos dll y tienen conjuntos complejos de dependencias que se deben respetar para que las aplicaciones funcionen correctamente. En este documento se proporcionan directrices para que los desarrolladores de archivos DLL ayuden a crear archivos dll más sólidos, portátiles y extensibles.

Una sincronización incorrecta en [**DllMain**](dllmain.md) puede hacer que una aplicación se interbloquee o tenga acceso a datos o código en un archivo dll no inicializado. Llamar a determinadas funciones desde **DllMain** provoca estos problemas.

![¿Qué ocurre cuando se carga una biblioteca?](images/fig1.png)

## <a name="general-best-practices"></a>Procedimientos recomendados generales

Se llama a [**DllMain**](dllmain.md) mientras se mantiene el bloqueo del cargador. Por lo tanto, se imponen restricciones significativas en las funciones a las que se puede llamar en **DllMain**. Como tal, **DllMain** está diseñada para realizar tareas de inicialización mínimas, mediante el uso de un pequeño subconjunto de Microsoft® Windows® API. No se puede llamar a ninguna función de **DllMain** que intente adquirir directa o indirectamente el bloqueo del cargador. De lo contrario, introducirá la posibilidad de que la aplicación se bloquee o se bloquee. Un error en una implementación de **DllMain** puede poner en peligro todo el proceso y todos los subprocesos.

La opción [**DllMain**](dllmain.md) ideal sería simplemente un código auxiliar vacío. Sin embargo, dada la complejidad de muchas aplicaciones, suele ser demasiado restrictiva. Una buena regla general para **DllMain** es posponer la máxima inicialización posible. La inicialización diferida aumenta la solidez de la aplicación, ya que esta inicialización no se realiza mientras se mantiene el bloqueo del cargador. Además, la inicialización diferida le permite usar de forma segura mucho más la API de Windows.

No se pueden posponer algunas tareas de inicialización. Por ejemplo, una DLL que depende de un archivo de configuración debería no cargarse si el archivo tiene un formato incorrecto o contiene elementos no utilizados. Para este tipo de inicialización, el archivo DLL debe intentar la acción y producir un error rápido en lugar de desperdiciar recursos mediante la finalización de otro trabajo.

Nunca debe realizar las siguientes tareas desde [**DllMain**](dllmain.md):

-   Llame a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (ya sea directa o indirectamente). Esto puede producir un interbloqueo o un bloqueo.
-   Llame a [**GetStringTypeA**](/windows/desktop/api/winnls/nf-winnls-getstringtypea), [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw)o [**GetStringTypeW**](/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew) (directa o indirectamente). Esto puede producir un interbloqueo o un bloqueo.
-   Sincronizar con otros subprocesos. Esto puede producir un interbloqueo.
-   Adquiera un objeto de sincronización que sea propiedad del código que está esperando para adquirir el bloqueo del cargador. Esto puede producir un interbloqueo.
-   Inicialice los subprocesos COM mediante [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). En determinadas condiciones, esta función puede llamar a [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa).
-   Llame a las funciones del registro. Estas funciones se implementan en Advapi32.dll. Si Advapi32.dll no se inicializa antes que el archivo DLL, el archivo DLL puede tener acceso a la memoria sin inicializar y provocar el bloqueo del proceso.
-   Llame a [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa). La creación de un proceso puede cargar otro archivo DLL.
-   Llame a [**ExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). Salir de un subproceso durante la desasociación de DLL puede provocar que se vuelva a adquirir el bloqueo del cargador, lo que provocaría un interbloqueo o un bloqueo.
-   Llame a [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread). La creación de un subproceso puede funcionar si no se sincroniza con otros subprocesos, pero es arriesgado.
-   Cree una canalización con nombre u otro objeto con nombre (solo Windows 2000). En Windows 2000, los objetos con nombre se proporcionan mediante el Terminal Services DLL. Si no se inicializa este archivo DLL, las llamadas a la DLL pueden provocar que el proceso se bloquee.
-   Utilice la función de administración de memoria de la Run-Time de C dinámica (CRT). Si el archivo DLL de CRT no se ha inicializado, las llamadas a estas funciones pueden provocar el bloqueo del proceso.
-   Llamar a funciones en User32.dll o Gdi32.dll. Algunas funciones cargan otro archivo DLL, que no se puede inicializar.
-   Usar código administrado.

Las siguientes tareas se pueden realizar con seguridad en **DllMain**:

-   Inicializar miembros y estructuras de datos estáticos en tiempo de compilación.
-   Cree e inicialice objetos de sincronización.
-   Asigne memoria e inicialice estructuras de datos dinámicos (evitando las funciones enumeradas anteriormente).
-   Configurar el almacenamiento local de subprocesos (TLS).
-   Abrir, leer y escribir en archivos.
-   Llamar a funciones en Kernel32.dll (excepto las funciones enumeradas anteriormente).
-   Establezca punteros globales en NULL y salga de la inicialización de los miembros dinámicos. En Microsoft Windows Vista™, puede usar las funciones de inicialización únicas para asegurarse de que un bloque de código se ejecuta solo una vez en un entorno multiproceso.

## <a name="deadlocks-caused-by-lock-order-inversion"></a>Interbloqueos causados por la inversión del orden de bloqueo

Cuando se implementa código que utiliza varios objetos de sincronización, como bloqueos, es fundamental respetar el orden de los bloqueos. Cuando es necesario adquirir más de un bloqueo a la vez, debe definir una prioridad explícita que se llame una jerarquía de bloqueos o un orden de bloqueo. Por ejemplo, si se adquiere el bloqueo A antes de bloquear B en algún lugar del código, y el bloqueo B se adquiere antes que el bloque C en otro lugar del código, el orden de bloqueo es a, B, C y este orden debe seguirse en todo el código. La inversión del orden de bloqueo se produce cuando no se sigue el orden de bloqueo; por ejemplo, si se adquiere el bloqueo B antes de bloquear un. la inversion del orden de bloqueo puede producir interbloqueos difíciles de depurar. Para evitar estos problemas, todos los subprocesos deben adquirir bloqueos en el mismo orden.

Es importante tener en cuenta que el cargador llama a [**DllMain**](dllmain.md) con el bloqueo del cargador ya adquirido, por lo que el bloqueo del cargador debe tener la prioridad más alta en la jerarquía de bloqueos. Tenga en cuenta también que el código solo tiene que adquirir los bloqueos necesarios para la sincronización correcta; no tiene que adquirir cada bloqueo único que se define en la jerarquía. Por ejemplo, si una sección de código solo requiere bloqueos A y C para la sincronización correcta, el código debe adquirir el bloqueo A antes de adquirir el bloqueo C; no es necesario que el código también adquiera el bloqueo B. Además, el código DLL no puede adquirir explícitamente el bloqueo del cargador. Si el código debe llamar a una API como [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) que pueda adquirir indirectamente el bloqueo del cargador y el código también debe adquirir un bloqueo privado, el código debe llamar a **GetModuleFileName** antes de adquirir el bloqueo P, lo que garantiza que se respete el orden de carga.

En la ilustración 2 se muestra un ejemplo que ilustra la inversión del orden de bloqueo. Considere una DLL cuyo subproceso principal contiene [**DllMain**](dllmain.md). El cargador de la biblioteca adquiere el bloqueo de cargador L y, a continuación, llama a **DllMain**. El subproceso principal crea los objetos de sincronización a, B y G para serializar el acceso a sus estructuras de datos y, a continuación, intenta adquirir el bloqueo G. Un subproceso de trabajo que ya ha adquirido correctamente el bloqueo G llama a una función como GetModuleHandle que intenta adquirir el bloqueo del cargador L. Por lo tanto, el subproceso de trabajo se bloquea en L y el subproceso principal se bloquea en G, lo que produce un interbloqueo.

![interbloqueo causado por la inversión del orden de bloqueo](images/fig2.png)

Para evitar interbloqueos causados por la inversion del orden de bloqueo, todos los subprocesos deben intentar adquirir objetos de sincronización en el orden de carga definido en todo momento.

## <a name="best-practices-for-synchronization"></a>Prácticas recomendadas para la sincronización

Considere un archivo DLL que crea subprocesos de trabajo como parte de su inicialización. Tras la limpieza de archivos DLL, es necesario sincronizar con todos los subprocesos de trabajo para asegurarse de que las estructuras de datos están en un estado coherente y, a continuación, terminar los subprocesos de trabajo. En la actualidad, no hay ninguna manera sencilla de resolver por completo el problema de la sincronización y el cierre correctos de los archivos dll en un entorno multiproceso. En esta sección se describen las prácticas recomendadas actuales para la sincronización de subprocesos durante el cierre de DLL.

Sincronización de subprocesos en [**DllMain**](dllmain.md) durante la salida del proceso

-   En el momento en que se llama a [**DllMain**](dllmain.md) al salir del proceso, todos los subprocesos del proceso se han limpiado forzosamente y existe la posibilidad de que el espacio de direcciones sea incoherente. En este caso, no es necesaria la sincronización. En otras palabras, el controlador de \_ desasociación de procesos de dll ideal \_ está vacío.
-   Windows Vista garantiza que las estructuras de datos principales (variables de entorno, directorio actual, montón de procesos, etc.) se encuentran en un estado coherente. Sin embargo, se pueden dañar otras estructuras de datos, por lo que la limpieza de la memoria no es segura.
-   El estado persistente que debe guardarse debe vaciarse en el almacenamiento permanente.

Sincronización de subprocesos en **DllMain** para \_ desasociar el subproceso dll \_ durante la descarga de dll

-   Cuando se descarga el archivo DLL, no se produce el espacio de direcciones. Por lo tanto, se espera que el archivo DLL realice un cierre correcto. Esto incluye la sincronización de subprocesos, los identificadores abiertos, el estado persistente y los recursos asignados.
-   La sincronización de subprocesos es complicada porque esperar a que los subprocesos salgan en [**DllMain**](dllmain.md) puede producir un interbloqueo. Por ejemplo, el archivo DLL A contiene el bloqueo del cargador. Indica al subproceso T que salga y espera a que el subproceso se cierre. El subproceso T se cierra y el cargador intenta adquirir el bloqueo del cargador para llamar a **DllMain** de la dll a de la \_ desasociación de subprocesos dll \_ . Esto provoca un interbloqueo. Para minimizar el riesgo de un interbloqueo:
    -   El archivo DLL A obtiene \_ un \_ mensaje de desasociación de subprocesos dll en su [**DllMain**](dllmain.md) y establece un evento para el subproceso T, señalando su salida.
    -   Thread T finaliza su tarea actual, se convierte en un estado coherente, señala a la DLL A y espera infinitamente. Tenga en cuenta que las rutinas de comprobación de coherencia deben seguir las mismas restricciones que [**DllMain**](dllmain.md) para evitar el interbloqueo.
    -   El archivo DLL A termina T y sabe que está en un estado coherente.

Si se descarga un archivo DLL una vez que se han creado todos los subprocesos, pero antes de que empiecen a ejecutarse, los subprocesos pueden bloquearse. Si el archivo DLL crea subprocesos en su **DllMain** como parte de su inicialización, es posible que algunos subprocesos no hayan finalizado la inicialización y que el \_ mensaje de \_ adjuntar el subproceso dll todavía esté esperando a entregarse al archivo dll. En esta situación, si se descarga el archivo DLL, comenzará a terminar los subprocesos. Sin embargo, algunos subprocesos pueden bloquearse detrás del bloqueo del cargador. Los \_ \_ mensajes adjuntos del subproceso de la dll se procesan después de que se haya desasignado el archivo dll, lo que provoca el bloqueo del proceso.

## <a name="recommendations"></a>Recomendaciones

Se recomiendan las siguientes directrices:

-   Utilice comprobador de aplicaciones para detectar los errores más comunes en [**DllMain**](dllmain.md).
-   Si usa un bloqueo privado dentro de [**DllMain**](dllmain.md), defina una jerarquía de bloqueo y úsela de forma coherente. El bloqueo del cargador debe estar en la parte inferior de esta jerarquía.
-   Compruebe que no haya ninguna llamada que dependa de otra DLL que no se haya cargado todavía completamente.
-   Realice inicializaciones simples de forma estática en tiempo de compilación, en lugar de en [**DllMain**](dllmain.md).
-   Postergue cualquier llamada en [**DllMain**](dllmain.md) que pueda esperar hasta más adelante.
-   Diferir las tareas de inicialización que pueden esperar hasta más adelante. Ciertas condiciones de error se deben detectar pronto para que la aplicación pueda controlar correctamente los errores. Sin embargo, hay contrapartidas entre esta detección temprana y la pérdida de solidez que puede derivar de ella. La desconcesión de la inicialización suele ser mejor.

 

 
