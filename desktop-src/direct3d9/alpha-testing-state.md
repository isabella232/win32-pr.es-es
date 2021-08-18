---
description: Las aplicaciones de C++ pueden usar pruebas alfa para controlar cuándo se escriben píxeles en la superficie de destino de representación.
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: Estado de prueba alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b853eb779860d5fc490f4061fde03c852a9c3d9f7bda48baa8e5a84ebd43173c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989445"
---
# <a name="alpha-testing-state-direct3d-9"></a>Estado de prueba alfa (Direct3D 9)

Las aplicaciones de C++ pueden usar pruebas alfa para controlar cuándo se escriben píxeles en la superficie de destino de representación. Mediante el uso del estado de representación [**\_ ALPHATESTENABLE de D3DRS,**](./d3drenderstatetype.md) la aplicación establece el dispositivo Direct3D actual para que pruebe cada píxel según una función de prueba alfa. Si la prueba se realiza correctamente, el píxel se escribe en la superficie. Si no es así, Direct3D omite el píxel. Seleccione la función de prueba alfa con el estado de representación **D3DRS \_ ALPHAFUNC.** La aplicación puede establecer un valor alfa de referencia para todos los píxeles con los que comparar mediante el estado de representación **D3DRS \_ ALPHAREF.**

El uso más común para las pruebas alfa es mejorar el rendimiento al rasterizar objetos que son casi transparentes. Si los datos de color que se rasterizan son más opacos que el color de un píxel determinado (D3DPCMPCAPS GREATEREQUAL), se escribe \_ el píxel. De lo contrario, el rasterizador omite el píxel por completo, guardando el procesamiento necesario para combinar los dos colores. En el ejemplo de código siguiente se comprueba si se admite una función de comparación determinada y, si es así, se establecen los parámetros de función de comparación necesarios para mejorar el rendimiento durante la representación.


```
// This code example assumes that pCaps is a
// D3DCAPS9 structure that was filled with a 
// previous call to IDirect3D9::GetDeviceCaps.

if (pCaps.AlphaCmpCaps & D3DPCMPCAPS_GREATEREQUAL)
{
    dev->SetRenderState(D3DRS_ALPHAREF, (DWORD)0x00000001);
    dev->SetRenderState(D3DRS_ALPHATESTENABLE, TRUE); 
    dev->SetRenderState(D3DRS_ALPHAFUNC, D3DCMP_GREATEREQUAL);
}

// If the comparison is not supported, render anyway. 
// The only drawback is no performance gain.
```



No todo el hardware admite todas las características de pruebas alfa. Puede comprobar las funcionalidades del dispositivo llamando al [**método IDirect3D9::GetDeviceCaps.**](/windows/desktop/api) Después de recuperar las funcionalidades del dispositivo, compruebe el miembro AlphaCmpCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) asociada para la función de comparación deseada. Si el miembro AlphaCmpCaps solo contiene la funcionalidad D3DPCMPCAPS ALWAYS o solo la funcionalidad \_ D3DPCMPCAPS NEVER, el controlador no admite pruebas \_ alfa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar estados](render-states.md)
</dt> </dl>

 

 
