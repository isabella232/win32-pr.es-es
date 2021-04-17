---
title: Procedimientos recomendados de la infraestructura de gráficos de DirectX (DXGI)
description: En este artículo se describen los problemas de portabilidad de claves.
ms.assetid: 2df92ffe-1bfc-d682-2770-20cf0c831c9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f576368674d05af74e3161d4251301ebc066a489
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421170"
---
# <a name="directx-graphics-infrastructure-dxgi-best-practices"></a>Infraestructura de gráficos de DirectX (DXGI): procedimientos recomendados

Microsoft DirectX Graphics Infrastructure (DXGI) es un nuevo subsistema que se presentó con Windows Vista que encapsula algunas de las tareas de bajo nivel que son necesarias en Direct3D 10, 10,1, 11 y 11,1. Desde el punto de vista de un programador de Direct3D 9, DXGI abarca la mayor parte del código para la enumeración, la creación de la cadena de intercambio y la presentación que anteriormente se empaquetaba en las API de Direct3D 9. Al migrar una aplicación a DXGI y Direct3D 10. x y Direct3D 11. x, debe tener en cuenta algunas consideraciones para asegurarse de que el proceso se ejecuta sin problemas.

En este artículo se describen los problemas de portabilidad de claves.

-   [Problemas de pantalla completa](#full-screen-issues)
-   [Varios monitores](#multiple-monitors)
-   [Estilos de ventana y DXGI](#window-styles-and-dxgi)
-   [Multithreading y DXGI](#multithreading-and-dxgi)
-   [Gamma y DXGI](#gamma-and-dxgi)
-   [DXGI 1,1](#dxgi-11)
-   [DXGI 1,2](#dxgi-12)

## <a name="full-screen-issues"></a>Problemas de Full-Screen

En la migración de Direct3D 9 a DXGI y a Direct3D 10. x o Direct3D 11. x, los problemas asociados con el cambio de ventanas al modo de pantalla completa pueden provocar problemas de los desarrolladores. Los principales problemas surgen porque las aplicaciones de Direct3D 9, a diferencia de las aplicaciones de DXGI, requieren un enfoque más práctico para el seguimiento de los estilos de ventana y los Estados de las ventanas. Cuando el código que cambia el modo se traslada para ejecutarse en DXGI, a menudo provoca un comportamiento inesperado.

A menudo, las aplicaciones de Direct3D 9 controlaban la transición al modo de pantalla completa mediante la configuración de la resolución del búfer frontal, forzando el dispositivo al modo exclusivo de pantalla completa y, después, estableciendo las resoluciones del búfer de reserva para que coincidan. Se usó una ruta de acceso independiente para los cambios en el tamaño de la ventana porque tenían que administrarse desde el proceso de la ventana cada vez que la aplicación recibía un mensaje de tamaño de WM \_ .

DXGI intenta simplificar este enfoque mediante la combinación de los dos casos. Por ejemplo, cuando el borde de la ventana se arrastra en modo de ventana, la aplicación recibe un \_ mensaje de tamaño de WM. DXGI intercepta este mensaje y cambia automáticamente el tamaño del búfer frontal. Todo lo que la aplicación tiene que hacer es llamar a [**IDXGISwapChain:: ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) para cambiar el tamaño del búfer de reserva al tamaño que se pasó como parámetro en \_ el tamaño de WM. De forma similar, cuando la aplicación necesita cambiar entre el modo de pantalla completa y el de ventanas, la aplicación simplemente puede llamar a [**IDXGISwapChain:: SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate). DXGI cambia el tamaño del búfer frontal para que coincida con el modo de pantalla completa recién seleccionado y envía un mensaje de tamaño de WM \_ a la aplicación. De nuevo, la aplicación llama a **ResizeBuffers**, tal como lo haría si se arrastrase el borde de la ventana.

La metodología de la explicación anterior sigue una ruta de acceso muy determinada. DXGI establezca la resolución de pantalla completa en la resolución del escritorio de forma predeterminada. Sin embargo, muchas aplicaciones cambian a una resolución de pantalla completa preferida. En tal caso, DXGI proporciona [**IDXGISwapChain:: ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget). Se debe llamar a este método antes de llamar a [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate). Aunque se puede llamar a estos métodos en el orden opuesto (**SetFullscreenState** en primer lugar, seguido de **ResizeTarget**), hacerlo hace que se envíe un mensaje de tamaño de WM adicional \_ a la aplicación. (Si lo hace, también puede provocar parpadeos, ya que DXGI podría verse obligado a realizar dos cambios en el modo). Después de llamar a **SetFullscreenState**, es aconsejable llamar de nuevo a **ResizeTarget** **con el miembro** de la frecuencia del [**modo de DXGI \_ \_**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) en cero. Esto se remonta en una instrucción de no operación en DXGI, pero puede evitar problemas con la frecuencia de actualización, que se explican a continuación.

En el modo de pantalla completa, el Administrador de ventanas de escritorio (DWM) está deshabilitado. DXGI puede realizar una operación Flip para presentar el contenido del búfer de retroceso en lugar de realizar una operación blit, lo que haría en el modo de ventana. Este aumento de rendimiento se puede deshacer, sin embargo, si no se cumplen determinados requisitos. Para asegurarse de que DXGI realiza una volteo en lugar de una blit, el búfer frontal y el búfer de reserva deben tener un tamaño idéntico. Si la aplicación controla correctamente \_ los mensajes de tamaño de WM, esto no debería ser un problema. Además, los formatos deben ser idénticos.

El problema de la mayoría de las aplicaciones es la frecuencia de actualización. La frecuencia de actualización que se especifica en la llamada a [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) debe ser una frecuencia de actualización enumerada por el objeto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) que usa la cadena de intercambio. DXGI puede calcular automáticamente este valor si la aplicación pone en cero el **miembro de** frecuencia de la [**\_ \_ Descripción del modo DXGI**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) que se pasa a **ResizeTarget**. Es importante no asumir que ciertas frecuencias de actualización se admitirán siempre y simplemente codificar un valor. A menudo, los desarrolladores eligen 60 Hz como la frecuencia de actualización, sin saber que la frecuencia de actualización enumerada desde el monitor es de aproximadamente 60.000/1.001 Hz en el monitor. Si la frecuencia de actualización no coincide con la frecuencia de actualización esperada de 60, se fuerza a DXGI a que realice una blit en el modo de pantalla completa en lugar de un volteo.

El último problema al que suelen encontrarse los desarrolladores es cómo cambiar las resoluciones de pantalla completa mientras permanecen en el modo de pantalla completa. La llamada a [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) y [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) a veces se realiza correctamente, pero la resolución de pantalla completa sigue siendo la resolución del escritorio. Además, los desarrolladores pueden crear una cadena de intercambio de pantalla completa y proporcionar una resolución específica, solo para buscar que DXGI tenga como valor predeterminado la resolución del escritorio, independientemente de los números que se hayan pasado. A menos que se indique lo contrario, DXGI tiene como valor predeterminado la resolución del escritorio para las cadenas de intercambio de pantalla completa. Al crear una cadena de intercambio de pantalla completa, el miembro **Flags** de la estructura de DESC de la cadena de intercambio de dxgi debe establecerse en el [**\_ \_ \_**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) [**\_ \_ \_ \_ \_ \_ modificador de modo permitir**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) de la cadena de intercambio de dxgi para invalidar el comportamiento predeterminado de dxgi. Esta marca también se puede pasar a **ResizeTarget** para habilitar o deshabilitar esta funcionalidad de forma dinámica.

## <a name="multiple-monitors"></a>Varios monitores

Al usar DXGI con varios monitores, hay dos reglas que deben seguirse.

La primera regla se aplica a la creación de dos o más cadenas de intercambio de pantalla completa en varios monitores. Al crear tales cadenas de intercambio, es mejor crear todas las cadenas de intercambio como ventana y, a continuación, establecerlas en pantalla completa. Si las cadenas de intercambio se crean en el modo de pantalla completa, la creación de una segunda cadena de intercambio hace que se envíe un cambio de modo a la primera cadena de intercambio, lo que podría provocar la terminación del modo de pantalla completa.

La segunda regla se aplica a las salidas. Esté atento a las salidas utilizadas al crear cadenas de intercambio. Con DXGI, el objeto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) controla qué monitor usa la cadena de intercambio cuando se convierte en pantalla completa. A diferencia de DXGI, Direct3D 9 no tenía ningún concepto de salidas.

## <a name="window-styles-and-dxgi"></a>Estilos de ventana y DXGI

Las aplicaciones de Direct3D 9 tenían mucho trabajo para cambiar entre los modos de pantalla completa y de ventana. Gran parte de este trabajo implica cambiar los estilos de ventana para agregar y quitar bordes, agregar barras de desplazamiento, etc. Cuando las aplicaciones se trasladan a DXGI y Direct3D 10. x o Direct3D 11. x, este código se deja en su lugar. Dependiendo de los cambios que se realicen, el cambio entre modos puede producir un comportamiento inesperado. Por ejemplo, al cambiar al modo de ventana, es posible que la aplicación deje de tener un marco de ventana o un borde de ventana a pesar de tener código que establezca específicamente estos estilos. Esto se debe a que DXGI ahora controla gran parte de este estilo cambiando por sí mismo. La configuración manual de los estilos de ventana puede interferir con DXGI y esto puede provocar un comportamiento inesperado.

El comportamiento recomendado es realizar el menor trabajo posible y permitir que DXGI controle la mayor parte de la interacción con las ventanas. Sin embargo, si la aplicación necesita controlar su propio comportamiento de ventana, se puede usar [**IDXGIFactory:: MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation) para indicar a DXGI que deshabilite parte de su control automático de ventanas.

## <a name="multithreading-and-dxgi"></a>Multithreading y DXGI

Se debe tener especial cuidado al usar DXGI en una aplicación multiproceso para garantizar que no se produzcan interbloqueos. Debido a la interacción estrecha de DXGI con las ventanas, en ocasiones envía mensajes de ventana a la ventana de la aplicación asociada. DXGI necesita que los cambios en las ventanas se realicen antes de poder continuar, por lo que usará [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), que es una llamada sincrónica. La aplicación debe procesar el mensaje de ventana antes de que se devuelva **SendMessage** .

En una aplicación en la que las llamadas de DXGI y el bombeo de mensajes se encuentran en el mismo subproceso (o en una aplicación de un solo subproceso), es necesario hacer poco. Cuando la llamada de DXGI está en el mismo subproceso que el bombeo de mensajes, [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) llama a la [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))de la ventana. Esto omite el bombeo de mensajes y permite que continúe la ejecución después de la llamada a **SendMessage**. Recuerde que las llamadas a [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) , como [**IDXGISwapChain::P reenviados**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present), también se consideran llamadas de DXGI; DXGI puede diferir el trabajo de [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) o [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) hasta que se llama a **present** .

Si la llamada de DXGI y el bombeo de mensajes están en distintos subprocesos, debe tener cuidado para evitar los interbloqueos. Cuando el bombeo de mensajes y SendMessage están en subprocesos diferentes, [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) agrega un mensaje a la cola de mensajes de la ventana y espera a que la ventana procese ese mensaje. Si el procedimiento de ventana está ocupado o no lo llama el bombeo de mensajes, es posible que el mensaje no se procese nunca y DXGI espere indefinidamente.

Por ejemplo, si una aplicación tiene su bombeo de mensajes en un subproceso y su representación en otro, puede que desee cambiar los modos. El subproceso de bombeo de mensajes indica al subproceso de representación que cambie los modos y espera hasta que se complete el cambio de modo. Sin embargo, el subproceso de representación llama a las funciones de DXGI, que a su vez llaman a [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), que se bloquea hasta que el bombeo de mensajes procesa el mensaje. Se produce un interbloqueo porque los dos subprocesos ahora están bloqueados y están esperando entre sí. Para evitar esto, no bloquee nunca el bombeo de mensajes. Si un bloque es inevitable, todas las interacciones de DXGI deben realizarse en el mismo subproceso que el bombeo de mensajes.

## <a name="gamma-and-dxgi"></a>Gamma y DXGI

Aunque el valor de gamma puede controlarse mejor en Direct3D 10. x o Direct3D 11. x mediante el uso de texturas SRGB, la rampa de gamma todavía puede ser útil para los desarrolladores que quieren un valor gamma diferente que 2,2 o que usan un formato de destino de representación que no admite SRGB. Tenga en cuenta dos problemas al establecer la rampa de gamma a través de DXGI. El primer problema es que los valores de rampa pasados en [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) son valores Float, no valores de **palabra** . Además, asegúrese de que el código que se portó desde Direct3D 9 no intente convertir a valores de **Word** antes de pasarlos a **SetGammaControl**.

El segundo problema es que, después de cambiar al modo de pantalla completa, puede que [**SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) no funcione, dependiendo del objeto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) que se está usando. Al cambiar al modo de pantalla completa, DXGI crea un nuevo objeto de salida y usa el objeto para todas las operaciones posteriores en la salida. Si se llama a **SetGammaControl** en una salida que se enumera antes que un modificador en modo de pantalla completa, la llamada no se dirige hacia la salida que DXGI está usando actualmente. Para evitar esto, llame a [**IDXGISwapChain:: GetContainingOutput**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput) para obtener la salida actual y, a continuación, llame a **SetGammaControl** fuera de esta salida para obtener el comportamiento correcto.

Para obtener información sobre el uso de la corrección gamma, vea [usar corrección Gamma](/windows/desktop/direct3ddxgi/using-gamma-correction).

## <a name="dxgi-11"></a>DXGI 1,1

El tiempo de ejecución de Direct3D 11 incluido en Windows 7 e instalado en Windows Vista (vea [KB971644](https://support.microsoft.com/kb/971644)) incluye la versión 1,1 de DXGI. Esta actualización agrega definiciones para varios formatos nuevos (en particular, BGRA, la diferencia x2 de 10 bits y la compresión de textura BC6H y BC7 de Direct3D 11), así como una nueva versión de las interfaces de adaptador y adaptador de DXGI ([**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1), [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1), [**IDXGIAdapter1**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1)) para enumerar las conexiones de escritorio remoto.

Cuando se usa Direct3D 11, el Runtime usará DXGI 1,1 de forma predeterminada al llamar a [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) con un puntero [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) nulo. No se admite la combinación del uso de DXGI 1,0 y DXGI 1,1 en el mismo proceso. Tampoco se admite la combinación de instancias de objeto de DXGI desde diferentes fábricas en el mismo proceso. Por lo tanto, cuando se usa DirectX 11, cualquier uso explícito de las interfaces de DXGI usa un [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) creado por el punto de entrada de [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) en "DXGI.DLL" para asegurarse de que la aplicación siempre usa DXGI 1,1.

## <a name="dxgi-12"></a>DXGI 1,2

El tiempo de ejecución de Direct3D 11,1 que se incluye en Windows 8 también incluye la versión 1,2 de DXGI.

DXGI 1,2 habilita estas características:

-   representación de estéreo
-   formatos de 16 bits por píxel

    -   El \_ formato \_ de dxgi B5G6R5 \_ UNORM y el formato de dxgi \_ \_ B5G5R5A1 \_ UNORM ahora son totalmente compatibles
    -   se ha agregado un nuevo formato de \_ \_ B5G5R5A1 \_ UNORM formato de DXGI

-   formatos de vídeo
-   nuevas interfaces de DXGI

Para obtener más información sobre las características de DXGI 1,2, consulte [mejoras de dxgi 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements).

 

 