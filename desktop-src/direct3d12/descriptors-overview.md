---
title: Información general sobre los descriptores
description: Los descriptores se crean mediante llamadas API e identifican recursos.
ms.assetid: 64721226-5533-4816-865E-9429032FCC86
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95cb5834c513b99e737ba8a106ea5303a978751573ffd2ca1a97fb59e385b5ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733852"
---
# <a name="descriptors-overview"></a>Información general sobre los descriptores

Los descriptores se crean mediante llamadas API e identifican recursos.

-   [Datos descriptores](#descriptor-data)
-   [Identificadores de descriptor](#descriptor-handles)
-   [Descriptores NULL](#null-descriptors)
-   [Descriptores predeterminados](#default-descriptors)
-   [Temas relacionados](#related-topics)

## <a name="descriptor-data"></a>Datos descriptores

Un descriptor es un bloque de datos relativamente pequeño que describe completamente un objeto para la GPU, en un formato opaco específico de GPU. Hay varios tipos diferentes de descriptores que representan vistas de destino (RTV), vistas de galería de símbolos de profundidad (DSV), vistas de recursos de sombreador (SRV), vistas de acceso desordenado (UAV), vistas de búfer constante &mdash; (CBV) y muestreadores.

Los descriptores varían de tamaño, dependiendo del hardware de GPU. Puede consultar el tamaño de un SRV, UAV o CBV llamando a [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize). Los descriptores se muestran en esta documentación como unidades indivisibles; este es un ejemplo.

![srv, cbv, uav y sampler](images/single-descriptor.png)

Los descriptores se crean mediante llamadas API e incluirán información como el recurso y mip-maps que desea que contenga el descriptor.

El controlador no realiza el seguimiento ni contiene referencias a descriptores, es la aplicación la que debe asegurarse de que el tipo de descriptor correcto está en uso y que la información está actualizada. Hay una pequeña excepción a esto; el controlador inspecciona los enlaces de destino de representación para asegurarse de que las cadenas de intercambio funcionan correctamente.

No es necesario liberar ni liberar descriptores de objetos. Los controladores no asocian ninguna asignación a la creación de un descriptor. Sin embargo, un descriptor puede codificar referencias a otras asignaciones para las que la aplicación posee la duración. Por ejemplo, un descriptor para un SRV debe contener la dirección virtual del recurso D3D (por ejemplo, una textura) a la que hace referencia el SRV. Es responsabilidad de la aplicación asegurarse de que no usa un descriptor SRV cuando el recurso D3D subyacente del que depende se ha destruyedo o se está modificando (por ejemplo, se declara como no irreidente).

La manera principal de usar descriptores es colocarlos en montones de descriptores, que son memoria de respaldo para descriptores.

## <a name="descriptor-handles"></a>Identificadores de descriptor

Un identificador de descriptor es la dirección única del descriptor. Es similar a un puntero, pero es opaco, ya que su implementación es específica del hardware. El identificador es único entre montones de descriptores, por lo que, por ejemplo, una matriz de identificadores puede hacer referencia a descriptores en varios montones.

Los identificadores de CPU son para su uso inmediato, como copiar donde se deben identificar tanto el origen como el destino. Inmediatamente después de su uso (por ejemplo, una llamada a [**ID3D12GraphicsCommandList::OMSetRenderTargets),**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)se pueden reutilizar o se puede eliminar su montón subyacente.

Los identificadores de GPU no son para uso inmediato, ya que identifican ubicaciones de una &mdash; lista de comandos, para su uso en tiempo de ejecución de GPU. Deben conservarse hasta que las listas de comandos que hacen referencia a ellas se ejecuten por completo.

Para crear un identificador de descriptor para el inicio de un montón, después de crear el propio montón del descriptor, llame a uno de los métodos siguientes:

-   [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)
-   [**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart)

Estos métodos devuelven las estructuras siguientes:

-   [**IDENTIFICADOR DEL DESCRIPTOR DE CPU D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)
-   [**IDENTIFICADOR DEL DESCRIPTOR DE GPU D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

A medida que el tamaño de los descriptores varía según el hardware, para obtener el incremento entre cada descriptor de un montón, use:

-   [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)

Es seguro desplazar una ubicación inicial con una serie de incrementos, copiar identificadores y pasar identificadores a las llamadas API. No es seguro desreferenciar un identificador como si fuera un puntero de CPU válido, ni analizar los bits dentro de un identificador.

Se han agregado algunas estructuras auxiliares, con miembros de inicialización, para facilitar un poco la administración de identificadores.

-   [**IDENTIFICADOR DEL DESCRIPTOR DE \_ CPU CD3DX12 \_ \_**](cd3dx12-cpu-descriptor-handle.md)
-   [**IDENTIFICADOR DEL \_ DESCRIPTOR DE GPU CD3DX12 \_ \_**](cd3dx12-gpu-descriptor-handle.md)

## <a name="null-descriptors"></a>Descriptores NULL

Al crear descriptores mediante llamadas API, las aplicaciones pasan NULL para el puntero de recurso en la definición del descriptor a fin de lograr el efecto de nada enlazado cuando un sombreador tiene acceso a él.

El resto del descriptor debe rellenarse tanto como sea posible. Por ejemplo, en el caso de las vistas de recursos de sombreador (SRV), el descriptor se puede usar para distinguir el tipo de vista que es (Texture1D, Texture2D, y así sucesivamente). Los parámetros numéricos del descriptor de vista, como el número de mapas mip, deben establecerse en valores válidos para un recurso.

En muchos casos, hay un comportamiento definido para acceder a un recurso sin enlazar, como los SRV que devuelven valores predeterminados. Se respetarán al acceder a un descriptor NULL siempre que el tipo de acceso del sombreador sea compatible con el tipo de descriptor. Por ejemplo, si un sombreador espera un SRV de Texture2D y accede a un SRV NULL definido como Texture1D, el comportamiento es indefinido y podría dar lugar al restablecimiento del dispositivo.

En resumen, para crear un descriptor null, pase para el parámetro pResource al crear la vista con métodos como `null` [**CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview).  Para el parámetro de descripción de vista *pDesc*, establezca una configuración que funcione si el recurso no es NULL (de lo contrario, puede producirse un bloqueo en algún hardware).

Sin embargo, los descriptores raíz no deben establecerse en NULL.

En el hardware de nivel 1 (consulte Niveles de hardware ), todos los descriptores [**enlazados**](./hardware-support.md)(a través de tablas de descriptores) deben inicializarse, ya sea como descriptores reales o descriptores null, aunque el hardware no tenga acceso a ellos; de lo contrario, el comportamiento no está definido.

En el hardware de nivel 2, esto se aplica a los descriptores CBV y UAV enlazados, pero no a los descriptores SRV.

En el hardware de nivel 3, no hay ninguna restricción al respecto, siempre que nunca se acceda a descriptores sin inicializar.

## <a name="default-descriptors"></a>Descriptores predeterminados

Para crear un descriptor predeterminado para una vista determinada, pase un parámetro *pResource* válido al método create view (como [**CreateShaderResourceView),**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)pero pase **NULL** para el *parámetro pDesc.* Por ejemplo, si el recurso contenía 14 mips, la vista contendrá 14 mips. El caso predeterminado trata la asignación más obvia de un recurso a una vista. Esto requiere que el recurso se asigne con un nombre de formato completo (por **ejemplo, DXGI_FORMAT_R8G8B8A8_UNORM_SRGB** en lugar **de DXGI_FORMAT_R8G8B8A8_TYPELESS**).

Los descriptores predeterminados no se pueden usar con una vista de estructura de aceleración de raytracing, porque el parámetro *pResource* proporcionado debe ser **NULL** y la ubicación debe pasarse a través de [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**]/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv).

## <a name="related-topics"></a>Temas relacionados

[Descriptores de](descriptors.md)