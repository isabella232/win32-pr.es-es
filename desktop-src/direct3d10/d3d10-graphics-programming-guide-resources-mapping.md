---
description: Copia y acceso a datos de recursos (Direct3D 10)
ms.assetid: 34fd4d15-ee64-4acf-967d-a4afb6f26329
title: Copia y acceso a datos de recursos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdbe3ec1dc970635a08cea455927f21d8928f48d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466842"
---
# <a name="copying-and-accessing-resource-data-direct3d-10"></a>Copia y acceso a datos de recursos (Direct3D 10)

Ya no es necesario pensar en los recursos como creados en la memoria de vídeo o en la memoria del sistema. O si el tiempo de ejecución debe administrar o no la memoria. Gracias a la arquitectura del nuevo WDDM (Windows Display Driver Model), las aplicaciones ahora [](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) crean recursos de Direct3D 10 con diferentes marcas de uso para indicar cómo pretende la aplicación usar los datos de recursos. El nuevo modelo de controlador virtualiza la memoria utilizada por los recursos; A continuación, se convierte en responsabilidad del sistema operativo, controlador o administrador de memoria colocar los recursos en el área de memoria de mayor rendimiento posible dado el uso esperado.

El caso predeterminado es que los recursos estén disponibles para la GPU. Por supuesto, dicho esto, hay ocasiones en las que los datos de recursos deben estar disponibles para la CPU. Copiar datos de recursos para que el procesador adecuado pueda acceder a ellos sin afectar al rendimiento requiere cierto conocimiento de cómo funcionan los métodos de API.

-   [Copia de datos de recursos](#copying-and-accessing-resource-data-direct3d-10)
-   [Acceso a los datos de recursos](#copying-and-accessing-resource-data-direct3d-10)

## <a name="copying-resource-data"></a>Copia de datos de recursos

Los recursos se crean en memoria cuando Direct3D ejecuta una llamada a Create. Se pueden crear en la memoria de vídeo, la memoria del sistema o cualquier otro tipo de memoria. Dado que el modelo de controlador WDDM virtualiza esta memoria, las aplicaciones ya no necesitan realizar un seguimiento del tipo de recursos de memoria en el que se crean.

Lo ideal sería que todos los recursos se encontraran en la memoria de vídeo para que la GPU pueda tener acceso inmediato a ellos. Sin embargo, a veces es necesario que la CPU lea los datos del recurso o que la GPU acceda a los datos de recursos en los que se ha escrito la CPU. Direct3D 10 controla estos distintos escenarios solicitando a la aplicación que especifique un uso y, a continuación, ofrece varios métodos para copiar datos de recursos cuando sea necesario.

En función de cómo se haya creado el recurso, no siempre es posible acceder directamente a los datos subyacentes. Esto puede significar que los datos del recurso deben copiarse del recurso de origen a otro recurso al que el procesador adecuado pueda acceder. En términos de Direct3D 10, la CPU puede acceder directamente a los recursos predeterminados mediante la GPU, los recursos dinámicos y de almacenamiento provisional.

Una vez creado un recurso, no [**se puede**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) cambiar su uso. En su lugar, copie el contenido de un recurso en otro recurso que se creó con un uso diferente. Direct3D 10 proporciona esta funcionalidad con tres métodos diferentes. Los dos primeros métodos( [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)) están diseñados para copiar datos de recursos de un recurso a otro. El tercer método ([**ID3D10Device::UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)) está diseñado para copiar datos de la memoria a un recurso.

Hay dos tipos principales de recursos: asignables y no asignables. Los recursos creados con usos dinámicos o de almacenamiento provisional se pueden asignar, mientras que los recursos creados con usos predeterminados o inmutables no se pueden asignar.

La copia de datos entre recursos no asignables es muy rápida porque este es el caso más común y se ha optimizado para que tenga un buen rendimiento. Dado que la CPU no puede acceder directamente a estos recursos, están optimizados para que la GPU pueda manipularlos rápidamente.

La copia de datos entre recursos asignables es más problemática porque el rendimiento dependerá del uso con el que se creó el recurso. Por ejemplo, la GPU puede leer un recurso dinámico con bastante rapidez, pero no puede escribir en ellos, y la GPU no puede leer ni escribir directamente en los recursos de almacenamiento provisional.

Las aplicaciones que desean copiar datos de un recurso con uso predeterminado en un recurso con uso de almacenamiento provisional (para permitir que la CPU lea los datos, es decir, el problema de la lectura de GPU) deben hacerlo con cuidado. Consulte [Acceso a los datos de recursos](#copying-and-accessing-resource-data-direct3d-10) para obtener más detalles sobre este último caso.

## <a name="accessing-resource-data"></a>Acceso a los datos de recursos

El acceso a un recurso requiere la asignación del recurso; Básicamente, la asignación significa que la aplicación está intentando proporcionar a la CPU acceso a la memoria. El proceso de asignación de un recurso para que la CPU pueda acceder a la memoria subyacente puede provocar algunos cuellos de botella de rendimiento y, por este motivo, se debe tener cuidado en cuanto a cómo y cuándo realizar esta tarea.

El rendimiento puede detenerse si la aplicación intenta asignar un recurso en un momento incorrecto. Si la aplicación intenta acceder a los resultados de una operación antes de que finalice esa operación, se producirá una detención de la canalización.

La realización de una operación de asignación en el momento incorrecto podría provocar una caída grave del rendimiento al forzar que la GPU y la CPU se sincronicen entre sí. Esta sincronización se producirá si la aplicación desea acceder a un recurso antes de que la GPU termine de copiarlo en un recurso que la CPU puede asignar.

La CPU solo puede leer de los recursos creados con la marca USAGE STAGING de D3D10. \_ \_ Puesto que los recursos creados con esta marca no se pueden establecer como salidas de la canalización, si la CPU quiere leer los datos de un recurso generado por la GPU, los datos deben copiarse en un recurso creado con la marca de almacenamiento provisional. La aplicación puede hacerlo mediante los métodos [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) para copiar el contenido de un recurso en otro. A continuación, la aplicación puede obtener acceso a este recurso mediante una llamada al método Map adecuado. Cuando ya no se necesita acceso al recurso, la aplicación debe llamar al método Unmap correspondiente. Por ejemplo, [**ID3D10Texture2D::Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) e [**ID3D10Texture2D::Unmap**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-unmap). Los distintos métodos map devuelven algunos valores específicos en función de las marcas de entrada. Consulte [**la sección Comentarios de mapa**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture1d-map) para obtener más información.

> [!Note]  
> Cuando la aplicación llama al método Map, recibe un puntero a los datos de recursos a los que se va a acceder. El tiempo de ejecución garantiza que el puntero tiene una alineación específica, en función del [nivel de característica](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md). Para [**D3D \_ FEATURE LEVEL \_ \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level) y superior, el puntero se alinea con 16 bytes. Para un valor inferior [**a D3D \_ FEATURE LEVEL \_ \_ 10 \_ 0,**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level)el puntero se alinea con 4 bytes. La alineación de 16 bytes permite a la aplicación realizar operaciones optimizadas para [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))en los datos de forma nativa, sin realineación ni copia.

 

### <a name="performance-considerations"></a>Consideraciones de rendimiento

Es mejor pensar en un equipo como una máquina que se ejecuta como una arquitectura paralela con dos tipos principales de procesadores: uno o más CPU y uno o más GPU. Al igual que en cualquier arquitectura paralela, se logra el mejor rendimiento cuando cada procesador se programa con suficientes tareas para evitar que se queda inactivo y cuando el trabajo de un procesador no espera el trabajo de otro.

El peor escenario para el paralelismo de GPU/CPU es la necesidad de forzar a un procesador a esperar los resultados del trabajo realizado por otro. Direct3D 10 intenta quitar este costo haciendo que los métodos [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) se vuelvan asincrónicos; la copia no se ha ejecutado necesariamente en el momento en que devuelve el método. La ventaja de esto es que la aplicación no paga el costo de rendimiento de copiar realmente los datos hasta que la CPU accede a los datos, que es cuando se llama a Map. Si se llama al método Map una vez copiados realmente los datos, no se produce ninguna pérdida de rendimiento. Por otro lado, si se llama al método Map antes de copiar los datos, se producirá una detención de la canalización.

Las llamadas asincrónicas en Direct3D 10 (que son la gran mayoría de los métodos y, especialmente, las llamadas de representación) se almacenan en lo que se denomina búfer de comandos. Este búfer es interno del controlador de gráficos y se usa para procesar por lotes las llamadas al hardware subyacente para que el costoso cambio del modo de usuario al modo kernel en Microsoft Windows se produzca lo menos posible.

El búfer de comandos se vacía, lo que provoca un cambio de modo de usuario/kernel, en una de estas cuatro situaciones, que son las siguientes.

1.  Se llama a [**Present.**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present)
2.  [**Se llama a ID3D10Device::Flush.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-flush)
3.  El búfer de comandos está lleno; su tamaño es dinámico y está controlado por el sistema operativo y el controlador de gráficos.
4.  La CPU requiere acceso a los resultados de un comando que espera a ejecutarse en el búfer de comandos.

De las cuatro situaciones anteriores, el número cuatro es el más crítico para el rendimiento. Si la aplicación emite una llamada [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**ID3D10Device::CopySubresourceRegion,**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) esta llamada se pone en cola en el búfer de comandos. Si la aplicación intenta asignar el recurso de almacenamiento provisional que era el destino de la llamada de copia antes de vaciar el búfer de comandos, se producirá una detención de canalización porque no solo es necesario ejecutar la llamada al método Copy, sino que también se deben ejecutar todos los demás comandos almacenados en búfer en el búfer de comandos. Esto hará que la GPU y la CPU se sincronicen porque la CPU esperará a acceder al recurso de almacenamiento provisional mientras la GPU vacía el búfer de comandos y, por último, rellena el recurso que la CPU necesita. Una vez que la GPU finaliza la copia, la CPU comenzará a acceder al recurso de almacenamiento provisional, pero durante este tiempo, la GPU estará inactiva.

Si lo hace con frecuencia en tiempo de ejecución, el rendimiento se degradará gravemente. Por ese motivo, la asignación de los recursos creados con el uso predeterminado debe realizarse con cuidado. La aplicación debe esperar lo suficiente para que se vacie el búfer de comandos y, por tanto, todos esos comandos terminen de ejecutarse antes de intentar asignar el recurso de almacenamiento provisional correspondiente. ¿Cuánto tiempo debe esperar la aplicación? Al menos dos fotogramas porque esto permitirá aprovechar al máximo el paralelismo entre las CPU y la GPU. El funcionamiento de la GPU es que mientras la aplicación procesa el fotograma N mediante el envío de llamadas al búfer de comandos, la GPU está ocupada ejecutando las llamadas del marco anterior, N-1.

Por lo tanto, si una aplicación quiere asignar un recurso que se origina en la memoria de vídeo y llama a [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) en el fotograma N, esta llamada comenzará a ejecutarse realmente en el fotograma N+1, cuando la aplicación envíe llamadas para el fotograma siguiente. La copia debe finalizar cuando la aplicación está procesando el marco N+2.




| Fotograma | Estado de GPU/CPU | 
|-------|----------------|
| No | <ul><li>Los problemas de CPU representan llamadas para el marco actual.</li></ul> | 
| N+1 | <ul><li>GPU que ejecuta las llamadas enviadas desde la CPU durante el fotograma N.</li><li>Los problemas de CPU representan llamadas para el marco actual.</li></ul> | 
| N+2 | <ul><li>Gpu finalizó la ejecución de las llamadas enviadas desde la CPU durante el fotograma N. Resultados listos.</li><li>GPU que ejecuta las llamadas enviadas desde la CPU durante el fotograma N+1.</li><li>Los problemas de CPU representan llamadas para el marco actual.</li></ul> | 
| N+3 | <ul><li>Gpu finalizó la ejecución de las llamadas enviadas desde la CPU durante el fotograma N+1. Resultados listos.</li><li>GPU que ejecuta las llamadas enviadas desde la CPU durante el fotograma N+2.</li><li>Los problemas de CPU representan llamadas para el marco actual.</li></ul> | 
| N+4 | ... | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
