---
description: Un dispositivo Direct3D puede estar en un estado operativo o perdido.
ms.assetid: dc4326ba-2ebc-4bca-8fba-02d8db739b8f
title: Dispositivos perdidos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038d03f1d95e4beb90d0e592fc666972db4e92e5a2a986a7711023a6b9fa05b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728583"
---
# <a name="lost-devices-direct3d-9"></a>Dispositivos perdidos (Direct3D 9)

Un dispositivo Direct3D puede estar en un estado operativo o perdido. El estado operativo es el estado normal del dispositivo en el que se ejecuta el dispositivo y presenta toda la representación según lo previsto. El dispositivo realiza una transición al estado perdido cuando un evento, como la pérdida del foco del teclado en una aplicación de pantalla completa, hace que la representación sea imposible. El estado perdido se caracteriza por el error silencioso de todas las operaciones de representación, lo que significa que los métodos de representación pueden devolver códigos de operación correcta aunque se produce un error en las operaciones de representación. En esta situación, el código de error D3DERR DEVICELOST lo devuelve \_ [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

Por diseño, no se especifica el conjunto completo de escenarios que pueden hacer que un dispositivo se pierda. Algunos ejemplos típicos incluyen la pérdida de foco, como cuando el usuario presiona ALT+TAB o cuando se inicializa un cuadro de diálogo del sistema. Los dispositivos también se pueden perder debido a un evento de administración de energía o cuando otra aplicación asume una operación de pantalla completa. Además, cualquier error de [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) coloca el dispositivo en un estado perdido.

Se garantiza que todos los métodos que derivan de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) funcionarán después de que se pierda un dispositivo. Después de la pérdida del dispositivo, cada función generalmente tiene las tres opciones siguientes:

-   Error con D3DERR DEVICELOST: esto significa que la aplicación debe reconocer que el dispositivo se perdió, de modo que la aplicación identifique que algo no sucede según \_ lo previsto.
-   Error silencioso, devolver S OK o cualquier otro código de retorno: si se produce un error silencioso en una función, la aplicación generalmente no puede distinguir entre el resultado de \_ "correcto" y un "error silencioso".
-   La función devuelve un código de retorno.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> Un dispositivo Direct3D 9 devuelve D3DERR \_ DEVICELOST. Una vez que se ha devuelto desde [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), el comportamiento de emulación ya no funciona y todas las llamadas futuras producirán un error hasta que el dispositivo se restablezca correctamente.<br/> Un dispositivo Direct3D 9Ex nunca devuelve D3DERR DEVICELOST, pero puede devolver mensajes de estado nuevos (consulte cambios de comportamiento \_ [del dispositivo).](dx9lh.md)<br/> |



 

## <a name="responding-to-a-lost-device"></a>Respuesta a un dispositivo perdido

Un dispositivo perdido debe volver a crear recursos (incluidos los recursos de memoria de vídeo) una vez restablecido. Si se pierde un dispositivo, la aplicación consulta el dispositivo para ver si se puede restaurar al estado operativo. Si no es así, la aplicación espera hasta que se pueda restaurar el dispositivo.

Si el dispositivo se puede restaurar, la aplicación prepara el dispositivo mediante la destrucción de todos los recursos de memoria de vídeo y cualquier cadena de intercambio. A continuación, la aplicación llama [**al método IDirect3DDevice9::Reset.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) El restablecimiento es el único método que tiene efecto cuando se pierde un dispositivo y es el único método por el que una aplicación puede cambiar el dispositivo de un dispositivo perdido a un estado operativo. Se producirá un error en el restablecimiento a menos que la aplicación libere todos los recursos asignados en D3DPOOL DEFAULT, incluidos los creados por los métodos \_ [**IDirect3DDevice9::CreateRenderTarget**](/windows/desktop/api) e [**IDirect3DDevice9::CreateDepthStencilSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)

En su mayor parte, las llamadas de alta frecuencia de Direct3D no devuelven información sobre si se ha perdido el dispositivo. La aplicación puede seguir llamadas a métodos de representación, como [**IDirect3DDevice9::D rawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)sin recibir notificación de un dispositivo perdido. Internamente, estas operaciones se descartan hasta que el dispositivo se restablece al estado operativo.

La aplicación puede determinar qué hacer al encontrar un dispositivo perdido consultando el valor devuelto del método [**IDirect3DDevice9::TestCooperativeLevel.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)

## <a name="locking-operations"></a>Operaciones de bloqueo

Internamente, Direct3D hace suficiente trabajo para asegurarse de que una operación de bloqueo se realizará correctamente después de que se pierda un dispositivo. Sin embargo, no se garantiza que los datos del recurso de memoria de vídeo sean precisos durante la operación de bloqueo. Se garantiza que no se devolverá ningún código de error. Esto permite que las aplicaciones se escriban sin preocuparse por la pérdida de dispositivos durante una operación de bloqueo.

## <a name="resources"></a>Recursos

Los recursos pueden consumir memoria de vídeo. Dado que un dispositivo perdido se desconecta de la memoria de vídeo propiedad del adaptador, no es posible garantizar la asignación de memoria de vídeo cuando se pierde el dispositivo. Como resultado, todos los métodos de creación de recursos se implementan para que se realicen correctamente devolviendo D3D OK, pero de hecho solo asignan \_ memoria ficticia del sistema. Dado que cualquier recurso de memoria de vídeo debe destruirse antes de cambiar el tamaño del dispositivo, no hay ningún problema de sobreasignación de memoria de vídeo. Estas superficies ficticias permiten que las operaciones de bloqueo y copia parezcan funcionar con normalidad hasta que la aplicación llama a [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) y detecta que el dispositivo se ha perdido.

Toda la memoria de vídeo debe liberarse antes de que se pueda restablecer un dispositivo de un estado perdido a un estado operativo. Esto significa que la aplicación debe liberar todas las cadenas de intercambio creadas con [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) y los recursos colocados en la clase de memoria D3DPOOL \_ DEFAULT. La aplicación no necesita liberar recursos en las clases de memoria D3DPOOL \_ MANAGED o D3DPOOL \_ SYSTEMMEM. La transición a un estado operativo destruye automáticamente otros datos de estado.

Se recomienda desarrollar aplicaciones con una única ruta de acceso de código para responder a la pérdida de dispositivos. Es probable que esta ruta de acceso de código sea similar, si no idéntica, a la ruta de acceso del código realizada para inicializar el dispositivo en el inicio.

## <a name="retrieved-data"></a>Datos recuperados

Direct3D permite a las aplicaciones validar los estados de textura y representación en la representación de un solo paso por parte del hardware [**mediante IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice). Este método, que normalmente se invoca durante la inicialización de la aplicación, devolverá D3DERR DEVICELOST si se ha perdido \_ el dispositivo.

Direct3D también permite a las aplicaciones copiar imágenes generadas o escritas previamente de recursos de memoria de vídeo a recursos de memoria del sistema no volátiles. Dado que las imágenes de origen de dichas transferencias se pueden perder en cualquier momento, Direct3D permite que estas operaciones de copia no se puedan realizar cuando se pierde el dispositivo.

Con respecto a las consultas asincrónicas, [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) devuelve D3DERR DEVICELOST si se especifica la marca FLUSH, con el fin de indicar a la aplicación que \_ **IDirect3DQuery9::GetData** nunca devolverá S \_ OK.

La operación de copia, [**IDirect3DDevice9::GetFrontBufferData,**](/windows/desktop/api)puede producir un error con D3DERR DEVICELOST, ya que no hay ninguna superficie principal cuando se pierde \_ el dispositivo. [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) también puede producir un error con D3DERR DEVICELOST porque no se puede crear un búfer de reserva cuando se pierde el \_ dispositivo. Tenga en cuenta que estos casos son la única instancia de D3DERR DEVICELOST fuera de los métodos \_ [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), [**IDirect3DDevice9::TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)e [**IDirect3DDevice9::Reset.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)

## <a name="programmable-shaders"></a>Sombreadores programables

En Direct3D 9, los sombreadores de vértices y los sombreadores de píxeles no tienen que volver a crearse después del restablecimiento. Se recordarán. En versiones anteriores de DirectX, un dispositivo perdido requería que se vuelvan a crear los sombreadores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
