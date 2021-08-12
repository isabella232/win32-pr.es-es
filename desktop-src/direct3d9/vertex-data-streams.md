---
description: Las interfaces de representación para Direct3D constan de métodos que representan primitivas a partir de datos de vértice almacenados en uno o varios búferes de datos.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Vertex Data Secuencias (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f154621da4ba03f78beee87767130e37da9e9ab9ba899af737b968fb20f0609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290394"
---
# <a name="vertex-data-streams-direct3d-9"></a>Vertex Data Secuencias (Direct3D 9)

Las interfaces de representación para Direct3D constan de métodos que representan primitivas a partir de datos de vértice almacenados en uno o varios búferes de datos. Los datos de vértice constan de elementos de vértice combinados para formar componentes de vértice. Los elementos de vértice, la unidad más pequeña de un vértice, representan entidades como la posición, la normal o el color.

Los componentes de vértice son uno o varios elementos de vértice almacenados de forma contigua (intercalado por vértice) en un solo búfer de memoria. Un vértice completo consta de uno o varios componentes, donde cada componente está en un búfer de memoria independiente. Para representar una primitiva, se leen y ensamblan varios componentes de vértice para que los vértices completos estén disponibles para el procesamiento de vértices. En el diagrama siguiente se muestra el proceso de representación de primitivas mediante componentes de vértice.

![diagrama del proceso para representar primitivas mediante componentes de vértice](images/vertexdata.png)

La representación de primitivas consta de dos pasos. En primer lugar, configure uno o varios flujos de componentes de vértices; en segundo lugar, invoque un [**método IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para representar desde esas secuencias. El sombreador de vértices especifica la identificación de los elementos de vértice dentro de estos flujos de componentes.

Los [**métodos IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) especifican un desplazamiento en los flujos de datos de vértice para que se pueda representar un subconjunto contiguo arbitrario de las primitivas dentro de un conjunto de datos de vértice con cada invocación de dibujo. Esto le permite cambiar el estado de representación del dispositivo entre grupos de primitivos que se representan desde los mismos búferes de vértice.

Se admiten los métodos de dibujo indexado y no indexado. Para obtener más información, vea Representación desde búferes de vértices e [índices (Direct3D 9).](rendering-from-vertex-and-index-buffers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de primitivas](rendering-primitives.md)
</dt> </dl>

 

 
