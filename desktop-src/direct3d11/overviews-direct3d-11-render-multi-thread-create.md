---
title: Creación de objetos con multithreading
description: Use la interfaz ID3D11Device para crear recursos y objetos, use ID3D11DeviceContext para la representación.
ms.assetid: e1765192-865c-4a62-9be7-6e95280ee8ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cbfbe73efc96b301216deb5ccbf623354ddbb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994251"
---
# <a name="object-creation-with-multithreading"></a>Creación de objetos con multithreading

Use la interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) para crear recursos y objetos, use [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) para la [representación](overviews-direct3d-11-render-multi-thread-render.md).

Estos son algunos ejemplos de cómo crear recursos:

-   [Cómo: crear un búfer de vértices](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
-   [Cómo: crear un búfer de índice](overviews-direct3d-11-resources-buffers-index-how-to.md)
-   [Cómo: crear un búfer de constantes](overviews-direct3d-11-resources-buffers-constant-how-to.md)
-   [Cómo: inicializar una textura desde un archivo](overviews-direct3d-11-resources-textures-how-to.md)

## <a name="multithreading-considerations"></a>Consideraciones sobre multithreading

La cantidad de simultaneidad de la creación y representación de recursos que puede alcanzar la aplicación depende del nivel de compatibilidad con multithreading que implementa el controlador. Si el controlador admite las operaciones de creación simultáneas, la aplicación debe tener muchos menos problemas de simultaneidad. Sin embargo, si el controlador no admite la creación de objetos simultáneos, la cantidad de simultaneidad es muy limitada. Para comprender la cantidad de soporte técnico disponible en un controlador, consulte en el controlador el valor del miembro **DriverConcurrentCreates** de la estructura de [**\_ \_ \_ subprocesos de datos de la característica D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) . Para obtener más información acerca de cómo comprobar la compatibilidad de los controladores con multithreading, consulte [Cómo: comprobar la compatibilidad](overviews-direct3d-11-render-multi-thread-support.md)de los controladores.

Las operaciones simultáneas no implican necesariamente un mejor rendimiento. Por ejemplo, la creación y carga de una textura suele estar limitada por el ancho de banda de memoria. Es posible que el intento de crear y cargar varias texturas no sea más rápido que la realización de una textura a la vez, incluso si esto deja inactivas varios núcleos de CPU. Sin embargo, la creación de varios sombreadores con varios subprocesos puede aumentar el rendimiento, ya que esta operación es menos dependiente de los recursos del sistema, como el ancho de banda de memoria.

Cuando el controlador y el hardware de gráficos admiten el multithreading, normalmente se pueden inicializar de forma más eficaz los recursos recién creados pasando un puntero a los datos iniciales en el parámetro *pInitialData* (por ejemplo, en una llamada al método [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) ).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




