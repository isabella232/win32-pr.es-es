---
description: El término blit es una abreviatura para &\# 0034; transferencia de bloque de bits, &\# 0034; que es el proceso de transferir bloques de datos de un lugar de memoria a otro.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Copiar superficies (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50000e3b620c4d2fd217695551d898e5892430ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696120"
---
# <a name="copying-surfaces-direct3d-9"></a>Copiar superficies (Direct3D 9)

El término blit es una abreviatura de "transferencia de bloque de bits", que es el proceso de transferir bloques de datos de un lugar de memoria a otro. La interfaz de controlador de dispositivo (DDI) de blitting se sigue usando en Direct3D 9 como el mecanismo principal para mover grandes rectángulos de píxeles en cada fotograma, el mecanismo detrás del IDirect3DDevice9 orientado a copia [**::P método reenviado**](/windows/desktop/api) . El transporte de material gráfico en la operación de blit lo realiza el método [**IDirect3DDevice9:: UpdateTexture**](/windows/desktop/api) . También se puede copiar material gráfico en Direct3D 9 mediante el método [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) , que copia un subconjunto rectangular de píxeles.

> [!Note]  
> Direct3D 9 proporciona funciones de D3DX que permiten cargar ilustraciones desde archivos, aplicar la conversión de colores y cambiar el tamaño de la ilustración. Para obtener más información sobre las funciones disponibles, consulte [funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

**IDirect3DDevice9::StretchRect**
</dt> </dl>

 

 
