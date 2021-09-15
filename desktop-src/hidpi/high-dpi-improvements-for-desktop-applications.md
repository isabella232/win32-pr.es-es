---
title: Mixed-Mode DE ESCALADO DE PPP y API con reconocimiento de PPP
description: Mixed-Mode DE ESCALADO DE PPP y API con reconocimiento de PPP
ms.assetid: 44AC0B29-3283-4801-90F5-3E78CCD87B9F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f5b16e4c438cfe1f0d04e61524899e213b25ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474281"
---
# <a name="mixed-mode-dpi-scaling-and-dpi-aware-apis"></a>Mixed-Mode DE ESCALADO DE PPP y API con reconocimiento de PPP

## <a name="sub-process-dpi-awareness-support"></a>Sub-Process reconocimiento de PPP

[**SetThreadDpiAwarenessContext permite**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) el uso de diferentes modos de escalado de PPP dentro de un único proceso. Antes de la actualización de aniversario de Windows 10, el reconocimiento de PPP de una ventana estaba enlazado al modo de reconocimiento de PPP en todo el proceso (PPP no consciente, compatible con PPP del sistema o Per-Monitor reconocimiento de PPP). Pero ahora, con **SetThreadDpiAwarenessContext,** las ventanas de nivel superior pueden tener un modo de reconocimiento de PPP diferente del modo de reconocimiento de PPP para todo el proceso. Esto también afecta a las ventanas secundarias, ya que siempre tendrán el mismo modo de reconocimiento de PPP que su ventana primaria.

El uso de **SetThreadDpiAwarenessContext** permite a los desarrolladores decidir dónde quieren centrar sus esfuerzos de desarrollo al definir el comportamiento específico de PPP para las aplicaciones de escritorio. Por ejemplo, la ventana de nivel superior principal de una aplicación se podría escalar por monitor, mientras que el sistema operativo podría escalar las ventanas secundarias de nivel superior mediante el escalado de mapas de bits.

## <a name="the-dpi-awareness-context"></a>Contexto de reconocimiento de PPP

Antes de la disponibilidad de **SetThreadDpiAwarenessContext,** el reconocimiento de PPP de un proceso se definió en el manifiesto del binario de la aplicación o mediante una llamada a [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) durante la inicialización del proceso. Con **SetThreadDpiAwarenessContext,** cada subproceso puede tener un contexto de reconocimiento de PPP individual que puede ser diferente del modo de reconocimiento de PPP en todo el proceso. El contexto de reconocimiento de PPP de un subproceso se representa con el tipo [*:CONTEXTO DE RECONOCIMIENTO DE \_ \_ PPP*"](dpi-awareness-context.md) y se comporta de las maneras siguientes:

-   Un subproceso puede cambiar su contexto de reconocimiento de PPP en cualquier momento.
-   Las llamadas API que se realizan después de cambiar el contexto se ejecutarán en el contexto de PPP correspondiente (y se pueden virtualizar).
-   Cuando se crea una ventana, su reconocimiento de PPP se define como el reconocimiento de PPP del subproceso que realiza la llamada en ese momento.
-   Cuando se llama al procedimiento de ventana para una ventana, el subproceso cambia automáticamente al contexto de reconocimiento de PPP que estaba en uso cuando se creó la ventana.

Un escenario común para el uso de **SetThreadDpiAwarenessContext** es el siguiente: Comience con un subproceso que se ejecuta con un contexto (por ejemplo, CONTEXTO DE RECONOCIMIENTO DE **PPP PER MONITOR \_ \_ \_ \_ \_ AWARE**) cambie temporalmente a un contexto diferente (CONTEXTO DE RECONOCIMIENTO DE **PPP \_ \_ \_ UNAWARE),** cree una ventana y, a continuación, vuelva a cambiar inmediatamente el contexto del subproceso a su estado anterior. La ventana creada tendrá un contexto de PPP de CONTEXTO DE RECONOCIMIENTO DE **PPP \_ \_ \_ UNAWARE**, mientras que el contexto del subproceso que realiza la llamada se restaurará a CONTEXTO DE RECONOCIMIENTO DE **PPP PER MONITOR \_ \_ \_ \_ \_ AWARE** con una llamada posterior a **SetThreadDpiAwarenessContext**. En este escenario, la ventana asociada al subproceso que realiza la llamada se ejecutaría con un contexto por monitor (y, por lo tanto, el sistema operativo no ajustaría el mapa de bits), mientras que la ventana recién creada no sería compatible con PPP (y, por lo tanto, se ajustaría automáticamente el mapa de bits en un conjunto de pantalla >escala al 100 %).

En la figura 1 se muestra cómo se ejecuta el subproceso de proceso principal con EL CONTEXTO DE RECONOCIMIENTO DE **PPP \_ POR \_ \_ \_ MONITOR,** cambia su contexto a CONTEXTO DE RECONOCIMIENTO DE **PPP \_ \_ \_ UNAWARE** y crea una nueva ventana. A continuación, la ventana recién creada se ejecuta con un contexto de reconocimiento de PPP de CONTEXTO DE RECONOCIMIENTO DE **PPP \_ \_ \_ UNAWARE** cada vez que se le envía un mensaje o se realizan llamadas API desde él. Inmediatamente después de crear la nueva ventana, el subproceso principal se restaura a su contexto anterior de **CONTEXTO DE RECONOCIMIENTO DE PPP POR \_ \_ \_ \_ MONITOR.**

![diagrama que muestra el reconocimiento de ppp por monitor en acción](images/dpi-awareness-context.png)

## <a name="new-dpi-related-apis"></a>Nuevas API relacionadas con PPP

Además de la compatibilidad con diferentes modos de reconocimiento de PPP dentro de un único proceso que **ofrece SetThreadDpiAwarenessContext,** se ha agregado la siguiente funcionalidad específica de PPP para las aplicaciones de escritorio:<dl> <dd>[EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)<dl> <dt>



> [!Note]  
> El modo de reconocimiento de PPP por monitor **V2** habilita automáticamente esta funcionalidad y, por tanto, no es necesario llamar a **EnableNonClientDpiScaling** en las aplicaciones que la usan.

 

Al llamar a **EnableNonClientDpiScaling** desde dentro del controlador **\_ WM NCCREATE** de una ventana, el área no cliente de una ventana de nivel superior se escalará automáticamente para PPP. Si la ventana de nivel superior es compatible con PPP por monitor (ya sea porque el propio proceso es compatible con PPP por monitor o porque la ventana se creó dentro de un subproceso compatible con PPP por monitor), la barra de subtítulos, las barras de desplazamiento, los menús y las barras de menú de estas ventanas escalarán ppp cada vez que cambie el VALOR DE PPP de la ventana.
</dt> <dt>

Tenga en cuenta que las áreas que no son cliente de una ventana secundaria, como las barras de desplazamiento que no son de cliente de un control de edición secundario, no escalarán ppp automáticamente cuando se utilice esta API.
</dt> <dt>

> [!Note]  
> **Se debe llamar a EnableNonClientDpiScaling** desde el **controlador \_ NCCREATE de WM.**

</dt> </dl> </dd> <dd> <b> Las API *ForDpi </b>

-   Varias API usadas con frecuencia, como [**GetSystemMetrics,**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) no tienen ningún contexto de HWND y, por lo tanto, no tienen ninguna manera de inducir el reconocimiento de PPP adecuado para sus valores devueltos. Llamar a estas API desde un subproceso que se ejecuta en un contexto o modo de reconocimiento de PPP diferente puede devolver valores que no se escalan para el contexto del subproceso que realiza la llamada. [***GetSystemMetricForDpi*,***SystemParametersInfoForDpi**](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)y [***AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) realizarán la misma funcionalidad que sus homólogos sin reconocimiento de PPP, pero tomarán un VALOR DE PPP como argumento e deducirán el reconocimiento de ppp del contexto del subproceso actual. [](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)
-   **GetSystemMetricForDpi** y **SystemParametersInfoForDpi** devolverán valores de métricas del sistema con escalado de PPP y valores de parámetros del sistema de acuerdo con esta ecuación:

    
    GetSystemMetrics(...) @ ppp == GetSystemMetricsForDpi(..., ppp)

    

     

    Por lo tanto, al llamar a **GetSystemMetrics** (o **SystemParametersInfoForDpi),** mientras se ejecuta en un dispositivo con un determinado valor de PPP del sistema, se devolverá el mismo valor que sus variantes con reconocimiento de PPP **(GetSystemMetricsForDpi** y **SystemParametersInfoForDpi),** dado el mismo valor de PPP que la entrada.

-   [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) toma un HWND y calculará el tamaño necesario de un rectángulo de ventana de una manera sensible a PPP.

</dd> <dd>

</dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow">GetDpiForWindow</a></b><dl> <dt><b>GetDpiForWindow devolverá</b> el valor de PPP asociado al HWND proporcionado. La respuesta dependerá del modo de reconocimiento de PPP del HWND:

| Modo de reconocimiento de PPP de HWND | Valor devuelto                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Conscientes                    | 96                                                                                                                                                                                                            |
| Sistema                     | Ppp del sistema                                                                                                                                                                                                |
| Per-Monitor                | Ppp de la pantalla en la que se encuentra principalmente la ventana de nivel superior asociada <br/> (Si se proporciona una ventana secundaria, se devolverá el valor de PPP de la ventana primaria de nivel superior correspondiente).<br/> |

</dt> </dl> </dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem">GetDpiForSystem</a></b><dl> <dt>

Llamar **a GetDpiForSystem es** más eficaz que llamar a [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) y [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) para obtener el ppp del sistema.
</dt> <dt>

Cualquier componente que pueda estar ejecutándose en una aplicación que use reconocimiento de PPP del sub process no debe suponer que el PPP del sistema es estático durante el ciclo de vida del proceso. Por ejemplo, si un subproceso que se ejecuta en CONTEXTO DE RECONOCIMIENTO DE **PPP \_ \_ \_ UNWARE** consulta el VALOR DE PPP del sistema, la respuesta será 96. Sin embargo, si ese mismo subproceso cambia al contexto de reconocimiento del SISTEMA DE RECONOCIMIENTO DE PPP y vuelve a consultar el VALOR DE PPP del sistema, la respuesta podría ser diferente. **\_ \_ \_** Para evitar el uso de un valor de PPP del sistema almacenado en caché (y posiblemente obsoleto), use **GetDpiForSystem** para recuperar el VALOR DE PPP del sistema con respecto al modo de reconocimiento de PPP del subproceso que realiza la llamada. 
</dt> </dl> </dd> </dl>
