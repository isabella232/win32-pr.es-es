---
title: Mapas en un grupo de iconos
description: Cuando se crea un recurso con la marca MISC TILED del RECURSO D3D11, los iconos que lo crean proceden de apuntar a ubicaciones de un grupo \_ \_ de \_ mosaicos.
ms.assetid: 1DBE23B2-A1E6-4491-9B74-4E92508A68FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a31d2e8cd4457281c047db514dd2450d3bf70d85be7e4933cb7e5f5e026a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045623"
---
# <a name="mappings-are-into-a-tile-pool"></a>Mapas en un grupo de iconos

Cuando se crea un recurso con la marca [**\_ \_ MISC \_ TILED de D3D11 RESOURCE,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) los iconos que lo crean proceden de apuntar a ubicaciones de un grupo de mosaicos. Un grupo de mosaicos es un grupo de memoria (con el respaldo de una o varias asignaciones en segundo plano, que la aplicación no ve). El sistema operativo y el controlador de pantalla administran este grupo de memoria, y una aplicación entiende fácilmente la superficie de memoria. Los recursos en mosaico asignan regiones de 64 KB apuntando a ubicaciones de un grupo de mosaicos. Una parte de esta configuración es que permite que varios recursos compartan y reutilicen los mismos iconos, así como que los mismos iconos se reutilicen en diferentes ubicaciones dentro de un recurso si lo desea.

El costo de la flexibilidad de rellenar los iconos de un recurso de un grupo de mosaicos es que el recurso tiene que realizar el trabajo de definir y mantener la asignación de los iconos del grupo de mosaicos que representan los iconos necesarios para el recurso. Se pueden cambiar las asignaciones de mosaicos. Además, no todos los iconos de un recurso deben asignarse a la vez; un recurso puede tener **asignaciones NULL.** Una **asignación** NULL define un icono como que no está disponible desde el punto de vista del recurso que accede a él.

Se pueden crear varios grupos de mosaicos y cualquier número de recursos en mosaico se puede asignar a un grupo de mosaicos determinado al mismo tiempo. Los grupos de mosaicos también se pueden crecer o encodeñar. Para obtener más información, vea Tile pool resizing (Tamaño [del grupo de mosaicos).](tile-pool-resizing.md) Una restricción que existe para simplificar la implementación del controlador de visualización y el tiempo de ejecución es que un recurso en mosaico determinado solo puede tener asignaciones a como máximo un grupo de mosaicos a la vez (en lugar de tener asignaciones simultáneas a varios grupos de mosaicos).

La cantidad de almacenamiento asociada a un recurso en mosaico (es decir, memoria independiente del grupo de mosaicos) es aproximadamente proporcional al número de iconos asignados realmente al grupo en un momento dado. En el hardware, este hecho se reduce a la reducción de la superficie de memoria para el almacenamiento de tablas de página aproximadamente con la cantidad de iconos asignados (por ejemplo, mediante un esquema de tabla de página de varios niveles según corresponda).

El grupo de mosaicos se puede pensar en una abstracción completamente de software que permite a las aplicaciones de Direct3D programar eficazmente las tablas de página en la unidad de procesamiento gráfico (GPU) sin tener que conocer los detalles de implementación de bajo nivel (o tratar directamente con direcciones de puntero). Los grupos de mosaicos no aplican ningún nivel adicional de direccionamiento indirecto en el hardware. Las optimizaciones de una tabla de página de un solo nivel mediante construcciones como directorios de página son independientes del concepto de grupo de mosaicos.

Vamos a explorar qué almacenamiento podría requerir la propia tabla de páginas en el peor de los casos (aunque en la práctica las implementaciones solo requieren almacenamiento aproximadamente proporcional a lo que se asigna).

Supongamos que cada entrada de tabla de página es de 64 bits.

Para el peor de los casos en que se alcanzó el tamaño de tabla de página para una sola superficie, dados los límites de recursos de Direct3D 11, suponga que se crea un recurso en mosaico con un formato de 128 bits por elemento (por ejemplo, un float RGBA), por lo que un icono de 64 KB solo contiene 4096 píxeles. El tamaño máximo admitido de [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) de 16384 \* 16384 2048 (pero solo con un solo mipmap) requeriría aproximadamente 1 GB de almacenamiento en la tabla de páginas si se rellena completamente (sin incluir mipmaps) mediante entradas de tabla de \* 64 bits. La adición de mapas mip aumentaría el almacenamiento de tablas de páginas totalmente asignado (en el peor de los casos) en aproximadamente un tercero, hasta unos 1,3 GB.

Este caso daría acceso a unos 10,6 terabytes de memoria direccionable. Sin embargo, puede haber un límite en la cantidad de memoria direccionable, lo que reduciría estas cantidades, quizás a alrededor del intervalo de terabytes.

Otro caso a tener en cuenta es un único recurso en mosaico [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) de 16384 16384 con un formato \* de 32 bits por elemento, incluidos los mapas mip. El espacio necesario en una tabla de páginas totalmente rellenada sería aproximadamente de 170 KB con entradas de tabla de 64 bits.

Por último, considere un ejemplo con un formato BC, por ejemplo BC7 con 128 bits por mosaico de 4 x 4 píxeles. Es decir, un byte por píxel. Una [**texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) de 16384 \* 16384 2048 que incluya mapas mip requeriría aproximadamente 85 MB para rellenar completamente esta memoria en una tabla de \* páginas. Esto no está mal teniendo en cuenta que permite que un recurso en mosaico abarque 550 gigapixeles (512 GB de memoria en este caso).

En la práctica, se definirían cerca de estas asignaciones completa, dado que la cantidad de memoria física disponible no permitiría asignar y hacer referencia a una cantidad cercana a esa cantidad a la vez. Sin embargo, con un grupo de mosaicos, las aplicaciones podrían optar por reutilizar iconos (por ejemplo, reutilizar un icono de color "negro" para regiones de color negro grandes en una imagen), usando de forma eficaz el grupo de mosaicos (es decir, las asignaciones de tablas de páginas) como herramienta para la compresión de memoria.

El contenido inicial de la tabla de páginas **es NULL** para todas las entradas. Las aplicaciones tampoco pueden pasar datos iniciales para el contenido de memoria de la superficie, ya que se inician sin respaldo de memoria.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creación de grupos de iconos](tile-pool-creation.md)<br/>                                                 | Un grupo de mosaicos se crea a través de la API [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) pasando la marca GRUPO DE MOSAICOS MISC DE RECURSOS de [**D3D11 \_ \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) en el miembro **MiscFlags** de la estructura [**\_ \_ DESC buffer de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a la que apunta el *parámetro pDesc.* <br/> |
| [Cambio del tamaño de los grupos de iconos](tile-pool-resizing.md)<br/>                                                 | Use la API [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) para aumentar el tamaño de un grupo de mosaicos si la aplicación necesita más espacio de trabajo para la asignación de recursos en mosaico en él o para reducir si se necesita menos espacio. <br/>                                                                                                                    |
| [Seguimiento de peligros frente a recursos de grupos de iconos](hazard-tracking-versus-tile-pool-resources.md)<br/> | En el caso de los recursos que no están en mosaico, Direct3D puede evitar ciertas condiciones de peligro durante la representación, pero dado que el seguimiento de riesgos se realizaría en un nivel de mosaico para los recursos en mosaico, el seguimiento de las condiciones de peligro durante la representación de los recursos en mosaico podría ser demasiado costoso. <br/>                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de recursos en mosaico](creating-tiled-resources.md)
</dt> </dl>

 

