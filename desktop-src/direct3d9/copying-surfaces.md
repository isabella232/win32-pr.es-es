---
description: El término blit es una abreviatura de &0034;transferencia de bloques de \# bits,&0034; que es el proceso de transferencia de bloques de datos de un lugar en memoria a \# otro.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Copiar superficies (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d31d897bcb9e1a8fefa45a7770959ecb4121f807e4ca51d26ca7da5b5f5f5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123382"
---
# <a name="copying-surfaces-direct3d-9"></a>Copiar superficies (Direct3D 9)

El término blit es una abreviatura de "transferencia de bloques de bits", que es el proceso de transferir bloques de datos de un lugar en memoria a otro. La interfaz de controlador de dispositivos (DDI) de borrado se sigue usando en Direct3D 9 como mecanismo principal para mover rectángulos grandes de píxeles por fotograma, el mecanismo detrás del método [**IDirect3DDevice9::P resent**](/windows/desktop/api) orientado a copias. El transporte de ilustraciones en la operación blit se realiza mediante el [**método IDirect3DDevice9::UpdateTexture.**](/windows/desktop/api) Las ilustraciones también se pueden copiar en Direct3D 9 mediante el método [**IDirect3DDevice9::UpdateSurface,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) que copia un subconjunto rectangular de píxeles.

> [!Note]  
> Direct3D 9 proporciona funciones D3DX que permiten cargar ilustraciones de archivos, aplicar conversión de color y cambiar el tamaño de las ilustraciones. Para obtener más información sobre las funciones disponibles, vea [Funciones de textura en D3DX 9.](dx9-graphics-reference-d3dx-functions-texture.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

**IDirect3DDevice9::StretchRect**
</dt> </dl>

 

 
