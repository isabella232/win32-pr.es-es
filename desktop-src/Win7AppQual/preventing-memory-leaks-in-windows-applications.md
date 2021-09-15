---
description: Obtenga información sobre cómo evitar pérdidas de memoria en Windows aplicaciones para Windows 7 y Windows Server 2008 R2.
ms.assetid: c5dedcab-3e6f-433f-95de-d741321c683e
title: Evitar fugas de memoria en Windows aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e973da19d075ac94824df340d1741fd9cefb3486
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474548"
---
# <a name="preventing-memory-leaks-in-windows-applications"></a>Evitar fugas de memoria en Windows aplicaciones

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  

## <a name="description"></a>Descripción

Las fugas de memoria son una clase de errores en los que la aplicación no puede liberar memoria cuando ya no se necesita. Con el tiempo, las pérdidas de memoria afectan al rendimiento tanto de la aplicación concreta como del sistema operativo. Una fuga grande podría dar lugar a tiempos de respuesta inaceptables debido a una paginación excesiva. Finalmente, la aplicación y otras partes del sistema operativo experimentarán errores.

Windows liberará toda la memoria asignada por la aplicación al finalizar el proceso, por lo que las aplicaciones de ejecución corta no afectarán significativamente al rendimiento general del sistema. Sin embargo, las pérdidas en procesos de ejecución larga, como servicios o incluso complementos del Explorador, pueden afectar enormemente a la confiabilidad del sistema y podrían obligar al usuario a reiniciar Windows para que el sistema se pueda usar de nuevo.

Las aplicaciones pueden asignar memoria en su nombre por varios medios. Cada tipo de asignación puede producir una pérdida si no se libera después de su uso. Estos son algunos ejemplos de patrones de asignación comunes:

-   Memoria del montón a través [**de la función HeapAlloc**](/windows/win32/api/heapapi/nf-heapapi-heapalloc) o su entorno de ejecución de C/C++ equivalente a **malloc** o **new**
-   Asignaciones directas desde el sistema operativo a través de [**la función VirtualAlloc.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   Los identificadores de kernel creados a través de las API de Kernel32, como [**CreateFile,**](/windows/win32/api/fileapi/nf-fileapi-createfilea) [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)o [**CreateThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)mantienen la memoria del kernel en nombre de la aplicación.
-   Identificadores GDI y USER creados mediante las API User32 y Gdi32 (de forma predeterminada, cada proceso tiene una cuota de 10 000 identificadores)

## <a name="best-practices"></a>Prácticas recomendadas

La supervisión del consumo de recursos de la aplicación a lo largo del tiempo es el primer paso para detectar y diagnosticar pérdidas de memoria. Use Windows Administrador de tareas y agregue las columnas siguientes: "Tamaño de confirmación", "Identificadores", "Objetos de usuario" y "Objetos GDI". Esto le permitirá establecer una línea base para la aplicación y supervisar el uso de recursos a lo largo del tiempo.

![Captura de pantalla que muestra la página "Procesos" en Windows Administrador de tareas.](images/preventingmemoryleaks-windowstaskmanager.gif)

Las siguientes herramientas de Microsoft proporcionan información más detallada y pueden ayudar a detectar y diagnosticar pérdidas para los distintos tipos de asignación de la aplicación:

-   Monitor de rendimiento y Monitor de recursos forman parte de Windows 7 y pueden supervisar y usar recursos de grafos con el tiempo
-   La versión más reciente de Application Verifier diagnóstico de pérdidas de montón en Windows 7
-   UMDH, que forma parte de las herramientas de depuración para Windows, analiza las asignaciones de memoria del montón para un proceso determinado y puede ayudar a encontrar pérdidas y otros patrones de uso inusuales.
-   Xperf es una sofisticada herramienta de análisis de rendimiento compatible con seguimientos de asignación de montón
-   El montón de depuración de CRT realiza un seguimiento de las asignaciones de montón y puede ayudar a crear sus propias características de depuración de montón.

Ciertas prácticas de codificación y diseño pueden limitar el número de pérdidas en el código.

-   Use punteros inteligentes en código de C++, tanto para las asignaciones de montón como para los recursos de Win32, como los **identificadores de** kernel. La biblioteca estándar de C++ proporciona la **\_ clase auto ptr** para las asignaciones de montón. Para otros tipos de asignación, deberá escribir sus propias clases. La biblioteca ATL proporciona un amplio conjunto de clases para la administración automática de recursos para objetos de montón y identificadores de kernel.
-   Use características intrínsecas del compilador como **\_ com \_ ptr \_ t** para encapsular los punteros de interfaz COM en "punteros inteligentes" y ayudar con el recuento de referencias. Hay clases similares para otros tipos de datos COM: **\_ bstr \_ t** y **\_ variant \_ t**
-   Supervise el uso inusual de memoria del código .NET. El código administrado no es insótez a las pérdidas de memoria. Consulte ["Seguimiento de pérdidas de memoria administradas"](/archive/blogs/ricom/) sobre cómo encontrar fugas de GC.
-   Tenga en cuenta los patrones de fuga en el código del lado cliente web. Las referencias circulares entre objetos COM y motores de scripting como JScript pueden provocar grandes pérdidas en las aplicaciones web. ["Understanding and Solving Internet Explorer Leak Patterns"](/previous-versions/ms976398(v=msdn.10)) (Descripción y resolución de Internet Explorer de fugas de datos) tiene más información sobre estos tipos de pérdidas. Puede usar el Detector de fugas de memoria de JavaScript para depurar fugas de memoria en el código. Aunque Windows Internet Explorer 8, que se está enviando con Windows 7, mitiga la mayoría de estos problemas, los exploradores más antiguos siguen siendo vulnerables a estos errores.
-   Evite usar varias rutas de acceso de salida de una función. Las asignaciones asignadas a variables en el ámbito de la función deben liberarse en un bloque determinado al final de la función.
-   No use excepciones en el código sin liberar todas las variables locales en las funciones. Si usa excepciones nativas, libera todas las asignaciones dentro del \_ \_ bloque finally. Si usa excepciones de C++, todos los montones y las asignaciones de identificadores deben encapsularse en punteros inteligentes.
-   No descarte ni reinicialice un objeto [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) sin llamar a la [**función PropVariantClear.**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

## <a name="links-to-resources"></a>Vínculos a recursos

*Patrones de asignación comunes:*

-   [**Función de asignación de montón**](/windows/win32/api/heapapi/nf-heapapi-heapalloc)
-   [**Función de asignación de memoria**](https://msdn.microsoft.com/library/6ewkz86d(v=VS.71).aspx)
-   [**Operador New (C++)**](https://msdn.microsoft.com/library/kewsb8ba(v=VS.71).aspx)
-   [**Función de asignación virtual**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   [Objetos de kernel](../sysinfo/kernel-objects.md)
-   [Identificadores de objetos GDI](../sysinfo/gdi-objects.md)
-   [Interfaz de usuario identificadores de objeto](../sysinfo/user-objects.md)

*Herramientas de Microsoft:*

-   [Comprobador de aplicación](application-verifier.md)
-   [Herramientas de depuración para Windows](/windows-hardware/drivers/debugger/)
-   [Montón de volcado de modo de usuario](/windows-hardware/drivers/debugger/umdh)
-   [Herramienta de captura, procesamiento y análisis de seguimiento](https://msdn.microsoft.com/performance/cc825801.aspx)
-   [Montón de depuración de CRT](/visualstudio/debugger/crt-debug-heap-details?view=vs-2015)

*Vínculos adicionales:*

-   [**auto \_ ptr (clase)**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [Active Template Library de memoria (ATL)](https://msdn.microsoft.com/library/44yh1z4f(v=VS.71).aspx)
-   [**\_com \_ ptr \_ t (objeto)**](https://msdn.microsoft.com/library/417w8b3b(v=VS.71).aspx)
-   [**\_bstr \_ t (Clase)**](https://msdn.microsoft.com/library/zthfhkd6(v=VS.71).aspx)
-   [**\_variant \_ yt (Clase)**](https://msdn.microsoft.com/library/x295h94e(v=VS.71).aspx)
-   ["Seguimiento de pérdidas de memoria administradas"](/archive/blogs/ricom/)
-   ["Understanding and Solving Internet Explorer Leak Patterns"](/previous-versions/ms976398(v=msdn.10))
-   ["Detector de fugas de memoria de JavaScript"](/archive/blogs/gpde/new-javascript-memory-leak-detector-from-our-team)
-   [Mitigación de fugas de memoria circular (en exploradores):](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd361842(v=vs.85))
-   [**try-finally (Instrucción)**](https://msdn.microsoft.com/library/yb3kz605(v=VS.71).aspx)
-   [**PROPVARIANT (estructura)**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)
-   [**PropVariantClear (Función)**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

 

 
