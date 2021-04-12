---
description: En Direct3D 9, Direct3D permitirá que el controlador devuelva códigos de error como E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY y D3DERR UNSUPPORTEDCOLORARG, de \_ modo que una aplicación pueda responder a ellos.
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: Errores internos del controlador (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b0ee8ba50edb3c14fbd9a22c9fa9dc93aab8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152416"
---
# <a name="driver-internal-errors-direct3d-9"></a>Errores internos del controlador (Direct3D 9)

En Direct3D 9, Direct3D permitirá que el controlador devuelva códigos de error como E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY y D3DERR UNSUPPORTEDCOLORARG, de \_ modo que una aplicación pueda responder a ellos. Sin embargo, a veces, las llamadas a la API que generaron estos tipos de valor devueltos se cargan en un búfer de comandos y se envían por lotes para enviarlos a la GPU (consulte [control del tiempo de ejecución y optimización](accurately-profiling-direct3d-api-calls.md)de los controladores). En este caso, los errores no se pueden retransmitir a la aplicación cuando es necesario realizar una acción, por lo que el tiempo de ejecución consume el código de error y se realiza una nota en el objeto de dispositivo que se ha producido. Más adelante, cuando la aplicación invoque [**IDirect3DDevice9::P reenviar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), **IDirect3DDevice9::P reenviar** devolverá D3DERR \_ DRIVERINTERNALERROR. Este es el motivo por el que la mejor opción para que una aplicación lleve a cabo al recibir un \_ DRIVERINTERNALERROR de D3DERR de **IDirect3DDevice9::P reenviados** es destruir y volver a crear el dispositivo.

Si desea intentar depurar más, aquí hay un par de sugerencias para intentar averiguar qué llamada API está generando el error:

-   Dado que la lista de valores devueltos posibles no está completa, puede intentar averiguar en qué llamada se produce un error incluyendo cada llamada de API de la siguiente manera:

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    A continuación, el flujo de depuración de salida debería mostrar la llamada que está causando el problema.

-   Además, para fines de depuración, intente llamar a [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) inmediatamente antes de cada [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para ver si hay un problema adicional con el controlador de dispositivo (operación no compatible, combinación inutilizable de formatos de textura, etc.).

    > [!Note]  
    > [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) debe usarse con cuidado y con moderación debido a la cantidad de trabajo de validación que el controlador debe realizar para devolver una respuesta.

     

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sugerencias de programación](programming-tips.md)
</dt> </dl>

 

 
