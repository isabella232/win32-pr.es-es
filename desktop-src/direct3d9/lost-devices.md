---
description: Un dispositivo Direct3D puede estar en un estado operativo o en un estado perdido.
ms.assetid: dc4326ba-2ebc-4bca-8fba-02d8db739b8f
title: Dispositivos perdidos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a808cb113f5c2fd35a741e0efc7c6b8af9e127df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359965"
---
# <a name="lost-devices-direct3d-9"></a>Dispositivos perdidos (Direct3D 9)

Un dispositivo Direct3D puede estar en un estado operativo o en un estado perdido. El estado operativo es el estado normal del dispositivo en el que se ejecuta el dispositivo y presenta todas las representaciones según lo previsto. El dispositivo realiza una transición al estado perdido cuando un evento, como la pérdida del foco de teclado en una aplicación de pantalla completa, hace que la representación sea imposible. El estado perdido se caracteriza por el error silencioso de todas las operaciones de representación, lo que significa que los métodos de representación pueden devolver códigos correctos aunque se produzca un error en las operaciones de representación. En esta situación, IDirect3DDevice9 devuelve el código de error D3DERR \_ DEVICELOST [**::P reenviar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

Por diseño, no se especifica el conjunto completo de escenarios que pueden provocar que se pierda un dispositivo. Algunos ejemplos típicos incluyen la pérdida del foco, como cuando el usuario presiona ALT + TAB o cuando se inicializa un cuadro de diálogo de sistema. Los dispositivos también se pueden perder debido a un evento de administración de energía o cuando otra aplicación asume una operación de pantalla completa. Además, los errores de [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) ponen el dispositivo en un estado perdido.

Se garantiza que todos los métodos que se derivan de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) funcionan después de que se pierda un dispositivo. Después de la pérdida del dispositivo, cada función tiene generalmente las tres opciones siguientes:

-   Error con D3DERR \_ DEVICELOST: Esto significa que la aplicación debe reconocer que el dispositivo se perdió, por lo que la aplicación identifica que algo no está ocurriendo según lo esperado.
-   Se produce un error en modo silencioso, se devuelve un \_ valor correcto o cualquier otro código de retorno; si una función produce un error en modo silencioso, la aplicación generalmente no puede distinguir entre el resultado de "Success" y un "error silencioso".
-   La función devuelve un código de retorno.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> Un dispositivo de Direct3D 9 devuelve D3DERR \_ DEVICELOST. Una vez que se ha devuelto desde [**IDirect3DDevice9::P reenviados**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), el comportamiento de la emulación ya no funciona y se producirá un error en todas las llamadas futuras hasta que el dispositivo se restablezca correctamente.<br/> Un dispositivo 9Ex de Direct3D nunca devuelve D3DERR \_ DEVICELOST, pero puede devolver nuevos mensajes de estado (vea [cambios de comportamiento del dispositivo](dx9lh.md)).<br/> |



 

## <a name="responding-to-a-lost-device"></a>Responder a un dispositivo perdido

Un dispositivo perdido debe volver a crear los recursos (incluidos los recursos de memoria de vídeo) una vez que se haya restablecido. Si se pierde un dispositivo, la aplicación consulta el dispositivo para ver si se puede restaurar al estado operativo. Si no es así, la aplicación espera hasta que el dispositivo se pueda restaurar.

Si el dispositivo se puede restaurar, la aplicación prepara el dispositivo destruyendo todos los recursos de memoria de vídeo y cualquier cadena de intercambio. A continuación, la aplicación llama al método [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) . RESET es el único método que tiene un efecto cuando se pierde un dispositivo y es el único método por el que una aplicación puede cambiar el dispositivo de un estado de pérdida a operativo. El restablecimiento producirá un error a menos que la aplicación libere todos los recursos asignados en D3DPOOL \_ default, incluidos los creados por los métodos [**IDirect3DDevice9:: CreateRenderTarget**](/windows/desktop/api) y [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) .

En su mayor parte, las llamadas de alta frecuencia de Direct3D no devuelven ninguna información acerca de si el dispositivo se ha perdido. La aplicación puede seguir llamando a métodos de representación, como [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), sin recibir la notificación de un dispositivo perdido. Internamente, estas operaciones se descartan hasta que el dispositivo se restablece al estado operativo.

La aplicación puede determinar qué hacer al encontrar un dispositivo perdido consultando el valor devuelto del método [**IDirect3DDevice9:: TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) .

## <a name="locking-operations"></a>Operaciones de bloqueo

De forma interna, Direct3D hace suficientes trabajos para asegurarse de que una operación de bloqueo se realizará correctamente después de que se pierda un dispositivo. Sin embargo, no se garantiza que los datos del recurso de memoria de vídeo serán precisos durante la operación de bloqueo. Se garantiza que no se devolverá ningún código de error. Esto permite escribir aplicaciones sin preocuparse por la pérdida de dispositivos durante una operación de bloqueo.

## <a name="resources"></a>Recursos

Los recursos pueden consumir memoria de vídeo. Dado que un dispositivo perdido está desconectado de la memoria de vídeo propiedad del adaptador, no es posible garantizar la asignación de memoria de vídeo cuando se pierde el dispositivo. Como resultado, todos los métodos de creación de recursos se implementan para que se realicen correctamente devolviendo D3D \_ OK, pero en realidad asignan solo la memoria del sistema ficticia. Dado que los recursos de memoria de vídeo deben destruirse antes de que se cambie el tamaño del dispositivo, no hay ningún problema de asignación excesiva de memoria de vídeo. Estas superficies ficticias permiten que las operaciones de bloqueo y copia parezcan funcionar con normalidad hasta que la aplicación llama a [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) reenvía y detecta que el dispositivo se ha perdido.

Se debe liberar toda la memoria de vídeo antes de que un dispositivo se pueda restablecer desde un estado de pérdida a un estado operativo. Esto significa que la aplicación debe liberar cualquier cadena de intercambio creada con [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) y cualquier recurso colocado en la \_ clase de memoria predeterminada de D3DPOOL. La aplicación no necesita liberar recursos en las \_ clases de memoria D3DPOOL administradas o D3DPOOL \_ SYSTEMMEM. Los demás datos de estado se destruyen automáticamente por la transición a un estado operativo.

Se recomienda desarrollar aplicaciones con una única ruta de acceso de código para responder a la pérdida del dispositivo. Es probable que esta ruta de acceso del código sea similar, si no idéntica, a la ruta de acceso del código tomada para inicializar el dispositivo en el inicio.

## <a name="retrieved-data"></a>Datos recuperados

Direct3D permite que las aplicaciones validen las texturas y los Estados de representación en la representación de un solo paso por parte del hardware mediante [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice). Este método, que normalmente se invoca durante la inicialización de la aplicación, devolverá D3DERR \_ DEVICELOST si el dispositivo se ha perdido.

Direct3D también permite que las aplicaciones copien imágenes generadas o escritas previamente desde recursos de memoria de vídeo a recursos de memoria del sistema no volátiles. Dado que las imágenes de origen de tales transferencias podrían perderse en cualquier momento, Direct3D permite que se produzcan errores en las operaciones de copia cuando se pierde el dispositivo.

Con respecto a las consultas asincrónicas, [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) devuelve D3DERR \_ DEVICELOST si se especifica la marca Flush, para indicar a la aplicación que **IDirect3DQuery9:: GetData** nunca devolverá los valores \_ correctos.

La operación de copia, [**IDirect3DDevice9:: GetFrontBufferData**](/windows/desktop/api), puede generar un error con D3DERR \_ DEVICELOST, ya que no hay ninguna superficie principal cuando se pierde el dispositivo. [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) también puede generar un error con D3DERR \_ DEVICELOST porque no se puede crear un búfer de reserva cuando se pierde el dispositivo. Tenga en cuenta que estos casos son la única instancia de D3DERR \_ DEVICELOST fuera de [**IDirect3DDevice9::P reenviar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), [**IDirect3DDevice9:: TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)y [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) .

## <a name="programmable-shaders"></a>Sombreadores programables

En Direct3D 9, no es necesario volver a crear los sombreadores de vértices y los sombreadores de píxeles después del restablecimiento. Se recordarán. En versiones anteriores de DirectX, un dispositivo perdió los sombreadores necesarios para volver a crearlos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
