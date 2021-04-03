---
description: Un bloque de estado es un grupo de Estados de dispositivo.
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: Estado de guardado y restauración de bloques de estado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8f19d6409e0dc9c40f1d4c7711440a0dc09fe2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997634"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a>Estado de guardado y restauración de bloques de estado (Direct3D 9)

Un bloque de estado es un grupo de Estados de dispositivo. El estado del dispositivo se compone del estado de representación, el estado del vértice, el estado del píxel o todo lo anterior. Un bloque de estado contiene una instantánea del estado actual de un dispositivo o puede crear un bloque de estado que registre cada cambio de estado que realiza la aplicación.

## <a name="capture-a-block-of-state"></a>Captura de un bloque de estado

Elija el tipo de estado que desea capturar y cree un bloque de estado similar al siguiente:


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



[**IDirect3DDevice9:: CreateStateBlock**](/windows/desktop/api) crea un bloque de estado y captura automáticamente el estado del dispositivo. El estado del dispositivo se especifica mediante el tipo de bloque de estado en el primer argumento. Este estado puede ser uno de los siguientes: todo el estado del dispositivo (vea [guardar todos los Estados de los dispositivos con un StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), todo el estado de los píxeles (vea [guardar el estado de los píxeles con un StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)) o todo el estado del vértice (vea [guardar los Estados de los vértices con un StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).

El sistema de efectos usa un bloque de estado para guardar el estado. Después de llamar a [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) , se crea un bloque de estado y se captura el estado. Cuando se llama a [**ID3DXEffect:: end**](id3dxeffect--end.md) , el estado del bloque de estado se vuelve a aplicar al dispositivo.

## <a name="capture-individual-states"></a>Capturar Estados individuales

Para guardar una secuencia de estado personalizada, ajuste el estado que desea guardar en un par [**IDirect3DDevice9:: BeginStateBlock**](/windows/desktop/api) y [**IDirect3DDevice9:: EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) . BeginStateBlock indica al dispositivo actual que configure un bloque de estado y le agregue todos los cambios de estado que se producen hasta que se llama a EndStateBlock. Este es un ejemplo:


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



Esto guardará cualquier número de cambios de estado en cualquier secuencia en un stateblock personalizado. Más adelante, cuando quiera usar stateblock para restablecer el estado del dispositivo, llame a [**IDirect3DStateBlock9:: Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply). Esto sobrescribirá solo el estado del dispositivo capturado en el bloque de estado. No se cambiará ningún otro estado de dispositivo que no se haya capturado con el stateblock personalizado. Una vez más, como el objeto stateblock es una interfaz, tendrá que liberarlo cuando haya terminado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estados (Direct3D 9)](states.md)
</dt> </dl>

 

 
