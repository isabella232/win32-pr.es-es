---
title: Información general sobre descriptores
description: Los descriptores se crean mediante llamadas API e identifican recursos.
ms.assetid: 64721226-5533-4816-865E-9429032FCC86
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d83b2fbfd5c5df2738c61aea4f1d1115d6c874
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104549132"
---
# <a name="descriptors-overview"></a>Información general sobre descriptores

Los descriptores se crean mediante llamadas API e identifican recursos.

-   [Descriptor datos](#descriptor-data)
-   [Identificadores de descriptor](#descriptor-handles)
-   [Descriptores null](#null-descriptors)
-   [Descriptores predeterminados](#default-descriptors)
-   [Temas relacionados](#related-topics)

## <a name="descriptor-data"></a>Descriptor datos

Un descriptor es un bloque de datos relativamente pequeño que describe por completo un objeto para la GPU, en un formato opaco específico de GPU. Hay varios tipos diferentes de descriptores que &mdash; representan vistas de destino (RTVs), las vistas de estarcido de profundidad (DSV), las vistas de recursos del sombreador (SRVs), las vistas de acceso desordenado (UAVs), las vistas de búfer de constantes (CBVs) y los muestreadores.

Los descriptores varían en tamaño en función del hardware de la GPU. Puede consultar el tamaño de un SRV, UAV o CBV mediante una llamada a [**ID3D12Device:: GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize). Los descriptores se muestran en esta documentación como unidades indivisibles; a continuación se muestra un ejemplo.

![SRV, CBV, UAV y muestreador](images/single-descriptor.png)

Los descriptores se crean mediante llamadas API y incluirán información como el recurso y mapas MIP que quiere que contenga el descriptor.

El controlador no realiza un seguimiento de las referencias a los descriptores ni los mantiene, sino que depende de la aplicación asegurarse de que el tipo de descriptor correcto está en uso y que la información está actualizada. Hay una pequeña excepción a esto; el controlador inspecciona los enlaces de destino de representación para asegurarse de que las cadenas de intercambio funcionan correctamente.

No es necesario que los descriptores de objeto se liberen o se liberen. Los controladores no adjuntan ninguna asignación a la creación de un descriptor. Sin embargo, un descriptor puede codificar las referencias a otras asignaciones para las que la aplicación es propietaria de la duración. Por ejemplo, un descriptor de un SRV debe contener la dirección virtual del recurso D3D (por ejemplo, una textura) a la que se refiere el SRV. Es responsabilidad de la aplicación asegurarse de que no usa un descriptor SRV cuando el recurso D3D subyacente del que depende se ha destruido o se está modificando (por ejemplo, se ha declarado como no residente).

La forma principal de utilizar descriptores es colocarlos en montones de descriptor, que son la memoria de respaldo de los descriptores.

## <a name="descriptor-handles"></a>Identificadores de descriptor

Un identificador de descriptor es la dirección única del descriptor. Es similar a un puntero, pero es opaco porque su implementación es específica del hardware. El identificador es único entre montones de descriptores, por lo que, por ejemplo, una matriz de identificadores puede hacer referencia a los descriptores en varios montones.

Los identificadores de CPU son para su uso inmediato, como la copia en la que se debe identificar el origen y el destino. Inmediatamente después de usar (por ejemplo, una llamada a [**ID3D12GraphicsCommandList:: OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)), se pueden reutilizar o se puede eliminar su montón subyacente.

Los identificadores de GPU no son para su uso inmediato &mdash; identifican ubicaciones de una lista de comandos, para usarlas en el momento de la ejecución de la GPU. Deben conservarse hasta que las listas de comandos que hagan referencia a ellas se ejecuten por completo.

Para crear un identificador de descriptor para el inicio de un montón, después de crear el montón del descriptor, llame a uno de los métodos siguientes:

-   [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)
-   [**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart)

Estos métodos devuelven las siguientes estructuras:

-   [**\_Identificador de \_ descriptor de CPU de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)
-   [**\_Identificador de \_ descriptor de GPU de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

Dado que el tamaño de los descriptores varía según el hardware, para obtener el incremento entre cada descriptor de un montón, use:

-   [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)

Es seguro desplazar una ubicación inicial con un número de incrementos, copiar los identificadores y pasar los identificadores a las llamadas API. No es seguro desreferenciar un identificador como si fuera un puntero de CPU válido, ni para analizar los bits dentro de un identificador.

Se han agregado algunas estructuras auxiliares, con miembros de inicialización, para facilitar la administración de los controladores.

-   [**\_Identificador de \_ descriptor de CPU de CD3DX12 \_**](cd3dx12-cpu-descriptor-handle.md)
-   [**\_Identificador de \_ descriptor de GPU de CD3DX12 \_**](cd3dx12-gpu-descriptor-handle.md)

## <a name="null-descriptors"></a>Descriptores null

Al crear descriptores mediante llamadas API, las aplicaciones pasan NULL para el puntero de recurso en la definición del descriptor para lograr el efecto de nada enlazado cuando un sombreador obtiene acceso a él.

El resto del descriptor debe rellenarse lo máximo posible. Por ejemplo, en el caso de las vistas de recursos del sombreador (SRVs), el descriptor se puede usar para distinguir el tipo de vista que es (Texture1D, Texture2D, etc.). Los parámetros numéricos del descriptor de la vista, como el número de mapas de información, deben establecerse en valores que sean válidos para un recurso.

En muchos casos, hay un comportamiento definido para tener acceso a un recurso sin enlazar, como SRVs, que devuelven los valores predeterminados. Se respetarán cuando se tenga acceso a un descriptor NULL siempre que el tipo de acceso del sombreador sea compatible con el tipo de descriptor. Por ejemplo, si un sombreador espera un Texture2D SRV y accede a un SRV nulo definido como Texture1D, el comportamiento es indefinido y puede dar lugar a un restablecimiento del dispositivo.

En Resumen, para crear un descriptor null, pase `null` para el parámetro *PreSource* al crear la vista con métodos como [**CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview). Para el parámetro View Description *pDesc*, establezca una configuración que funcione si el recurso no era null (de lo contrario, se puede producir un bloqueo en algún hardware).

Sin embargo, los descriptores raíz no deben establecerse en NULL.

En el hardware de Tier1 (consulte los [**niveles de hardware**](./hardware-support.md), se deben inicializar todos los descriptores que están enlazados (a través de tablas de descriptores), ya sea como descriptores reales o descriptores de valores NULL, aunque no se tenga acceso a ellos en el hardware, en caso contrario, el comportamiento es indefinido.

En el hardware Tier2, esto se aplica a los descriptores CBV y UAV enlazados, pero no a los descriptores SRV.

En el hardware nivel 3, no hay ninguna restricción sobre esto, siempre que no se tenga acceso a los descriptores no inicializados.

## <a name="default-descriptors"></a>Descriptores predeterminados

Para crear un descriptor predeterminado para una vista determinada, pase un parámetro de *PreSource* válido al método Create View (como [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)), pero pase **null** para el parámetro *pDesc* . Por ejemplo, si el recurso contenía 14 MIPS, la vista contendría 14 MIPS. El caso predeterminado abarca la asignación más obvia de un recurso a una vista. Esto requiere que el recurso esté asignado con un nombre de formato completo (como **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB** en lugar de **DXGI_FORMAT_R8G8B8A8_TYPELESS**).

Los descriptores predeterminados no se pueden usar con una vista de estructura de aceleración de raytracing, porque el parámetro de *código fuente* proporcionado debe ser **null** y la ubicación se debe pasar a través de [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**]/Windows/Win32/API/d3d12/NS-d3d12-d3d12_raytracing_acceleration_structure_srv).

## <a name="related-topics"></a>Temas relacionados

[Descriptores de](descriptors.md)