---
description: En Direct3D 9, Direct3D permitirá al controlador devolver códigos de error como E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY y D3DERR UNSUPPORTEDCOLORARG para que una aplicación pueda responder \_ a ellos.
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: Errores internos del controlador (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b0ee8ba50edb3c14fbd9a22c9fa9dc93aab8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174794"
---
# <a name="driver-internal-errors-direct3d-9"></a>Errores internos del controlador (Direct3D 9)

En Direct3D 9, Direct3D permitirá al controlador devolver códigos de error como E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY y D3DERR UNSUPPORTEDCOLORARG para que una aplicación pueda responder \_ a ellos. Sin embargo, en [ocasiones,](accurately-profiling-direct3d-api-calls.md)las llamadas API que generaron estos tipos de valor devuelto se cargan en un búfer de comandos y se agrupan por lotes para enviarse a la GPU (consulte Control del tiempo de ejecución y las optimizaciones de controladores). En este caso, los errores no se pueden retransmitir a la aplicación cuando es necesario realizar la acción, por lo que el tiempo de ejecución consume el código de error y se toma una nota en el objeto de dispositivo de que esto ha ocurrido. Más adelante, cuando la aplicación invoca [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), **IDirect3DDevice9::P resent** devolverá D3DERR \_ DRIVERINTERNALERROR. Este es el motivo por el que el mejor enfoque para una aplicación al recibir un D3DERR \_ DRIVERINTERNALERROR de **IDirect3DDevice9::P resent** es destruir y volver a crear el dispositivo.

Si desea intentar depurar más, estas son algunas sugerencias para intentar averiguar qué llamada API está generando el error:

-   Dado que la lista de posibles valores devueltos no está completa, puede intentar averiguar qué llamada está fallando rodeando cada llamada API de la siguiente manera:

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    A continuación, el flujo de depuración de salida debe mostrar la llamada que está causando el problema.

-   Además, para fines de depuración, intente llamar a [**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) inmediatamente antes de cada [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para ver si hay un problema adicional con el controlador de dispositivo (operación no admitida, combinación inutilizable de formatos de textura, etc.).

    > [!Note]  
    > [**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) debe usarse con cuidado y moderación debido a la cantidad de trabajo de validación que debe realizar el controlador para devolver una respuesta.

     

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programación Sugerencias](programming-tips.md)
</dt> </dl>

 

 
