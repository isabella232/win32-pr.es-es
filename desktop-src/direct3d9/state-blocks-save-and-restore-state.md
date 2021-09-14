---
description: Un bloque de estado es un grupo de estados de dispositivo.
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: Estado de guardado y restauración de bloques de estado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104010f2ea057870b70e9887e5b325f1de68c463
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160430"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a>Estado de guardado y restauración de bloques de estado (Direct3D 9)

Un bloque de estado es un grupo de estados de dispositivo. El estado del dispositivo se forma de estado de representación, estado de vértice, estado de píxel o todo lo anterior. Un bloque de estado contiene una instantánea del estado actual de un dispositivo o puede crear un bloque de estado que registra cada cambio de estado que realiza la aplicación.

## <a name="capture-a-block-of-state"></a>Capturar un bloque de estado

Elija el tipo de estado que desea capturar y cree un bloque de estado como este:


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



[**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock) crea un bloque de estado y captura automáticamente el estado del dispositivo. El estado del dispositivo se especifica mediante el tipo de bloque de estado en el primer argumento. Este estado puede ser uno de los siguientes: todo el estado del dispositivo (consulte Guardar todos los estados del dispositivo con un [StateBlock (Direct3D 9),](saving-all-device-states-with-a-stateblock.md)todo el estado de píxel (vea Guardar el estado de píxel con un [StateBlock (Direct3D 9) )](saving-pixel-states-with-a-stateblock.md)o todo el estado de vértice (vea Guardar estados de vértice con un [StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).

El sistema de efectos usa un bloque de estado para guardar el estado. Después [**de llamar a ID3DXEffect::Begin,**](id3dxeffect--begin.md) se crea un bloque de estado y se captura el estado. Cuando [**se llama a ID3DXEffect::End,**](id3dxeffect--end.md) el estado del bloque de estado se vuelve a aplicar al dispositivo.

## <a name="capture-individual-states"></a>Capturar estados individuales

Para guardar una secuencia de estado personalizada, ajuste el estado que desea guardar en un par [**IDirect3DDevice9::BeginStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-beginstateblock) e [**IDirect3DDevice9::EndStateBlock.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) BeginStateBlock indica al dispositivo actual que configure un bloque de estado y que le agregue todos los cambios de estado que se produzcan hasta que se llame a EndStateBlock. Este es un ejemplo:


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



Esto guardará cualquier número de cambios de estado de cualquier secuencia en un bloque de estado personalizado. Más adelante, cuando quiera usar el bloque de estado para restablecer el estado del dispositivo, llame a [**IDirect3DStateBlock9::Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply). Esto sobrescribirá solo el estado del dispositivo que se ha capturado en el bloque de estado. No se cambiará ningún otro estado de dispositivo que no se haya capturado con el bloque de estado personalizado. Una vez más, como el objeto stateblock es una interfaz, deberá liberarlo cuando haya terminado con él.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estados (Direct3D 9)](states.md)
</dt> </dl>

 

 
