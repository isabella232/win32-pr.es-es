---
description: Una fase de combinación es un conjunto de operaciones de textura y sus argumentos que definen cómo se combinan las texturas.
ms.assetid: 7f9e3041-a270-44a9-a8e1-bca5ea25a71e
title: Crear fases de fusión (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f5029d540433b22b1380435dd8092546917338
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153128"
---
# <a name="creating-blending-stages-direct3d-9"></a>Crear fases de fusión (Direct3D 9)

Una fase de combinación es un conjunto de operaciones de textura y sus argumentos que definen cómo se combinan las texturas. Al realizar una fase de combinación, las aplicaciones de C++ invocan el método [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) . La primera llamada especifica la operación que se realiza. Dos llamadas adicionales definen los argumentos a los que se aplica la operación. En el ejemplo de código siguiente se muestra la creación de una fase de fusión.


```
// This example assumes that lpD3DDev is a valid pointer to an
// IDirect3DDevice9 interface.

// Set the operation for the first texture.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_ADD);

// Set argument 1 to the texture color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);

// Set argument 2 to the iterated diffuse color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
```



Los datos de textura en las texturas contienen valores de color y alfa. Las aplicaciones pueden definir operaciones independientes para los valores de color y alfa en una sola fase de mezcla. Cada operación, color y alfa tienen sus propios argumentos. Para obtener más información, consulte [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).

Aunque no forme parte de la API de Direct3D, puede insertar las siguientes macros en la aplicación para abreviar el código necesario para crear fases de fusión de texturas.


```
#define SetTextureColorStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_COLOROP, op);      \
    dev->SetTextureStageState( i, D3DTSS_COLORARG1, arg1 ); \
    dev->SetTextureStageState( i, D3DTSS_COLORARG2, arg2 );

#define SetTextureAlphaStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_ALPHAOP, op);      \
    dev->SetTextureStageState( i, D3DTSS_ALPHAARG1, arg1 );  \
    dev->SetTextureStageState( i  D3DTSS_ALPHAARG2, arg2 );
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación de texturas](texture-blending.md)
</dt> </dl>

 

 
