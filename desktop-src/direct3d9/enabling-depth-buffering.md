---
description: 'Después de crear un búfer de profundidad, como se describe en crear un búfer de profundidad (Direct3D 9), puede habilitar el almacenamiento en búfer de profundidad llamando al método IDirect3DDevice9:: SetRenderState.'
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: Habilitar el almacenamiento en búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935d4f2e1db164a3aac2a39627be88d71887cc14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359884"
---
# <a name="enabling-depth-buffering-direct3d-9"></a>Habilitar el almacenamiento en búfer de profundidad (Direct3D 9)

Después de crear un búfer de profundidad, como se describe en [crear un búfer de profundidad (Direct3D 9)](creating-a-depth-buffer.md), puede habilitar el almacenamiento en búfer de profundidad llamando al método [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) . Establezca el estado de representación de ZENABLE de D3DRS \_ para habilitar el almacenamiento en búfer de profundidad. Use el \_ miembro true D3DZB del tipo enumerado [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) (o **true**) para habilitar el almacenamiento en búfer z, D3DZB \_ USEW para habilitar el almacenamiento en búfer de w o D3DZB \_ false (o **false**) para deshabilitar el almacenamiento en búfer de profundidad.

> [!Note]  
> Para usar el almacenamiento en búfer de w, la aplicación debe establecer una matriz de proyección compatible incluso si no usa la canalización de transformación de Direct3D. Para obtener información sobre cómo proporcionar una matriz de proyección adecuada, vea [una matriz de proyección fácil](projection-transform.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de profundidad](depth-buffers.md)
</dt> </dl>

 

 
