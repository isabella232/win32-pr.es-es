---
description: Windows 8 agrega compatibilidad con el modelo de presentación de volteo y sus estadísticas presentes asociadas en DXGI 1.2.
ms.assetid: E132DAF5-80B7-4C52-A760-3779CC140CE7
title: Modelo de volteo DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b4b4cf8f792a23d4d32e5cb4b4273594745283cb803a638ea3d0cf4c45977f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289458"
---
# <a name="dxgi-flip-model"></a>Modelo de volteo DXGI

Windows 8 agrega compatibilidad con el modelo de presentación de volteo y sus estadísticas presentes asociadas en DXGI 1.2. Windows 8 modelo de presentación de volteo DXGI de Windows la presentación del modo de volteo de [Direct3D 9EX](../direct3darticles/direct3d-9ex-improvements.md)de 7. Las aplicaciones de presentación basadas en velocidad de fotogramas o vídeo, como los juegos, pueden beneficiarse más mediante el modelo de presentación de volteo. Las aplicaciones que usan el modelo de presentación de volteo DXGI reducen la carga de recursos del sistema y aumentan el rendimiento. Las aplicaciones también pueden usar mejoras de estadísticas presentes con el modelo de presentación de volteo para controlar mejor la tasa de presentación proporcionando comentarios en tiempo real y mecanismos de corrección.

-   [Comparación del modelo de volteo DXGI y el modelo BitBlt](#comparing-the-dxgi-flip-model-and-the-bitblt-model)
-   [Uso del modelo de volteo DXGI](#how-to-use-dxgi-flip-model)
-   [Sincronización de fotogramas de aplicaciones de modelo de volteo DXGI](#frame-synchronization-of-dxgi-flip-model-apps)
-   [Evitar, detectar y recuperarse de problemas](#avoiding-detecting-and-recovering-from-glitches)
-   [Temas relacionados](#related-topics)

## <a name="comparing-the-dxgi-flip-model-and-the-bitblt-model"></a>Comparación del modelo de volteo DXGI y el modelo BitBlt

El tiempo de ejecución usa la transferencia de bloques de bits (bitblt) y los modelos de presentación de volteo para presentar contenido gráfico en los monitores de pantalla. La diferencia más importante entre los modelos de presentación bitblt y flip es cómo el contenido del búfer de reserva obtiene el Windows 8 DWM para la composición. En el modelo bitblt, el contenido del búfer de reserva se copia en la superficie de redireccionamiento en cada llamada a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). En el modelo de volteo, todos los búferes de reserva se comparten con el Administrador de ventanas de escritorio (DWM). Por lo tanto, dwm puede crear directamente desde esos búferes de reserva sin ninguna operación de copia adicional. En general, el modelo de volteo es más eficaz. El modelo de volteo también proporciona más características, como estadísticas actuales mejoradas.

Si tiene componentes heredados que usan Windows Interfaz de dispositivo gráfico (GDI) para escribir directamente en [**un HWND,**](../winprog/windows-data-types.md) use el modelo bitblt.

Las mejoras de rendimiento del modelo de volteo DXGI son significativas cuando la aplicación está en modo de ventana. La secuencia de esta tabla y la ilustración comparan los usos de ancho de banda de memoria y las lecturas y escrituras del sistema de las aplicaciones en ventanas que eligen el modelo de volteo frente al modelo bitblt.



| Paso | Modelo de BitBlt presente en DWM                                                                               | Modelo de volteo DXGI presente en DWM                                   |
|------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 1.   | La aplicación actualiza su marco (escritura)<br/>                                                              | La aplicación actualiza su marco (escritura)<br/>                     |
| 2.   | El tiempo de ejecución de Direct3D copia el contenido de la superficie en una superficie de redireccionamiento de DWM (lectura, escritura)<br/>            | El entorno de ejecución de Direct3D pasa la superficie de la aplicación a DWM<br/>        |
| 3.   | Una vez completada la copia de la superficie compartida, DWM representa la superficie de la aplicación en la pantalla (lectura, escritura)<br/> | DWM representa la superficie de la aplicación en la pantalla (lectura, escritura)<br/> |



 

![ilustración de una comparación del modelo blt y el modelo de volteo](images/blt-flip-mode-present.png)

El cambio de modelo reduce el uso de memoria del sistema al reducir el número de lecturas y escrituras por el tiempo de ejecución de Direct3D para la composición de fotogramas en ventanas mediante DWM.

## <a name="how-to-use-dxgi-flip-model"></a>Uso del modelo de volteo DXGI

Las aplicaciones de Direct3D 11.1 que tienen como destino Windows 8 usan el modelo de volteo mediante la creación de la cadena de intercambio con el valor de enumeración DESC1 [**DXGI \_ SWAP EFFECT \_ FLIP \_ \_ establecido**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) en el miembro **SwapEffect** de la estructura [**DXGI SWAP CHAIN \_ \_ \_ DESC1.**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) Al establecer **SwapEffect** en **DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL**, establezca también estos miembros de **DXGI SWAP CHAIN \_ \_ \_ DESC1** en los valores indicados:

-   **BufferCount** en un valor entre 2 y 16 para evitar una penalización del rendimiento como resultado de esperar a que DWM libere el búfer de presentación anterior.
-   **Formato** a DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT, DXGI \_ FORMAT \_ B8G8R8A8 UNORM o \_ DXGI FORMAT \_ \_ R8G8B8A8 \_ UNORM
-   **Miembro Count** de la estructura [**\_ DXGI SAMPLE \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc) que el miembro **SampleDesc** especifica en uno y el miembro **Quality** de **DXGI \_ SAMPLE \_ DESC** a cero porque no se admite el suavizado de contorno de varias muestras (MSAA).

Si usa [**DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) en Windows sistema operativo 7 o versiones anteriores, se produce un error en la creación del dispositivo. Al usar el modelo de volteo, puede usar estadísticas de presentación de pantalla completa en modo de ventana. El comportamiento de pantalla completa no se ve afectado. Si pasa **NULL** al parámetro *pFullscreenDesc* de [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) para una cadena de intercambio en ventanas y establece **SwapEffect** en **DXGI SWAP EFFECT FLIP \_ \_ \_ \_ SEQUENTIAL**, el tiempo de ejecución crea un búfer de reserva adicional y gira el controlador que pertenezca al búfer que se convierta en el búfer front-time en tiempo de presentación.

Cuando use el modelo de volteo, tenga en cuenta estas sugerencias:

-   Use una cadena de intercambio de modelos de volteo [**por HWND.**](../winprog/windows-data-types.md) No dirigir varias cadenas de intercambio de modelos de volteo al mismo **HWND.**
-   No use la cadena de intercambio de modelos de volteo con las funciones [**ScrollWindow**](/windows/win32/api/winuser/nf-winuser-scrollwindow) o [**ScrollWindowEx de**](/windows/win32/api/winuser/nf-winuser-scrollwindowex) GDI. Algunas aplicaciones de Direct3D usan las funciones **ScrollWindow** y **ScrollWindowEx** de GDI para actualizar el contenido de la ventana después de que se produzca un evento de desplazamiento del usuario. **ScrollWindow** y **ScrollWindowEx** realizan bitblts de contenido de la ventana en pantalla a medida que el usuario se desplaza por una ventana. Estas funciones también requieren actualizaciones del modelo bitblt para el contenido de GDI y Direct3D. Las aplicaciones que usan cualquiera de las funciones no mostrarán necesariamente el contenido visible de la ventana que se desplaza en pantalla cuando la aplicación está en modo de ventana. Se recomienda no usar las funciones **ScrollWindow** y **ScrollWindowEx** de GDI y, en su lugar, volver a dibujar el contenido de GDI y Direct3D en la pantalla en respuesta al desplazamiento.
-   Use el modelo de volteo en [**un HWND**](../winprog/windows-data-types.md) que no sea el destino de otras API, incluido el modelo de presentación de bitblt DXGI, otras versiones de Direct3D o GDI. Dado que el modelo bitblt mantiene una copia adicional de la superficie, puede agregar GDI y otros contenidos de Direct3D al mismo **HWND** mediante actualizaciones por fragmentos de Direct3D y GDI. Cuando se usa el modelo de volteo, solo se puede ver el contenido de Direct3D en las cadenas de intercambio del modelo de volteo que el tiempo de ejecución pasa a DWM. El tiempo de ejecución omite todas las demás actualizaciones de contenido direct3D o GDI del modelo bitblt.

## <a name="frame-synchronization-of-dxgi-flip-model-apps"></a>Sincronización de fotogramas de aplicaciones de modelo de volteo DXGI

Las estadísticas presentes son información de tiempo de fotogramas que las aplicaciones multimedia usan para sincronizar secuencias de vídeo y audio y recuperarse de problemas de reproducción de vídeo. Las aplicaciones pueden usar la información de tiempo de fotogramas en las estadísticas actuales para ajustar la velocidad de presentación de sus fotogramas de vídeo para una presentación más fluida. Para obtener información de estadísticas actual, llame al método [**IDXGISwapChain::GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) para obtener la [**estructura \_ DXGI FRAME \_ STATISTICS.**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) **DXGI \_ FRAME \_ STATISTICS** contiene estadísticas sobre [**las llamadas IDXGISwapChain1::P resent1.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) Una cadena de intercambio de modelos de volteo proporciona información de estadísticas presente en los modos de ventana y de pantalla completa. Para las cadenas de intercambio de modelos bitblt en modo de ventana, todos los **valores de DXGI \_ FRAME \_ STATISTICS** son ceros.

Para las estadísticas presentes del modelo de volteo, [**IDXGISwapChain::GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) devuelve **DXGI \_ ERROR FRAME \_ \_ STATISTICS \_ DISJOINT** en estas situaciones:

-   Primera llamada a [**GetFrameStatistics,**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics)que indica el principio de una secuencia
-   Cambio de modo: modo con ventanas hacia o desde pantalla completa o de pantalla completa a transiciones de pantalla completa

Los valores de **los miembros PresentRefreshCount**, **SyncRefreshCount** y **SyncQPCTime** de [**DXGI FRAME \_ \_ STATISTICS**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) tienen las siguientes características:

-   **PresentRefreshCount** es igual a **SyncRefreshCount** cuando la aplicación se presenta en cada vsync.
-   **SyncRefreshCount** se obtiene en el intervalo de vsync cuando se envió el presente, **SyncQPCTime** es aproximadamente el tiempo asociado al intervalo de vsync.

El método [**IDXGISwapChain::GetLastPresentCount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount) devuelve el último recuento actual, es decir, el identificador actual de la última llamada [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) realizada por un dispositivo de visualización asociado a la cadena de intercambio. Este identificador actual es el valor del **miembro PresentCount** de la [**estructura \_ DXGI FRAME \_ STATISTICS.**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) Para las cadenas de intercambio de modelos bitblt, mientras que en modo de ventana, todos los **valores de DXGI \_ FRAME \_ STATISTICS** son ceros.

## <a name="avoiding-detecting-and-recovering-from-glitches"></a>Evitar, detectar y recuperarse de problemas

Realice estos pasos para evitar, detectar y recuperarse de problemas en la presentación de fotogramas:

1.  Poner [**en cola llamadas IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) (es decir, llamar a **IDXGISwapChain1::P resent1** varias veces, lo que hace que se recopile en una cola).
2.  Cree una estructura present-queue para almacenar todos los valores [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)(devueltos por [**IDXGISwapChain::GetLastPresentCount)**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount)y los valores **presentRefreshCount** asociados, calculados o esperados.
3.  Para detectar un problema:

    -   Llame [**a IDXGISwapChain::GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics).
    -   Para este marco, obtenga el identificador actual (**PresentCount**) y el recuento de vsync donde el sistema operativo presentó la última imagen al monitor (**PresentRefreshCount**).
    -   Recupere el **presentRefreshCount esperado** que está asociado al identificador actual y que ha almacenado previamente en la estructura present-queue.
    -   Si el **valor de PresentRefreshCount real** es posterior al **presentRefreshCount** esperado, se ha producido un problema.

4.  Para recuperarse del problema:

    -   Calcule el número de fotogramas que se omitirán para recuperarse del problema. Por ejemplo, si el paso 3 revela que el recuento de vsync esperado (**PresentRefreshCount**) para un identificador actual (**PresentCount**) es 5 y el recuento de vsync real para el identificador actual es 8, el número de fotogramas que se omitirán para recuperarse del problema es de 3 fotogramas.
    -   Pase 0 al parámetro *SyncInterval* en este número de llamadas a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) para descartar y omitir este número de fotogramas.

        > [!Note]  
        > Si el problema consta de un gran número de fotogramas, llame a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) con el parámetro *Flags* establecido en [**DXGI \_ PRESENT \_ RESTART**](dxgi-present.md) para descartar y omitir todos los presentaciones en cola pendientes.

         

Este es un escenario de ejemplo de recuperación de problemas en la presentación de fotogramas:

![ilustración de un escenario de ejemplo de recuperación de problemas en la presentación de fotogramas](images/frame-sync-glitch-recover.png)

En el escenario de ejemplo, espera que el fotograma A se vaya a la pantalla con un recuento de vsync de 1. Pero realmente se detecta el recuento de vsync que el fotograma A aparece en pantalla como 4. Por lo tanto, se determina que se produjo un problema. A continuación, puede descartar 3 fotogramas, es decir, puede pasar 0 al parámetro *SyncInterval* en 3 llamadas a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). En el escenario de ejemplo anterior, para recuperarse del problema, necesita un total de 8 llamadas **IDXGISwapChain1::P resent1.** Después, el no.9 fotograma es visible según el recuento de vsync que se espera.

Esta es una línea de tiempo de eventos de presentación. Cada línea vertical representa una vsync. La dirección horizontal es el tiempo, que aumenta a la derecha. Puede usar la ilustración para imaginar cómo pueden producirse problemas.

![ilustración de una línea de tiempo de eventos de presentaciónl](images/present-timeline.png)

En la ilustración se muestra esta secuencia:

1.  La aplicación se reactiva en vsync, se representa en azul, llama a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)y, a continuación, vuelve a suspensión.
2.  La unidad de procesamiento gráfico (GPU) se reactiva de inactividad, realiza la representación en azul y, a continuación, vuelve a suspensión.
3.  DwM se reactiva en la siguiente instancia de vsync, se compone de azul en su búfer de reserva, llama a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)y, a continuación, vuelve a suspensión.
4.  La aplicación se reactiva, se representa en verde, llama a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)y, a continuación, vuelve a suspensión.
    > [!Note]  
    > La aplicación se ejecuta simultáneamente mientras la GPU realiza la composición de azul.

     

5.  A continuación, la GPU se representa en verde para la aplicación.
6.  Por último, el convertidor digital a análogo (DAC) muestra los resultados de la composición de DWM en el monitor en la siguiente vsync.

Desde la línea de tiempo, puede imaginar la latencia de las estadísticas actuales y cómo se pueden producir problemas. Por ejemplo, para mostrar un problema de DWM para el color verde que aparece en la pantalla, imagine ampliar el cuadro verde/rojo para que el lado derecho del cuadro verde/rojo coincida con el lado derecho del cuadro púrpura/rojo. En este escenario, la DAC muestra dos fotogramas de azul y, a continuación, el marco verde. Puede ver que este problema se produjo al leer las estadísticas actuales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejora de la presentación con el modelo de volteo, rectángulos sucios y áreas desplazadas](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
