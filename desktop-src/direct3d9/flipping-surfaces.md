---
description: Normalmente, una aplicación direct3D muestra una secuencia animada generando los fotogramas de la animación en búferes de reserva y presentándolos en secuencia.
ms.assetid: 4ca9a845-f433-4d4a-939e-4b9ab2983927
title: Volteo de superficies (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dafd263de0f907b33ff6f20ffcbb2cce69943da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465385"
---
# <a name="flipping-surfaces-direct3d-9"></a>Volteo de superficies (Direct3D 9)

Normalmente, una aplicación direct3D muestra una secuencia animada generando los fotogramas de la animación en búferes de reserva y presentándolos en secuencia. Los búferes de reserva se organizan en cadenas de intercambio. Una cadena de intercambio es una serie de búferes que se "voltea" a la pantalla una tras otra. Se puede usar para representar una escena en memoria y, a continuación, voltear la escena a la pantalla cuando se complete la representación. Esto evita el fenómeno conocido como desgarro y permite una animación más suave.

Cada dispositivo creado en Direct3D tiene al menos una cadena de intercambio. Al inicializar el primer dispositivo Direct3D, establece el miembro BackBufferCount de [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md), que indica a Direct3D el número de búferes de reserva que estarán en la cadena de intercambio. La llamada a [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) crea el dispositivo Direct3D y la cadena de intercambio correspondiente.

Cuando se [**usa IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para solicitar una operación de volteo de superficie, se intercambian los punteros a la memoria de superficie para el búfer frontal y los búferes de reserva. La volteo se realiza mediante el cambio de punteros que el dispositivo de visualización usa para hacer referencia a la memoria, no mediante la copia de la memoria de la superficie. Cuando una cadena de volteo contiene un búfer frontal y más de un búfer de reserva, los punteros se cambian en un patrón circular, como se muestra en el diagrama siguiente.

![diagrama de una cadena de volteo con un búfer frontal y dos búferes de reserva](images/trplflip.png)

Puede crear cadenas de intercambio de suma para un dispositivo llamando a [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/desktop/api). Una aplicación puede crear una cadena de intercambio por vista y asociar cada cadena de intercambio a una ventana determinada. La aplicación representa imágenes en los búferes de reserva de cada cadena de intercambio y, a continuación, las presenta individualmente. Los dos parámetros que **toma IDirect3DDevice9::CreateAdditionalSwapChain** son un puntero a una estructura [**PARAMETERS D3DPRESENT \_**](d3dpresent-parameters.md) y la dirección de un puntero a una interfaz [**IDirect3DSwapChain9.**](/windows/desktop/api) A continuación, puede usar [**IDirect3DSwapChain9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) para mostrar el contenido del siguiente búfer de reserva en el búfer front-buffer. Tenga en cuenta que un dispositivo solo puede tener una cadena de intercambio de pantalla completa.

Puede obtener acceso a un búfer de reserva específico llamando a los métodos [**IDirect3DDevice9::GetBackBuffer**](/windows/desktop/api) o [**IDirect3DSwapChain9::GetBackBuffer,**](/windows/desktop/api) que devuelven un puntero a una interfaz [**IDirect3DSurface9**](/windows/desktop/api) que representa la superficie de búfer de reserva devuelta. Tenga en cuenta que llamar a este método aumenta el recuento de referencias internas en la interfaz [**IDirect3DDevice9,**](/windows/desktop/api) por lo que debe asegurarse de llamar a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) cuando haya terminado de usar esta superficie o tenga una pérdida de memoria.

Recuerde que Direct3D invierte superficies intercambiando punteros de memoria de superficie dentro de la cadena de intercambio, no intercambiando las superficies por sí mismas. Esto significa que siempre se representará en el búfer de reserva que se mostrará a continuación.

Es importante tener en cuenta la distinción entre una "operación de volteo", tal como realiza un controlador de adaptador de pantalla, y una operación "Present" aplicada a una cadena de intercambio creada con D3DSWAPEFFECT \_ FLIP.

El término "volteo" denota convencionalmente una operación que modifica el intervalo de direcciones de memoria de vídeo que usa un adaptador de pantalla para generar su señal de salida, lo que hace que se muestre el contenido de un búfer de reserva previamente oculto. En Direct3D 9, el término se suele usar con más frecuencia para describir la presentación de un búfer de reserva en cualquier cadena de intercambio creada con el efecto de intercambio FLIP D3DSWAPEFFECT. \_

Aunque estas operaciones "presentes" se implementan casi invariablemente mediante operaciones de volteo cuando la cadena de intercambio es una de pantalla completa, las operaciones de copia las implementan necesariamente cuando se abren ventanas en la cadena de intercambio. Además, un controlador de adaptador de pantalla puede usar volteo para implementar operaciones Present en cadenas de intercambio de pantalla completa basadas en D3DSWAPEFFECT DISCARD y \_ D3DSWAPEFFECT \_ COPY.

La explicación anterior se aplica al caso más usado de una cadena de intercambio de pantalla completa creada con D3DSWAPEFFECT \_ FLIP.

Para obtener una explicación más general de los distintos efectos de intercambio para las cadenas de intercambio de ventana y de pantalla completa, vea [**D3DSWAPEFFECT**](./d3dswapeffect.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
