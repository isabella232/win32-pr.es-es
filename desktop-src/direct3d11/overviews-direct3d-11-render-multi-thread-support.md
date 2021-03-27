---
title: Cómo comprobar la compatibilidad de controladores
description: En este tema se muestra cómo determinar si las características de multithreading (incluida la creación de recursos y las listas de comandos) se admiten para la aceleración de hardware.
ms.assetid: f577357c-c2e5-4e58-9870-2e995bdc6782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae42bbb3eedb76d049479839d497a79db81b5697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996756"
---
# <a name="how-to-check-for-driver-support"></a>Cómo: comprobar la compatibilidad de controladores

En este tema se muestra cómo determinar si las características de multithreading (incluida la [creación de recursos](overviews-direct3d-11-render-multi-thread-intro.md) y [las listas de comandos](overviews-direct3d-11-render-multi-thread-command-list.md)) se admiten para la aceleración de hardware.

Se recomienda que las aplicaciones comprueben la compatibilidad de hardware de gráficos con multithreading. Si el controlador y el hardware de gráficos no admiten la creación de objetos multiproceso, el rendimiento se puede limitar de las siguientes maneras:

-   Es posible que se limite la creación de varios objetos (incluso de tipos diferentes) al mismo tiempo.
-   La creación de un objeto mientras se representan los comandos de gráficos mediante un [contexto inmediato](overviews-direct3d-11-render-multi-thread-render.md) podría estar limitada. Por ejemplo, si el hardware no admite el multithreading, una aplicación debe evitar crear en un subproceso en segundo plano un objeto que requiera mucho tiempo de creación. Una operación de creación que tarda mucho tiempo puede bloquear la representación de contexto inmediata y aumentar el riesgo de una velocidad de fotogramas visual intermitente.

El motor en tiempo de ejecución admite multithreading y listas de comandos, independientemente de la compatibilidad de controladores y hardware. Si no hay compatibilidad con controladores y hardware para multithreads o listas de comandos, el tiempo de ejecución emulará la funcionalidad. Para obtener más información sobre el multithreading, vea [Introducción al multithreading en Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md).

**Para comprobar la compatibilidad de los controladores con multithreading:**

1.  Inicialice un objeto de interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) . De forma predeterminada, el multithreading está habilitado.
2.  Llame a [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Pase el valor de **\_ \_ subproceso de la característica D3D11** al parámetro de *característica* , pase la estructura de [**\_ \_ \_ subprocesos de datos de la característica D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) al parámetro *pFeatureSupportData* y pase el tamaño de la estructura de **\_ \_ \_ subprocesos de datos de la característica D3D11** al parámetro *FeatureSupportDataSize* .
3.  Si el método [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) se ejecuta correctamente, la estructura de [**\_ \_ \_ subprocesos de datos de la característica D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) que pasó en el paso anterior se inicializará con información sobre la compatibilidad con multithreading.
    -   Si **DriverConcurrentCreates** es **true**, un controlador puede crear más de un recurso al mismo tiempo (simultáneamente) en subprocesos diferentes.

        Si **DriverCommandLists** es **true**, el controlador admite listas de comandos. Es decir, los comandos de representación emitidos por un contexto inmediato pueden estar simultáneos con la creación de objetos en subprocesos independientes con un bajo riesgo de una velocidad de fotogramas intermitente.

    -   Si **DriverConcurrentCreates** es **false**, un controlador no admite la creación simultánea, lo que significa que la cantidad de simultaneidad posible es muy limitada. El hardware gráfico no puede crear objetos de tipos diferentes en diferentes subprocesos simultanueously. Además, el hardware gráfico no puede usar un contexto inmediato para emitir comandos de representación mientras el hardware gráfico intenta crear un recurso en otro subproceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




