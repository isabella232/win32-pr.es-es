---
title: Mejoras de Direct3D 9Ex
description: En este tema se Windows compatibilidad agregada de Windows 7 para el modo de volteo presente y sus estadísticas presentes asociadas en Direct3D 9Ex y Administrador de ventanas de escritorio.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3221b805f07408b27e19a00a42ca0c4733ea725bd32a51b5b3e340b48d2070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797021"
---
# <a name="direct3d-9ex-improvements"></a>Mejoras de Direct3D 9Ex

En este tema se Windows compatibilidad agregada de Windows 7 para el modo de volteo presente y sus estadísticas presentes asociadas en Direct3D 9Ex y Administrador de ventanas de escritorio. Las aplicaciones de destino incluyen aplicaciones de presentación basadas en velocidad de fotogramas o vídeo. Las aplicaciones que usan direct3D 9Ex Flip Mode Present reducen la carga de recursos del sistema cuando DWM está habilitado. Presentar mejoras de estadísticas asociadas con el modo de volteo presente permite que las aplicaciones de Direct3D 9Ex controle mejor la tasa de presentación al proporcionar comentarios en tiempo real y mecanismos de corrección. Se incluyen explicaciones detalladas y punteros a recursos de ejemplo.

En este tema se incluyen las siguientes secciones.

-   [Mejoras en Direct3D 9Ex para Windows 7](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [Presentación del modo de volteo de Direct3D 9EX](#direct3d-9ex-flip-mode-presentation)
-   [Modelo de programación y API](#programming-model-and-apis)
    -   [Cómo participar en el modelo de volteo de Direct3D 9Ex](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [Directrices de diseño para aplicaciones direct3D 9Ex Flip Model](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [Sincronización de fotogramas de aplicaciones de modelo de Volteo de Direct3D 9Ex](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [Sincronización de fotogramas para aplicaciones en ventanas cuando DWM está desactivado](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [Recorrido por un modelo de volteo de Direct3D 9Ex y ejemplo de presentación de estadísticas](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [Resumen de la programación de Recomendaciones sincronización de fotogramas](#summary-of-programming-recommendations-for-frame-synchronization)
-   [Conclusiones sobre las mejoras de Direct3D 9Ex](#conclusion-about-direct3d-9ex-improvements)
-   [Llamada a la acción](#call-to-action)
-   [Temas relacionados](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a>Mejoras en Direct3D 9Ex para Windows 7

La presentación en modo de volteo de Direct3D 9Ex es un modo mejorado de presentación de imágenes en Direct3D 9Ex que entrega eficazmente imágenes representados Windows 7 Administrador de ventanas de escritorio (DWM) para la composición. A partir Windows Vista, DWM compone todo el escritorio. Cuando DWM está habilitado, las aplicaciones en modo de ventana presentan su contenido en el escritorio mediante un método denominado Blt Mode Present to DWM (o Blt Model). Con el modelo Blt, DWM mantiene una copia de la superficie representada de Direct3D 9Ex para la composición de escritorio. Cuando se actualiza la aplicación, el nuevo contenido se copia en la superficie dwm a través de un blt. En el caso de las aplicaciones que contienen contenido de Direct3D y GDI, los datos de GDI también se copian en la superficie dwm.

Disponible en Windows 7, el modo de volteo presente en DWM (o Flip Model) es un nuevo método de presentación que básicamente permite pasar identificadores de superficies de aplicación entre aplicaciones en modo de ventana y DWM. Además de guardar recursos, Flip Model admite estadísticas actuales mejoradas.

Las estadísticas presentes son información de tiempo de fotogramas que las aplicaciones pueden usar para sincronizar secuencias de vídeo y audio y recuperarse de problemas de reproducción de vídeo. La información de tiempo de fotogramas de las estadísticas actuales permite a las aplicaciones ajustar la velocidad de presentación de sus fotogramas de vídeo para una presentación más fluida. En Windows Vista, donde DWM mantiene una copia correspondiente de la superficie de marco para la composición de escritorio, las aplicaciones pueden usar las estadísticas actuales proporcionadas por DWM. Este método de obtención de estadísticas actuales seguirá estando disponible en Windows 7 para las aplicaciones existentes.

En Windows 7, las aplicaciones basadas en Direct3D 9Ex que adoptan flip model deben usar las API D3D9Ex para obtener las estadísticas actuales. Cuando DWM está habilitado, las aplicaciones direct3D 9Ex en modo de ventana y modo exclusivo de pantalla completa pueden esperar la misma información de estadísticas presentes cuando se usa Voltear modelo. Direct3D 9Ex Flip Model presenta estadísticas que permiten a las aplicaciones consultar las estadísticas actuales en tiempo real, en lugar de después de que el fotograma se haya mostrado en pantalla. la misma información de estadísticas actual está disponible para las aplicaciones en modo Flip-Model habilitadas como aplicaciones de pantalla completa; Una marca agregada en las API de D3D9Ex permite que las aplicaciones flip model descarten eficazmente los fotogramas en tiempo de presentación.

Las nuevas aplicaciones de presentación basadas en velocidad de fotogramas o vídeo que tienen como destino direct3D 9Ex Flip Model deben usar Windows 7. Debido a la sincronización entre DWM y el entorno de ejecución de Direct3D 9Ex, las aplicaciones que usan flip model deben especificar entre 2 y 4 búferes de reserva para garantizar una presentación fluida. Las aplicaciones que usan la información de estadísticas actuales se beneficiarán del uso de las mejoras de estadísticas actuales habilitadas para flip model.

## <a name="direct3d-9ex-flip-mode-presentation"></a>Presentación del modo de volteo de Direct3D 9EX

Las mejoras de rendimiento de Direct3D 9Ex Flip Mode Present son significativas en el sistema cuando DWM está en modo de ventana y no en modo exclusivo de pantalla completa. En la tabla e ilustración siguientes se muestra una comparación simplificada de los usos de ancho de banda de memoria y las lecturas y escrituras del sistema de las aplicaciones en ventanas que eligen Voltear modelo frente al modelo Blt de uso predeterminado.



| Modo Blt presente en DWM                                                                                                 | D3D9Ex Flip Mode Present to DWM                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 1. La aplicación actualiza su marco (escritura)<br/>                                                                 | 1. La aplicación actualiza su marco (escritura)<br/>                     |
| 2. El tiempo de ejecución de Direct3D copia el contenido de la superficie en una superficie de redireccionamiento de DWM (lectura, escritura)<br/>                       | 2. El entorno de ejecución de Direct3D pasa la superficie de la aplicación a DWM<br/>        |
| 3. Una vez completada la copia de la superficie compartida, DWM representa la superficie de la aplicación en la pantalla (lectura, escritura)<br/> | 3. DWM representa la superficie de la aplicación en la pantalla (lectura, escritura)<br/> |



 

![ilustración de una comparación del modelo blt y el modelo de volteo](images/blt-flip-mode-present.png)

El modo de volteo presente reduce el uso de memoria del sistema al reducir el número de lecturas y escrituras por el tiempo de ejecución de Direct3D para la composición de fotogramas en ventanas mediante DWM. Esto reduce el consumo de energía del sistema y el uso general de memoria.

Las aplicaciones pueden aprovechar las ventajas del modo de volteo de Direct3D 9Ex presentar mejoras de estadísticas cuando DWM está on, independientemente de si la aplicación está en modo de ventana o en modo exclusivo de pantalla completa.

## <a name="programming-model-and-apis"></a>Modelo de programación y API

Las nuevas aplicaciones de velocidad de fotogramas o vídeo que usan direct3D 9Ex API en Windows 7 pueden aprovechar el ahorro de memoria y energía y la presentación mejorada que ofrece el modo de volteo presente cuando se ejecuta en Windows 7. (Cuando se ejecuta en versiones Windows anteriores, el entorno de ejecución de Direct3D tiene como valor predeterminado la aplicación en Modo Blt presente).

Modo de volteo Presente implica que la aplicación puede aprovechar los comentarios de estadísticas presentes en tiempo real y los mecanismos de corrección cuando DWM está en funcionamiento. Sin embargo, las aplicaciones que usan el modo de volteo presente deben tener en cuenta las limitaciones cuando usan la representación simultánea de la API de GDI.

Puede modificar las aplicaciones existentes para aprovechar el modo de volteo presente, con las mismas ventajas y advertencias que las aplicaciones recién desarrolladas.

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a>Cómo participar en el modelo de volteo de Direct3D 9Ex

Las aplicaciones direct3D 9Ex que tienen como destino Windows 7 pueden participar en el modelo de volteo mediante la creación de la cadena de intercambio con el valor de enumeración [**\_ FLIPEX D3DSWAPEFFECT.**](/windows/desktop/direct3d9/d3dswapeffect) Para participar en el modelo flip, las aplicaciones especifican la estructura [**PARAMETERS \_ D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) y, a continuación, pasan un puntero a esta estructura cuando llaman a la API [**IDirect3D9Ex::CreateDeviceEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) En esta sección se describe cómo las aplicaciones que tienen como destino Windows 7 **usan IDirect3D9Ex::CreateDeviceEx** para participar en el modelo flip. Para obtener más información sobre la API **IDirect3D9Ex::CreateDeviceEx,** vea **IDirect3D9Ex::CreateDeviceEx en MSDN.**

Para mayor comodidad, la sintaxis de [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) e [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) se repite aquí.

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

``` syntax
typedef struct D3DPRESENT_PARAMETERS {
    UINT BackBufferWidth, BackBufferHeight;
    D3DFORMAT BackBufferFormat;
    UINT BackBufferCount;
    D3DMULTISAMPLE_TYPE MultiSampleType;
    DWORD MultiSampleQuality;
    D3DSWAPEFFECT SwapEffect;
    HWND hDeviceWindow;
    BOOL Windowed;
    BOOL EnableAutoDepthStencil;
    D3DFORMAT AutoDepthStencilFormat;
    DWORD Flags;
    UINT FullScreen_RefreshRateInHz;
    UINT PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```

Al modificar las aplicaciones de Direct3D 9Ex para Windows 7 para participar en el modelo flip, debe tener en cuenta los siguientes elementos sobre los miembros especificados de [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters):

<dl> <dt>

**BackBufferCount**
</dt> <dd>

(solo Windows 7)

Cuando **SwapEffect** se establece en el nuevo tipo de efecto de cadena de intercambio FLIPEX D3DSWAPEFFECT, el recuento de búferes de reserva debe ser igual o mayor que 2, para evitar una penalización del rendimiento de la aplicación como resultado de esperar a que DWM liberara el búfer present \_ anterior.

Cuando la aplicación también usa estadísticas actuales asociadas a D3DSWAPEFFECT FLIPEX, se recomienda establecer el recuento de búferes de reserva en de \_ 2 a 4.

El uso de D3DSWAPEFFECT FLIPEX en Windows Vista o versiones anteriores del sistema operativo devolverá un error \_ [**de CreateDeviceEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)

</dd> <dt>

**SwapEffect**
</dt> <dd>

(solo Windows 7)

El nuevo tipo de efecto de cadena de intercambio FLIPEX D3DSWAPEFFECT designa cuando una aplicación adopta el modo de volteo \_ presente en DWM. Permite a la aplicación un uso más eficaz de la memoria y la energía, y también permite que la aplicación aproveche las estadísticas presentes de pantalla completa en modo de ventana. El comportamiento de la aplicación a pantalla completa no se ve afectado. Si Windowed se establece en **TRUE** y **SwapEffect** se establece en D3DSWAPEFFECT FLIPEX, el tiempo de ejecución crea un búfer de reserva adicional y gira el controlador que pertenece al búfer que se convierte en el búfer front-time en tiempo de \_ presentación.

</dd> <dt>

**Marcas**
</dt> <dd>

(solo Windows 7)

No se puede establecer la marca [ \_ \_ BACKBUFFER D3DPRESENTFLAG LOCKABLE](/windows/desktop/direct3d9/d3dpresentflag) si **SwapEffect** está establecido en el nuevo tipo de efecto de cadena de intercambio [**\_ FLIPEX D3DSWAPEFFECT.**](/windows/desktop/direct3d9/d3dswapeffect)

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a>Directrices de diseño para aplicaciones direct3D 9Ex Flip Model

Use las instrucciones de las secciones siguientes para diseñar las aplicaciones de Direct3D 9Ex Flip Model.

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a>Usar el modo de volteo presente en un HWND independiente del modo Blt presente

Las aplicaciones deben usar direct3D 9Ex Flip Mode Present en un HWND que no sea el destino de otras API, incluido el modo Blt Presente Direct3D 9Ex, otras versiones de Direct3D o GDI. El modo de volteo presente se puede usar para presentar a las ventanas secundarias; Es decir, las aplicaciones pueden usar Flip Model cuando no se mezcla con Blt Model en el mismo HWND, como se muestra en las ilustraciones siguientes.

![ilustración de la ventana primaria direct3d y una ventana secundaria gdi, cada una con su propio hwnd](images/parent-d3d.png)

![ilustración de la ventana primaria gdi y una ventana secundaria direct3d, cada una con su propio hwnd](images/parent-gdi.png)

Dado que Blt Model mantiene una copia adicional de la superficie, GDI y otros contenidos de Direct3D se pueden agregar al mismo HWND a través de actualizaciones por fragmentos de Direct3D y GDI. Con el modelo flip, solo estará visible el contenido de Direct3D 9Ex en las cadenas de intercambio [**\_ FLIPEX D3DSWAPEFFECT**](/windows/desktop/direct3d9/d3dswapeffect) que se pasan a DWM. Todas las demás actualizaciones de contenido de Blt Model Direct3D o GDI se omitirán, como se muestra en las ilustraciones siguientes.

![ilustración de texto gdi que podría no mostrarse si se usa el modelo de inversión y el contenido de direct3d y gdi está en el mismo hwnd](images/d3d-gdi-same-hwnd.png)

![ilustración del contenido de direct3d y gdi en el que dwm está habilitado y la aplicación está en modo de ventana](images/d3d-gdinotext-same-hwnd.png)

Por lo tanto, flip model debe estar habilitado para las superficies de búferes de cadena de intercambio en las que el modelo de volteo de Direct3D 9Ex solo se representa en todo hwnd.

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a>No usar el modelo de volteo con ScrollWindow o ScrollWindowEx de GDI

Algunas aplicaciones de Direct3D 9Ex usan las funciones ScrollWindow o ScrollWindowEx de GDI para actualizar el contenido de la ventana cuando se desencadena un evento de desplazamiento del usuario. ScrollWindow y ScrollWindowEx realizan análisis del contenido de la ventana en pantalla a medida que se desplaza una ventana. Estas funciones también requieren actualizaciones del modelo Blt para el contenido de GDI y Direct3D 9Ex. Las aplicaciones que usan cualquiera de las funciones no mostrarán necesariamente el contenido visible de la ventana que se desplaza en pantalla cuando la aplicación está en modo de ventana y DWM está habilitado. Se recomienda no usar las API ScrollWindow y ScrollWindowEx de GDI en las aplicaciones y, en su lugar, volver a dibujar su contenido en pantalla en respuesta al desplazamiento.

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a>Usar una cadena de intercambio FLIPEX D3DSWAPEFFECT \_ por HWND

Las aplicaciones que usan el modelo de volteo no deben usar varias cadenas de intercambio de flip model destinadas al mismo HWND.

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a>Sincronización de fotogramas de aplicaciones de modelo de Volteo de Direct3D 9Ex

Las estadísticas presentes son información de tiempo de fotogramas que las aplicaciones multimedia usan para sincronizar secuencias de vídeo y audio y recuperarse de problemas de reproducción de vídeo. Para habilitar la disponibilidad actual de las estadísticas, la aplicación Direct3D 9Ex debe asegurarse de que el parámetro *BehaviorFlags* que la aplicación pasa a [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contiene la marca de comportamiento del dispositivo [D3DCREATE \_ ENABLE \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).

Para mayor comodidad, la [**sintaxis de IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) se repite aquí.

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

Direct3D 9Ex Flip Model agrega la marca de presentación [D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) que aplica el comportamiento de marca de presentación [D3DPRESENT \_ INTERVAL \_ IMMEDIATE.](/windows/desktop/direct3d9/d3dpresent) La aplicación Direct3D 9Ex especifica estas marcas de presentación en el parámetro *dwFlags* que la aplicación pasa a [**IDirect3DDevice9Ex::P resentEx,**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)como se muestra aquí.

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

Al modificar la aplicación Direct3D 9Ex para Windows 7, debe tener en cuenta la siguiente información sobre las marcas de presentación [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) especificadas:

<dl> <dt>

[D3DPRESENT \_ DONOTFLIP](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

Esta marca solo está disponible en modo de pantalla completa o

(solo Windows 7)

cuando la aplicación establece el **miembro SwapEffect** de [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) en [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) en una llamada a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).

</dd> <dt>

[D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

(solo Windows 7)

Esta marca solo se puede especificar si la aplicación establece el miembro **SwapEffect** de [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) en [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) en una llamada a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex). La aplicación puede usar esta marca para actualizar inmediatamente una superficie con varios fotogramas más adelante en la cola DWM Present, omitiendo básicamente los fotogramas intermedios.

Las aplicaciones habilitadas para FlipEx en ventanas pueden usar esta marca para actualizar inmediatamente una superficie con un marco que se encuentra más adelante en la cola DWM Present, omitiendo fotogramas intermedios. Esto es especialmente útil para las aplicaciones multimedia que desean descartar fotogramas detectados como retrasados y presentar fotogramas posteriores en tiempo de composición. [**IDirect3DDevice9Ex::P resentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) devuelve un error de parámetro no válido si esta marca se especifica incorrectamente.

</dd> </dl>

Para obtener información de estadísticas actual, la aplicación obtiene la estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) llamando a la API [**IDirect3DSwapChain9Ex::GetPresentStatistics.**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85))

La [**estructura D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) contiene estadísticas sobre [**las llamadas IDirect3DDevice9Ex::P resentEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) El dispositivo debe crearse mediante una llamada [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) con la [marca D3DCREATE \_ ENABLE \_ PRESENTSTATS.](/windows/desktop/direct3d9/d3dcreate) De lo contrario, los datos [**devueltos por GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) no están definidos. Una cadena de intercambio direct3D 9Ex habilitada para flip-model proporciona información de estadísticas presente en los modos de ventana y de pantalla completa.

En el caso de las cadenas de intercambio direct3D 9Ex habilitadas para Blt-Model en modo de ventana, todos los valores de la estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) serán ceros.

En el caso de las estadísticas actuales de FlipEx, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) devuelve D3DERR \_ PRESENT \_ STATISTICS \_ DISJOINT en las situaciones siguientes:

-   Primera llamada a [**GetPresentStatistics,**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) que indica el principio de una secuencia
-   Transición de DWM de on a off
-   Cambio de modo: modo de ventana hacia o desde pantalla completa o de pantalla completa a transiciones de pantalla completa

Para mayor comodidad, la sintaxis [**de GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) se repite aquí.

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

El método [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) devuelve el último PresentCount, es decir, el identificador present de la última llamada present correcta realizada por un dispositivo de visualización asociado a la cadena de intercambio. Este identificador present es el valor del **miembro PresentCount** de la [**estructura D3DPRESENTSTATS.**](/windows/desktop/direct3d9/d3dpresentstats) En el caso de las cadenas de intercambio direct3D 9Ex habilitadas para Blt-Model, mientras que en modo de ventana, todos los valores de la estructura **D3DPRESENTSTATS** serán ceros.

Para mayor comodidad, la [**sintaxis de IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) se repite aquí.

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

Al modificar la aplicación Direct3D 9Ex para Windows 7, debe tener en cuenta la siguiente información sobre la estructura [**D3DPRESENTSTATS:**](/windows/desktop/direct3d9/d3dpresentstats)

-   El valor presentCount que [**devuelve GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) no se actualiza cuando una llamada [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT DONOTWAIT especificado en el parámetro \_ *dwFlags* devuelve un error.
-   Cuando se llama a [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT DONOTFLIP, una llamada a GetPresentStatistics se realiza correctamente, pero no devuelve una estructura \_ [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) actualizada cuando la aplicación está en modo de ventana. [](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85))
-   **PresentRefreshCount frente** **a SyncRefreshCount** en [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):
    -   **PresentRefreshCount** es igual a **SyncRefreshCount** cuando la aplicación se presenta en cada vsync.
    -   **SyncRefreshCount** se obtiene en el intervalo de vsync cuando se envió el presente, **SyncQPCTime** es aproximadamente el tiempo asociado al intervalo de vsync.

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a>Sincronización de fotogramas para aplicaciones en ventanas cuando DWM está desactivado

Cuando DWM está desactivado, las aplicaciones con ventanas se muestran directamente en la pantalla del monitor sin pasar por una cadena de volteo. En Windows Vista, no hay compatibilidad para obtener información de estadísticas de fotogramas para aplicaciones con ventanas cuando DWM está desactivado. Para mantener una API en la que las aplicaciones no necesiten tener en cuenta DWM, Windows 7 devolverá información de estadísticas de fotogramas para las aplicaciones en ventanas cuando DWM esté desactivado. Las estadísticas de fotogramas devueltas cuando DWM está desactivado son solo estimaciones.

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a>Walk-Through de un modelo de volteo de Direct3D 9Ex y ejemplo de estadísticas presentes

**Para participar en la presentación de FlipEx para el ejemplo 9Ex de Direct3D**

1.  Asegúrese de que la aplicación de ejemplo se ejecuta Windows versión 7 o posterior del sistema operativo.
2.  Establezca el **miembro SwapEffect** de [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) en [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) en una llamada a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).


```C++
    OSVERSIONINFO version;
    ZeroMemory(&version, sizeof(version));
    version.dwOSVersionInfoSize = sizeof(version);
    GetVersionEx(&version);
    
    // Sample would run only on Win7 or higher
    // Flip Model present and its associated present statistics behavior are only available on Windows 7 or higher operating system
    bool bIsWin7 = (version.dwMajorVersion > 6) || 
        ((version.dwMajorVersion == 6) && (version.dwMinorVersion >= 1));

    if (!bIsWin7)
    {
        MessageBox(NULL, L"This sample requires Windows 7 or higher", NULL, MB_OK);
        return 0;
    }
```



**Para participar también en el ejemplo present statistics for Direct3D 9Ex asociado a FlipEx**

-   Establezca [D3DCREATE \_ ENABLE \_ PRESENTSTATS en](/windows/desktop/direct3d9/d3dcreate) el parámetro *BehaviorFlags* [**de CreateDeviceEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)


```C++
    // Set up the structure used to create the D3DDevice
    D3DPRESENT_PARAMETERS d3dpp;
    ZeroMemory(&d3dpp, sizeof(d3dpp));

    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_FLIPEX;        // Opts into Flip Model present for D3D9Ex swapchain
    d3dpp.BackBufferFormat = D3DFMT_X8R8G8B8;
    d3dpp.BackBufferWidth = 256;                
    d3dpp.BackBufferHeight = 256;
    d3dpp.BackBufferCount = QUEUE_SIZE;
    d3dpp.PresentationInterval = D3DPRESENT_INTERVAL_ONE;

    g_iWidth = d3dpp.BackBufferWidth;
    g_iHeight = d3dpp.BackBufferHeight;

    // Create the D3DDevice with present statistics enabled - set D3DCREATE_ENABLE_PRESENTSTATS for behaviorFlags parameter
    if(FAILED(g_pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_HARDWARE_VERTEXPROCESSING | D3DCREATE_ENABLE_PRESENTSTATS,
                                      &d3dpp, NULL, &g_pd3dDevice)))
    {
        return E_FAIL;
    }
```



**Para evitar, detectar y recuperarse de problemas**

1.  Cola Llamadas presentes: el recuento recomendado de búferes de seguridad es de 2 a 4.
2.  El ejemplo de Direct3D 9Ex agrega un búfer de seguridad implícito; la longitud real de la cola actual es el recuento de búferes de copia de seguridad + 1.
3.  Cree el asistente Present queue structure para almacenar todos los present ID (PresentCount) enviados correctamente y asociados, calculados o esperados PresentRefreshCount.
4.  Para detectar la aparición de problemas:

    -   Llame [**a GetPresentStatistics.**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85))
    -   Obtenga el id. de presente (PresentCount) y el recuento de vsync donde se muestra el fotograma (PresentRefreshCount) del fotograma cuyas estadísticas actuales se obtienen.
    -   Recupere el presentRefreshCount esperado (TargetRefresh en el código de ejemplo) asociado al identificador present.
    -   Si presentRefreshCount real es posterior al esperado, se ha producido un problema.

5.  Para recuperarse de problemas:

    -   Calcule el número de fotogramas que se omitirán (g \_ iImmediates variable en el código de ejemplo).
    -   Presente los fotogramas omitido con el intervalo D3DPRESENT \_ FORCEIMMEDIATE.

**Consideraciones para la detección y recuperación de problemas**

1.  La recuperación de Glitch toma N (variable g iQueueDelay en el código de ejemplo) número de llamadas present donde \_ N (g \_ iQueueDelay) es igual a g iImmediates más la longitud de la cola Present, es \_ decir:

    -   Omitir fotogramas con present interval D3DPRESENT \_ FORCEIMMEDIATE, más
    -   Presentaciones en cola que deben procesarse

2.  Establezca un límite en la longitud del problema (GLITCH \_ RECOVERY LIMIT en la \_ muestra). Si la aplicación de ejemplo no puede recuperarse de un problema que es demasiado largo (es decir, 1 segundo o 60 vsyncs en el monitor de 60Hz), salte por encima de la animación intermitente y restablezca la cola del asistente Present.


```C++
VOID Render()
{
    g_pd3dDevice->Clear(0, NULL, D3DCLEAR_TARGET, D3DCOLOR_XRGB(0, 0, 0), 1.0f, 0);

    g_pd3dDevice->BeginScene();

    // Compute new animation parameters for time and frame based animations

    // Time-based is a difference between base and current SyncRefreshCount
    g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
    // Frame-based is incrementing frame value
    g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;

    RenderBlurredMesh(TRUE);    // Time-based
    RenderBlurredMesh(FALSE);   // Frame-based

    g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;

    DrawText();

    g_pd3dDevice->EndScene();

    // Performs glitch recovery if glitch was detected
    if (g_bGlitchRecovery && (g_iImmediates > 0))
    {
        // If we have present immediates queued as a result of glitch detected, issue forceimmediate Presents for glitch recovery 
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE);
        g_iImmediates--;
        g_iShowingGlitchRecovery = MESSAGE_SHOW;
    }
    // Otherwise, Present normally
    else
    {
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, 0);
    }

    // Add to helper Present queue: PresentID + expected present refresh count of last submitted Present
    UINT PresentCount;
    g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
    g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);
    
    // QueueDelay specifies # Present calls to be processed before another glitch recovery attempt
    if (g_iQueueDelay > 0)
    {
        g_iQueueDelay--;
    }

    if (g_bGlitchRecovery)
    {
        // Additional DONOTFLIP presents for frame conversions, which basically follows the same logic, but without rendering
        for (DWORD i = 0; i < g_iDoNotFlipNum; i++)
        {
            if (g_TargetRefreshCount != -1)
            {
                g_TargetRefreshCount++;
                g_iFrameNumber++;
                g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
                g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;
                g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;
            }
            
            if (g_iImmediates > 0)
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE | D3DPRESENT_DONOTFLIP);
                g_iImmediates--;
            }
            else
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_DONOTFLIP);
            }
            UINT PresentCount;
            g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
            g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);

            if (g_iQueueDelay > 0)
            {
                g_iQueueDelay--;
            }
        }
    }

    // Check Present Stats info for glitch detection 
    D3DPRESENTSTATS PresentStats;

    // Obtain present statistics information for successfully displayed presents
    HRESULT hr = g_pd3dSwapChain->GetPresentStats(&PresentStats);

    if (SUCCEEDED(hr))
    {
        // Time-based update
        g_LastSyncRefreshCount = PresentStats.SyncRefreshCount;
        if ((g_SyncRefreshCount == -1) && (PresentStats.PresentCount != 0))
        {
            // First time SyncRefreshCount is reported, use it as base
            g_SyncRefreshCount = PresentStats.SyncRefreshCount;
        }

        // Fetch frame from the queue...
        UINT TargetRefresh = g_Queue.DequeueFrame(PresentStats.PresentCount);

        // If PresentStats returned a really old frame that we no longer have in the queue, just don't do any glitch detection
        if (TargetRefresh == FRAME_NOT_FOUND)
            return;

        if (g_TargetRefreshCount == -1)
        {
            // This is first time issued frame is confirmed by present stats, so fill target refresh count for all frames in the queue
            g_TargetRefreshCount = g_Queue.FillRefreshCounts(PresentStats.PresentCount, g_SyncRefreshCount);
        } 
        else
        {
            g_TargetRefreshCount++;
            g_iFrameNumber++;

            // To determine whether we're glitching, see if our estimated refresh count is confirmed
            // if the frame is displayed later than the expected vsync count
            if (TargetRefresh < PresentStats.PresentRefreshCount)
            {
                // then, glitch is detected!

                // If glitch is too big, don't bother recovering from it, just jump animation
                if ((PresentStats.PresentRefreshCount - TargetRefresh) > GLITCH_RECOVERY_LIMIT)
                {
                    g_iStartFrame += PresentStats.SyncRefreshCount - g_SyncRefreshCount;
                    ResetAnimation();
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;    
                } 
                // Otherwise, compute number of immediate presents to recover from it -- if we?re not still trying to recover from another glitch
                else if (g_iQueueDelay == 0)
                {
                      // skip frames to catch up to expected refresh count
                    g_iImmediates = PresentStats.PresentRefreshCount - TargetRefresh;
                    // QueueDelay specifies # Present calls before another glitch recovery 
                    g_iQueueDelay = g_iImmediates + QUEUE_SIZE;
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;
                }
            }
            else
            {
                // No glitch, reset glitch count
                g_iGlitchesInaRow = 0;
            }
        }
    }
    else if (hr == D3DERR_PRESENT_STATISTICS_DISJOINT)
    {
        // D3DERR_PRESENT_STATISTICS_DISJOINT means measurements should be started from the scratch (could be caused by mode change or DWM on/off transition)
        ResetAnimation();
    }

    // If we got too many glitches in a row, reduce framerate conversion factor (that is, render less frames)
    if (g_iGlitchesInaRow == FRAMECONVERSION_GLITCH_LIMIT)
    {
        if (g_iDoNotFlipNum < FRAMECONVERSION_LIMIT)
        {
            g_iDoNotFlipNum++;
        }
        g_iGlitchesInaRow = 0;
        g_iShowingDoNotFlipBump = MESSAGE_SHOW;
    }
}
```



**Escenario de ejemplo**

-   En la ilustración siguiente se muestra una aplicación con el recuento de búferes de reserva de 4. Por lo tanto, la longitud real de la cola Actual es 5.

    ![ilustración de los fotogramas representados por applicas y la cola presente](images/sample-scenario.png)

    El fotograma A está destinado a pasar a la pantalla en el recuento de intervalos de sincronización de 1, pero se detectó que se mostró en el recuento de intervalos de sincronización de 4. Por lo tanto, se ha producido un problema. Los 3 fotogramas siguientes se presentan con D3DPRESENT \_ INTERVAL \_ FORCEIMMEDIATE. El problema debe tomar un total de 8 Llamadas presentes antes de recuperarse; el siguiente fotograma se mostrará según su recuento de intervalos de sincronización de destino.

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a>Resumen de la programación de Recomendaciones sincronización de fotogramas

-   Cree una lista de copia de seguridad de todos los IDs de LastPresentCount (obtenidos a través de [**GetLastPresentCount)**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)y el valor estimado presentRefreshCount asociado de todos los present enviados.
    > [!Note]  
    > Cuando la aplicación llama a [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT DONOTFLIP, la llamada a GetPresentStatistics se realiza correctamente, pero no devuelve una estructura \_ [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) actualizada cuando la aplicación está en modo de ventana. [](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85))

     

-   Llame [**a GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) para obtener el presentRefreshCount real asociado a cada present ID de fotogramas mostrados, para asegurarse de que la aplicación controla los errores que se devuelven de la llamada.
-   Si presentRefreshCount real es posterior al valor estimado de PresentRefreshCount, se detecta un problema. Compensa mediante el envío de fotogramas de retraso presentes con D3DPRESENT \_ FORCEIMMEDIATE.
-   Cuando un fotograma se presenta tarde en la cola Present, todos los fotogramas en cola posteriores se presentarán tarde. D3DPRESENT FORCEIMMEDIATE corregirá solo el siguiente fotograma que se presentará \_ después de todos los fotogramas en cola. Por lo tanto, el recuento de cola present o backbuffer no debe ser demasiado largo, por lo que hay menos problemas de fotogramas con los que ponerse al día. El número óptimo de búferes de reserva es de 2 a 4.
-   Si presentRefreshCount estimado es posterior al presentRefreshCount real, es posible que se haya producido una limitación de DWM. Las siguientes soluciones son posibles:

    -   reducir la longitud de cola actual
    -   reducir los requisitos de memoria de GPU con cualquier otro medio, además de reducir la longitud de cola presente (es decir, reducir la calidad, quitar efectos, entre otros)
    -   especificar [**DwmEnableMMCSS para**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) evitar la limitación de DWM en general

-   Compruebe la funcionalidad de visualización de la aplicación y el rendimiento de las estadísticas de fotogramas en los escenarios siguientes:

    -   con DWM en y desactivado
    -   modos exclusivos y de ventana de pantalla completa
    -   hardware de funcionalidad inferior

-   Cuando las aplicaciones no pueden recuperarse de un gran número de fotogramas con problemas con D3DPRESENT \_ FORCEIMMEDIATE Present, pueden realizar las siguientes operaciones:

    -   reducir el uso de CPU y GPU mediante la representación con menos carga de trabajo.
    -   en el caso de la descodificación de vídeo, descodifique más rápido al reducir la calidad y, por tanto, el uso de CPU y GPU.

## <a name="conclusion-about-direct3d-9ex-improvements"></a>Conclusiones sobre las mejoras de Direct3D 9Ex

En Windows 7, las aplicaciones que muestran velocidad de fotogramas de vídeo o medidor durante la presentación pueden optar por voltear modelo. Las mejoras de estadísticas actuales asociadas con Flip Model Direct3D 9Ex pueden beneficiar a las aplicaciones que sincronizan la presentación por velocidad de fotogramas, con comentarios en tiempo real para la detección y recuperación de problemas. Los desarrolladores que adoptan el modelo de volteo de Direct3D 9Ex deben tener en cuenta el destino de un HWND independiente del contenido GDI y la sincronización de velocidad de fotogramas. Consulte los detalles de este tema y la documentación de MSDN. Para obtener documentación adicional, [vea Centro para desarrolladores de DirectX en MSDN.](/previous-versions/windows/apps/hh452744(v=win.10))

## <a name="call-to-action"></a>Pasar a la acción

Le recomendamos que use direct3D 9Ex Flip Model y sus estadísticas actuales en Windows 7 al crear aplicaciones que intenten sincronizar la velocidad de fotogramas de presentación o recuperarse de problemas de pantalla.

## <a name="related-topics"></a>Temas relacionados

[Centro para desarrolladores de DirectX en MSDN](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> </dl>