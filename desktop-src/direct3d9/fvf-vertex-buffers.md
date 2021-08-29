---
description: Establecer el parámetro FVF del método IDirect3DDevice9::CreateVertexBuffer en un valor distinto de cero, que debe ser un código FVF válido, indica que el contenido del búfer se caracterizará por un código FVF.
ms.assetid: 7cab559f-3e9d-46bd-b00f-439e0922aeeb
title: Búferes de vértices FVF (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c99267945970e48c9447ad592433b304bd43d33ec05a8ebcef3287d2f3e68fd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564235"
---
# <a name="fvf-vertex-buffers-direct3d-9"></a>Búferes de vértices FVF (Direct3D 9)

Establecer el parámetro FVF del método [**IDirect3DDevice9::CreateVertexBuffer**](/windows/desktop/api) en un valor distinto de cero, que debe ser un código FVF válido, indica que el contenido del búfer se caracterizará por un código FVF. Un búfer de vértices que se crea con un código FVF se conoce como búfer de vértice FVF. Algunos métodos o usos de [**IDirect3DDevice9**](/windows/desktop/api) requieren búferes de vértice FVF y otros requieren búferes de vértices que no son FVF. Los búferes de vértices FVF son necesarios como argumento de búfer de vértice de destino para [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices).

Los búferes de vértices FVF se pueden enlazar a un flujo de datos de origen para cualquier número de flujo.

La presencia del componente D3DFVF XYZRHW en los búferes de vértices FVF indica que se han procesado los vértices de \_ ese búfer. Los búferes de vértices usados para [**IDirect3DDevice9::P vertices búferes**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) de vértices de destino deben procesarse posteriormente. Los búferes de vértices usados para las entradas del sombreador de funciones fijas se pueden preprocesar o postprocesar. Si el búfer de vértices se procesa posteriormente, el sombreador se omite eficazmente y los datos se pasan directamente al módulo primitivo de recorte y configuración.

Los búferes de vértices FVF se pueden usar con sombreadores de vértices. Además, los flujos de vértices pueden representar los mismos formatos de vértice que los búferes de vértice que no son FVF. No tienen que usarse para introducir datos de búferes de vértices independientes. La flexibilidad adicional de los nuevos flujos de vértices permite que las aplicaciones que necesitan mantener los datos separados funcionen mejor, pero no es necesario. Si la aplicación puede mantener los datos intercalados de antemano, eso es un aumento del rendimiento. Si la aplicación solo intercalará los datos antes de cada llamada de representación, debe permitir que la API o el hardware lo hagan con varias secuencias.

Lo más importante con el rendimiento de los vértices es usar un vértice de 32 bytes y mantener un orden de caché bueno.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de vértices](vertex-buffers.md)
</dt> </dl>

 

 
