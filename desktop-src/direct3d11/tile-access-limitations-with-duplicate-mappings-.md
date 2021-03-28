---
title: Limitaciones de acceso de iconos con asignaciones duplicadas
description: En esta sección se describen las limitaciones de acceso a los mosaicos con asignaciones duplicadas.
ms.assetid: 7A498E0D-9151-4A89-B7C3-C4F476457D17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0909b0d10e286e5f774f6893b692abdeb19d3ef7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075244"
---
# <a name="tile-access-limitations-with-duplicate-mappings"></a>Limitaciones de acceso de iconos con asignaciones duplicadas

En esta sección se describen las limitaciones de acceso a los mosaicos con asignaciones duplicadas.

## <a name="copying-tiled-resources-with-overlapping-source-and-destination"></a>Copiar recursos en mosaico con origen y destino superpuestos

Si los mosaicos del área de origen y de destino de una operación de copia \* tienen asignaciones duplicadas en el área de copia que se habrían superpuesto aunque ambos recursos no estuvieran en mosaico y la operación de copia \* admita copias que se superpongan, la operación de copia \* se comportará correctamente (como si el origen se copiara en una ubicación temporal antes de pasar al destino) Pero si la superposición no es obvia (como los recursos de origen y de destino son diferentes, pero las asignaciones o asignaciones de recursos compartidos se duplican en una superficie determinada), los resultados de la operación de copia en los mosaicos que se comparten no están definidos.

## <a name="copying-to-tiled-resource-with-duplicated-tiles-in-destination-area"></a>Copiar a un recurso en mosaico con iconos duplicados en el área de destino

La copia a un recurso en mosaico con mosaicos duplicados en el área de destino produce resultados sin definir en estos mosaicos a menos que los datos sean idénticos; los distintos mosaicos pueden escribir los mosaicos en pedidos diferentes.

## <a name="uav-accesses-to-duplicate-tiles-mappings"></a>UAV accede a asignaciones de mosaicos duplicadas

Supongamos que una vista de acceso desordenado (UAV) de un recurso en mosaico tiene asignaciones de mosaicos duplicadas en su área o con otros recursos enlazados a la canalización. El orden de los accesos a estos mosaicos duplicados es indefinido si lo realizan varios subprocesos, de la misma forma que cualquier ordenación del acceso a la memoria de UAVs en general no está ordenada.

## <a name="rendering-after-tile-mapping-changes-or-content-updates-from-outside-mappings"></a>Representación tras cambios de asignación de iconos o actualizaciones de contenido desde asignaciones externas

Si las asignaciones de iconos de un recurso en mosaico han cambiado o el contenido de los mosaicos de grupos en mosaico asignados ha cambiado a través de otras asignaciones de recursos en mosaico, y el recurso en mosaico se representará a través de la vista de destino de presentación o de la vista de galería de símbolos de profundidad, la aplicación debe borrar (con la función Fixed API Clear) o copiar por completo mediante Copy \* /Update \* API los mosaicos que han cambiado en el área que se representa (asignado o no). Si un error de una aplicación se borra o se copia en estos casos, las estructuras de optimización de hardware de la vista de destino de presentación o la vista de galería de símbolos de profundidad indicadas serán obsoletas y darán lugar a resultados de representación de elementos no utilizados en hardware e incoherencias en el hardware diferente. Estas estructuras de datos de optimización ocultas que usa el hardware pueden ser locales para asignaciones individuales y no visibles para otras asignaciones a la misma memoria.

La operación [**ID3D11DeviceContext1:: Clearview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview) permite borrar vistas de destino de representación con rectángulos. En el caso de hardware que admita recursos en mosaico, **Clearview** también debe admitir el borrado de las vistas de estarcido de profundidad con rectángulos, solo con la profundidad de las superficies (sin estarcido). Esta operación permite a las aplicaciones borrar solo el área necesaria de una superficie.

Si una aplicación necesita conservar el contenido de la memoria existente de las áreas de un recurso en mosaico en el que han cambiado las asignaciones, esa aplicación debe solucionar el requisito de borrado. La aplicación puede llevar a cabo esta solución alternativa, para lo que debe guardar primero el contenido en el que han cambiado las asignaciones de iconos (copiándolo en una superficie temporal, por ejemplo, mediante [**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)), emitiendo el comando CLEAR necesario y copiando el contenido de nuevo. Aunque esto llevaría a cabo la tarea de conservar el contenido de la superficie para la representación incremental, el inconveniente es que el rendimiento de la representación subsiguiente en la superficie puede verse afectado porque se podrían perder las optimizaciones de representación.

Si un mosaico se asigna a varios recursos en mosaico al mismo tiempo y el contenido de los mosaicos se manipula por cualquier medio (representación, copia, etc.) a través de uno de los recursos en mosaico, si el mismo mosaico se va a representar a través de cualquier otro recurso en mosaico, el icono se debe borrar primero tal y como se ha descrito anteriormente.

## <a name="rendering-to-tiles-shared-outside-render-area"></a>Representar en mosaicos compartidos fuera del área de representación

Supongamos que se está representando un área en un recurso en mosaico y que el área de representación a la que se hace referencia en el área de representación también se asigna desde fuera del área de representación (incluidos a través de otros recursos en mosaico, al mismo tiempo o no). No se garantiza que los datos representados en estos mosaicos aparezcan correctamente cuando se ven a través de las otras asignaciones, aunque el diseño de memoria subyacente sea compatible. Este hecho se debe a que las estructuras de datos de optimización tienen algún uso de hardware que puede ser local para las asignaciones individuales para las superficies representables y no visibles para otras asignaciones a la misma ubicación de memoria. Para solucionar esta restricción, puede copiar desde la asignación representada a todas las demás asignaciones a la misma memoria a la que se puede tener acceso (o borrar esa memoria o copiar otros datos en ella si ya no se necesita el contenido anterior). Aunque parece ser redundante, el resto de las asignaciones a la misma memoria comprenden correctamente cómo obtener acceso a su contenido y, al menos, el ahorro de memoria de tener solo una copia de seguridad de memoria física permanece intacto. Además, cuando se cambia entre el uso de diferentes recursos en mosaico que comparten asignaciones (a menos que solo se lean), debe llamar a la API [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) entre los modificadores.

## <a name="rendering-to-tiles-shared-within-render-area"></a>Representar en mosaicos compartidos dentro del área de representación

Si un área de un recurso en mosaico se está representando en el área de representación, varios mosaicos se asignan a la misma ubicación del grupo de mosaicos y los resultados de la representación no se definen en esos mosaicos.

## <a name="data-compatibility-across-tiled-resources-sharing-tiles"></a>Compatibilidad de datos en recursos en mosaico compartir iconos

Suponga que varios recursos en mosaico tienen asignaciones a las mismas ubicaciones de grupo de mosaicos y cada recurso se usa para tener acceso a los mismos datos. Este escenario solo es válido si se evitan las demás reglas sobre cómo evitar problemas con las estructuras de optimización de hardware, se realizan las llamadas adecuadas a [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) y los recursos en mosaico son compatibles entre sí. Este último se describe aquí en lo que se refiere a lo que significa que los recursos en mosaico comparten iconos para que no sean compatibles. Las condiciones de incompatibilidad para tener acceso a los mismos datos a través de asignaciones de mosaicos duplicadas son el uso de diferentes dimensiones o formato de superficie, o diferencias en la presencia de marcadores de destino de representación o de estarcido de profundidad en los recursos. La escritura en la memoria con un tipo de asignación produce resultados no definidos si posteriormente se lee o se representa a través de una asignación de un recurso incompatible. Si las otras asignaciones de uso compartido de recursos se inicializan por primera vez con nuevos datos (reciclando la memoria para un propósito diferente), la operación de lectura o de presentación subsiguiente es correcta, ya que los datos no se purgan entre interpretaciones incompatibles. Sin embargo, debe llamar a la API **TiledResourceBarrier** cuando cambie entre el acceso a asignaciones incompatibles como este.

Si el marcador de enlace de la galería de símbolos de profundidad o destino de representación no está establecido en ninguno de los recursos que comparten asignaciones entre sí, hay muchas menos restricciones. Siempre que los tipos de formato y superficie (por ejemplo, Texture2D) sean los mismos, se pueden compartir los mosaicos. Los distintos formatos compatibles son casos como superficies de BC \* y el tamaño equivalente sin comprimir 32 bits o 16 bits por formato de componente, como BC6H y R32G32B32A32. Muchos formatos de elementos de 32 bits por elemento también pueden tener alias R32 \_ \* (R10G10B10A2 \_ \* , R8G8B8A8 \_ \* , B8G8R8A8 \_ \* , B8G8R8X8 \_ \* , R16G16 \_ \* ); esta operación siempre se permite para los recursos no en mosaico.

El uso compartido entre mosaicos empaquetados y no empaquetados es correcto si los formatos son compatibles y los mosaicos se rellenan con colores sólidos.

Por último, si no hay nada más común sobre las asignaciones de iconos de uso compartido de recursos, excepto si ninguno tiene marcadores de destino de representación o de estarcido de profundidad, solo se puede compartir de forma segura la memoria rellenada con 0. la asignación aparecerá como cualquier 0 descodifica en para la definición del formato de recurso especificado (normalmente solo 0).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso de canalización a recursos en mosaico](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




