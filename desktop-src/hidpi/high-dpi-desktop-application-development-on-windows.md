---
title: Desarrollo de aplicaciones de escritorio con valores altos de PPP en Windows
description: Este contenido está dirigido a desarrolladores que buscan actualizar aplicaciones de escritorio para controlar el factor de escala de pantalla dinámica (también es decir,
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c6389553ce2265752e3552fdaaf848e3ac70eede8df3b4fd9e560861bf15f33d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036262"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a>Desarrollo de aplicaciones de escritorio con valores altos de PPP en Windows

Este contenido está dirigido a desarrolladores que buscan actualizar las aplicaciones de escritorio para controlar dinámicamente los cambios del factor de escala de pantalla (puntos por pulgada o PPP), lo que permite que sus aplicaciones estén nítidas en cualquier pantalla en la que se representen.

Para empezar, si va a crear una nueva aplicación Windows desde cero, se recomienda encarecidamente crear una aplicación de plataforma Windows universal [(UWP).](/windows/uwp/get-started/whats-a-uwp) Las aplicaciones para UWP se escalan de forma automática y dinámica para cada pantalla en la &mdash; &mdash; que se ejecutan.

Las aplicaciones de escritorio que usan tecnologías de programación de Windows anteriores (programación sin procesar de Win32, Windows Forms, Windows Presentation Framework (WPF), etc.) no pueden controlar automáticamente el escalado de PPP sin trabajo adicional del desarrollador. Sin este trabajo, las aplicaciones aparecerán desenfoque o con un tamaño incorrecto en muchos escenarios de uso comunes. En este documento se proporciona contexto e información sobre lo que implica actualizar una aplicación de escritorio para que se represente correctamente.

## <a name="display-scale-factor--dpi"></a>Mostrar factor de escala & PPP

A medida que ha progresado la tecnología de visualización, los fabricantes de paneles de pantalla han empaquetado un número creciente de píxeles en cada unidad de espacio físico en sus paneles. Esto ha dado lugar a que los puntos por pulgada (PPP) de los paneles de pantalla modernos sean mucho más altos de lo que han sido históricamente. En el pasado, la mayoría de las pantallas tenían 96 píxeles por pulgada lineal de espacio físico (96 PPP); en 2017, las pantallas con casi 300 PPP o superior están disponibles.

La mayoría de los marcos de interfaz de usuario de escritorio heredados tienen suposiciones integradas de que el ppp de visualización no cambiará durante la vigencia del proceso.  Esta suposición ya no es cierta, ya que las DPI de pantalla normalmente cambian varias veces a lo largo de la duración de un proceso de aplicación. Algunos escenarios comunes en los que el factor de escala de pantalla o los cambios de PPP son:

-   Configuraciones de varios monitores en las que cada pantalla tiene un factor de escala diferente y la aplicación se mueve de una pantalla a otra (por ejemplo, una pantalla de 4K y una pantalla de 1080p).
-   Acoplamiento y desacoplamiento de un portátil con valores altos de PPP con una pantalla externa de bajo PPP (o viceversa)
-   Conexión mediante Escritorio remoto desde un portátil o tableta con valores altos de PPP a un dispositivo de bajo ppp (o viceversa)
-   Realizar un cambio en la configuración del factor de escalado de pantalla mientras se ejecutan las aplicaciones

En estos escenarios, las aplicaciones para UWP se dibujan automáticamente para el nuevo PPP. De forma predeterminada, y sin trabajo adicional del desarrollador, las aplicaciones de escritorio no lo hacen. Las aplicaciones de escritorio que no hacen este trabajo adicional para responder a los cambios de PPP pueden parecer desenfocados o con un tamaño incorrecto para el usuario.

## <a name="dpi-awareness-mode"></a>Modo de reconocimiento de PPP

Las aplicaciones de escritorio deben Windows si admiten el escalado de PPP. De forma predeterminada, el sistema considera que las aplicaciones de escritorio no son conscientes de ppp y que el mapa de bits extiende sus ventanas. Al establecer uno de los siguientes modos de reconocimiento de PPP disponibles, las aplicaciones pueden Windows cómo desean controlar el escalado de PPP:

### <a name="dpi-unaware"></a>PPP no consciente

Las aplicaciones sin reconocimiento de PPP se representan con un valor de PPP fijo de 96 (100 %). Siempre que estas aplicaciones se ejecuten en una pantalla con una escala de pantalla superior a 96 PPP, Windows ajustará el mapa de bits de la aplicación al tamaño físico esperado. Esto hace que la aplicación aparezca desenfoque.

### <a name="system-dpi-awareness"></a>Reconocimiento de PPP del sistema

Las aplicaciones de escritorio que tienen reconocimiento de PPP del sistema normalmente reciben el valor de PPP del monitor conectado principal en el momento del inicio de sesión del usuario. Durante la inicialización, la interfaz de usuario se encuentra correctamente (controles de tamaño, elección de tamaños de fuente, carga de recursos, etc.) con ese valor de PPP del sistema. Por lo tanto, las aplicaciones con reconocimiento de PPP del sistema no se escalan con PPP (mapa de bits extendido) Windows en las pantallas que se muestran en ese solo PPP. Cuando la aplicación se mueve a una pantalla con un factor de escala diferente, o si el factor de escala de pantalla cambia, Windows escalará las ventanas de la aplicación, lo que hará que parezcan desenfoque. De forma eficaz, las aplicaciones de escritorio con reconocimiento de PPP del sistema solo se representan de forma nítida en un único factor de escala de pantalla, desenfocándose cada vez que cambia el ppp.

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a>Per-Monitor y Per-Monitor reconocimiento de PPP (V2)

Se recomienda actualizar las aplicaciones de escritorio para usar el modo de reconocimiento de PPP por monitor, lo que les permite representarse inmediatamente correctamente cada vez que cambia el valor de PPP. Cuando una aplicación informa Windows que quiere ejecutarse en este modo, Windows no ajustará el mapa de bits de la aplicación cuando cambie el valor de PPP, en su lugar enviará [WM \_ PPPCHANGED](wm-dpichanged.md) a la ventana de la aplicación. A continuación, es responsabilidad completa de la aplicación controlar el ajuste de tamaño para el nuevo PPP. La mayoría de los marcos de interfaz de usuario que usan las aplicaciones de escritorio (controles comunes de Windows (comctl32), Windows Forms, Windows Presentation Framework, etc.) no admiten el escalado automático de PPP, lo que requiere que los desarrolladores cambien el tamaño y cambien la posición del contenido de sus propias ventanas.

Hay dos versiones de Per-Monitor que una aplicación puede registrarse como: versión 1 y versión 2 (PMv2). Al registrar un proceso como en ejecución en el modo de reconocimiento PMv2, se produce lo siguiente:

1.  La aplicación a la que se notifica cuando cambia el VALOR DE PPP (hwnd de nivel superior y secundario)
2.  La aplicación que ve los píxeles sin procesar de cada pantalla
3.  Nunca se escala el mapa de bits de la aplicación Windows
4.  Área no cliente automática (título de ventana, barras de desplazamiento, etc.) Escalado de PPP Windows
5.  Los cuadros de diálogo de Win32 (desde [CreateDialog)](/windows/desktop/api/winuser/nf-winuser-createdialogw)escalan automáticamente los valores de PPP Windows
6.  Recursos de mapa de bits dibujados con tema en controles comunes (casillas, fondos de botón, etc.) que se representan automáticamente en el factor de escala de PPP adecuado

Cuando se ejecuta en Per-Monitor de reconocimiento v2, las aplicaciones se notifican cuando su PPP ha cambiado. Si una aplicación no cambia de tamaño para el nuevo PPP, la interfaz de usuario de la aplicación aparecerá demasiado pequeña o demasiado grande (dependiendo de la diferencia en los valores de PPP anteriores y nuevos).

> [!Note]  
> Per-Monitor v1 (PMv1) es muy limitado. Se recomienda que las aplicaciones usen PMv2.

En la tabla siguiente se muestra cómo se representarán las aplicaciones en distintos escenarios:

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Modo de reconocimiento de PPP</th>
<th>Windows Versión introducida</th>
<th>Vista de PPP de la aplicación</th>
<th>Comportamiento en cambio de PPP</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Conscientes</td>
<td>N/D</td>
<td>Todas las pantallas tienen 96 PPP</td>
<td>Extensión de mapa de bits (desenfoque)</td>
</tr>
<tr class="even">
<td>Sistema</td>
<td>Vista</td>
<td>Todas las pantallas tienen el mismo PPP (el ppp de la pantalla principal en el momento en que se inició la sesión de usuario actual)</td>
<td>Extensión de mapa de bits (desenfoque)</td>
</tr>
<tr class="odd">
<td>Per-Monitor</td>
<td>8.1</td>
<td>Ppp de la pantalla en la que se encuentra principalmente la ventana de la aplicación</td>
<td><ul>
<li>Se notifica a HWND de nivel superior el cambio de PPP.</li>
<li>Sin escalado de PPP de ningún elemento de la interfaz de usuario.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Per-Monitor V2</td>
<td>Windows 10 Creators Update (1703)</td>
<td>Ppp de la pantalla en la que se encuentra principalmente la ventana de la aplicación</td>
<td><ul>
<li>Se notifica a <span class="underline">los</span> HWND de nivel superior y secundario el cambio de PPP.</li>
</ul>
<br/> <span class="underline">Escalado automático de PPP de:</span>
<ul>
<li>Área que no es de cliente</li>
<li>Mapas de bits dibujados por temas en controles comunes (comctl32 V6)</li>
<li>Diálogos (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>

### <a name="per-monitor-v1-dpi-awareness"></a>Reconocimiento de PPP por monitor (V1)

Per-Monitor el modo de reconocimiento de PPP V1 (PMv1) se introdujo con Windows 8.1. Este modo de reconocimiento de PPP es muy limitado y solo ofrece la funcionalidad que se muestra a continuación. Se recomienda que las aplicaciones de escritorio usen Per-Monitor de reconocimiento v2, compatible con Windows 10 1703 o posterior.

La compatibilidad inicial con el reconocimiento por monitor solo ofrecía a las aplicaciones lo siguiente:

1.  Se notifica a los HWND de nivel superior un cambio de PPP y se proporciona un nuevo tamaño sugerido.
2.  Windows mapa de bits ajustará la interfaz de usuario de la aplicación
3.  La aplicación ve todas las pantallas en píxeles físicos (consulte virtualización).

En Windows 10 1607 o posterior, las aplicaciones PMv1 también pueden llamar a [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) durante WM NCCREATE para solicitar que Windows escale correctamente el área no cliente de la \_ ventana.

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a>Compatibilidad con el escalado de PPP por monitor por marco de interfaz de usuario/tecnología

En la tabla siguiente se muestra el nivel de compatibilidad con reconocimiento de PPP por monitor que ofrecen varios marcos de interfaz de usuario de Windows desde Windows 10 1703:

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Marco de trabajo/tecnología</th>
<th>Soporte técnico</th>
<th>Versión del SO.</th>
<th>Ajuste de escala de PPP que controla</th>
<th>Lecturas adicionales</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Plataforma universal de Windows (UWP)</td>
<td>Completo</td>
<td>1607</td>
<td>Marco de interfaz de usuario</td>
<td><a href="/windows/uwp/get-started/whats-a-uwp">Plataforma universal de Windows (UWP)</a></td>
</tr>
<tr class="even">
<td>Controles win32/common sin formato V6 (comctl32.dll)</td>
<td><ul>
<li>Mensajes de notificación de cambio de PPP enviados a todos los HWND</li>
<li>Los recursos dibujados con tema se representan correctamente en los controles comunes</li>
<li>Escalado automático de PPP para diálogos</li>
</ul></td>
<td>1703</td>
<td>Application</td>
<td><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub Muestra</a></td>
</tr>
<tr class="odd">
<td>Windows Forms</td>
<td>Escalado de PPP por monitor automático limitado para algunos controles</td>
<td>1703</td>
<td>Marco de interfaz de usuario</td>
<td><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Compatibilidad con valores altos de PPP en Windows Forms</a></td>
</tr>
<tr class="even">
<td>Windows Presentation Framework (WPF)</td>
<td>Las aplicaciones wpf nativas escalarán wpf hospedados en otros marcos de trabajo y otros marcos hospedados en WPF no escalarán automáticamente</td>
<td>1607</td>
<td>Marco de interfaz de usuario</td>
<td><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub Muestra</a></td>
</tr>
<tr class="odd">
<td>GDI</td>
<td>None</td>
<td>N/D</td>
<td>Application</td>
<td>Consulte <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">Escalado de valores altos de PPP de GDI.</a></td>
</tr>
<tr class="even">
<td>GDI+</td>
<td>None</td>
<td>N/D</td>
<td>Application</td>
<td>Consulte <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">Escalado de valores altos de PPP de GDI.</a></td>
</tr>
<tr class="odd">
<td>MFC</td>
<td>None</td>
<td>N/D</td>
<td>Application</td>
<td>N/D</td>
</tr>
</tbody>
</table>



 

## <a name="updating-existing-applications"></a>Actualizar aplicaciones existentes

Para actualizar una aplicación de escritorio existente para controlar correctamente el escalado de PPP, es necesario actualizarla para que, como mínimo, se actualicen las partes importantes de su interfaz de usuario para responder a los cambios de PPP.

La mayoría de las aplicaciones de escritorio se ejecutan en modo de reconocimiento de PPP del sistema. Las aplicaciones que tienen en cuenta los valores de PPP del sistema normalmente se escalan al valor de PPP de la pantalla principal (la pantalla en la que se encontraba la bandeja del sistema en el momento en que se inició la Windows sesión). Cuando cambia el valor de PPP, Windows mapa de bits ajustará la interfaz de usuario de estas aplicaciones, lo que suele hacer que se desenfoque. Al actualizar una aplicación compatible con PPP del sistema para que sea compatible con PPP por monitor, el código que controla el diseño de la interfaz de usuario debe actualizarse para que se realice no solo durante la inicialización de la aplicación, sino también siempre que se reciba una notificación de cambio de PPP[(WM \_ PPPCHANGED](wm-dpichanged.md) en el caso de Win32). Normalmente, esto implica volver a examinar las suposiciones en el código de que la interfaz de usuario solo debe escalarse una vez.

Además, en el caso de la programación win32, muchas API de Win32 no tienen ningún valor de PPP ni contexto de presentación, por lo que solo devolverán valores relativos al VALOR DE PPP del sistema. Puede ser útil pasar por el código para buscar algunas de estas API y reemplazarlas por variantes con reconocimiento de PPP. Algunas de las API comunes que tienen variantes que tienen reconocimiento de PPP son:



| Versión de PPP único   | Per-Monitor versión        |
|----------------------|----------------------------|
| GetSystemMetrics     | GetSystemMetricsForDpi     |
| AdjustWindowRectEx   | AdjustWindowRectExForDpi   |
| SystemParametersInfo | SystemParametersInfoForDpi |
| GetDpiForMonitor     | GetDpiForWindow            |



 

También es una buena idea buscar tamaños codificados de forma fuerte en el código base que asumen un PPP constante, reemplazándolos por código que tiene en cuenta correctamente el escalado de PPP. A continuación se muestra un ejemplo que incorpora todas estas sugerencias:

### <a name="example"></a>Ejemplo:

En el ejemplo siguiente se muestra un caso win32 simplificado de creación de un HWND secundario. La llamada a CreateWindow supone que la aplicación se ejecuta a 96 PPP y que ni el tamaño ni la posición del botón serán correctos en las DPI superiores:


```
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON,  
        50,  
        50,  
        100,  
        50,  
        hWnd, (HMENU)NULL, NULL, NULL); 
} 
```



El código actualizado siguiente muestra:

1.  El valor de PPP del código de creación de ventana escala la posición y el tamaño del HWND secundario para el valor de PPP de su ventana primaria.
2.  Respuesta al cambio de PPP al cambiar la posición y cambiar el tamaño del HWND secundario
3.  Se han quitado los tamaños codificados de forma hard-code y se han reemplazado por código que responde a los cambios de PPP.


```
#define INITIALX_96DPI 50 
#define INITIALY_96DPI 50 
#define INITIALWIDTH_96DPI 100 
#define INITIALHEIGHT_96DPI 50 
 
 
// DPI scale the position and size of the button control 
void UpdateButtonLayoutForDpi(HWND hWnd) 
{ 
    int iDpi = GetDpiForWindow(hWnd); 
    int dpiScaledX = MulDiv(INITIALX_96DPI, iDpi, 96); 
    int dpiScaledY = MulDiv(INITIALY_96DPI, iDpi, 96); 
    int dpiScaledWidth = MulDiv(INITIALWIDTH_96DPI, iDpi, 96); 
    int dpiScaledHeight = MulDiv(INITIALHEIGHT_96DPI, iDpi, 96); 
    SetWindowPos(hWnd, hWnd, dpiScaledX, dpiScaledY, dpiScaledWidth, dpiScaledHeight, SWP_NOZORDER | SWP_NOACTIVATE); 
} 
 
... 
 
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON, 
        0, 
        0, 
        0, 
        0, 
        hWnd, (HMENU)NULL, NULL, NULL); 
    if (hWndChild != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndChild); 
    } 
} 
break; 
 
case WM_DPICHANGED: 
{ 
    // Find the button and resize it 
    HWND hWndButton = FindWindowEx(hWnd, NULL, NULL, NULL); 
    if (hWndButton != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndButton); 
    } 
} 
break; 
```



Al actualizar una aplicación compatible con PPP del sistema, algunos pasos comunes que se deben seguir son:

1.  Marque el proceso como compatible con PPP por monitor (V2) mediante un manifiesto de aplicación (u otro método, en función de los marcos de interfaz de usuario usados).
2.  Hacer que la lógica de diseño de la interfaz de usuario sea reutilizable y sacarla del código de inicialización de la aplicación para que se pueda reutilizar cuando se produzca un cambio de PPP (WM PPPCHANGED en el caso de la programación Windows \_ (Win32).
3.  Invalide cualquier código que suponga que nunca es necesario actualizar los datos confidenciales de PPP (PPP/fuentes/tamaños/etc.). Es una práctica muy común almacenar en caché los tamaños de fuente y los valores de PPP durante la inicialización del proceso. Al actualizar una aplicación para que sea compatible con PPP por monitor, los datos confidenciales de PPP se deben volver a evaluar cada vez que se encuentre un nuevo PPP.
4.  Cuando se produce un cambio de PPP, vuelva a cargar (o volver a rasterizar) los recursos de mapa de bits para el nuevo PPP o, opcionalmente, ajuste los recursos cargados actualmente al tamaño correcto.
5.  Grep para las API que no son Per-Monitor reconocimiento de PPP y reemplazarlas por Per-Monitor API con reconocimiento de PPP (si procede). Ejemplo: reemplace GetSystemMetrics por GetSystemMetricsForDpi.
6.  Pruebe la aplicación en un sistema de varias pantallas o varios PPP.
7.  En el caso de las ventanas de nivel superior de la aplicación que no pueda actualizar a la escala de PPP correctamente, use el escalado de PPP en modo mixto (que se describe a continuación) para permitir el ajuste de mapa de bits de estas ventanas de nivel superior por parte del sistema.

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a>Mixed-Mode de PPP (ajuste de escala de PPP de sub process)

Al actualizar una aplicación para admitir el reconocimiento de PPP por monitor, a veces puede ser poco práctico o imposible actualizar todas las ventanas de la aplicación de una en una. Esto puede deberse simplemente al tiempo y al esfuerzo necesarios para actualizar y probar toda la interfaz de usuario, o bien porque no posee todo el código de la interfaz de usuario que necesita ejecutar (si la aplicación quizás carga la interfaz de usuario de terceros). En estas situaciones, Windows ofrece una manera de facilitar el reconocimiento por monitor al permitirle ejecutar algunas de las ventanas de la aplicación (solo de nivel superior) en su modo original de reconocimiento de PPP mientras centra el tiempo y la energía en la actualización de las partes más importantes de la interfaz de usuario.

A continuación se muestra una ilustración de cómo podría ser esto: actualice la interfaz de usuario de la aplicación principal ("Ventana principal" en la ilustración) para que se ejecute con reconocimiento de PPP por monitor mientras ejecuta otras ventanas en su modo existente ("Ventana secundaria").

![diferencias en el escalado de ppp entre modos de reconocimiento](images/hub-page-illustrations.png)

Antes de la Windows 10 de aniversario (1607), el modo de reconocimiento de PPP de un proceso era una propiedad para todo el proceso. A partir de la Windows 10 de aniversario, esta propiedad ahora se puede establecer por **ventana de nivel** superior. (**Las** ventanas secundarias deben seguir siendo iguales al tamaño de escalado de su elemento primario). Una ventana de nivel superior se define como una ventana sin elemento primario. Suele ser una ventana "normal" con botones minimizar, maximizar y cerrar. El escenario para el que está pensado el reconocimiento de PPP del subproceso es que la interfaz de usuario secundaria se escale mediante Windows (mapa de bits extendido) mientras se centra el tiempo y los recursos en actualizar la interfaz de usuario principal.

Para habilitar el reconocimiento de PPP del subproceso, llame a [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) antes y después de cualquier llamada de creación de ventana. La ventana que se crea se asociará con el reconocimiento de PPP que estableció a través de SetThreadDpiAwarenessContext. Use la segunda llamada para restaurar el reconocimiento de PPP del subproceso actual.

Aunque el escalado de PPP del sub process le permite confiar en Windows realizar parte del escalado de PPP para la aplicación, puede aumentar la complejidad de la aplicación. Es importante que comprenda las desventajas de este enfoque y la naturaleza de las complejidades que presenta. Para obtener más información sobre el reconocimiento de PPP de sub process, consulte [Mixed-Mode PPP Scaling and PPP-aware APIs (Api](high-dpi-improvements-for-desktop-applications.md) con reconocimiento de PPP y escalado de PPP en modo mixto).

## <a name="testing-your-changes"></a>Prueba de los cambios

Después de actualizar la aplicación para que sea compatible con PPP por monitor, es importante validar que la aplicación responde correctamente a los cambios de PPP en un entorno de PPP mixto. Entre los detalles que se deben probar se incluyen:

1.  Mover ventanas de aplicación de un lado a otro entre pantallas de distintos valores de PPP
2.  Inicio de la aplicación en pantallas de distintos valores de PPP
3.  Cambio del factor de escala para el monitor mientras se ejecuta la aplicación
4.  Cambiar la pantalla que se usa como pantalla principal, salir de Windows _y, a_ continuación, volver a probar la aplicación después de volver a iniciar sesión. Esto es especialmente útil para buscar código que usa dimensiones o tamaños codificados de forma fuerte.

## <a name="common-pitfalls-win32"></a>Problemas comunes (Win32)

**No usar el rectángulo sugerido que se proporciona en WM \_ PPPCHANGED**

Cuando Windows la ventana de la aplicación un mensaje [**\_ WM PPPCHANGED,**](wm-dpichanged.md) este mensaje incluye un rectángulo sugerido que debe usar para cambiar el tamaño de la ventana. Es fundamental que la aplicación use este rectángulo para cambiar su tamaño, ya que esto hará lo siguiente:

1.  Asegúrese de que el cursor del mouse permanecerá en la misma posición relativa en la ventana al arrastrar entre las pantallas.
2.  Impedir que la ventana de la aplicación entre en un ciclo de cambio de ppp recursivo donde un cambio de PPP desencadena un cambio posterior de PPP, lo que desencadena otro cambio de PPP.

Si tiene requisitos específicos de la aplicación que le impiden usar el rectángulo sugerido que Windows proporciona en el mensaje WM \_ PPPCHANGED, vea [**WM \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md). Este mensaje se puede usar para proporcionar a Windows un tamaño deseado que quiera usar una vez que se haya producido el cambio de PPP, a la vez que se evitan los problemas descritos anteriormente.

**Falta de documentación sobre virtualización**

Cuando un HWND o un proceso se ejecuta como PPP no consciente o compatible con PPP del sistema, se puede ajustar el mapa de bits Windows. Cuando esto sucede, Windows escala y convierte información confidencial de PPP de algunas API al espacio de coordenadas del subproceso que realiza la llamada. Por ejemplo, si un subproceso sin reconocimiento de PPP consulta el tamaño de la pantalla mientras se ejecuta en una pantalla de valores altos de PPP, Windows virtualizará la respuesta dada a la aplicación como si la pantalla estuviera en unidades de 96 PPP. Como alternativa, cuando un subproceso compatible con PPP del sistema interactúa con una pantalla con un PPP diferente al que estaba en uso cuando se inició la sesión del usuario actual, Windows escalará con PPP algunas llamadas API al espacio de coordenadas que usaría el HWND si se estaba ejecutando en su factor de escala de PPP original.

Al actualizar correctamente la aplicación de escritorio a un escalado de PPP, puede ser difícil saber qué llamadas API pueden devolver valores virtualizados en función del contexto del subproceso. Esta información no está suficientemente documentada actualmente por Microsoft. Tenga en cuenta que si llama a cualquier API del sistema desde un contexto de subproceso que no es consciente de PPP o compatible con PPP del sistema, el valor devuelto podría virtualizarse. Por lo tanto, asegúrese de que el subproceso se ejecuta en el contexto de PPP que espera al interactuar con la pantalla o ventanas individuales. Al cambiar temporalmente el contexto de PPP de un subproceso mediante [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), asegúrese de restaurar el contexto anterior cuando haya terminado para evitar que se provoque un comportamiento incorrecto en otra parte de la aplicación.

**Muchas Windows API no tienen un contexto de PPP**

Muchas API de Windows heredadas no incluyen un contexto DE PPP o HWND como parte de su interfaz. Como resultado, los desarrolladores a menudo tienen que realizar trabajo adicional para controlar el escalado de cualquier información confidencial de PPP, como tamaños, puntos o iconos. Por ejemplo, los desarrolladores que usan [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) deben usar iconos cargados extendidos de mapa de bits o usar API alternativas para cargar iconos con el tamaño correcto para el PPP adecuado, como [LoadImage.](/windows/desktop/api/winuser/nf-winuser-loadimagew)

**Restablecimiento forzado del reconocimiento de PPP en todo el proceso**

En general, el modo de reconocimiento de PPP del proceso no se puede cambiar después de la inicialización del proceso. Windows cambiar a la fuerza el modo de reconocimiento de PPP del proceso si intenta interrumpir el requisito de que todos los HWND de un árbol de ventana tengan el mismo modo de reconocimiento de PPP. En todas las versiones de Windows, a partir de Windows 10 1703, no es posible que los HWND diferentes de un árbol HWND se ejecuten en distintos modos de reconocimiento de PPP. Si intenta crear una relación de elementos primarios secundarios que interrumpe esta regla, se puede restablecer el reconocimiento de PPP de todo el proceso. Esto se puede desencadenar mediante:

1.  Una llamada a CreateWindow donde la ventana primaria pasada es de un modo de reconocimiento de PPP diferente que el subproceso que realiza la llamada.
2.  Una llamada SetParent donde las dos ventanas están asociadas a diferentes modos de reconocimiento de PPP.

En la tabla siguiente se muestra lo que sucede si intenta infringir esta regla:



| Operación                 | Windows 8.1                                  | Windows 10 (1607 y versiones anteriores)                | Windows 10 (1703 y versiones posteriores)                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| CreateWindow (en proceso)    | N/D                                          | **Herencias secundarias** (modo mixto)              | **Herencias secundarias** (modo mixto)              |
| CreateWindow (cross-proc) | **Restablecimiento forzado** (del proceso del autor de la llamada)       | **Herencias secundarias** (modo mixto)              | **Restablecimiento forzado** (del proceso del autor de la llamada)       |
| SetParent (In-Proc)       | N/D                                          | **Restablecimiento forzado** (del proceso actual)        | **Error** (ERROR \_ ESTADO NO \_ VÁLIDO)             |
| SetParent (cross-proc)    | **Restablecimiento forzado** (del proceso de la ventana secundaria) | **Restablecimiento forzado** (del proceso de la ventana secundaria) | **Restablecimiento forzado** (del proceso de la ventana secundaria) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de API de valores altos de PPP](high-dpi-reference.md)
</dt> <dt>

[API de escalado de PPP en modo mixto y API con reconocimiento de PPP.](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

