---
description: Windows 8 agrega compatibilidad con Flip Presentation Model y sus estadísticas presentes asociadas en DXGI 1,2.
ms.assetid: E132DAF5-80B7-4C52-A760-3779CC140CE7
title: Modelo de volteo de DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ee82febd13a3b57a06d93fd01eb8d230d6b78a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906660"
---
# <a name="dxgi-flip-model"></a>Modelo de volteo de DXGI

Windows 8 agrega compatibilidad con Flip Presentation Model y sus estadísticas presentes asociadas en DXGI 1,2. El modelo de presentación de Windows 8 DXGI Flip es similar a la [presentación del modo Flip de Direct3D 9EX](../direct3darticles/direct3d-9ex-improvements.md)de Windows 7. Las aplicaciones de presentación basadas en la velocidad de fotogramas y de vídeo, como los juegos, pueden beneficiarse de la mayoría mediante Flip Presentation Model. Las aplicaciones que usan el modelo de presentación de DXGI Flip reducen la carga de recursos del sistema y aumentan el rendimiento. Las aplicaciones también pueden usar mejoras de estadísticas presentes con Flip Presentation Model para controlar mejor la velocidad de presentación al proporcionar mecanismos de corrección y comentarios en tiempo real.

-   [Comparación del modelo de volteo de DXGI y el modelo de BitBlt](#comparing-the-dxgi-flip-model-and-the-bitblt-model)
-   [Cómo usar DXGI Flip Model](#how-to-use-dxgi-flip-model)
-   [Sincronización de fotogramas de las aplicaciones de DXGI Flip Model](#frame-synchronization-of-dxgi-flip-model-apps)
-   [Prevención, detección y recuperación de problemas](#avoiding-detecting-and-recovering-from-glitches)
-   [Temas relacionados](#related-topics)

## <a name="comparing-the-dxgi-flip-model-and-the-bitblt-model"></a>Comparación del modelo de volteo de DXGI y el modelo de BitBlt

El motor en tiempo de ejecución usa la transferencia de bloque de bits (bitblt) y los modelos de presentación de flip para presentar el contenido de los gráficos en monitores de pantalla. La diferencia más grande entre los modelos de presentación bitblt y de volteo es cómo el contenido del búfer de reserva se obtiene en el DWM de Windows 8 para su composición. En el modelo bitblt, el contenido del búfer de reserva se copia en la superficie de redirección en cada llamada a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). En el modelo Flip, todos los búferes de reserva se comparten con el Administrador de ventanas de escritorio (DWM). Por lo tanto, el DWM puede componerse directamente desde los búferes de reserva sin ninguna operación de copia adicional. En general, el modelo de volteo es más eficaz. El modelo Flip también proporciona más características, como estadísticas presentes mejoradas.

Si tiene componentes heredados que usan Windows Interfaz de dispositivo gráfico (GDI) para escribir directamente en un [**hWnd**](../winprog/windows-data-types.md) , use el modelo BitBlt.

Las mejoras de rendimiento de DXGI Flip Model son significativas cuando la aplicación está en modo de ventana. La secuencia de esta tabla y la ilustración comparan los usos de ancho de banda de memoria y las lecturas y escrituras del sistema de aplicaciones en ventanas que eligen Flip Model frente al modelo BitBlt.



| Paso | Modelo BitBlt presente en DWM                                                                               | Modelo de volteo de DXGI presente en DWM                                   |
|------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 1.   | La aplicación actualiza su marco (escritura)<br/>                                                              | La aplicación actualiza su marco (escritura)<br/>                     |
| 2.   | El tiempo de ejecución de Direct3D copia el contenido de la superficie en una superficie de redirección de DWM (lectura, escritura)<br/>            | El tiempo de ejecución de Direct3D pasa la superficie de la aplicación a DWM<br/>        |
| 3.   | Una vez completada la copia de la superficie compartida, DWM representa la superficie de la aplicación en la pantalla (lectura, escritura)<br/> | DWM representa la superficie de la aplicación en la pantalla (lectura, escritura)<br/> |



 

![Ilustración de una comparación del modelo BLT y el modelo Flip](images/blt-flip-mode-present.png)

Flip Model reduce el uso de memoria del sistema al reducir el número de lecturas y escrituras realizadas por el tiempo de ejecución de Direct3D para la composición de marcos en ventanas mediante DWM.

## <a name="how-to-use-dxgi-flip-model"></a>Cómo usar DXGI Flip Model

Las aplicaciones de Direct3D 11,1 que tienen como destino Windows 8 usan Flip Model mediante la creación de la cadena de intercambio con el valor de la enumeración [**\_ \_ \_ \_ secuencial Flip del efecto de intercambio de dxgi**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) establecido en el miembro **SwapEffect** de la estructura DESC1 de la [**\_ cadena de intercambio de \_ \_ dxgi**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) . Cuando establezca **SwapEffect** en el **efecto de intercambio de dxgi \_ \_ \_ Flip \_ Sequential**, establezca también estos miembros de la **cadena de intercambio de dxgi \_ \_ \_ DESC1** en los valores indicados:

-   **BufferCount** en un valor entre 2 y 16 para evitar una reducción del rendimiento como resultado de esperar a que DWM libere el búfer de presentación anterior.
-   **Dar formato** al formato de dxgi \_ \_ R16G16B16A16 \_ float, formato de dxgi \_ \_ B8G8R8A8 \_ UNORM o formato de dxgi \_ \_ R8G8B8A8 \_ UNORM
-   **Miembro Count** de la [**estructura \_ \_ DESC de ejemplo de dxgi**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc) que el miembro **SampleDesc** especifica a uno y el miembro **Quality** de **dxgi \_ Sample \_ DESC** en cero porque no se admite el suavizado de contorno de muestra múltiple (MSAA)

Si usa el [**efecto de intercambio de DXGI \_ \_ \_ Flip \_ Sequential**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) en Windows 7 o en un sistema operativo anterior, se produce un error en la creación del dispositivo. Cuando se usa Flip Model, se pueden usar las estadísticas presentes en modo de pantalla completa en modo de ventana. El comportamiento de la pantalla completa no se ve afectado. Si se pasa un **valor null** al parámetro *pFullscreenDesc* de [**IDXGIFactory2:: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) para una cadena de intercambio en ventana y se establece **SwapEffect** en el **efecto de intercambio de DXGI, \_ \_ \_ Flip \_ Sequential**, el tiempo de ejecución crea un búfer de reserva adicional y gira el identificador que pertenece al búfer que se convierte en el búfer frontal en el momento de la presentación.

Al usar Flip Model, tenga en cuenta estas sugerencias:

-   Use una cadena de intercambio de modelo de volteo por [**hWnd**](../winprog/windows-data-types.md). No tener como destino varias cadenas de intercambio de modelo de volteo en el mismo **hWnd**.
-   No use la cadena de intercambio de volteo del modelo con la función [**ScrollWindow**](/windows/win32/api/winuser/nf-winuser-scrollwindow) o [**ScrollWindowEx**](/windows/win32/api/winuser/nf-winuser-scrollwindowex) de GDI. Algunas aplicaciones de Direct3D usan las funciones **ScrollWindow** y **ScrollWindowEx** de GDI para actualizar el contenido de la ventana después de que se produzca un evento de desplazamiento del usuario. **ScrollWindow** y **ScrollWindowEx** realizan bitblts de contenido de la ventana en la pantalla cuando el usuario desplaza una ventana. Estas funciones también requieren actualizaciones del modelo bitblt para el contenido de GDI y de Direct3D. Las aplicaciones que usan cualquiera de las funciones no mostrarán necesariamente el desplazamiento del contenido de la ventana visible en la pantalla cuando la aplicación esté en modo de ventana. Se recomienda que no utilice las funciones **ScrollWindow** y **ScrollWindowEx** de GDI y que, en su lugar, vuelva a dibujar el contenido de GDI y Direct3D en la pantalla en respuesta al desplazamiento.
-   Use Flip Model en un [**hWnd**](../winprog/windows-data-types.md) que tampoco sea el destino de otras API, incluido el modelo de presentación de de DXGI bitblt, otras versiones de Direct3D o GDI. Dado que el modelo bitblt mantiene una copia adicional de la superficie, puede Agregar GDI y otro contenido de Direct3D al mismo **hWnd** a través de actualizaciones por etapas de Direct3D y GDI. Cuando se usa el modelo Flip, solo se puede ver el contenido de Direct3D en las cadenas de intercambio del modelo Flip que el tiempo de ejecución pasa a DWM. El tiempo de ejecución omite todas las demás actualizaciones de contenido de Direct3D o GDI del modelo BitBlt.

## <a name="frame-synchronization-of-dxgi-flip-model-apps"></a>Sincronización de fotogramas de las aplicaciones de DXGI Flip Model

Las estadísticas presentes son información de temporización de fotogramas que usan las aplicaciones multimedia para sincronizar secuencias de audio y vídeo y recuperarse de problemas de reproducción de vídeo. Las aplicaciones pueden usar la información de temporización de fotogramas en estadísticas presentes para ajustar la velocidad de presentación de los fotogramas de vídeo para una presentación más fluida. Para obtener información de estadísticas presentes, llame al método [**IDXGISwapChain:: GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) para obtener la estructura de [**\_ \_ estadísticas de fotogramas de DXGI**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) . **DXGI \_ \_Estadísticas de FOTOgramas** contiene estadísticas sobre [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) llamadas. Una cadena de intercambio de volteo del modelo proporciona información de estadísticas presentes en los modos de pantalla completa y de ventana. En el caso de las cadenas de intercambio del modelo bitblt en modo de ventana, todos los valores de las **\_ \_ estadísticas de fotogramas de DXGI** son ceros.

En el caso de las estadísticas de Flip Model Present, [**IDXGISwapChain:: GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) devuelve las **\_ \_ estadísticas de fotogramas de \_ \_ errores de DXGI** en estas situaciones:

-   Primera llamada a [**GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics), que indica el principio de una secuencia
-   Cambio de modo: modo de ventana a o desde pantalla completa o pantalla completa hasta transiciones de pantalla completa

Los valores de los miembros **PresentRefreshCount**, **SyncRefreshCount** y **SyncQPCTime** de [**las \_ \_ estadísticas de fotogramas de DXGI**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) tienen las siguientes características:

-   **PresentRefreshCount** es igual a **SyncRefreshCount** cuando la aplicación se presenta en cada VSYNC.
-   **SyncRefreshCount** se obtiene en el intervalo de VSYNC cuando se envió el presente, **SyncQPCTime** es aproximadamente el tiempo asociado con el intervalo de VSYNC.

El método [**IDXGISwapChain:: GetLastPresentCount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount) devuelve el último recuento presente, es decir, el identificador actual de la última llamada correcta [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) realizada por un dispositivo de pantalla que está asociado a la cadena de intercambio. Este identificador actual es el valor del miembro **PresentCount** de la estructura [**de \_ \_ estadísticas de fotogramas de DXGI**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) . En el caso de las cadenas de intercambio del modelo bitblt, mientras que en el modo de ventana, todos los valores de las **\_ \_ estadísticas de fotogramas de DXGI** son ceros.

## <a name="avoiding-detecting-and-recovering-from-glitches"></a>Prevención, detección y recuperación de problemas

Siga estos pasos para evitar, detectar y recuperarse de los problemas en la presentación de fotogramas:

1.  Queue [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) llama a (es decir, llamar a **IDXGISwapChain1::P resent1** varias veces, lo que hace que se recopilen en una cola).
2.  Cree una estructura present-Queue para almacenar todas las IDXGISwapChain1 enviadas correctamente [**:P:**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)el identificador actual de resent1 (devuelto por [**IDXGISwapChain:: GetLastPresentCount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount)) y los valores de **PresentRefreshCount** asociados, calculados o esperados.
3.  Para detectar un problema:

    -   Llame a [**IDXGISwapChain:: GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics).
    -   Para este marco, obtenga el identificador actual (**PresentCount**) y el recuento de VSYNC en el que el sistema operativo presentó la última imagen al monitor (**PresentRefreshCount**).
    -   Recupere el **PresentRefreshCount** esperado que está asociado al identificador actual y que almacenó anteriormente en la estructura present-Queue.
    -   Si el **PresentRefreshCount** real es posterior al **PresentRefreshCount** esperado, se ha producido un problema.

4.  Para recuperarse del problema:

    -   Calcule el número de fotogramas que se van a omitir para recuperarse del problema. Por ejemplo, si el paso 3 revela que el número de VSYNC esperado (**PresentRefreshCount**) para un identificador presente (**PresentCount**) es 5 y el número real de VSYNC para el ID. actual es 8, el número de fotogramas que se omitirá para recuperarse del problema es de 3 fotogramas.
    -   Pase 0 al parámetro *SyncInterval* en este número de llamadas a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) para descartar y omitir este número de Marcos.

        > [!Note]  
        > Si el problema consta de un gran número de fotogramas, llame a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) con el parámetro *Flags* establecido en [**DXGI \_ present \_ restart**](dxgi-present.md) para descartar y omitir todas las presentaciones en cola pendientes.

         

Este es un escenario de ejemplo de recuperación de problemas en la presentación de fotogramas:

![Ilustración de un escenario de ejemplo de recuperación de problemas en la presentación de fotogramas](images/frame-sync-glitch-recover.png)

En el escenario de ejemplo, se espera que el marco a vaya a la pantalla en un recuento de VSYNC de 1. Pero realmente detecta el número de VSYNC que el marco A aparece en la pantalla como 4. Por lo tanto, determinará que se ha producido un problema. Después, puede descartar 3 fotogramas, es decir, puede pasar 0 al parámetro *SyncInterval* en 3 llamadas a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). En el escenario de ejemplo anterior, para recuperarse del problema, necesita un total de 8 **IDXGISwapChain1::P resent1** llamadas. El fotograma noveno es visible según el recuento de VSYNC que espera.

Esta es una línea de tiempo de eventos de presentación. Cada línea vertical representa una VSYNC. La dirección horizontal es la hora, que aumenta a la derecha. Puede usar la figura para imaginar cómo se pueden producir los problemas.

![Ilustración de una línea de tiempo de eventos de presentación](images/present-timeline.png)

En la ilustración se muestra esta secuencia:

1.  La aplicación se activa en VSYNC, se representa en azul, llama a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)y, a continuación, vuelve a entrar en suspensión.
2.  La unidad de procesamiento de gráficos (GPU) se activa desde el estado inactivo, realiza la representación en azul y, a continuación, vuelve a entrar en suspensión.
3.  El DWM se activa en la siguiente VSYNC, se compone de azul en su búfer de reserva, llama a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)y, a continuación, vuelve a entrar en suspensión.
4.  La aplicación se activa, se representa en verde, llama a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)y, a continuación, vuelve a entrar en suspensión.
    > [!Note]  
    > La aplicación se ejecuta simultáneamente mientras la GPU realiza la redacción de azul.

     

5.  A continuación, la GPU se representa en verde para la aplicación.
6.  Por último, el convertidor digital a analógico (DAC) muestra los resultados de la composición DWM en el monitor en la siguiente VSYNC.

Desde la línea de tiempo, puede imaginarse la latencia de las estadísticas presentes y cómo se pueden producir los problemas. Por ejemplo, para mostrar un problema de DWM para el color verde que aparece en la pantalla, Imagine que amplía el cuadro verde/rojo para que el lado derecho del cuadro verde/rojo coincida con el lado derecho del cuadro púrpura/rojo. En este escenario, la DAC muestra dos fotogramas de azul y luego el marco verde. Puede ver que este problema se produjo al leer estadísticas actuales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejorar la presentación con el modelo de volteo, los rectángulos modificados y las áreas desplazadas](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
