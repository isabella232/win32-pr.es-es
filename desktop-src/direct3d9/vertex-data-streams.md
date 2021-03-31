---
description: Las interfaces de representación de Direct3D se componen de métodos que representan primitivos de los datos de vértice almacenados en uno o más búferes de datos.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Flujos de datos de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd45fc3f645de49060cd201a6a6e9e238712338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805726"
---
# <a name="vertex-data-streams-direct3d-9"></a>Flujos de datos de vértices (Direct3D 9)

Las interfaces de representación de Direct3D se componen de métodos que representan primitivos de los datos de vértice almacenados en uno o más búferes de datos. Los datos de vértice se componen de elementos de vértice combinados para formar componentes de vértice. Los elementos de vértice, la unidad más pequeña de un vértice, representan entidades como posición, normal o color.

Los componentes de vértice son uno o más elementos de vértice almacenados de forma contigua (intercalados por vértice) en un búfer de memoria único. Un vértice completo consta de uno o varios componentes, donde cada componente está en un búfer de memoria independiente. Para representar un primitivo, se leen y ensamblan varios componentes de vértice para que los vértices completos estén disponibles para el procesamiento de vértices. En el diagrama siguiente se muestra el proceso de representación de primitivas mediante componentes de vértices.

![diagrama del proceso para representar primitivas mediante componentes de vértice](images/vertexdata.png)

La representación de primitivas consta de dos pasos. En primer lugar, configure uno o varios flujos de componentes de vértices; en segundo lugar, invoque un método [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para representarlo desde esos flujos. La identificación de los elementos de vértice dentro de estos flujos de componentes se especifica mediante el sombreador de vértices.

Los métodos [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) especifican un desplazamiento en los flujos de datos de vértices para que se pueda representar un subconjunto contiguo arbitrario de los primitivos dentro de un conjunto de datos de vértices con cada invocación de dibujo. Esto le permite cambiar el estado de representación del dispositivo entre grupos de primitivas que se representan a partir de los mismos búferes de vértices.

Se admiten los métodos de dibujo indexados y no indexados. Para obtener más información, vea [representar a partir de búferes de vértices y de índices (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de primitivas](rendering-primitives.md)
</dt> </dl>

 

 
