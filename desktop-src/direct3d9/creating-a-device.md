---
description: Para crear un dispositivo Direct3D, primero debe crear un objeto de Direct3D (vea Direct3DCreate9).
ms.assetid: 06810f31-fa6c-416e-bd7b-65cfb3e6d7f2
title: Crear un dispositivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9c033ed25262f0a3bcdee9db73509ddf5cb53b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714783"
---
# <a name="creating-a-device-direct3d-9"></a>Crear un dispositivo (Direct3D 9)

Para crear un dispositivo Direct3D, primero debe crear un objeto de Direct3D (vea [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)). Todos los dispositivos de representación creados por un objeto de Direct3D comparten los mismos recursos físicos. Si crea varios dispositivos de representación a partir de un único objeto de Direct3D, se aplicarán penalizaciones extremas al rendimiento porque comparten el mismo hardware.

En primer lugar, inicialice los valores de la estructura de [**\_ parámetros D3DPRESENT**](d3dpresent-parameters.md) que se usa para crear el dispositivo Direct3D. En el ejemplo de código siguiente se especifica una aplicación de ventana en la que el búfer de reserva se copia en el búfer frontal durante una operación de sincronización vertical.


```
LPDIRECT3DDEVICE9 pDevice = NULL;

D3DPRESENT_PARAMETERS d3dpp; 

ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed   = TRUE;
d3dpp.SwapEffect = D3DSWAPEFFECT_COPY;
```



A continuación, cree el dispositivo Direct3D. La siguiente llamada a [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) especifica el adaptador predeterminado, un dispositivo de capa de abstracción de hardware (HAL) y el procesamiento de vértices de software.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                    &d3dpp, &d3dDevice ) ) )
    return E_FAIL;
```



Tenga en cuenta que una llamada para crear, liberar o restablecer el dispositivo solo debe ocurrir en el mismo subproceso que el procedimiento de ventana de la ventana de enfoque.

Después de crear el dispositivo, establezca su estado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
