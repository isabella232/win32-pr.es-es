---
description: 'Al establecer el parámetro FVF del método IDirect3DDevice9:: CreateVertexBuffer en un valor distinto de cero, que debe ser un código FVF válido, indica que el contenido del búfer se caracteriza por un código FVF.'
ms.assetid: 7cab559f-3e9d-46bd-b00f-439e0922aeeb
title: Búferes de vértices de FVF (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a86201c3ddc1cab6d492539caccc61c1430b3a2c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714675"
---
# <a name="fvf-vertex-buffers-direct3d-9"></a>Búferes de vértices de FVF (Direct3D 9)

Al establecer el parámetro FVF del método [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/desktop/api) en un valor distinto de cero, que debe ser un código FVF válido, indica que el contenido del búfer se caracteriza por un código FVF. Un búfer de vértices que se crea con un código FVF se denomina búfer de vértices FVF. Algunos métodos o usos de [**IDirect3DDevice9**](/windows/desktop/api) requieren búferes de vértices de FVF y otros requieren búferes de vértices que no sean de FVF. Los búferes de vértices FVF son necesarios como el argumento de búfer de vértice de destino para [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices).

Los búferes de vértices de FVF se pueden enlazar a un flujo de datos de origen para cualquier número de flujo.

La presencia del \_ componente XYZRHW de D3DFVF en búferes de vértices de FVF indica que se han procesado los vértices de ese búfer. Búferes de vértices usados para [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) los búferes de vértice de destino deben procesarse después. Los búferes de vértices usados para las entradas de sombreador de funciones fijas pueden ser preprocesados o postprocesamiento. Si el búfer de vértices se procesa después, el sombreador se omite realmente y los datos se pasan directamente al módulo de configuración y recorte primitivo.

Los búferes de vértices de FVF se pueden usar con sombreadores de vértices. Además, los flujos de vértices pueden representar los mismos formatos de vértices que los búferes de vértices que no son FVF. No tienen que usarse para introducir datos de búferes de vértices independientes. La flexibilidad adicional de los nuevos flujos de vértices permite a las aplicaciones que necesitan mantener sus datos separados para trabajar mejor, pero no es necesario. Si la aplicación puede mantener los datos intercalados por adelantado, eso es un aumento del rendimiento. Si la aplicación va a intercalar los datos solo antes de cada llamada de representación, debe habilitar la API o el hardware para hacer esto con varias secuencias.

Las cosas más importantes con el rendimiento del vértice es usar un vértice de 32 bytes y mantener una buena ordenación de la memoria caché.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de vértices](vertex-buffers.md)
</dt> </dl>

 

 
