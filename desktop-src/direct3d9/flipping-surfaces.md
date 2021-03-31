---
description: Normalmente, una aplicación de Direct3D muestra una secuencia animada generando los fotogramas de la animación en búferes de reserva y mostrándolos en secuencia.
ms.assetid: 4ca9a845-f433-4d4a-939e-4b9ab2983927
title: Voltear superficies (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dafd263de0f907b33ff6f20ffcbb2cce69943da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806301"
---
# <a name="flipping-surfaces-direct3d-9"></a>Voltear superficies (Direct3D 9)

Normalmente, una aplicación de Direct3D muestra una secuencia animada generando los fotogramas de la animación en búferes de reserva y mostrándolos en secuencia. Los búferes de reserva se organizan en cadenas de intercambio. Una cadena de intercambio es una serie de búferes que "voltean" a la pantalla una tras otra. Se puede usar para representar una escena en la memoria y, a continuación, voltear la escena a la pantalla cuando se complete la representación. Esto evita el fenómeno conocido como desgarro y permite una animación más fluida.

Cada dispositivo creado en Direct3D tiene al menos una cadena de intercambio. Cuando se inicializa el primer dispositivo Direct3D, se establece el miembro BackBufferCount de [**los \_ parámetros D3DPRESENT**](d3dpresent-parameters.md), que indica a Direct3D el número de búferes de reserva que estarán en la cadena de intercambio. La llamada a [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) crea el dispositivo Direct3D y la cadena de intercambio correspondiente.

Cuando se usa [**IDirect3DDevice9::P reenviar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para solicitar una operación de volteo de la superficie, se intercambian los punteros a la memoria de superficie para el búfer frontal y los búferes de reserva. El volteo se realiza cambiando los punteros que el dispositivo de pantalla utiliza para hacer referencia a la memoria, no mediante la copia de la memoria de la superficie. Cuando una cadena de volteo contiene un búfer frontal y más de un búfer de reserva, los punteros se cambian en un patrón circular, tal como se muestra en el diagrama siguiente.

![diagrama de una cadena de volteo con un búfer frontal y dos búferes de reserva](images/trplflip.png)

Puede crear cadenas de intercambio de suma para un dispositivo mediante una llamada a [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/desktop/api). Una aplicación puede crear una cadena de intercambio por cada vista y asociar cada cadena de intercambio a una ventana determinada. La aplicación representa las imágenes en los búferes de reserva de cada cadena de intercambio y, a continuación, las presenta individualmente. Los dos parámetros que **IDirect3DDevice9:: CreateAdditionalSwapChain** toman son un puntero a una estructura de [**\_ parámetros D3DPRESENT**](d3dpresent-parameters.md) y la dirección de un puntero a una interfaz [**IDirect3DSwapChain9**](/windows/desktop/api) . Después, puede usar [**IDirect3DSwapChain9::P reenviar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) para mostrar el contenido del siguiente búfer de reserva en el búfer frontal. Tenga en cuenta que un dispositivo solo puede tener una cadena de intercambio de pantalla completa.

Puede obtener acceso a un búfer de reserva específico mediante una llamada a los métodos [**IDirect3DDevice9:: GetBackBuffer**](/windows/desktop/api) o [**IDirect3DSwapChain9:: GetBackBuffer**](/windows/desktop/api) , que devuelven un puntero a una interfaz [**IDirect3DSurface9**](/windows/desktop/api) que representa la superficie del búfer de reserva devuelta. Tenga en cuenta que, al llamar a este método, se aumenta el recuento de referencias interno de la interfaz [**IDirect3DDevice9**](/windows/desktop/api) . por tanto, asegúrese de llamar a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) cuando haya terminado de usar esta superficie o se producirá una fuga de memoria.

Recuerde que Direct3D voltea las superficies intercambiando los punteros de memoria de la superficie dentro de la cadena de intercambio, no intercambiando las propias superficies. Esto significa que siempre se representará en el búfer de reserva que se mostrará a continuación.

Es importante tener en cuenta la distinción entre una "operación de volteo", tal y como la lleva a cabo un controlador de adaptador de pantalla, y una operación "Present" aplicada a una cadena de intercambio creada con D3DSWAPEFFECT \_ flip.

El término "volteo" denota convencionalmente una operación que altera el intervalo de direcciones de memoria de vídeo que usa un adaptador de pantalla para generar su señal de salida, lo que provoca que se muestre el contenido de un búfer de reserva previamente oculto. En Direct3D 9, el término se suele usar más en general para describir la presentación de un búfer de reserva en cualquier cadena de intercambio creada con el \_ efecto D3DSWAPEFFECT Flip swap.

Aunque estas operaciones "presentes" se implementan casi invariablemente mediante operaciones de volteo cuando la cadena de intercambio es una pantalla completa, se implementan necesariamente mediante operaciones de copia cuando la cadena de intercambio está en la ventana. Además, un controlador de adaptador de pantalla puede usar el volteo para implementar las operaciones presentes en las cadenas de intercambio de pantalla completa basadas en la \_ copia descartar D3DSWAPEFFECT y D3DSWAPEFFECT \_ .

La explicación anterior se aplica al caso de uso frecuente de una cadena de intercambio de pantalla completa creada con D3DSWAPEFFECT \_ flip.

Para obtener más información general sobre los diferentes efectos de intercambio para las cadenas de intercambio de pantalla completa y de ventana, vea [**D3DSWAPEFFECT**](./d3dswapeffect.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
