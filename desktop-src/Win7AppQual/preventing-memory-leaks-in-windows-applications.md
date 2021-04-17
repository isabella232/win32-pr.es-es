---
description: Obtenga información acerca de cómo evitar pérdidas de memoria en aplicaciones Windows para plataformas Windows 7 y Windows Server 2008 R2.
ms.assetid: c5dedcab-3e6f-433f-95de-d741321c683e
title: Evitar pérdidas de memoria en aplicaciones Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e973da19d075ac94824df340d1741fd9cefb3486
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104567390"
---
# <a name="preventing-memory-leaks-in-windows-applications"></a>Evitar pérdidas de memoria en aplicaciones Windows

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes** : Windows 7  
**Servidores** : Windows Server 2008 R2  

## <a name="description"></a>Descripción

Las pérdidas de memoria son una clase de errores en los que la aplicación no puede liberar memoria cuando ya no se necesitan. Con el tiempo, las pérdidas de memoria afectan al rendimiento de la aplicación concreta, así como del sistema operativo. Una pérdida grande podría producir tiempos de respuesta inaceptables debido a una paginación excesiva. Finalmente, la aplicación, así como otras partes del sistema operativo, experimentarán errores.

Windows liberará toda la memoria asignada por la aplicación al finalizar el proceso, por lo que las aplicaciones de ejecución reducida no afectarán de forma significativa al rendimiento global del sistema. Sin embargo, las pérdidas en procesos de ejecución prolongada como servicios o incluso complementos del explorador pueden afectar en gran medida a la confiabilidad del sistema y podrían obligar al usuario a reiniciar Windows para que el sistema pueda volver a usarse.

Las aplicaciones pueden asignar memoria en su nombre por varios medios. Cada tipo de asignación puede producir una pérdida si no se libera tras su uso. Estos son algunos ejemplos de patrones de asignación comunes:

-   Memoria del montón a través de la función [**HeapAlloc**](/windows/win32/api/heapapi/nf-heapapi-heapalloc) o sus equivalentes en tiempo de ejecución de C/C++ **malloc** o **New**
-   Dirija las asignaciones desde el sistema operativo a través de la función [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) .
-   Los identificadores de kernel creados a través de las API de Kernel32, como [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea), [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)o [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), contienen memoria de kernel en nombre de la aplicación.
-   GDI y los identificadores de usuario creados a través de las API user32 y Gdi32 (de forma predeterminada, cada proceso tiene una cuota de identificadores 10.000)

## <a name="best-practices"></a>Prácticas recomendadas

La supervisión del consumo de recursos de la aplicación a lo largo del tiempo es el primer paso para detectar y diagnosticar pérdidas de memoria. Use el administrador de tareas de Windows y agregue las siguientes columnas: "tamaño de confirmación", "identificadores", "objetos de usuario" y "objetos GDI". Esto le permitirá establecer una línea base para la aplicación y supervisar el uso de los recursos a lo largo del tiempo.

![Captura de pantalla que muestra la página "procesos" en el administrador de tareas de Windows.](images/preventingmemoryleaks-windowstaskmanager.gif)

Las siguientes herramientas de Microsoft proporcionan información más detallada y pueden ayudar a detectar y diagnosticar pérdidas para los distintos tipos de asignación de la aplicación:

-   El monitor de rendimiento y el Monitor de recursos forman parte de Windows 7 y pueden supervisar y usar los recursos de gráficos a lo largo del tiempo
-   La versión más reciente de comprobador de aplicaciones puede diagnosticar pérdidas de montones en Windows 7
-   UMDH, que forma parte de las herramientas de depuración para Windows, analiza las asignaciones de memoria del montón para un proceso determinado y puede ayudar a detectar pérdidas y otros patrones de uso inusuales.
-   Xperf es una herramienta de análisis de rendimiento sofisticada que admite seguimientos de asignación del montón.
-   El montón de depuración de CRT realiza un seguimiento de las asignaciones de montón y puede ayudar a crear sus propias características de depuración de montón

Ciertas prácticas de codificación y diseño pueden limitar el número de fugas en el código.

-   Use punteros inteligentes en el código de C++ tanto para las asignaciones de montón como para los recursos de Win32, como los **identificadores** de kernel. La biblioteca estándar de C++ proporciona la clase **auto \_ ptr** para las asignaciones de montón. En el caso de otros tipos de asignación, deberá escribir sus propias clases. La biblioteca ATL proporciona un amplio conjunto de clases para la administración automática de recursos tanto para los objetos de montón como para los identificadores de kernel
-   Use características intrínsecas del compilador como **\_ com \_ ptr \_ t** para encapsular los punteros de interfaz com en "punteros inteligentes" y ayudar con el recuento de referencias. Hay clases similares para otros tipos de datos COM: **\_ BSTR \_ t** y **\_ variante \_ t**
-   Supervise el uso de memoria inusual del código .NET. El código administrado no es inmune a pérdidas de memoria. Consulte ["seguimiento de pérdidas de memoria administrada"](/archive/blogs/ricom/) sobre cómo buscar pérdidas de GC
-   Tenga en cuenta los patrones de fuga en el código del lado cliente web. Las referencias circulares entre objetos COM y motores de scripting como JScript pueden provocar grandes fugas en las aplicaciones Web. ["Comprender y resolver patrones de fugas de Internet Explorer"](/previous-versions/ms976398(v=msdn.10)) contiene más información sobre estos tipos de fugas. Puede usar el detector de fugas de memoria de JavaScript para depurar pérdidas de memoria en el código. Aunque Windows Internet Explorer 8, que se distribuye con Windows 7, mitiga la mayoría de estos problemas, los exploradores más antiguos siguen siendo vulnerables a estos errores.
-   Evite el uso de varias rutas de acceso de salida de una función. Las asignaciones asignadas a variables en el ámbito de la función deben liberarse en un bloque determinado al final de la función.
-   No utilice excepciones en el código sin liberar todas las variables locales en las funciones. Si usa excepciones nativas, libere todas las asignaciones dentro del \_ \_ bloque Finally. Si usa excepciones de C++, todas las asignaciones de montón y de control deben ajustarse en punteros inteligentes
-   No descartar o reinicializar un objeto [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) sin llamar a la función [**PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

## <a name="links-to-resources"></a>Vínculos a recursos

*Patrones de asignación comunes:*

-   [**Función de asignación del montón**](/windows/win32/api/heapapi/nf-heapapi-heapalloc)
-   [**Función de asignación de memoria**](https://msdn.microsoft.com/library/6ewkz86d(v=VS.71).aspx)
-   [**New (operador) (C++)**](https://msdn.microsoft.com/library/kewsb8ba(v=VS.71).aspx)
-   [**Función de asignación virtual**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   [Objetos de kernel](../sysinfo/kernel-objects.md)
-   [Identificadores de objetos GDI](../sysinfo/gdi-objects.md)
-   [Identificadores de objeto de interfaz de usuario](../sysinfo/user-objects.md)

*Herramientas de Microsoft:*

-   [Comprobador de aplicación](application-verifier.md)
-   [Herramientas de depuración para Windows](/windows-hardware/drivers/debugger/)
-   [Montón de volcado de modo de usuario](/windows-hardware/drivers/debugger/umdh)
-   [Herramienta de captura, procesamiento y análisis de seguimiento](https://msdn.microsoft.com/performance/cc825801.aspx)
-   [Montón de depuración de CRT](/visualstudio/debugger/crt-debug-heap-details?view=vs-2015)

*Vínculos adicionales:*

-   [**auto- \_ ptr (clase)**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [Clases de memoria de Active Template Library (ATL)](https://msdn.microsoft.com/library/44yh1z4f(v=VS.71).aspx)
-   [**\_com \_ ptr \_ t (objeto)**](https://msdn.microsoft.com/library/417w8b3b(v=VS.71).aspx)
-   [**\_BSTR \_ t (clase)**](https://msdn.microsoft.com/library/zthfhkd6(v=VS.71).aspx)
-   [**\_Variant \_ YT (clase)**](https://msdn.microsoft.com/library/x295h94e(v=VS.71).aspx)
-   ["Seguimiento de pérdidas de memoria administrada"](/archive/blogs/ricom/)
-   ["Descripción y resolución de patrones de fugas de Internet Explorer"](/previous-versions/ms976398(v=msdn.10))
-   ["Detector de fugas de memoria de JavaScript"](/archive/blogs/gpde/new-javascript-memory-leak-detector-from-our-team)
-   [Mitigación de pérdida de memoria circular (en exploradores):](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd361842(v=vs.85))
-   [**try-finally (Instrucción)**](https://msdn.microsoft.com/library/yb3kz605(v=VS.71).aspx)
-   [**Estructura PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)
-   [**PropVariantClear función)**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

 

 
