---
title: Reloj compositor
description: La API de reloj compositor ofrece estadísticas y control de velocidad de fotogramas para presentar contenido en pantalla sin problemas, con la cadencia más rápida posible y en una variedad de configuraciones de hardware.
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 211684d8e199c61ec76fad6dbad168088056473a
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128524026"
---
# <a name="compositor-clock"></a>Reloj compositor

> [!NOTE]
> **Parte de la información hace referencia al producto de versión preliminar, el cual puede sufrir importantes modificaciones antes de que se publique la versión comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.**

## <a name="overview"></a>Información general

La API de reloj compositor ofrece estadísticas y control de velocidad de fotogramas para presentar contenido en pantalla sin problemas, con la cadencia más rápida posible y en una variedad de configuraciones de hardware. Tradicionalmente, esto se ha manipulado mediante las API de DirectX. Sin embargo, estos tienen vínculos fuertes con la frecuencia de actualización fija y las configuraciones de pantalla única. Por ejemplo, este es un fragmento simplificado de pseudocódigo que muestra cómo se suelen crear aplicaciones para dibujar a la velocidad de actualización de pantalla.

```cpp
void GameLoop()
{
    CreateRenderingObjects();
    auto pSwapChain = CreateSwapChain();

    while (pSwapChain->WaitForVerticalBlank())
    {
        ProcessInput();
        RenderFrame(pSwapChain);
        pSwapChain->Present();
    }
}
```

En este tipo de bucle, la suposición es que hay una única cadencia vertical en blanco (vblank). No está claro lo que debe hacer la aplicación si su ventana está desfilando a dos monitores cuyo examen está fuera de fase o que tienen frecuencias diferentes por completo. De hecho, la API de cadena de intercambio DXGI siempre usa la cadencia del monitor principal, independientemente de la ventana en la que se muestre la aplicación. Esto provoca problemas para las aplicaciones que desean una presentación sin problemas en todos los monitores. Un ejemplo real es la reproducción de vídeo en un monitor secundario que tiene una actualización diferente a la principal. un escenario que existe desde que se introdujeron varios monitores. y afecta de forma desproporcionada a los jugadores, que tienden a tener un monitor de 60Hz para la interfaz de usuario secundaria y un monitor de frecuencia mucho mayor (144 +Hz) para juegos.

El segundo problema común es el ajuste de la velocidad de fotogramas en función del rendimiento de la máquina. Esto es habitual para las aplicaciones de reproducción de vídeo, que quieren saber si el usuario está observando los fotogramas de vídeo en el momento esperado o si los problemas están haciendo que la presentación sea desigual, con la esperanza de ajustar la presentación para mejorar el rendimiento. Por ejemplo, un servicio de streaming de vídeo podría cambiar a una secuencia de menor calidad si la máquina no es capaz de mantener la velocidad de fotogramas deseada con la máxima calidad. Esto también se controla mediante las API de DXGI y, por lo tanto, se ve afectado por la misma limitación de exposición de la arquitectura y la API.

Por último, la API ofrece a las aplicaciones la oportunidad de participar en una nueva característica de potenciación de velocidad de fotogramas denominada Frecuencia de actualización dinámica, en la que el sistema se ejecuta a una velocidad de actualización relativamente baja para las operaciones normales, por ejemplo, 60Hz, pero se acelera hasta una frecuencia mayor, por &mdash; &mdash; &mdash; ejemplo, 120Hz cuando una aplicación realiza determinadas operaciones sensibles a la &mdash; latencia, como la entrada de lápiz,  o el movimiento panorámico táctil. La característica de aumento existe porque la ejecución con la alta frecuencia el 100 % del tiempo es prohibitiva desde el punto de vista del consumo de energía. Al mismo tiempo, debido a las mismas limitaciones de la API de DXGI, cambiar la frecuencia de actualización de la pantalla en momentos arbitrarios suele ser costoso, lo que implica notificaciones de cambio del modo de difusión a todas las aplicaciones y los costos de todas esas aplicaciones que ejecutan código para responder al cambio. Por lo tanto, la característica de aumento de frecuencia de actualización realiza un cambio de configuración ligero que no emite ninguna notificación, pero, por lo tanto, debe abstraerse de la mayoría de las aplicaciones, que siguen creyéndo que el sistema se ejecuta con la frecuencia más baja. Esta virtualización funciona mediante la emisión de aplicaciones solo entre las demás vblank, cada tres vblanks o cualquier otro intervalo entero, para que la aplicación vea una tasa de actualización efectiva que sea una fracción de entero de la frecuencia real. Esto permite que el mecanismo de vblank existente se utilice sin costo adicional para generar una frecuencia inferior perfectamente regular. El vblank alineado se representa mediante un modo de frecuencia de actualización dinámica en el sistema operativo (SO), como 60Hz/120Hz. Tenga en cuenta que, por lo tanto, la característica de aumento solo funciona para aumentar hasta una frecuencia superior, nunca a una menor, ya que no es igualmente barato insertar vblanks artificiales, ya que es omitir vblanks reales.

La API de reloj compositor permite que la aplicación no solo solicite que el sistema entre o deje el modo de aumento, sino que también observe la velocidad de actualización real cuando está en ese modo, para que pueda presentar contenido con la frecuencia más alta.

## <a name="the-api"></a>La API

La API tiene tres partes. La primera ofrece un latido independiente de la pantalla para las aplicaciones que desean presentarse a velocidad de fotogramas en varios monitores. El segundo permite a las aplicaciones solicitar un aumento de frecuencia con frecuencia de actualización dinámica. El tercero ofrece estadísticas sobre el comportamiento del motor de composición del sistema, separados por cada pantalla individual.

Cada parte de la API influye o observa el ciclo de trabajo del compositor del sistema. Este ciclo de trabajo es una cadencia regular que genera un fotograma compositor por ciclo. Ese ciclo puede o no estar alineado para mostrar vblanks, dependiendo de la carga de trabajo del sistema, el número de pantallas y otros factores.

## <a name="wait-for-the-compositor-clock"></a>Espera del reloj del compositor

El propósito de esta señal es reemplazar el uso del método [**IDXGIOutput::WaitForVBlank,**](/windows/win32/api/dxgi/nf-dxgi-idxgioutput-waitforvblank) a la vez que se proporciona una mayor flexibilidad en las distintas tasas de actualización y se simplifican los patrones de uso para los desarrolladores. Al igual que **con WaitForVBlank,** el sistema debe saber si una aplicación está esperando esta señal o no, de modo que cuando ninguna aplicación esté esperando, el sistema pueda dirigir la tarjeta de vídeo para desactivar la interrupción vertical en blanco. 

Esto es fundamental para la administración de energía, lo que restringe la arquitectura de la API para que sea una llamada de función de espera, en lugar de aceptar o devolver un evento (el sistema de gráficos no puede determinar si se está esperando o no). En este nivel bajo, se espera que las aplicaciones usen esta API para controlar los subprocesos de representación, independientes de los subprocesos de interfaz de usuario de uso general, de forma similar a como se usa **tradicionalmente IDXGIOutput::WaitForVBlank.**

Como se mencionó en la información general, hay varios aspectos que el reloj compositor puede dar cabida para **que WaitForVBlank** no pueda.

* Siguiente espacio en blanco vertical cuando el reloj del compositor no tiene necesariamente el origen de la pantalla principal.
* Activar aplicaciones a velocidades variables en las pantallas que admiten la tasa de actualización dinámica.
* Activar aplicaciones para eventos definidos por la aplicación.

En general, se espera que muchas aplicaciones permanezcan sincronizadas con el reloj del compositor para mejorar el tiempo de sus fotogramas. pero algunas excepciones pueden incluir marcos multimedia y juegos que necesitan reactivar en el espacio en blanco vertical de una pantalla específica.

### <a name="handle-usage-with-compositor-clock"></a>Control del uso con el reloj compositor

Actualmente, las aplicaciones se reactivan en cada espacio en blanco vertical mediante el mecanismo de DXGI, pero a menudo tienen otros eventos para los que también necesitan reactivar. En lugar de controlar estos eventos por separado, el reloj del compositor puede tomar identificadores para varios eventos y señalar en el siguiente fotograma y cada vez que se activa el evento. A continuación, la aplicación puede reactivarse a partir de una señal, conociendo el evento que hizo que se reactivase.

### <a name="cycle-for-compositor-clock-events"></a>Ciclo para eventos de reloj compositor

El reloj del compositor siempre se reactivará en el espacio en blanco vertical de un monitor o en otro temporizador. Cuando el compositor está en estado de inmoción, pero la pantalla todavía se está actualizando, esta señal se seguirá desencadenando en el vblank de la pantalla principal.

### <a name="c-example"></a>Ejemplo de C++

```cpp
void GameLoop(HANDLE hQuitGameEvent)
{
    DWORD waitResult;

    CreateRenderingObjects();
    auto pSwapChain = CreateSwapChain();

    do
    {
        // Do all of the work for a single frame
        ProcessInput();
        RenderFrame(pSwapChain);
        pSwapChain->Present();

        // Wait for the compositor heartbeat before starting a new frame
        waitResult = DCompositionWaitForCompositorClock(1, &hQuitGameEvent, INFINITE);

        // If we get WAIT_RESULT_0+count it means the compositor clock ticked,
        // and we should render another frame. Our count is one, as we're
        // passing only one extra handle. Otherwise, either we got a failure or
        // another thread signaled our "quit" event, and in either case we want
        // to exit the loop
    } while (waitResult == WAIT_OBJECT_0 + 1);
}
```

## <a name="boost-compositor-clock"></a>Aumento del reloj del compositor

Cuando el origen del reloj del compositor admite la frecuencia de actualización dinámica (esa característica está activada en la configuración de pantalla avanzada; solo se puede usar en las pantallas de frecuencia de actualización variable con controladores de soporte técnico), el sistema podrá cambiar dinámicamente entre dos velocidades. Hay un modo sin descomponer, que normalmente será de 60Hz, y una velocidad aumentada que normalmente es 2 veces mayor a 120Hz. Esta frecuencia de actualización más alta debe usarse para mejorar el contenido sensible a la latencia, como la entrada de entrada digital. En el diagrama siguiente se muestra cómo cambia el sistema entre ejecutarse a una velocidad base de 60Hz (volteo 1) y, después, para 6 fotogramas (2-7) con la entrada de lápiz digital a 120Hz. Por último, una vez que la entrada de lápiz digital ya no se actualiza, el sistema vuelve a un modo de 60Hz.

Esta es una ilustración de la velocidad de fotogramas dinámica para la potenciación.

![frecuencia de actualización aumentada al volt2; inking ends by flip8,and rate returns to 60Hz (inking ends by flip8) and rate returns to 60Hz (inking ends by flip8) and rate returns to 60Hz](images/dyn-refresh-rate.png)

Y este es el modo en que DWM controla las solicitudes de aumento.

![diagrama de flujo que muestra cómo DWM controla las solicitudes de aumento](images/dwm-boosting.png)

Si se finaliza una aplicación que solicita un aumento, también se finalizarán las solicitudes de aumento de la aplicación. Las aplicaciones que todavía están activas con varias solicitudes de aumento pueden comprobar el recuento de referencias para determinar cuántas veces se debe deshacer. La potenciación de llamadas es totalmente compatible, incluso si el sistema no está en modo de frecuencia de actualización dinámica, donde el multiplicador de potenciación sería 1x.

### <a name="c-example"></a>Ejemplo de C++

Este ejemplo procesa **WM_TOUCH** aumentar la frecuencia de actualización cada vez que esta aplicación recibe entrada táctil, con la intención de proporcionar una experiencia de desplazamiento táctil más fluida y de alta frecuencia. Una aplicación más sofisticada podría realizar primero el reconocimiento de gestos y aumentar solo si se detecta una panorámica.

```cpp
int g_activeTouchPoints = 0;

LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;
    UINT inputCount = LOWORD(wParam);
    auto hTouchInput = reinterpret_cast<HTOUCHINPUT>(lParam);

    // Allocate room for touch data (assume throwing new)
    auto pInputs = new TOUCHINPUT[inputCount];

    if (GetTouchInputInfo(hTouchInput, inputCount, pInputs, sizeof(TOUCHINPUT)))
    {
        for (int index = 0; index < inputCount; index++)
        {
            auto& touchInput = pInputs[index];

            // The first time we receive a touch down, boost the compositor
            // clock so we do our stuff at high frequency. Once the last touch
            // up happens, return to the base frequency
            if (touchInput.dwFlags & TOUCHEVENTF_DOWN)
            {
                if (!g_activeTouchPoints)
                {
                    // We're going from zero to one active points -- boost 
                    DCompositionBoostCompositorClock(true);
                }

                g_activeTouchPoints++;
            }
            else if (touchInput.dwFlags && TOUCHEVENTWF_UP)
            {
                g_activeTouchPoints--;

                if (g_activeTouchPoints == 0)
                {
                    DCompositionBoostCompositorClock(false);
                }
            }

            // Perform other normal touch processing here...
        }

        // We handled the window message; close the handle
        CloseTouchInputHandle(hTouchInput);
    }
    else
    {
        // We couldn't handle the message; forward it to the system
        result = DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
    }

    delete[] pInputs;
    return result;
}
```

## <a name="frame-statistics"></a>Estadísticas de fotogramas

> [!NOTE]
> Esperamos que las aplicaciones usen la característica de estadísticas de fotogramas principalmente para la telemetría, no para ajustar el contenido.

Windows aplicaciones suelen enviar contenido al compositor que se muestra en una variedad de ubicaciones entre adaptadores de pantalla y pantallas. No siempre se representa en una pantalla, por lo que en esta API usamos [*destinos*](#glossary). En lugar de depender de una sola estadística que se represente cuando un fotograma llega a la pantalla, [**DCompositionGetTargetStatistics**](/windows/win32/api/dcomp/nf-dcomp-dcompositiongettargetstatistics) ofrece estadísticas de fotogramas para cada fotograma compositor a medida que llega a cada destino. El compositor funciona de forma periódica, lo que puede producirse en un vblank o no. Esto significa que si una pantalla está duplicada o se muestra un contenido en varios lugares, la aplicación, el marco o la telemetría pueden tener en cuenta todo esto. Sin embargo, estos fotogramas compositor proporcionarán información incompleta sobre los fotogramas que no están compuestos, como *en iflip* (volteo independiente) en una cadena de intercambio.

Como ejemplo de uso, la nueva infraestructura de Media Foundation basada en la cadena de intercambio de composición se basa en [**DCompositionGetStatistics**](/windows/win32/api/dcomp/nf-dcomp-dcompositiongetstatistics) y [**DCompositionGetTargetStatistics**](/windows/win32/api/dcomp/nf-dcomp-dcompositiongettargetstatistics) para realizar determinaciones de la calidad de la presentación compuesta a través de la telemetría. Además de esta API, llamarán a una API independiente cuando sus fotogramas están en iflip y no van al compositor.

Para determinados usos, esperamos que las aplicaciones usen [**IDCompositionDevice::GetFrameStatistics**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-getframestatistics) para recibir una estimación de cuándo llegará el siguiente fotograma del compositor comprobando [**DCOMPOSITION_FRAME_STATISTICS::nextEstimatedFrameTime**](/windows/win32/api/dcomptypes/ns-dcomptypes-dcomposition_frame_statistics).

En primer lugar, la aplicación consultará el último fotograma relacionado con el estado de la presentación del marco a través de frases diferentes. La aplicación tendrá un *frameId* existente proporcionado por la cadena de intercambio de composición, o interfaces futuras sobre las que  desea obtener información, o bien puede llamar a [**DCompositionGetFrameId**](/windows/win32/api/dcomp/nf-dcomp-dcompositiongetframeid) para recuperar el COMPOSITION_FRAME_ID más reciente de la clase [**COMPOSITION_FRAME_ID_TYPE**](/windows/win32/api/dcomptypes/ne-dcomptypes-composition_frame_id_type).

* **COMPOSITION_FRAME_ID_CREATED**. Compositor ha empezado a trabajar en el marco.
* **COMPOSITION_FRAME_ID_CONFIRMED**. El identificador de fotograma en el que se completa el trabajo de CPU y se han realizado los presentes.
* **COMPOSITION_FRAME_ID_COMPLETED**. El trabajo de GPU se completa para todos los destinos asociados a un fotograma.

> [!NOTE]
> **COMPOSITION_Frame_ID** está aumentando de forma monótona; por lo que los fotogramas de compositor anteriores se pueden inferir de él.

A continuación, la aplicación consultará información básica sobre el marco de composición y una lista de *targetId* que forman parte del marco, llamando a [**DCompositionGetStatistics**](/windows/win32/api/dcomp/nf-dcomp-dcompositiongetstatistics). Por último, si la aplicación requiere información por destino, usará [**DCompositionGetTargetStatistics**](/windows/win32/api/dcomp/nf-dcomp-dcompositiongettargetstatistics) para recuperar la información de los valores frameId y targetId especificados.

### <a name="c-example"></a>Ejemplo de C++

En el ejemplo siguiente se muestra una colección gradual de estadísticas de fotogramas de la API, que luego se resumen en la función **TargetFrameRate** para deducir cuál fue la velocidad de fotogramas en un conjunto de fotogramas. De nuevo, este tipo de código se espera en telemetría o en marcos, en lugar de en una aplicación.

```cpp
class FrameStatisticsCollector
{
private:
    // Collect at most 4 target monitors
    static constexpr UINT sc_maxTargetCount = 4;

    struct CompositionTargetStats
    {
        COMPOSITION_FRAME_ID frameId;
        COMPOSITION_FRAME_STATS frameStats;

        COMPOSITION_TARGET_ID targetId;
        COMPOSITION_TARGET_STATS targetStats;
    };

    UINT64 m_qpcFrequency;
    COMPOSITION_FRAME_ID m_lastCollectedFrameId = 0;
    std::vector<CompositionTargetStats> m_targetStats;

public:
    FrameStatisticsCollector()
    {
        QueryPerformanceFrequency(&m_qpcFrequency);
        m_lastCollectedFrameId = CurrentFrameId();
    }

    // Queries the compositor clock statistics API to determine the last frame
    // completed by the composition engine
    COMPOSITION_FRAME_ID CurrentFrameId() const
    {
        COMPOSITION_FRAME_ID frameId;
        if (FAILED(_DCompositionGetFrameId(frameIdType, &frameId)))
        {
            frameId = 0;
        }

        return frameId;
    }

    // Queries the system to get information about the latest composition frames
    void CollectStats()
    {
        COMPOSITION_FRAME_ID currentFrameId = CurrentFrameId(COMPOSITION_FRAME_ID_COMPLETED);

        while (m_active && (currentFrameId > m_endFrameId))
        {
            auto newEndFrameId = m_endFrameId + 1;

            COMPOSITION_FRAME_STATS frameStats = {};
            COMPOSITION_TARGET_ID targetIds[sc_maxTargetCount] = {};
            UINT targetCount;

            hr = _DCompositionGetStatistics(newEndFrameId,
                &frameStats,
                _countof(targetIds),
                targetIds,
                &targetCount);
            if (SUCCEEDED(hr))
            {
                // We track up to sc_maxTargetCount targets per frame
                targetCount = min<UINT>(targetCount, _countof(targetIds));

                for (UINT uIndex = 0; uIndex < targetCount; uIndex++)
                {
                    COMPOSITION_TARGET_STATS targetStats = {};
                    hr = DCompositionGetTargetStatistics(newEndFrameId,
                        &targetIds[uIndex],
                        &targetStats);
                    if (SUCCEEDED(hr))
                    {
                        CompositionTargetStats compTargetStats = { newEndFrameId,
                                                                  frameStats,
                                                                  targetIds[uIndex],
                                                                  targetStats };

                        m_compTargetStats.push_back(compTargetStats);
                    }
                    else
                    {
                        m_active = false;
                    }
                }

                m_endFrameId = newEndFrameId;
            }
            else
            {
                m_active = false;
            }
        }
    }

    // Compute the frame rate for the given composition target in frames per
    // second, over the specified frame interval based on historical statistics
    // data
    float TargetFrameRate(
        _const COMPOSITION_TARGET_ID& targetId,
        COMPOSITION_FRAME_ID beginFrameId,
        COMPOSITION_FRAME_ID endFrameId)  const
    {
        UINT frameCount = 0;
        UINT64 beginTime = 0;
        UINT64 endTime = 0;

        for (const auto& stats : m_compTargetStats)
        {
            if ((stats.frameId >= beginFrameId) && (stats.frameId <= endFrameId))
            {
                if (stats.frameId == beginFrameId)
                {
                    beginTime = stats.frameStats.startTime;
                }

                if (stats.frameId == endFrameId)
                {
                    endTime = stats.frameStats.startTime +
                        stats.frameStats.framePeriod;
                }

                if ((stats.targetId == targetId) &&
                    (stats.targetStats.presentTime != 0))
                {
                    frameCount++;
                }
            }
        }

        if ((beginTime != 0) &&
            (endTime != 0) &&
            (endTime > beginTime) &&
            (frameCount != 0))
        {
            auto seconds = static_cast<float>(endTime - beginTime) /
                static_cast<float>(m_qpcFrequency);

            return static_cast<float>(frameCount) / seconds;
        }
        else
        {
            return 0.0f;
        }
    }
};
```

## <a name="glossary"></a>Glosario

* **Destino**. Mapa de bits en el que el motor de composición rasteriza el árbol visual. Este mapa de bits suele ser una presentación.
* **Marco compositor**. Un ciclo de trabajo &mdash; compositor no es necesariamente un vblank.
