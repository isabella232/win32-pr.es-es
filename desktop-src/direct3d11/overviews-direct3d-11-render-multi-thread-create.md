---
title: Creación de objetos con multithreading
description: Use la interfaz ID3D11Device para crear recursos y objetos y use id3D11DeviceContext para la representación.
ms.assetid: e1765192-865c-4a62-9be7-6e95280ee8ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 315775394133d62ec40b431d1de11b106b65c831b63f5557a6665f2773be3c9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913369"
---
# <a name="object-creation-with-multithreading"></a>Creación de objetos con multithreading

Use la [**interfaz ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) para crear recursos y objetos, use [**id3D11DeviceContext para**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) [representar](overviews-direct3d-11-render-multi-thread-render.md).

Estos son algunos ejemplos de cómo crear recursos:

-   [Cómo: Crear un búfer de vértices](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
-   [Cómo: Crear un búfer de índice](overviews-direct3d-11-resources-buffers-index-how-to.md)
-   [Cómo: Crear un búfer constante](overviews-direct3d-11-resources-buffers-constant-how-to.md)
-   [Cómo: Inicializar una textura a partir de un archivo](overviews-direct3d-11-resources-textures-how-to.md)

## <a name="multithreading-considerations"></a>Consideraciones sobre multithreading

La cantidad de simultaneidad de creación y representación de recursos que la aplicación puede lograr depende del nivel de compatibilidad con multithreading que implemente el controlador. Si el controlador admite creaciones simultáneas, la aplicación debe tener muchos menos problemas de simultaneidad. Sin embargo, si el controlador no admite la creación simultánea de objetos, la cantidad de simultaneidad es muy limitada. Para comprender la cantidad de compatibilidad disponible en un controlador, consulte al controlador para el valor del miembro **DriverConcurrentCreates** de la estructura [**FEATURE DATA \_ \_ \_ THREADING de D3D11.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) Para obtener más información sobre cómo comprobar la compatibilidad con controladores de multithreading, [vea Cómo: Comprobar la compatibilidad con controladores.](overviews-direct3d-11-render-multi-thread-support.md)

Las operaciones simultáneas no conducen necesariamente a un mejor rendimiento. Por ejemplo, la creación y carga de una textura suele estar limitada por el ancho de banda de memoria. Es posible que intentar crear y cargar varias texturas no sea más rápido que realizar una textura a la vez, incluso si esto deja varios núcleos de CPU inactivos. Sin embargo, la creación de varios sombreadores mediante varios subprocesos puede aumentar el rendimiento, ya que esta operación depende menos de los recursos del sistema, como el ancho de banda de memoria.

Cuando el controlador y el hardware gráfico admiten multithreading, normalmente puede inicializar los recursos recién creados de forma más eficaz pasando un puntero a los datos iniciales en el parámetro *pInitialData* (por ejemplo, en una llamada al método [**ID3D11Device::CreateTexture2D).**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




