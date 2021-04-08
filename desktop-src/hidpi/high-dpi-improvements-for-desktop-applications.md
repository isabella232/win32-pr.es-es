---
title: Mixed-Mode de escala de PPP y las API que reconocen PPP
description: .
ms.assetid: 44AC0B29-3283-4801-90F5-3E78CCD87B9F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9f8a8f72b199aaba195002134855155925b30d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995122"
---
# <a name="mixed-mode-dpi-scaling-and-dpi-aware-apis"></a>Mixed-Mode de escala de PPP y las API que reconocen PPP

## <a name="sub-process-dpi-awareness-support"></a>Compatibilidad con reconocimiento de PPP de Sub-Process

[**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) habilita el uso de diferentes modos de escala de PPP dentro de un único proceso. Antes de la actualización de aniversario de Windows 10, se ha enlazado un reconocimiento de PPP de ventana con el modo de reconocimiento de PPP para todo el proceso (no es consciente de PPP, reconocimiento de PPP del sistema o reconocimiento de PPP Per-Monitor). Pero ahora, con **SetThreadDpiAwarenessContext**, las ventanas de nivel superior pueden tener un modo de reconocimiento de PPP diferente del modo de reconocimiento de PPP para todo el proceso. Esto también afecta a las ventanas secundarias, ya que siempre tendrán el mismo modo de reconocimiento de PPP que su ventana primaria.

El uso de **SetThreadDpiAwarenessContext** permite a los desarrolladores decidir dónde desean centrar sus esfuerzos de desarrollo al definir un comportamiento específico de PPP para las aplicaciones de escritorio. Por ejemplo, la ventana principal de nivel superior de una aplicación se puede escalar por monitor, mientras que las ventanas secundarias de nivel superior podrían escalarse a través del sistema operativo mediante el escalado de mapa de bits.

## <a name="the-dpi-awareness-context"></a>El contexto de reconocimiento de PPP

Antes de la disponibilidad de **SetThreadDpiAwarenessContext** , el reconocimiento de PPP de un proceso se definió en el manifiesto del archivo binario de la aplicación o mediante una llamada a [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) durante la inicialización del proceso. Con **SetThreadDpiAwarenessContext**, cada subproceso puede tener un contexto de reconocimiento de PPP individual que puede ser diferente del modo de reconocimiento de PPP en todo el proceso. El contexto de reconocimiento de PPP de un subproceso se representa con el tipo de reconocimiento de reconocimiento * * * * [PPP \_ \_ *](dpi-awareness-context.md) * * * y se comporta de las siguientes maneras:

-   Un subproceso puede tener su contexto de reconocimiento de PPP cambiado en cualquier momento.
-   Cualquier llamada API que se realice después de cambiar el contexto se ejecutará en el contexto de PPP correspondiente (y se puede virtualizar).
-   Cuando se crea una ventana, su reconocimiento de PPP se define como el reconocimiento de PPP del subproceso de llamada en ese momento.
-   Cuando se llama al procedimiento de ventana de una ventana, el subproceso se cambia automáticamente al contexto de reconocimiento de PPP que estaba en uso al crear la ventana.

Un escenario común para el uso de **SetThreadDpiAwarenessContext** es el siguiente: comenzar con un subproceso que se ejecuta con un contexto (por ejemplo, el **contexto de reconocimiento de PPP \_ \_ \_ por \_ monitor \_**) se cambia temporalmente a un contexto diferente (no se reconoce el contexto de reconocimiento de PPP), se crea una ventana y, a continuación, se vuelve a cambiar inmediatamente el contexto del subproceso a su estado anterior.**\_ \_ \_** La ventana creada tendrá un contexto de PPP de **contexto de reconocimiento de PPP \_ \_ \_ inconsciente**, mientras que el contexto del subproceso que realiza la llamada se restaurará a un **contexto de reconocimiento de PPP \_ \_ \_ por \_ monitor \_** , con una llamada subsiguiente a **SetThreadDpiAwarenessContext**. En este escenario, la ventana asociada con el subproceso que realiza la llamada se ejecutaría con un contexto por monitor (y, por lo tanto, no se ajustará al mapa de bits por el sistema operativo), mientras que la ventana recién creada no tenía reconocimiento de PPP (y, por lo tanto, se ajustaría automáticamente el mapa de bits en un conjunto de pantallas para 100 >el escalado

La figura 1 muestra cómo se ejecuta el subproceso de proceso principal con el **contexto de reconocimiento de PPP \_ \_ \_ por \_ monitor**, cambia su contexto a un **contexto de reconocimiento de PPP no \_ \_ \_ compatible** y crea una nueva ventana. A continuación, la ventana recién creada se ejecuta con un contexto de reconocimiento de PPP de **contexto de reconocimiento de PPP sin tener en \_ \_ \_ cuenta** cuando se envía un mensaje a él o cuando se realizan llamadas a la API. Inmediatamente después de crear la nueva ventana, el subproceso principal se restaura a su contexto anterior de **contexto de reconocimiento de PPP \_ \_ \_ por \_ monitor**.

![diagrama que muestra el reconocimiento de PPP por monitor en acción](images/dpi-awareness-context.png)

## <a name="new-dpi-related-apis"></a>Nuevas API relacionadas con DPI

Además de la compatibilidad con los distintos modos de reconocimiento de PPP dentro de un único proceso que **SetThreadDpiAwarenessContext** ofrece, se ha agregado la siguiente funcionalidad específica de PPP para las aplicaciones de escritorio:<dl> <dd>[EnableNonClientDpiScaling****](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)<dl> <dt>



> [!Note]  
> El modo de reconocimiento de PPP **por monitor V2** habilita automáticamente esta funcionalidad y, por lo tanto, la llamada a **EnableNonClientDpiScaling** no es necesaria en las aplicaciones que la usan.

 

La llamada a **EnableNonClientDpiScaling** desde dentro de un controlador de Windows s **WM \_ NCCREATE** dará lugar a que el área no cliente de una ventana de nivel superior se ajuste automáticamente al valor de PPP. Si la ventana de nivel superior tiene en cuenta el reconocimiento de PPP por monitor (ya sea porque el propio proceso tiene reconocimiento de PPP por monitor o porque la ventana se ha creado en un subproceso con reconocimiento de PPP por monitor), la barra de título, las barras de desplazamiento, los menús y las barras de menús de estas ventanas tendrán una escala de PPP cada vez que cambie la ventana.
</dt> <dt>

Tenga en cuenta que las áreas que no son de cliente de una ventana secundaria, como las barras de desplazamiento que no son de cliente de un control de edición secundario, no reducirán automáticamente la escala de PPP cuando se use esta API.
</dt> <dt>

> [!Note]  
> Se debe llamar a **EnableNonClientDpiScaling** desde el controlador de **\_ NCCREATE de WM** .

</dt> </dl> </dd> <dd> <b> Las API de * ForDpi </b>

-   Varias API usadas con frecuencia, como [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) , no tienen ningún contexto de HWND y, por lo tanto, no tienen ninguna manera de deducir el reconocimiento de PPP adecuado para sus valores devueltos. Llamar a estas API desde un subproceso que se está ejecutando en un modo o contexto de reconocimiento de PPP diferente puede devolver valores que no se ajustan al contexto del subproceso que realiza la llamada. [* * * * GetSystemMetricForDpi * *](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)* *, [* * * * SystemParametersInfoForDpi * *](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)* *, y [* * * * AdjustWindowRectExForDpi *](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) * * * realizará la misma funcionalidad que sus homólogos sin reconocimiento de PPP, pero toma un DPI como argumento e infiere el reconocimiento de PPP del contexto del subproceso actual.
-   **GetSystemMetricForDpi** y **SystemParametersInfoForDpi** devolverán valores de métricas del sistema con escala de PPP y valores de parámetros del sistema de acuerdo con esta ecuación:

    |                                                                 |
    |-----------------------------------------------------------------|
    | GetSystemMetrics (...) @ DPI = = GetSystemMetricsForDpi (..., DPI) |

    

     

    Por lo tanto, al llamar a **GetSystemMetrics** (o **SystemParametersInfoForDpi**), mientras se ejecuta en un dispositivo con un determinado valor de PPP del sistema, se devolverá el mismo valor que sus variantes que reconocen PPP (**GetSystemMetricsForDpi** y **SystemParametersInfoForDpi**), dado el mismo valor de PPP que la entrada.

-   [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) toma un HWND y calcula el tamaño necesario del rectángulo de una ventana con distinción de PPP.

</dd> <dd>

</dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow">GetDpiForWindow</a></b><dl> <dt><b>GetDpiForWindow</b> devolverá el valor de PPP asociado al HWND proporcionado. La respuesta dependerá del modo de reconocimiento de PPP del HWND:

| Modo de reconocimiento de PPP de HWND | Valor devuelto                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Consciente                    | 96                                                                                                                                                                                                            |
| System                     | PPP del sistema                                                                                                                                                                                                |
| Per-Monitor                | El PPP de la pantalla en la que se encuentra principalmente la ventana de nivel superior asociada <br/> (Si se proporciona una ventana secundaria, se devolverá el PPP de la ventana primaria de nivel superior correspondiente)<br/> |

</dt> </dl> </dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem">GetDpiForSystem</a></b><dl> <dt>

Llamar a **GetDpiForSystem** es más eficaz que llamar a [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) y [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) para obtener el PPP del sistema.
</dt> <dt>

Cualquier componente que pueda ejecutarse en una aplicación que utilice el reconocimiento de PPP de subproceso no debe suponer que el PPP del sistema es estático durante el ciclo de vida del proceso. Por ejemplo, si un subproceso que se ejecuta con el contexto de reconocimiento de **PPP que \_ \_ \_ contenga** contexto de conocimiento no compatible consulta el PPP del sistema, la respuesta será 96. Sin embargo, si el mismo subproceso cambió al contexto de reconocimiento **\_ \_ \_ del sistema de contexto de reconocimiento de PPP** y vuelve a consultar el PPP del sistema, la respuesta podría ser diferente. Para evitar el uso de un valor de PPP del sistema (y posiblemente obsoleto) en caché, use **GetDpiForSystem** para recuperar el valor de PPP del sistema en relación con el modo de reconocimiento de PPP del subproceso que realiza la llamada. 
</dt> </dl> </dd> </dl>