---
title: Mejoras de Direct3D 9Ex
description: En este tema se describe la compatibilidad agregada de Windows 7 con el modo de volteo presente y sus estadísticas actuales asociadas en Direct3D 9Ex y Administrador de ventanas de escritorio.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42eef10b6caaa959cb750f073c97a0f665384463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421171"
---
# <a name="direct3d-9ex-improvements"></a>Mejoras de Direct3D 9Ex

En este tema se describe la compatibilidad agregada de Windows 7 con el modo de volteo presente y sus estadísticas actuales asociadas en Direct3D 9Ex y Administrador de ventanas de escritorio. Las aplicaciones de destino incluyen aplicaciones de presentación basadas en la velocidad de fotogramas o en vídeo. Las aplicaciones que usan el modo Flip de Direct3D 9Ex, reducen la carga de recursos del sistema cuando DWM está habilitado. Las mejoras presentes en las estadísticas asociadas con el modo de volteo permiten a las aplicaciones de Direct3D 9Ex controlar mejor la velocidad de presentación al proporcionar mecanismos de corrección y comentarios en tiempo real. Se incluyen explicaciones detalladas y punteros a los recursos de ejemplo.

En este tema se incluyen las siguientes secciones.

-   [Mejoras de Direct3D 9Ex para Windows 7](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [Presentación del modo Flip de Direct3D 9EX](#direct3d-9ex-flip-mode-presentation)
-   [Modelo de programación y API](#programming-model-and-apis)
    -   [Cómo participar en el modelo Flip de Direct3D 9Ex](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [Instrucciones de diseño para aplicaciones de modelo Flip 9Ex de Direct3D](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [Sincronización de fotogramas de aplicaciones de modelo Flip 9Ex de Direct3D](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [Sincronización de fotogramas para aplicaciones en ventanas cuando DWM está desactivado](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [Tutorial sobre un modelo Flip de Direct3D 9Ex y el ejemplo present Statistics](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [Resumen de las recomendaciones de programación para la sincronización de fotogramas](#summary-of-programming-recommendations-for-frame-synchronization)
-   [Conclusión sobre las mejoras de Direct3D 9Ex](#conclusion-about-direct3d-9ex-improvements)
-   [Llamada a la acción](#call-to-action)
-   [Temas relacionados](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a>Mejoras de Direct3D 9Ex para Windows 7

La presentación del modo de volteo de Direct3D 9Ex es un modo mejorado de presentar imágenes en Direct3D 9Ex que se entregan de forma eficaz imágenes representadas a Windows 7 Administrador de ventanas de escritorio (DWM) para su composición. A partir de Windows Vista, DWM compone todo el escritorio. Cuando DWM está habilitado, las aplicaciones en modo de ventana presentan su contenido en el escritorio mediante un método denominado BLT Mode present to DWM (o BLT Model). Con el modelo BLT, DWM mantiene una copia de la superficie representada de Direct3D 9Ex para la composición del escritorio. Cuando se actualiza la aplicación, el nuevo contenido se copia en la superficie de DWM a través de BLT. En el caso de las aplicaciones que contienen contenido de Direct3D y GDI, los datos GDI también se copian en la superficie DWM.

Disponible en Windows 7, el modo de volteo presente para DWM (o voltear modelo) es un nuevo método de presentación que habilita esencialmente los controladores de paso de las superficies de aplicación entre las aplicaciones en modo de ventana y DWM. Además de guardar los recursos, flip Model admite estadísticas actuales mejoradas.

Las estadísticas presentes son información de temporización de fotogramas que las aplicaciones pueden usar para sincronizar secuencias de audio y vídeo y recuperarse de problemas de reproducción de vídeo. La información de tiempo de marco de las estadísticas presentes permite a las aplicaciones ajustar la velocidad de presentación de los fotogramas de vídeo para una presentación más fluida. En Windows Vista, donde DWM mantiene una copia correspondiente de la superficie de marco para la composición del escritorio, las aplicaciones pueden usar estadísticas presentes proporcionadas por DWM. Este método de obtención de estadísticas actuales seguirá estando disponible en Windows 7 para las aplicaciones existentes.

En Windows 7, las aplicaciones basadas en Direct3D 9Ex que adopten Flip Model deben usar las API de D3D9Ex para obtener estadísticas actuales. Cuando DWM está habilitado, las aplicaciones en modo de ventana y de Direct3D 9Ex de modo exclusivo de pantalla completa pueden esperar la misma información de estadísticas presente al usar Flip Model. Las estadísticas presentes del modelo Flip de Direct3D 9Ex permiten que las aplicaciones consulten estadísticas presentes en tiempo real, en lugar de después de que el fotograma se muestre en la pantalla. la misma información de estadísticas presentes está disponible para las aplicaciones de modo de ventana Flip-Model habilitadas como aplicaciones de pantalla completa; una marca agregada en las API de D3D9Ex permite a las aplicaciones de Flip Model descartar eficazmente los fotogramas en tiempo de presentación.

El modelo Flip de Direct3D 9Ex debe usarse en las nuevas aplicaciones de presentación basadas en la velocidad de fotogramas y el vídeo que tienen como destino Windows 7. Debido a la sincronización entre DWM y el tiempo de ejecución de Direct3D 9Ex, las aplicaciones que usan Flip Model deben especificar entre 2 y 4 búferes retroversos para garantizar una presentación fluida. Las aplicaciones que usan información de estadísticas presentes se beneficiarán del uso de las mejoras de las estadísticas presentes de Flip Model enabled.

## <a name="direct3d-9ex-flip-mode-presentation"></a>Presentación del modo Flip de Direct3D 9EX

Las mejoras de rendimiento del modo de volteo 9Ex de Direct3D son significativas en el sistema cuando DWM está activado y cuando la aplicación está en modo de ventana, en lugar de en modo exclusivo de pantalla completa. En la siguiente tabla y ilustración se muestra una comparación simplificada de los usos de ancho de banda de memoria y las lecturas y escrituras del sistema que eligen Flip Model frente al modelo de uso predeterminado BLT.



| Modo BLT presente en DWM                                                                                                 | D3D9Ex modo de volteo presente en DWM                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 1. la aplicación actualiza su marco (escritura)<br/>                                                                 | 1. la aplicación actualiza su marco (escritura)<br/>                     |
| 2. el tiempo de ejecución de Direct3D copia el contenido de la superficie en una superficie de redirección de DWM (lectura, escritura)<br/>                       | 2. el tiempo de ejecución de Direct3D pasa la superficie de aplicación a DWM<br/>        |
| 3. una vez completada la copia de la superficie compartida, DWM representa la superficie de la aplicación en la pantalla (lectura, escritura)<br/> | 3. DWM representa la superficie de la aplicación en la pantalla (lectura, escritura)<br/> |



 

![Ilustración de una comparación del modelo BLT y el modelo Flip](images/blt-flip-mode-present.png)

El modo de volteo está presente reduce el uso de memoria del sistema al reducir el número de lecturas y escrituras realizadas por el tiempo de ejecución de Direct3D para la composición de fotogramas en ventanas por DWM. Esto reduce el consumo de energía del sistema y el uso de memoria general.

Las aplicaciones pueden beneficiarse de las mejoras de las estadísticas presentes del modo Flip de Direct3D 9Ex cuando DWM está activado, independientemente de si la aplicación está en modo de ventana o en el modo exclusivo de pantalla completa.

## <a name="programming-model-and-apis"></a>Modelo de programación y API

Las nuevas aplicaciones que usan las API de Direct3D 9Ex en Windows 7 pueden aprovechar las ventajas de la memoria y el ahorro de energía y de la presentación mejorada que ofrece el modo Flip cuando se ejecuta en Windows 7. (Cuando se ejecuta en versiones anteriores de Windows, el tiempo de ejecución de Direct3D utiliza de forma predeterminada la aplicación en el modo BLT).

El modo de volteo supone que la aplicación puede aprovechar las ventajas de los mecanismos de corrección y comentarios de estadísticas presentes en tiempo real cuando DWM está activado. Sin embargo, las aplicaciones que usan el modo de volteo presente deben tener en cuenta las limitaciones cuando usan la representación simultánea de la API de GDI.

Puede modificar las aplicaciones existentes para aprovechar el modo de volteo presente, con las mismas ventajas y advertencias que las aplicaciones recién desarrolladas.

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a>Cómo participar en el modelo Flip de Direct3D 9Ex

Las aplicaciones de Direct3D 9Ex que tienen como destino Windows 7 pueden participar en el modelo Flip mediante la creación de la cadena de intercambio con el valor de enumeración [**\_ FLIPEX de D3DSWAPEFFECT**](/windows/desktop/direct3d9/d3dswapeffect) . Para participar en el modelo Flip, las aplicaciones especifican la estructura de [**\_ parámetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) y, a continuación, pasan un puntero a esta estructura cuando llaman a la API [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) . En esta sección se describe cómo las aplicaciones que tienen como destino Windows 7 usan **IDirect3D9Ex:: CreateDeviceEx** para participar en el modelo de volteo. Para obtener más información sobre la API **IDirect3D9Ex:: CreateDeviceEx** , vea **IDirect3D9Ex:: CreateDeviceEx en MSDN**.

Para mayor comodidad, aquí se repite la sintaxis de [**\_ los parámetros de D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) y [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) .

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

Cuando se modifican las aplicaciones de Direct3D 9Ex para Windows 7 para participar en el modelo Flip, se deben tener en cuenta los siguientes elementos sobre los miembros especificados de los [**\_ parámetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters):

<dl> <dt>

**BackBufferCount**
</dt> <dd>

(Solo Windows 7)

Cuando **SwapEffect** se establece en el nuevo tipo de efecto de cadena de intercambio de D3DSWAPEFFECT \_ FLIPEX, el número de búferes de reserva debe ser igual o mayor que 2, para evitar una reducción del rendimiento de la aplicación como resultado de la espera en el búfer actual anterior para que DWM lo libere.

Cuando la aplicación también usa estadísticas presentes asociadas a D3DSWAPEFFECT \_ FLIPEX, se recomienda establecer el número de búferes de reserva en de 2 a 4.

El uso \_ de D3DSWAPEFFECT FLIPEX en Windows Vista o versiones anteriores del sistema operativo devolverá un error desde [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).

</dd> <dt>

**SwapEffect**
</dt> <dd>

(Solo Windows 7)

El nuevo tipo de efecto de cadena de intercambio de D3DSWAPEFFECT \_ FLIPEX designa cuando una aplicación está adoptando el modo de volteo presente para DWM. Permite a la aplicación un uso más eficaz de la memoria y la capacidad, y también permite a la aplicación aprovechar las estadísticas presentes en modo de pantalla completa en modo de ventana. El comportamiento de la aplicación de pantalla completa no se ve afectado. Si windowed está establecido en **true** y **SwapEffect** se establece en D3DSWAPEFFECT \_ FLIPEX, el tiempo de ejecución crea un búfer de reserva adicional y gira el identificador que pertenece al búfer que se convierte en el búfer frontal en el momento de la presentación.

</dd> <dt>

**Marcas**
</dt> <dd>

(Solo Windows 7)

No se puede establecer la marca de [ \_ búfer de \_ reserva con bloqueos D3DPRESENTFLAG](/windows/desktop/direct3d9/d3dpresentflag) si **SwapEffect** está establecido en el tipo de efecto nueva cadena de intercambio de [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) .

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a>Instrucciones de diseño para aplicaciones de modelo Flip 9Ex de Direct3D

Siga las instrucciones de las secciones siguientes para diseñar las aplicaciones de modelo Flip de Direct3D 9Ex.

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a>Usar el modo de volteo presente en un HWND independiente del modo BLT presente

Las aplicaciones deben usar el modo Flip de Direct3D 9Ex presente en un HWND que no sea también dirigido por otras API, incluido el modo BLT presente Direct3D 9Ex, otras versiones de Direct3D o GDI. El modo de volteo presente se puede usar para presentar a las ventanas secundarias; es decir, las aplicaciones pueden usar Flip Model cuando no está mezclado con el modelo BLT en el mismo HWND, tal y como se muestra en las siguientes ilustraciones.

![Ilustración de la ventana primaria de Direct3D y una ventana secundaria de GDI, cada una con su propio HWND](images/parent-d3d.png)

![Ilustración de la ventana primaria de GDI y una ventana secundaria de Direct3D, cada una con su propio HWND](images/parent-gdi.png)

Dado que el modelo BLT mantiene una copia adicional de la superficie, se pueden agregar GDI y otros contenidos de Direct3D al mismo HWND a través de actualizaciones por etapas de Direct3D y GDI. Con el modelo Flip, solo estará visible el contenido de Direct3D 9Ex en [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) cadenas de intercambio que se pasan a DWM. Se omitirán todas las demás actualizaciones de contenido de la modelo de Direct3D o GDI, tal y como se muestra en las ilustraciones siguientes.

![Ilustración del texto GDI que podría no mostrarse si se usa Flip Model y el contenido de Direct3D y GDI está en el mismo HWND](images/d3d-gdi-same-hwnd.png)

![Ilustración del contenido de Direct3D y GDI en el que DWM está habilitado y la aplicación está en modo de ventana](images/d3d-gdinotext-same-hwnd.png)

Por lo tanto, el modelo de volteo debe estar habilitado para las superficies de búferes de cadena de intercambio en las que el modelo de volteo de Direct3D 9Ex se representa en todo el HWND.

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a>No usar Flip Model con ScrollWindow o ScrollWindowEx de GDI

Algunas aplicaciones de Direct3D 9Ex usan las funciones ScrollWindow o ScrollWindowEx de GDI para actualizar el contenido de la ventana cuando se desencadena un evento de desplazamiento del usuario. ScrollWindow y ScrollWindowEx realizan blts de contenido de la ventana en la pantalla cuando se desplaza una ventana. Estas funciones también requieren las actualizaciones del modelo BLT para el contenido de 9Ex y de GDI. Las aplicaciones que usan cualquiera de las funciones no mostrarán necesariamente el desplazamiento del contenido de la ventana visible en la pantalla cuando la aplicación esté en modo de ventana y se habilite DWM. Se recomienda no usar las API ScrollWindow y ScrollWindowEx de GDI en las aplicaciones y, en su lugar, volver a dibujar el contenido en pantalla en respuesta a un desplazamiento.

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a>Usar una cadena de intercambio de D3DSWAPEFFECT \_ FLIPEX por HWND

Las aplicaciones que utilizan Flip Model no deben usar varias cadenas de intercambio de volteo del modelo que tienen como destino el mismo HWND.

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a>Sincronización de fotogramas de aplicaciones de modelo Flip 9Ex de Direct3D

Las estadísticas presentes son información de temporización de fotogramas que usan las aplicaciones multimedia para sincronizar secuencias de audio y vídeo y recuperarse de problemas de reproducción de vídeo. Para habilitar la disponibilidad de las estadísticas presentes, la aplicación 9Ex de Direct3D debe asegurarse de que el parámetro *BehaviorFlags* que la aplicación pasa a [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contiene la marca de comportamiento del dispositivo [D3DCREATE \_ enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).

Para mayor comodidad, aquí se repite la sintaxis de [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) .

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

El modelo Flip de Direct3D 9Ex agrega la marca de presentación [D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) que aplica el comportamiento de marca de presentación [ \_ \_ inmediata de intervalo de D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) . La aplicación Direct3D 9Ex especifica estas marcas de presentación en el parámetro *dwFlags* que la aplicación pasa a [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), como se muestra aquí.

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

(Solo Windows 7)

Cuando la aplicación establece el miembro **SwapEffect** de [**D3DPRESENT \_ Parameters**](/windows/desktop/direct3d9/d3dpresent-parameters) en [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) en una llamada a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).

</dd> <dt>

[D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

(Solo Windows 7)

Esta marca solo se puede especificar si la aplicación establece el miembro **SwapEffect** de [**D3DPRESENT \_ Parameters**](/windows/desktop/direct3d9/d3dpresent-parameters) en [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) en una llamada a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex). La aplicación puede usar esta marca para actualizar inmediatamente una superficie con varios fotogramas más adelante en la cola de la presentación de DWM, omitiendo básicamente los marcos intermedios.

Las aplicaciones habilitadas para FlipEx en ventanas pueden usar esta marca para actualizar inmediatamente una superficie con un marco que se encuentra más adelante en la cola de presentación de DWM, omitiendo los marcos intermedios. Esto es especialmente útil para las aplicaciones multimedia que desean descartar fotogramas detectados en tiempo de espera y presentan fotogramas posteriores en el momento de la composición. [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) devuelve un error de parámetro no válido si esta marca no se ha especificado correctamente.

</dd> </dl>

Para obtener información de estadísticas presentes, la aplicación obtiene la estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) llamando a la API [**IDirect3DSwapChain9Ex:: GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) .

La estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) contiene estadísticas sobre [**IDirect3DDevice9Ex::P llamadas resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) . El dispositivo se debe crear mediante una llamada a [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) con la marca [D3DCREATE \_ enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) . De lo contrario, los datos devueltos por [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) no están definidos. Una cadena de intercambio 9Ex de Direct3D habilitada para Flip Model proporciona información de estadísticas presentes en los modos de pantalla completa y de ventana.

En el caso de las cadenas de intercambio 9Ex de Direct3D habilitadas para BLT-Model en modo de ventana, todos los valores de estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) serán ceros.

En el caso de las estadísticas presentes en FlipEx, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) devuelve D3DERR \_ \_ estadísticas presentes \_ en las siguientes situaciones:

-   Primera llamada a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) Ever, que indica el principio de una secuencia
-   Transición de DWM de on a OFF
-   Cambio de modo: modo de ventana a o desde pantalla completa o pantalla completa hasta transiciones de pantalla completa

Para mayor comodidad, aquí se repite la sintaxis de [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) .

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

El método [**IDirect3DSwapChain9Ex:: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) devuelve el último PresentCount, es decir, el identificador actual de la última llamada presente correcta realizada por un dispositivo de pantalla que está asociado a la cadena de intercambio. Este identificador actual es el valor del miembro **PresentCount** de la estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) . En el caso de las cadenas de intercambio 9Ex de Direct3D habilitadas para BLT-Model, mientras que en el modo de ventana, todos los valores de estructura **D3DPRESENTSTATS** serán ceros.

Para mayor comodidad, aquí se repite la sintaxis de [**IDirect3DSwapChain9Ex:: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) .

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

Al modificar la aplicación Direct3D 9Ex para Windows 7, debe tener en cuenta la siguiente información sobre la estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) :

-   El valor PresentCount que devuelve [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) no se actualiza cuando una llamada [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT \_ DONOTWAIT especificada en el parámetro *dwFlags* devuelve un error.
-   Cuando se llama a [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT \_ DONOTFLIP, una llamada a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) se realiza correctamente, pero no devuelve una estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) actualizada cuando la aplicación está en modo de ventana.
-   **PresentRefreshCount** frente a **SyncRefreshCount** en [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):
    -   **PresentRefreshCount** es igual a **SyncRefreshCount** cuando la aplicación presenta en cada VSYNC.
    -   **SyncRefreshCount** se obtiene en el intervalo de VSYNC cuando se envió el presente, **SyncQPCTime** es aproximadamente el tiempo asociado con el intervalo de VSYNC.

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

Cuando DWM está desactivado, las aplicaciones en ventanas se muestran directamente en la pantalla del monitor sin pasar por una cadena de volteo. En Windows Vista, no se admite la obtención de información de estadísticas de fotogramas para aplicaciones en ventanas cuando DWM está desactivado. Para mantener una API en la que las aplicaciones no necesitan ser compatibles con DWM, Windows 7 devolverá información de estadísticas de fotogramas para aplicaciones en ventanas cuando DWM esté desactivado. Las estadísticas de fotogramas que se devuelven cuando DWM es OFF solo se estiman.

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a>Walk-Through de un modelo Flip 9Ex de Direct3D y el ejemplo present Statistics

**Para participar en el ejemplo de presentación de FlipEx para Direct3D 9Ex**

1.  Asegúrese de que la aplicación de ejemplo se está ejecutando en la versión del sistema operativo Windows 7 o posterior.
2.  Establezca el miembro **SwapEffect** de [**D3DPRESENT \_ Parameters**](/windows/desktop/direct3d9/d3dpresent-parameters) en [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) en una llamada a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).


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



**Para participar también en FlipEx estadísticas presentes asociadas para el ejemplo de 9Ex de Direct3D**

-   Establezca [D3DCREATE \_ enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) en el parámetro *BehaviorFlags* de [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).


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

1.  Llamadas de la cola presente: el número de búferes de reserva recomendado es de 2 a 4.
2.  El ejemplo Direct3D 9Ex agrega un búfer de reserva implícito, la longitud actual de la cola actual es el número de búferes de reserva + 1.
3.  Crear la estructura de cola de la aplicación auxiliar para almacenar todos los IDENTIFICADOres actuales del presente (PresentCount) enviados correctamente y asociados, calculados o esperados, PresentRefreshCount.
4.  Para detectar la ocurrencia del problema:

    -   Llame a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).
    -   Obtiene el identificador actual (PresentCount) y el recuento de VSYNC en el que se muestra el fotograma (PresentRefreshCount) del marco cuyas estadísticas presentes se obtienen.
    -   Recupere el PresentRefreshCount esperado (TargetRefresh en el código de ejemplo) asociado al identificador actual.
    -   Si la PresentRefreshCount real es posterior a la esperada, se ha producido un problema.

5.  Para recuperarse de un problema:

    -   Calcular el número de fotogramas que se van a omitir (g \_ iImmediates variable en el código de ejemplo).
    -   Presente los marcos omitidos con Interval D3DPRESENT \_ FORCEIMMEDIATE.

**Consideraciones sobre la detección y recuperación de problemas**

1.  La recuperación con problemas toma la variable N (g \_ iQueueDelay en el código de ejemplo) del número de llamadas presentes, donde N (g \_ iQueueDelay) es igual a g \_ iImmediates más la longitud de la cola actual, es decir:

    -   Omitir fotogramas con el intervalo presente D3DPRESENT \_ FORCEIMMEDIATE, más
    -   Queued presenta que debe procesarse

2.  Establezca un límite en la longitud del problema ( \_ \_ límite de recuperación por problema en el ejemplo). Si la aplicación de ejemplo no puede recuperarse de un problema que es demasiado largo (por ejemplo, 1 segundo o 60 vsyncs en el monitor de 60 Hz), salte la animación intermitente y restablezca la cola del ayudante actual.


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

-   En la ilustración siguiente se muestra una aplicación con el recuento de búferes de reserva de 4. Por lo tanto, la longitud actual de la cola es 5.

    ![Ilustración de un applicas representado frames y present Queue](images/sample-scenario.png)

    El marco a está destinada a pasar a la pantalla en el recuento de intervalos de sincronización de 1, pero se detectó que se mostró en el recuento de intervalos de sincronización de 4. Por lo tanto, se ha producido un problema. Los 3 fotogramas siguientes se presentan con el intervalo de D3DPRESENT \_ \_ FORCEIMMEDIATE. El problema debe llevar un total de 8 llamadas presentes antes de que se recuperen: el siguiente fotograma se mostrará según el número de intervalos de sincronización de destino.

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a>Resumen de las recomendaciones de programación para la sincronización de fotogramas

-   Cree una lista de copia de seguridad de todos los identificadores de LastPresentCount (obtenidos a través de [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) y el PresentRefreshCount Estimado asociado de todas las presentaciones enviadas.
    > [!Note]  
    > Cuando la aplicación llama a [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT \_ DONOTFLIP, la llamada [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) se realiza correctamente, pero no devuelve una estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) actualizada cuando la aplicación está en modo de ventana.

     

-   Llame a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) para obtener el PresentRefreshCount real asociado a cada identificador presente de los fotogramas mostrados, para asegurarse de que la aplicación controla las devoluciones de errores de la llamada.
-   Si PresentRefreshCount real es posterior a la estimación de PresentRefreshCount, se detecta un problema. Compensar enviando fotogramas atrasados con D3DPRESENT \_ FORCEIMMEDIATE.
-   Cuando un fotograma se presenta en la cola actual, todos los fotogramas en cola subsiguientes se presentarán en tiempo de espera. D3DPRESENT \_ FORCEIMMEDIATE corregirá solo el siguiente fotograma que se presentará después de todos los marcos en cola. Por lo tanto, la cola actual o el número de búferes de reserva no deben ser demasiado largos, por lo que hay menos problemas de fotogramas con los que ponerse al día. El número de búferes de reserva óptimo es de 2 a 4.
-   Si el PresentRefreshCount Estimado es posterior al PresentRefreshCount real, es posible que se haya producido una limitación de DWM. Las siguientes soluciones son posibles:

    -   reducción de la longitud de la cola actual
    -   reducir los requisitos de memoria de GPU con cualquier otro medio además de reducir la longitud de la cola actual (es decir, reducir la calidad, quitar efectos, etc.)
    -   especificar [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) para evitar la limitación DWM en general

-   Compruebe la funcionalidad de presentación de la aplicación y el rendimiento de las estadísticas de fotogramas en los escenarios siguientes:

    -   con DWM activado y desactivado
    -   modos exclusivo y en ventana de pantalla completa
    -   hardware de funcionalidad inferior

-   Cuando las aplicaciones no pueden recuperarse de un gran número de fotogramas con problemas con D3DPRESENT \_ FORCEIMMEDIATE presentes, pueden realizar las siguientes operaciones:

    -   reduzca el uso de la CPU y la GPU mediante la representación de menos carga de trabajo.
    -   en el caso de la descodificación de vídeo, descodifique más rápido reduciendo la calidad y, por lo tanto, el uso de la CPU y la GPU.

## <a name="conclusion-about-direct3d-9ex-improvements"></a>Conclusión sobre las mejoras de Direct3D 9Ex

En Windows 7, las aplicaciones que muestran la velocidad de fotogramas de vídeo o medidor durante la presentación pueden optar por voltear el modelo. Las mejoras presentes en las estadísticas asociadas a Flip Model Direct3D 9Ex pueden beneficiar a las aplicaciones que sincronizan la presentación por velocidad de fotogramas, con comentarios en tiempo real para la detección y recuperación de problemas. Los desarrolladores que adopten el modelo Flip 9Ex de Direct3D deben tener en cuenta un HWND independiente del contenido GDI y la sincronización de la velocidad de fotogramas. Consulte los detalles de este tema y la documentación de MSDN. Para obtener documentación adicional, consulte el [Centro para desarrolladores de DirectX en MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).

## <a name="call-to-action"></a>Pasar a la acción

Le recomendamos que use Direct3D 9Ex Flip Model y sus estadísticas presentes en Windows 7 cuando cree aplicaciones que intenten sincronizar la velocidad de fotogramas de presentación o recuperarse de los problemas de visualización.

## <a name="related-topics"></a>Temas relacionados

[Centro para desarrolladores de DirectX en MSDN](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> </dl>