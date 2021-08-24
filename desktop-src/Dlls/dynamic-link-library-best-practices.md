---
description: La creación de archivos DLL presenta una serie de desafíos para los desarrolladores.
ms.assetid: 44EFC4B5-7A2F-43A6-914E-D4EB7446AC35
title: procedimientos recomendados de la biblioteca de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d02314b15a13de7658c0b87ba7cd998f48a0a3d9f2f2682b36539bd9f5bde3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696594"
---
# <a name="dynamic-link-library-best-practices"></a>procedimientos recomendados de la biblioteca de Dynamic-Link

**Actualizado: **

-   17 de mayo de 2006

**API importantes**

-   [**DllMain**](dllmain.md)
-   [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

La creación de archivos DLL presenta una serie de desafíos para los desarrolladores. Los archivos DLL no tienen control de versiones aplicado por el sistema. Cuando existen varias versiones de un archivo DLL en un sistema, la facilidad de sobrescribirse junto con la falta de un esquema de control de versiones crea conflictos de dependencia y API. La complejidad del entorno de desarrollo, la implementación del cargador y las dependencias dll han creado la elasticidad en el orden de carga y el comportamiento de la aplicación. Por último, muchas aplicaciones se basan en archivos DLL y tienen conjuntos complejos de dependencias que se deben respetar para que las aplicaciones funcionen correctamente. En este documento se proporcionan instrucciones para que los desarrolladores de DLL le ayuden a crear archivos DLL más sólidos, portátiles y extensibles.

Una sincronización incorrecta [**en DllMain**](dllmain.md) puede hacer que una aplicación interbloquee o acceda a datos o código en un archivo DLL sin inicializar. Llamar a determinadas funciones desde **DllMain** provoca estos problemas.

![lo que sucede cuando se carga una biblioteca](images/fig1.png)

## <a name="general-best-practices"></a>Procedimientos recomendados generales

[**Se llama a DllMain**](dllmain.md) mientras se mantiene el bloqueo del cargador. Por lo tanto, se imponen restricciones significativas en las funciones a las que se puede llamar **en DllMain**. Por lo tanto, **DllMain está** diseñado para realizar tareas de inicialización mínimas, mediante un pequeño subconjunto de microsoft® Windows® API. No se puede llamar a ninguna función **de DllMain** que intente adquirir directa o indirectamente el bloqueo del cargador. De lo contrario, presentará la posibilidad de que la aplicación se interbloquee o se bloquea. Un error en una **implementación de DllMain** puede poner en peligro todo el proceso y todos sus subprocesos.

El archivo [**DllMain ideal**](dllmain.md) sería simplemente un código auxiliar vacío. Sin embargo, dada la complejidad de muchas aplicaciones, esto suele ser demasiado restrictivo. Una buena regla general para **DllMain** es posponer tanta inicialización como sea posible. La inicialización diferida aumenta la solidez de la aplicación porque esta inicialización no se realiza mientras se mantiene el bloqueo del cargador. Además, la inicialización diferida le permite usar mucho más de la API Windows segura.

Algunas tareas de inicialización no se pueden posponer. Por ejemplo, un archivo DLL que depende de un archivo de configuración no se puede cargar si el archivo tiene un formato correcto o contiene elementos no utilizados. Para este tipo de inicialización, el archivo DLL debe intentar la acción y producir un error rápidamente en lugar de desperdiciar recursos completando otro trabajo.

Nunca debe realizar las siguientes tareas desde [**DllMain**](dllmain.md):

-   Llame [**a LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**o LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (directa o indirectamente). Esto puede provocar un interbloqueo o un bloqueo.
-   Llame [**a GetStringTypeA**](/windows/desktop/api/winnls/nf-winnls-getstringtypea), [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw)o [**GetStringTypeW**](/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew) (directa o indirectamente). Esto puede provocar un interbloqueo o un bloqueo.
-   Sincronice con otros subprocesos. Esto puede provocar un interbloqueo.
-   Adquiera un objeto de sincronización que sea propiedad del código que está esperando adquirir el bloqueo del cargador. Esto puede provocar un interbloqueo.
-   Inicialice subprocesos COM mediante [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). En determinadas condiciones, esta función puede llamar [**a LoadLibraryEx.**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   Llame a las funciones del Registro. Estas funciones se implementan en Advapi32.dll. Si Advapi32.dll se inicializa antes del archivo DLL, el archivo DLL puede acceder a la memoria sin inicializar y hacer que el proceso se bloquee.
-   Llame [**a CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) La creación de un proceso puede cargar otro archivo DLL.
-   Llame [**a ExitThread.**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread) Salir de un subproceso durante la desasocie del archivo DLL puede hacer que el bloqueo del cargador se vuelva a adquirir, lo que provoca un interbloqueo o un bloqueo.
-   Llame [**a CreateThread.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread) La creación de un subproceso puede funcionar si no se sincroniza con otros subprocesos, pero es arriesgado.
-   Cree una canalización con nombre u otro objeto con nombre (solo Windows 2000). En Windows 2000, el archivo DLL de Terminal Services proporciona objetos con nombre. Si no se inicializa este archivo DLL, las llamadas al archivo DLL pueden hacer que el proceso se bloquea.
-   Use la función de administración de memoria de la función dinámica de C Run-Time (CRT). Si no se inicializa el archivo DLL de CRT, las llamadas a estas funciones pueden hacer que el proceso se bloquea.
-   Llame a funciones en User32.dll o Gdi32.dll. Algunas funciones cargan otro archivo DLL, que puede que no se inicialice.
-   Use código administrado.

Las siguientes tareas son seguras para realizar en **DllMain**:

-   Inicializar miembros y estructuras de datos estáticos en tiempo de compilación.
-   Cree e inicialice objetos de sincronización.
-   Asigne memoria e inicialice estructuras de datos dinámicos (evitando las funciones enumeradas anteriormente).
-   Configure el almacenamiento local de subprocesos (TLS).
-   Abra, lea y escriba en archivos.
-   Llame a funciones Kernel32.dll (excepto las funciones enumeradas anteriormente).
-   Establezca punteros globales en NULL, lo que desactivará la inicialización de miembros dinámicos. En Microsoft Windows Vista™, puede usar las funciones de inicialización únicas para asegurarse de que un bloque de código se ejecuta solo una vez en un entorno multiproceso.

## <a name="deadlocks-caused-by-lock-order-inversion"></a>Interbloqueos causados por la inversión de orden de bloqueo

Al implementar código que usa varios objetos de sincronización, como bloqueos, es fundamental respetar el orden de bloqueo. Cuando sea necesario adquirir más de un bloqueo a la vez, debe definir una precedencia explícita que se denomina jerarquía de bloqueo o orden de bloqueo. Por ejemplo, si el bloqueo A se adquiere antes del bloqueo B en algún lugar del código y el bloqueo B se adquiere antes que el bloqueo C en otra parte del código, el orden de bloqueo es A, B, C y este orden debe seguirse a lo largo del código. La inversión del orden de bloqueo se produce cuando no se sigue el orden de bloqueo, por ejemplo, si se adquiere el bloqueo B antes del bloqueo A. La inversión del orden de bloqueo puede provocar interbloqueos que son difíciles de depurar. Para evitar estos problemas, todos los subprocesos deben adquirir bloqueos en el mismo orden.

Es importante tener en cuenta que el cargador llama a [**DllMain**](dllmain.md) con el bloqueo del cargador ya adquirido, por lo que el bloqueo del cargador debe tener la prioridad más alta en la jerarquía de bloqueo. Tenga en cuenta también que el código solo tiene que adquirir los bloqueos que requiere para la sincronización adecuada. no tiene que adquirir todos los bloqueos que se definen en la jerarquía. Por ejemplo, si una sección de código solo requiere bloqueos A y C para una sincronización adecuada, el código debe adquirir el bloqueo A antes de adquirir el bloqueo C; No es necesario que el código también adquiera el bloqueo B. Además, el código DLL no puede adquirir explícitamente el bloqueo del cargador. Si el código debe llamar a una API como [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) que puede adquirir indirectamente el bloqueo del cargador y el código también debe adquirir un bloqueo privado, el código debe llamar a **GetModuleFileName** antes de adquirir el bloqueo P, lo que garantiza que se respeta el orden de carga.

La figura 2 es un ejemplo que muestra la inversión de orden de bloqueo. Considere un archivo DLL cuyo subproceso principal contiene [**DllMain**](dllmain.md). El cargador de bibliotecas adquiere el bloqueo L del cargador y, a continuación, llama **a DllMain**. El subproceso principal crea objetos de sincronización A, B y G para serializar el acceso a sus estructuras de datos y, a continuación, intenta adquirir el bloqueo G. Un subproceso de trabajo que ya ha adquirido correctamente el bloqueo G llama a una función como GetModuleHandle que intenta adquirir el bloqueo del cargador L. Por lo tanto, el subproceso de trabajo se bloquea en L y el subproceso principal se bloquea en G, lo que produce un interbloqueo.

![interbloqueo causado por la inversión del orden de bloqueo](images/fig2.png)

Para evitar interbloqueos causados por la inversión de orden de bloqueo, todos los subprocesos deben intentar adquirir objetos de sincronización en el orden de carga definido en todo momento.

## <a name="best-practices-for-synchronization"></a>Procedimientos recomendados para la sincronización

Considere un archivo DLL que crea subprocesos de trabajo como parte de su inicialización. Tras la limpieza del archivo DLL, es necesario sincronizar con todos los subprocesos de trabajo para asegurarse de que las estructuras de datos están en un estado coherente y, a continuación, finalizar los subprocesos de trabajo. En la actualidad, no hay ninguna manera sencilla de resolver completamente el problema de sincronizar y apagar correctamente los archivos DLL en un entorno multiproceso. En esta sección se describen los procedimientos recomendados actuales para la sincronización de subprocesos durante el cierre de dll.

Sincronización de subprocesos [**en DllMain durante**](dllmain.md) la salida del proceso

-   En el momento en que se llama a [**DllMain**](dllmain.md) al salir del proceso, todos los subprocesos del proceso se han limpiado forzadamente y existe la posibilidad de que el espacio de direcciones sea incoherente. En este caso, no se requiere sincronización. En otras palabras, el controlador DLL \_ PROCESS \_ DETACH ideal está vacío.
-   Windows Vista garantiza que las estructuras de datos principales (variables de entorno, directorio actual, montón de procesos, entre otros) están en un estado coherente. Sin embargo, otras estructuras de datos pueden estar dañadas, por lo que la limpieza de la memoria no es segura.
-   El estado persistente que debe guardarse debe vaciarse en un almacenamiento permanente.

Sincronización de subprocesos **en DllMain** para DLL \_ THREAD \_ DETACH durante la descarga de DLL

-   Cuando se descarga el archivo DLL, no se descarta el espacio de direcciones. Por lo tanto, se espera que el archivo DLL realice un apagado limpio. Esto incluye la sincronización de subprocesos, los identificadores abiertos, el estado persistente y los recursos asignados.
-   La sincronización de subprocesos es complicada porque esperar a que los subprocesos se cierren [**en DllMain**](dllmain.md) puede provocar un interbloqueo. Por ejemplo, dll A contiene el bloqueo del cargador. Indica al subproceso T que salga y espera a que el subproceso salga. El subproceso T se cierra y el cargador intenta adquirir el bloqueo del cargador para llamar a **DllMain** de DLL A con DLL \_ THREAD \_ DETACH. Esto provoca un interbloqueo. Para minimizar el riesgo de un interbloqueo:
    -   DLL A obtiene un mensaje DLL \_ THREAD \_ DETACH en su [**DllMain**](dllmain.md) y establece un evento para el subproceso T, lo que indica que debe salir.
    -   El subproceso T finaliza su tarea actual, se pone en un estado coherente, señala el archivo DLL A y espera infinitamente. Tenga en cuenta que las rutinas de comprobación de coherencia deben seguir las mismas restricciones [**que DllMain**](dllmain.md) para evitar interbloqueos.
    -   DLL A finaliza T, sabiendo que está en un estado coherente.

Si se descarga un archivo DLL después de crear todos sus subprocesos, pero antes de empezar a ejecutarse, los subprocesos pueden bloquearse. Si el archivo DLL creó subprocesos en **su DllMain** como parte de su inicialización, es posible que algunos subprocesos no tengan finalizada la inicialización y su mensaje DLL THREAD ATTACH todavía esté esperando para entregarse al \_ archivo \_ DLL. En esta situación, si se descarga el archivo DLL, comenzará a terminar los subprocesos. Sin embargo, es posible que algunos subprocesos se bloqueen detrás del bloqueo del cargador. Sus mensajes DLL THREAD ATTACH se procesan después de que el archivo DLL se haya desaple, lo que hace \_ que el proceso se \_ bloquea.

## <a name="recommendations"></a>Recomendaciones

A continuación se recomiendan las siguientes directrices:

-   Use Application Verifier para detectar los errores más comunes [**en DllMain**](dllmain.md).
-   Si usa un bloqueo privado dentro de [**DllMain,**](dllmain.md)defina una jerarquía de bloqueo y úsela de forma coherente. El bloqueo del cargador debe estar en la parte inferior de esta jerarquía.
-   Compruebe que ninguna llamada dependa de otro archivo DLL que todavía no se haya cargado por completo.
-   Realice inicializaciones simples estáticamente en tiempo de compilación, en lugar de [**en DllMain**](dllmain.md).
-   Aplazar las llamadas de [**DllMain**](dllmain.md) que puedan esperar hasta más adelante.
-   Aplazar las tareas de inicialización que pueden esperar hasta más adelante. Ciertas condiciones de error deben detectarse pronto para que la aplicación pueda controlar los errores correctamente. Sin embargo, hay un equilibrio entre esta detección temprana y la pérdida de solidez que puede producirse. Aplazar la inicialización suele ser mejor.

 

 
