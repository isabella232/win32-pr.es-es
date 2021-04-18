---
description: Las aplicaciones de C++ pueden usar las pruebas alfa para controlar el momento en que se escriben los píxeles en la superficie de representación-destino.
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: Estado de la prueba alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020322ee31bc08352dbb2796ea5e7141d03c77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714863"
---
# <a name="alpha-testing-state-direct3d-9"></a>Estado de la prueba alfa (Direct3D 9)

Las aplicaciones de C++ pueden usar las pruebas alfa para controlar el momento en que se escriben los píxeles en la superficie de representación-destino. Mediante el estado de representación de [**D3DRS \_ ALPHATESTENABLE**](./d3drenderstatetype.md) , la aplicación establece el dispositivo Direct3D actual para que pruebe cada píxel según una función de prueba alfa. Si la prueba se realiza correctamente, el píxel se escribe en la superficie. Si no es así, Direct3D omite el píxel. Seleccione la función de prueba alfa con el estado de representación de **D3DRS \_ ALPHAFUNC** . La aplicación puede establecer un valor alfa de referencia para todos los píxeles que se van a comparar mediante el estado de representación de **\_ ALPHAREF de D3DRS** .

El uso más común de las pruebas alfa es mejorar el rendimiento al rasterizar objetos que son casi transparentes. Si los datos de color que se están rasterizando son más opacos que el color de un píxel determinado (D3DPCMPCAPS \_ mayor criticalthreshold), se escribe el píxel. De lo contrario, el rasterizador omite el píxel por completo, lo que ahorra el procesamiento necesario para combinar los dos colores. En el ejemplo de código siguiente se comprueba si se admite una función de comparación determinada y, si es así, se establecen los parámetros de función de comparación necesarios para mejorar el rendimiento durante la representación.


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



No todo el hardware es compatible con todas las características de pruebas alfa. Puede comprobar las funcionalidades del dispositivo llamando al método [**IDirect3D9:: GetDeviceCaps**](/windows/desktop/api) . Después de recuperar las funcionalidades del dispositivo, compruebe el miembro AlphaCmpCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) asociada para la función de comparación deseada. Si el miembro AlphaCmpCaps contiene solo la capacidad de D3DPCMPCAPS \_ siempre o solo la \_ capacidad de D3DPCMPCAPS nunca, el controlador no admite pruebas alfa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estados de representación](render-states.md)
</dt> </dl>

 

 
