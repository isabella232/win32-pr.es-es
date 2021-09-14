---
description: Después de crear un búfer de profundidad, como se describe en Creación de un búfer de profundidad (Direct3D 9), se habilita el almacenamiento en búfer de profundidad mediante una llamada al método IDirect3DDevice9::SetRenderState.
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: Habilitar el almacenamiento en búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935d4f2e1db164a3aac2a39627be88d71887cc14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964955"
---
# <a name="enabling-depth-buffering-direct3d-9"></a>Habilitar el almacenamiento en búfer de profundidad (Direct3D 9)

Después de crear un búfer de profundidad, como se describe en Creación de un búfer de profundidad [(Direct3D 9),](creating-a-depth-buffer.md)se habilita el almacenamiento en búfer de profundidad mediante una llamada al método [**IDirect3DDevice9::SetRenderState.**](/windows/desktop/api) Establezca el estado de representación ZENABLE de D3DRS \_ para habilitar el almacenamiento en búfer de profundidad. Use el miembro TRUE D3DBUFFER del tipo enumerado \_ [**D3BUFFERTYPE**](./d3dzbuffertype.md) (o **TRUE)** para habilitar el almacenamiento en búfer z, D3DOPEN USEW para habilitar el almacenamiento en búfer \_ w o D3DOPEN \_ FALSE (o **FALSE)** para deshabilitar el almacenamiento en búfer de profundidad.

> [!Note]  
> Para usar w-buffering, la aplicación debe establecer una matriz de proyección compatible incluso si no usa la canalización de transformación de Direct3D. Para obtener información sobre cómo proporcionar una matriz de proyección adecuada, vea [A W-Friendly Projection Matrix](projection-transform.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de profundidad](depth-buffers.md)
</dt> </dl>

 

 
