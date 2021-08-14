---
title: procedimientos recomendados de Infraestructura de gráficos de DirectX (DXGI)
description: En este artículo se de abordan los principales problemas de porte.
ms.assetid: 2df92ffe-1bfc-d682-2770-20cf0c831c9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be992fe2346868eb3481482325297a2c9ec27ee61bdd2c65f83b0f916fc22308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290242"
---
# <a name="directx-graphics-infrastructure-dxgi-best-practices"></a>Infraestructura de gráficos de DirectX (DXGI): Procedimientos recomendados

Microsoft Infraestructura de gráficos de DirectX (DXGI) es un nuevo subsistema que se introdujo con Windows Vista que encapsula algunas de las tareas de bajo nivel que necesitan Direct3D 10, 10.1, 11 y 11.1. Desde la perspectiva de un programador de Direct3D 9, DXGI abarca la mayor parte del código para enumeración, creación de cadena de intercambio y presentación que anteriormente se empaquetaba en las API de Direct3D 9. Al portabilidad de una aplicación a DXGI, Direct3D 10.x y Direct3D 11.x, debe tener en cuenta algunas consideraciones para asegurarse de que el proceso se ejecuta sin problemas.

En este artículo se de abordan los principales problemas de porte.

-   [Problemas de pantalla completa](#full-screen-issues)
-   [Varios monitores](#multiple-monitors)
-   [Estilos de ventana y DXGI](#window-styles-and-dxgi)
-   [Multithreading y DXGI](#multithreading-and-dxgi)
-   [Gamma y DXGI](#gamma-and-dxgi)
-   [DXGI 1.1](#dxgi-11)
-   [DXGI 1.2](#dxgi-12)

## <a name="full-screen-issues"></a>Full-Screen problemas

En la porción de Direct3D 9 a DXGI y a Direct3D 10.x o Direct3D 11.x, los problemas asociados con el paso del modo de ventana a pantalla completa a menudo pueden causar problemas a los desarrolladores. Los principales problemas surgen porque las aplicaciones de Direct3D 9, a diferencia de las aplicaciones DXGI, requieren un enfoque más práctico para realizar el seguimiento de los estilos de ventana y los estados de las ventanas. Cuando el código de cambio de modo se porte para ejecutarse en DXGI, a menudo provoca un comportamiento inesperado.

A menudo, las aplicaciones de Direct3D 9 administraban la transición al modo de pantalla completa estableciendo la resolución del búfer frontal, forzando el dispositivo al modo exclusivo de pantalla completa y, a continuación, estableciendo las resoluciones del búfer de reserva para que coincidan. Se usó una ruta de acceso independiente para los cambios en el tamaño de la ventana porque tenían que administrarse desde el proceso de ventana cada vez que la aplicación recibe un mensaje \_ WM SIZE.

DXGI intenta simplificar este enfoque combinando los dos casos. Por ejemplo, cuando el borde de la ventana se arrastra en modo de ventana, la aplicación recibe un mensaje WM \_ SIZE. DXGI intercepta este mensaje y cambia automáticamente el tamaño del búfer frontal. Lo único que debe hacer la aplicación es llamar a [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) para cambiar el tamaño del búfer de reserva al tamaño que se pasó como parámetros en WM \_ SIZE. Del mismo modo, cuando la aplicación necesita cambiar entre el modo de pantalla completa y el modo de ventana, la aplicación puede llamar simplemente a [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate). DXGI cambia el tamaño del búfer frontal para que coincida con el modo de pantalla completa recién seleccionado y envía un mensaje WM SIZE a \_ la aplicación. La aplicación llama de nuevo **a ResizeBuffers,** igual que lo haría si se arrastrara el borde de la ventana.

La metodología de la explicación anterior sigue una ruta muy determinada. DXGI establece la resolución de pantalla completa en la resolución de escritorio de forma predeterminada. Sin embargo, muchas aplicaciones cambian a una resolución de pantalla completa preferida. En tal caso, DXGI proporciona [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget). Se debe llamar a este método antes de llamar a [**SetFullscreenState.**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) Aunque se puede llamar a estos métodos en el orden opuesto (**SetFullscreenState** primero, seguido de **ResizeTarget**), si lo hace, se envía un mensaje WM SIZE adicional a \_ la aplicación. (Esto también puede provocar parpadeo, ya que DXGI podría forzarse a realizar dos cambios de modo). Después de **llamar a SetFullscreenState,** es aconsejable volver a llamar a **ResizeTarget** con el miembro **RefreshRate** de [**DXGI MODE \_ \_ DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) con ceros. Esto equivale a una instrucción sin operación en DXGI, pero puede evitar problemas con la frecuencia de actualización, que se deba a continuación.

Cuando está en modo de pantalla completa, el Administrador de ventanas de escritorio (DWM) está deshabilitado. DXGI puede realizar un volteo para presentar el contenido del búfer de reserva en lugar de realizar una operación blit, lo que haría en modo de ventana. Sin embargo, esta ganancia de rendimiento se puede deshacer si no se cumplen determinados requisitos. Para asegurarse de que DXGI realiza un volteo en lugar de un blit, el búfer front-and-back debe tener el mismo tamaño. Si la aplicación controla correctamente sus mensajes \_ WM SIZE, esto no debería ser un problema. Además, los formatos deben ser idénticos.

El problema de la mayoría de las aplicaciones es la frecuencia de actualización. La frecuencia de actualización especificada en la llamada a [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) debe ser una frecuencia de actualización enumerada por el objeto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) que usa la cadena de intercambio. DXGI puede calcular automáticamente este valor si la aplicación cero el miembro **RefreshRate** de [**DXGI \_ MODE \_ DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) que se pasa a **ResizeTarget**. Es importante no suponer que siempre se admiten determinadas tasas de actualización y simplemente codificar de forma hard-code un valor. A menudo, los desarrolladores eligen 60 Hz como frecuencia de actualización, sin saber que la frecuencia de actualización enumerada del monitor es aproximadamente de 60 000 /1001 Hz del monitor. Si la frecuencia de actualización no coincide con la tasa de actualización esperada de 60, DXGI se ve obligado a realizar una blit en modo de pantalla completa en lugar de un volteo.

El último problema al que se enfrentan a menudo los desarrolladores es cómo cambiar las resoluciones de pantalla completa mientras permanecen en modo de pantalla completa. Llamar [**a ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) [**y SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) a veces se realiza correctamente, pero la resolución de pantalla completa sigue siendo la resolución del escritorio. Además, los desarrolladores pueden crear una cadena de intercambio de pantalla completa y proporcionar una resolución específica, solo para encontrar que DXGI tiene como valor predeterminado la resolución de escritorio independientemente de los números pasados. A menos que se indique lo contrario, DXGI tiene como valor predeterminado la resolución de escritorio para cadenas de intercambio de pantalla completa. Al crear una cadena de intercambio de pantalla completa, el miembro **Flags** de la estructura [**\_ \_ \_ DESC DXGI SWAP CHAIN**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) debe establecerse en [**DXGI SWAP CHAIN FLAG \_ ALLOW MODE \_ \_ \_ \_ \_ SWITCH**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) para invalidar el comportamiento predeterminado de DXGI. Esta marca también se puede pasar a **ResizeTarget** para habilitar o deshabilitar esta funcionalidad dinámicamente.

## <a name="multiple-monitors"></a>Varios monitores

Al usar DXGI con varios monitores, hay dos reglas a seguir.

La primera regla se aplica a la creación de dos o más cadenas de intercambio de pantalla completa en varios monitores. Al crear estas cadenas de intercambio, es mejor crear todas las cadenas de intercambio como ventanas y, a continuación, establecerlas en pantalla completa. Si se crean cadenas de intercambio en modo de pantalla completa, la creación de una segunda cadena de intercambio hace que se envíe un cambio de modo a la primera cadena de intercambio, lo que podría provocar la terminación del modo de pantalla completa.

La segunda regla se aplica a las salidas. Esté atento a las salidas usadas al crear cadenas de intercambio. Con DXGI, el objeto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) controla que supervisa los usos de la cadena de intercambio al convertirse en pantalla completa. A diferencia de DXGI, Direct3D 9 no tenía ningún concepto de salidas.

## <a name="window-styles-and-dxgi"></a>Estilos de ventana y DXGI

Las aplicaciones de Direct3D 9 tenían mucho trabajo que hacer al cambiar entre los modos de pantalla completa y de ventana. Gran parte de este trabajo implicaba cambiar los estilos de ventana para agregar y quitar bordes, para agregar barras de desplazamiento, y así sucesivamente. Cuando las aplicaciones se porte a DXGI y Direct3D 10.x o Direct3D 11.x, este código a menudo se deja en su lugar. En función de los cambios que se realicen, el cambio entre modos puede provocar un comportamiento inesperado. Por ejemplo, al cambiar al modo de ventana, es posible que la aplicación ya no tenga un marco de ventana o un borde de ventana a pesar de tener código que establece específicamente estos estilos. Esto sucede porque DXGI ahora controla gran parte de este estilo cambiando por sí mismo. La configuración manual de estilos de ventana puede interferir con DXGI, lo que puede provocar un comportamiento inesperado.

El comportamiento recomendado es realizar el menos trabajo posible y permitir que DXGI controle la mayor parte de la interacción con las ventanas. Sin embargo, si la aplicación necesita controlar su propio comportamiento de ventana, se puede usar [**IDXGIFactory::MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation) para decir a DXGI que deshabilite parte de su control automático de ventanas.

## <a name="multithreading-and-dxgi"></a>Multithreading y DXGI

Debe tener especial cuidado al usar DXGI en una aplicación multiproceso para asegurarse de que no se producen interbloqueos. Debido a la interacción cercana de DXGI con las ventanas, en ocasiones envía mensajes de ventana a la ventana de aplicación asociada. DXGI necesita que los cambios de ventana se produzcan antes de poder continuar, por lo que usará [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), que es una llamada sincrónica. La aplicación debe procesar el mensaje de ventana antes de **que se devuelva SendMessage.**

En una aplicación donde las llamadas DXGI y el bombeo de mensajes están en el mismo subproceso (o en una aplicación de un solo subproceso), es poco necesario hacer. Cuando la llamada DXGI está en el mismo subproceso que el bombeo de mensajes, [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) llama a [*WindowProc de la ventana.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Esto omite el bombeo de mensajes y permite que la ejecución continúe después de la llamada a **SendMessage**. Recuerde que [**las llamadas IDXGISwapChain,**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) como [**IDXGISwapChain::P resent,**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)también se consideran llamadas DXGI; DXGI puede aplazar el trabajo desde [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) o [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) hasta que se **llama** a Present.

Si la llamada DXGI y el bombeo de mensajes están en subprocesos diferentes, se debe tener cuidado para evitar interbloqueos. Cuando el bombeo de mensajes y SendMessage están en subprocesos diferentes, [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) agrega un mensaje a la cola de mensajes de la ventana y espera a que la ventana procese ese mensaje. Si el procedimiento de ventana está ocupado o el bombeo de mensajes no llama a este, es posible que el mensaje nunca se procese y DXGI espere indefinidamente.

Por ejemplo, si una aplicación que tiene su bombeo de mensajes en un subproceso y su representación en otro, puede que desee cambiar los modos. El subproceso de bombeo de mensajes indica al subproceso de representación que cambie de modo y espera hasta que se complete el cambio de modo. Sin embargo, el subproceso de representación llama a funciones DXGI, que a su vez llaman a [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), que se bloquea hasta que el bombeo del mensaje procesa el mensaje. Se produce un interbloqueo porque ambos subprocesos ahora están bloqueados y se están esperando entre sí. Para evitar esto, nunca bloquee el bombeo de mensajes. Si un bloque es inevitable, toda la interacción de DXGI debe producirse en el mismo subproceso que la bomba de mensajes.

## <a name="gamma-and-dxgi"></a>Gamma y DXGI

Aunque gamma puede controlarse mejor en Direct3D 10.x o Direct3D 11.x mediante texturas SRGB, la rampa gamma todavía puede ser útil para los desarrolladores que desean un valor gamma diferente a 2.2 o que usan un formato de destino de representación que no admite SRGB. Tenga en cuenta dos problemas al establecer la rampa gamma a través de DXGI. El primer problema es que los valores de rampa pasados a [**IDXGIOutput::SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) son valores float, no **valores WORD.** Además, asegúrese de que el código portado desde Direct3D 9 no intente convertir a **valores WORD** antes de pasar estos a **SetGammaControl**.

El segundo problema es que, después de cambiar al modo de pantalla completa, es posible que [**SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) no parezca funcionar, en función del objeto [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) que se esté utilizando. Al cambiar al modo de pantalla completa, DXGI crea un nuevo objeto de salida y usa el objeto para todas las operaciones posteriores en la salida. Si se llama a **SetGammaControl** en una salida que se enumera antes de un modificador de modo de pantalla completa, la llamada no se dirige a la salida que DXGI usa actualmente. Para evitar esto, llame a [**IDXGISwapChain::GetContainingOutput**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput) para obtener la salida actual y, a continuación, llame a **SetGammaControl** fuera de esta salida para obtener el comportamiento correcto.

Para obtener información sobre el uso de la corrección gamma, consulte [Uso de la corrección gamma.](/windows/desktop/direct3ddxgi/using-gamma-correction)

## <a name="dxgi-11"></a>DXGI 1.1

El entorno de ejecución de Direct3D 11 incluido en Windows 7 e instalado en Windows Vista (consulte [KB971644)](https://support.microsoft.com/kb/971644)incluye la versión 1.1 de DXGI. Esta actualización agrega definiciones para varios formatos nuevos (especialmente BGRA, sesgo X2 de 10 bits y compresión de textura BC6H y BC7 de Direct3D 11), así como una nueva versión de las interfaces de generador y adaptador de DXGI [**(CreateDXGIFactory1,**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) [**IDXGIFactory1,**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) [**IDXGIAdapter1)**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1)para enumerar las conexiones de escritorio remoto.

Cuando se usa Direct3D 11, el tiempo de ejecución usará DXGI 1.1 de forma predeterminada al llamar a [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) con un puntero [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) NULL. No se admite la combinación del uso de DXGI 1.0 y DXGI 1.1 en el mismo proceso. Tampoco se admite la combinación de instancias de objetos DXGI de distintos generadores en el mismo proceso. Por lo tanto, cuando se usa DirectX 11, cualquier uso explícito de las interfaces DXGI usa un [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) creado por el punto de entrada [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) en "DXGI.DLL" para asegurarse de que la aplicación siempre usa DXGI 1.1.

## <a name="dxgi-12"></a>DXGI 1.2

El entorno de ejecución de Direct3D 11.1 que se incluye en Windows 8 también incluye la versión 1.2 de DXGI.

DXGI 1.2 habilita estas características:

-   representación estéreo
-   Formatos de 16 bits por píxel

    -   DXGI \_ FORMAT \_ B5G6R5 \_ UNORM y DXGI \_ FORMAT \_ B5G5R5A1 \_ UNORM ahora son totalmente compatibles
    -   Se ha agregado un nuevo \_ formato DXGI FORMAT \_ B5G5R5A1 \_ UNORM

-   formatos de vídeo
-   nuevas interfaces DXGI

Para obtener más información sobre las características de DXGI 1.2, vea Mejoras de [DXGI 1.2.](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)

 

 