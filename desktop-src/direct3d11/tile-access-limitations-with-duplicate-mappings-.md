---
title: Limitaciones de acceso de iconos con asignaciones duplicadas
description: En esta sección se describen las limitaciones de acceso a los mosaicos con asignaciones duplicadas.
ms.assetid: 7A498E0D-9151-4A89-B7C3-C4F476457D17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0909b0d10e286e5f774f6893b692abdeb19d3ef7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966895"
---
# <a name="tile-access-limitations-with-duplicate-mappings"></a>Limitaciones de acceso de iconos con asignaciones duplicadas

En esta sección se describen las limitaciones de acceso a los mosaicos con asignaciones duplicadas.

## <a name="copying-tiled-resources-with-overlapping-source-and-destination"></a>Copia de recursos en mosaico con origen y destino superpuestos

Si los iconos del área de origen y destino de una operación de copia tienen asignaciones duplicadas en el área de copia que se hubieran superpuesto incluso si ambos recursos no fueran recursos en mosaico y la operación de copia admite copias superpuestas, la operación de copia se comportará correctamente (como si el origen se copiara en una ubicación temporal antes de ir \* \* al \* destino). Pero si la superposición no es obvia (como los recursos de origen y destino son diferentes, pero las asignaciones o asignaciones de recursos compartidos se duplican en una superficie determinada), los resultados de la operación de copia en los iconos que se comparten no están definidos.

## <a name="copying-to-tiled-resource-with-duplicated-tiles-in-destination-area"></a>Copia en un recurso en mosaico con iconos duplicados en el área de destino

La copia en un recurso en mosaico con iconos duplicados en el área de destino produce resultados indefinidos en estos iconos a menos que los propios datos sean idénticos; diferentes iconos pueden escribir los iconos en distintos pedidos.

## <a name="uav-accesses-to-duplicate-tiles-mappings"></a>Accesos de UAV a asignaciones de iconos duplicados

Supongamos que una vista de acceso no ordenado (UAV) en un recurso en mosaico tiene asignaciones de mosaico duplicadas en su área o con otros recursos enlazados a la canalización. El orden de los accesos a estos iconos duplicados no está definido si lo realizan subprocesos diferentes, igual que cualquier ordenación del acceso a memoria a los UAV en general no está ordenado.

## <a name="rendering-after-tile-mapping-changes-or-content-updates-from-outside-mappings"></a>Representación después de cambios de asignación de mosaicos o actualizaciones de contenido desde asignaciones externas

Si las asignaciones de mosaicos de un recurso en mosaico han cambiado o el contenido de los iconos del grupo de mosaicos asignados ha cambiado a través de las asignaciones de otro recurso en mosaico y el recurso en mosaico se va a representar a través de la vista de destino de representación o la vista de galería de símbolos de profundidad, la aplicación debe borrar (mediante la función fija Borrar API) o copiar completamente mediante las API copy/update los iconos que han cambiado dentro del área que se representa (asignada o \* \* no). Si una aplicación no se borra o copia en estos casos, las estructuras de optimización de hardware para la vista de destino de representación o la vista de galería de símbolos de profundidad dadas están obsoletas y darán lugar a resultados de representación de elementos no utilizados en algún hardware e incoherencia en distintos hardware. Estas estructuras de datos de optimización ocultas que usa el hardware pueden ser asignaciones locales a asignaciones individuales y no visibles para otras asignaciones a la misma memoria.

La [**operación ID3D11DeviceContext1::ClearView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview) admite borrar las vistas de destino de representación con rectángulos. En el caso del hardware que admite recursos en mosaico, **ClearView** también debe admitir el borrado de vistas de galería de símbolos de profundidad con rectángulos, solo para superficies de profundidad (sin galería de símbolos). Esta operación permite a las aplicaciones borrar solo el área necesaria de una superficie.

Si una aplicación necesita conservar el contenido de memoria existente de las áreas de un recurso en mosaico donde las asignaciones han cambiado, esa aplicación debe evitar el requisito claro. La aplicación puede realizar esta solución si primero guarda el contenido en el que han cambiado las asignaciones de mosaicos (al copiarlas en una superficie temporal, por ejemplo, mediante [**ID3D11DeviceContext2::CopyTiles),**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)emitiendo el comando clear necesario y copiando el contenido de nuevo. Aunque esto realizaría la tarea de conservar el contenido de la superficie para la representación incremental, el inconveniente es que el rendimiento de la representación posterior en la superficie podría sufrir porque se podrían perder optimizaciones de representación.

Si un icono se asigna a varios recursos en mosaico al mismo tiempo y el contenido del icono se manipula por cualquier medio (representación, copia, entre otros) a través de uno de los recursos en mosaico, si el mismo icono se va a representar a través de cualquier otro recurso en mosaico, el icono debe borrarse primero como se ha descrito anteriormente.

## <a name="rendering-to-tiles-shared-outside-render-area"></a>Representación en iconos compartidos fuera del área de representación

Supongamos que se representa un área de un recurso en mosaico y que los iconos del grupo de mosaicos a los que hace referencia el área de representación también se asignan desde fuera del área de representación (incluidos otros recursos en mosaico, al mismo tiempo o no). No se garantiza que los datos representados en estos iconos aparezcan correctamente cuando se ven a través de las otras asignaciones, aunque el diseño de memoria subyacente sea compatible. Este hecho se debe a las estructuras de datos de optimización que usan algunos hardware y que pueden ser locales a asignaciones individuales para superficies procesables y no visibles para otras asignaciones en la misma ubicación de memoria. Puede evitar esta restricción copiando desde la asignación representada a todas las demás asignaciones en la misma memoria a la que se puede acceder (o borrando esa memoria o copiando otros datos en ella si el contenido anterior ya no es necesario). Aunque este trabajo parece redundante, hace que todas las demás asignaciones a la misma memoria comprendan correctamente cómo acceder a su contenido y, al menos, el ahorro de memoria de tener solo un único respaldo de memoria física permanece intacto. Además, al cambiar entre el uso de diferentes recursos en mosaico que comparten asignaciones (a menos que solo se lea), debe llamar a la API [**ID3D11DeviceContext2::TiledResourceBarkvm**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) entre los modificadores.

## <a name="rendering-to-tiles-shared-within-render-area"></a>Representación en iconos compartidos dentro del área de representación

Si un área de un recurso en mosaico se representa en y dentro del área de representación se asignan varios iconos a la misma ubicación del grupo de mosaicos, los resultados de la representación no están definidos en esos iconos.

## <a name="data-compatibility-across-tiled-resources-sharing-tiles"></a>Compatibilidad de datos entre recursos en mosaico que comparten iconos

Supongamos que varios recursos en mosaico tienen asignaciones a las mismas ubicaciones del grupo de mosaicos y cada recurso se usa para acceder a los mismos datos. Este escenario solo es válido si se evitan las demás reglas para evitar problemas con las estructuras de optimización de hardware, se realizan las llamadas adecuadas a [**ID3D11DeviceContext2::TiledResourceBarlda**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) y los recursos en mosaico son compatibles entre sí. Este último se describe aquí en términos de lo que significa que los recursos en mosaico que comparten iconos sean incompatibles. Las condiciones de incompatibilidad para acceder a los mismos datos en asignaciones de mosaico duplicadas son el uso de diferentes dimensiones o formatos de superficie, o diferencias en la presencia de marcas de enlace de galería de símbolos de profundidad o destino de representación en los recursos. La escritura en la memoria con un tipo de asignación genera resultados no definidos si posteriormente lee o representa a través de una asignación de un recurso incompatible. Si las otras asignaciones de uso compartido de recursos se inicializan primero con nuevos datos (reciclando la memoria para un propósito diferente), la operación de lectura o representación subsiguiente es correcta, ya que los datos no se cruzan en interpretaciones incompatibles. Sin embargo, debe llamar a la API **TiledResourceBarincompatibilidad** al cambiar entre acceder a asignaciones incompatibles como esta.

Si la marca de enlace de galería de símbolos de profundidad o destino de representación no está establecida en ninguno de los recursos que comparten asignaciones entre sí, hay muchas menos restricciones. Siempre que los tipos de formato y superficie (por ejemplo, Texture2D) sean los mismos, se pueden compartir iconos. Los distintos formatos que son compatibles son casos como las superficies BC y el formato de 32 o 16 bits sin comprimir de tamaño equivalente por componente, como \* BC6H y R32G32B32A32. Muchos formatos de 32 bits por elemento también se pueden usar como alias con R32 \_ \* (R10G10B10A2, \_ \* R8G8B8A8, \_ \* B8G8R8A8 \_ \* , B8G8R8X8 \_ \* , R16G16 ); \_ \* esta operación siempre se ha permitido para recursos que no están en mosaico.

Compartir entre iconos empaquetados y no empaquetados es bueno si los formatos son compatibles y los iconos se rellenan con color sólido.

Por último, si no hay nada común sobre los recursos que comparten asignaciones de mosaicos, salvo que ninguno tiene marcas de enlace de galería de símbolos de profundidad o destino de representación, solo se puede compartir de forma segura la memoria rellenada con 0. la asignación aparecerá como cualquier 0 descodifica a para la definición del formato de recurso especificado (normalmente solo 0).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso de canalización a recursos en mosaico](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




