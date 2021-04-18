---
description: Direct3D 9 admite texturas con paletas a través de un conjunto de 256 paletas de entradas asociadas al objeto IDirect3DDevice9.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Paletas de texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a0fbb1c5d6766b879b898145ec2385a41d94b8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705205"
---
# <a name="texture-palettes-direct3d-9"></a>Paletas de texturas (Direct3D 9)

Direct3D 9 admite texturas con paletas a través de un conjunto de 256 paletas de entradas asociadas al objeto [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) . Una paleta se convierte en actual llamando al método [**IDirect3DDevice9:: SetCurrentTexturePalette**](/windows/desktop/api) . La paleta actual se usa para traducir todas las texturas de paleta para todas las fases de textura activas. [**IDirect3DDevice9:: SetPaletteEntries**](/windows/desktop/api) actualiza todas las entradas 256 de la paleta. Cada entrada es una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) con el formato D3DFMT \_ A8R8G8B8. De forma predeterminada, todas las entradas son 0xFFFFFFFF.

Las paletas [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) contienen un canal alfa. Este canal alfa se puede usar cuando \_ se establece la marca de capacidad del dispositivo D3DPTEXTURECAPS ALPHAPALETTE, lo que indica que el dispositivo admite Alpha de la paleta. El canal alfa de la paleta se utiliza cuando el formato de la textura no tiene un canal alfa. Si el dispositivo no admite alfa de la paleta y el formato de textura no tiene un canal alfa, se usa un valor de 0xFF para alpha.

Hay un máximo de 65.536 (0x0000FFFF). Dado que los recursos de memoria asociados al conjunto de paletas son proporcionales al número de paleta máximo al que hace referencia una aplicación, use números de paleta contiguos a partir de cero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de la texturización](basic-texturing-concepts.md)
</dt> </dl>

 

 
