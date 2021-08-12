---
description: Direct3D 9 admite texturas de paleta a través de un conjunto de 256 paletas de entrada asociadas al objeto IDirect3DDevice9.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Paletas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d755abb638ab1dd94e25edd98b2daef5e65d5a54cca7baf21a74e7d06173eed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291170"
---
# <a name="texture-palettes-direct3d-9"></a>Paletas de textura (Direct3D 9)

Direct3D 9 admite texturas de paleta a través de un conjunto de 256 paletas de entrada asociadas al objeto [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) Una paleta se hace actual mediante una llamada [**al método IDirect3DDevice9::SetCurrentTexturePalette.**](/windows/desktop/api) La paleta actual se usa para traducir todas las texturas de paleta para todas las fases de textura activas. [**IDirect3DDevice9::SetPaletteEntries**](/windows/desktop/api) actualiza todas las 256 entradas de una paleta. Cada entrada es una [**estructura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) con el formato D3DFMT \_ A8R8G8B8. Todas las entradas tienen como valor predeterminado 0xFFFFFFFF.

Las [**paletas IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) contienen un canal alfa. Este canal alfa se puede usar cuando se establece la marca de funcionalidad del dispositivo D3DPTEXTURECAPS ALPHAPALETTE, lo que indica que el dispositivo admite alfa desde \_ la paleta. El canal alfa de la paleta se usa cuando el formato de textura no tiene un canal alfa. Si el dispositivo no admite alfa desde la paleta y el formato de textura no tiene un canal alfa, se usa un valor de 0xFF para alfa.

Hay un máximo de 65 536 paletas (0x0000FFFF). Dado que los recursos de memoria asociados al conjunto de paletas son proporcionales al número máximo de paletas a los que hace referencia una aplicación, use números de paleta contiguos a partir de cero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de texturing](basic-texturing-concepts.md)
</dt> </dl>

 

 
