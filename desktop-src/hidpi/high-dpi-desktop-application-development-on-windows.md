---
title: Desarrollo de aplicaciones de escritorio de alto nivel de PPP en Windows
description: Este contenido está destinado a los desarrolladores que desean actualizar las aplicaciones de escritorio para controlar el factor de escala de la pantalla dinámica (también conocido como
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7af4a7a1d65077838dfa65f7cf89dee475a0b4dc
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104149696"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a>Desarrollo de aplicaciones de escritorio de alto nivel de PPP en Windows

Este contenido está destinado a los desarrolladores que desean actualizar las aplicaciones de escritorio para controlar los cambios en el factor de escala de la pantalla (puntos por pulgada o PPP) dinámicamente, lo que permite que sus aplicaciones sean nítidas en cualquier pantalla en la que se representen.

Para empezar, si va a crear una nueva aplicación de Windows desde cero, se recomienda encarecidamente que cree una aplicación [plataforma universal de Windows (UWP)](/windows/uwp/get-started/whats-a-uwp) . Las aplicaciones de UWP &mdash; &mdash; se escalan de forma automática y dinámica para cada pantalla en la que se ejecutan.

Las aplicaciones de escritorio que usan tecnologías de programación de Windows anteriores (programación de Win32 sin formato, Windows Forms, Windows Presentation Framework (WPF), etc.) no pueden controlar automáticamente el escalado de PPP sin ningún trabajo de desarrollador adicional. Sin este trabajo, las aplicaciones se verán borrosas o con un tamaño incorrecto en muchos escenarios de uso comunes. En este documento se proporciona contexto e información sobre lo que implica actualizar una aplicación de escritorio para que se represente correctamente.

## <a name="display-scale-factor--dpi"></a>Mostrar factor de escala & PPP

A medida que la tecnología de visualización ha progresado, los fabricantes de paneles de pantalla han empaquetado un número cada vez mayor de píxeles en cada unidad de espacio físico en sus paneles. Esto ha dado como resultado que los puntos por pulgada (PPP) de los paneles de pantalla modernos sean mucho más altos de lo que históricamente lo han hecho. En el pasado, la mayoría de las pantallas tenían 96 píxeles por pulgada lineal de espacio físico (96 PPP). en 2017, se muestra con casi 300 ppp o una versión superior.

La mayoría de los marcos de interfaz de usuario de escritorio heredados tienen suposiciones integradas que los PPP de la pantalla no cambiarán durante la vigencia del proceso.  Esta suposición ya no tiene el valor true, con Mostrar PPP que normalmente cambian varias veces a lo largo de la duración de un proceso de aplicación. Algunos escenarios comunes en los que los cambios en el factor de escala de presentación/PPP son:

-   Configuraciones de varios monitores en las que cada pantalla tiene un factor de escala diferente y la aplicación se mueve de una pantalla a otra (por ejemplo, una pantalla de 4K y 1080p)
-   Acoplar y desacoplar un portátil de PPP alto con una pantalla externa de PPP bajo (o viceversa)
-   Conexión a través de Escritorio remoto desde un portátil o tableta con un alto PPP a un dispositivo con pocos PPP (o viceversa)
-   Cambiar la configuración de un factor de escala de presentación mientras se ejecutan las aplicaciones

En estos casos, las aplicaciones UWP se vuelven a dibujar automáticamente para el nuevo ppp. De forma predeterminada, y sin trabajo adicional para desarrolladores, las aplicaciones de escritorio no lo hacen. Las aplicaciones de escritorio que no realizan este trabajo adicional para responder a los cambios de PPP pueden aparecer borrosas o con un tamaño incorrecto para el usuario.

## <a name="dpi-awareness-mode"></a>Modo de reconocimiento de PPP

Las aplicaciones de escritorio deben indicar a Windows si admiten la escala de PPP. De forma predeterminada, el sistema considera que los PPP de las aplicaciones de escritorio no reconocen y el mapa de bits ajusta sus ventanas. Al establecer uno de los siguientes modos de reconocimiento de PPP disponibles, las aplicaciones pueden indicar explícitamente a Windows cómo desean administrar el escalado de PPP:

### <a name="dpi-unaware"></a>PPP no compatible

Las aplicaciones sin reconocimiento de PPP se representan con un valor de PPP fijo de 96 (100%). Cuando estas aplicaciones se ejecutan en una pantalla con una escala de pantalla superior a 96 PPP, Windows extenderá el mapa de bits de la aplicación al tamaño físico esperado. Esto hace que la aplicación parezca borrosa.

### <a name="system-dpi-awareness"></a>Reconocimiento de PPP del sistema

Las aplicaciones de escritorio que reconocen el sistema PPP normalmente reciben el PPP del monitor conectado principal en el momento del inicio de sesión del usuario. Durante la inicialización, diseñan su interfaz de usuario de forma adecuada (control de tamaño, elección de tamaños de fuente, carga de recursos, etc.) usando ese valor de PPP del sistema. Por lo tanto, las aplicaciones que tienen en cuenta los PPP del sistema no tienen una escala de PPP (mapa de bits ajustada) por Windows en muestra la representación en ese único ppp. Cuando la aplicación se mueve a una pantalla con un factor de escala diferente, o si el factor de escala de la pantalla cambia en otro caso, Windows escalará el mapa de bits de las ventanas de la aplicación, de forma que aparezcan borrosas. De hecho, las aplicaciones de escritorio con reconocimiento de PPP del sistema solo se representan de forma nítida en un solo factor de escala de pantalla, lo que se vuelve borrosa cada vez que cambia el PPP.

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a>Reconocimiento de PPP de Per-Monitor y Per-Monitor (V2)

Se recomienda que las aplicaciones de escritorio se actualicen para usar el modo de reconocimiento de PPP por monitor, lo que permite que se representen de inmediato siempre que cambie el PPP. Cuando una aplicación notifica a Windows que desea ejecutar en este modo, Windows no creará un mapa de bits de la aplicación cuando cambie el PPP, sino que enviará [WM \_ DPICHANGED](wm-dpichanged.md) a la ventana de la aplicación. Después, es responsabilidad completa de la aplicación controlar el cambio de tamaño para el nuevo ppp. La mayoría de los marcos de interfaz de usuario que usan las aplicaciones de escritorio (controles comunes de Windows (comctl32), Windows Forms, Windows Presentation Framework, etc.) no admiten el escalado de PPP automático, lo que obliga a los desarrolladores a cambiar el tamaño y la posición del contenido de sus propias ventanas.

Hay dos versiones de Per-Monitor reconocimiento de que una aplicación puede registrarse como: versión 1 y versión 2 (PMv2). El registro de un proceso como en ejecución en el modo de reconocimiento de PMv2 produce:

1.  La aplicación a la que se notifica cuando cambia el PPP (el HWND de nivel superior y el secundario)
2.  La aplicación ve los píxeles sin formato de cada pantalla
3.  La aplicación nunca está escalada como mapa de bits de Windows
4.  Área no cliente automática (título de ventana, barras de desplazamiento, etc.) Ajuste de escala de PPP por Windows
5.  Cuadros de diálogo Win32 (desde [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) ajuste automático de PPP por Windows
6.  Los recursos de mapa de bits dibujados por temas en controles comunes (casillas, el fondo de los botones, etc.) se representan automáticamente en el factor de escala de PPP adecuado.

Cuando se ejecuta en el modo de reconocimiento de Per-Monitor V2, se notifica a las aplicaciones cuando cambia su ppp. Si una aplicación no cambia de tamaño para el nuevo valor de PPP, la interfaz de usuario de la aplicación aparecerá demasiado pequeña o demasiado grande (dependiendo de la diferencia en los valores de PPP anterior y nuevo).

> [!Note]  
> El reconocimiento de Per-Monitor V1 (PMv1) es muy limitado. Se recomienda que las aplicaciones usen PMv2.

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
<th>Versión de Windows introducida</th>
<th>Vista de PPP de la aplicación</th>
<th>Comportamiento en cambio de PPP</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Consciente</td>
<td>N/D</td>
<td>Todas las pantallas tienen 96 PPP</td>
<td>Expansión de mapas de bits (borrosa)</td>
</tr>
<tr class="even">
<td>System</td>
<td>Vista</td>
<td>Todas las pantallas tienen el mismo PPP (el PPP de la pantalla principal en el momento en que se inició la sesión de usuario actual)</td>
<td>Expansión de mapas de bits (borrosa)</td>
</tr>
<tr class="odd">
<td>Per-Monitor</td>
<td>8.1</td>
<td>El PPP de la pantalla en la que se encuentra principalmente la ventana de la aplicación</td>
<td><ul>
<li>El HWND de nivel superior recibe una notificación de cambio de PPP</li>
<li>Sin escala de PPP de ningún elemento de la interfaz de usuario.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Per-Monitor V2</td>
<td>Windows 10 Creators Update (1703)</td>
<td>El PPP de la pantalla en la que se encuentra principalmente la ventana de la aplicación</td>
<td><ul>
<li>Los HWND de nivel superior <span class="underline">y</span> secundarios reciben una notificación de cambio de PPP</li>
</ul>
<br/> <span class="underline">Escala de PPP automática de:</span>
<ul>
<li>Área no cliente</li>
<li>Mapas de bits dibujados por temas en controles comunes (comctl32 V6)</li>
<li>Cuadros de diálogo (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>

### <a name="per-monitor-v1-dpi-awareness"></a>Reconocimiento de PPP por monitor (V1)

Per-Monitor el modo de reconocimiento de PPP (PMv1) V1 se presentó con Windows 8.1. Este modo de reconocimiento de PPP es muy limitado y solo ofrece la funcionalidad que se indica a continuación. Se recomienda que las aplicaciones de escritorio usen el modo de reconocimiento de Per-Monitor V2, compatible con Windows 10 1703 o posterior.

La compatibilidad inicial para el reconocimiento por monitor solo ofrecía las aplicaciones siguientes:

1.  Los HWND de nivel superior reciben una notificación de un cambio de PPP y proporcionan un nuevo tamaño sugerido
2.  Windows no ajustará el mapa de bits de la interfaz de usuario de la aplicación
3.  La aplicación ve todas las pantallas en píxeles físicos (consulte virtualización)

En Windows 10 1607 o posterior, las aplicaciones de PMv1 también pueden llamar a [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) durante WM \_ NCCREATE para solicitar que Windows escale correctamente el área no cliente de la ventana.

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a>Compatibilidad con el ajuste de escala de PPP por monitor mediante la tecnología/marco de interfaz de usuario

En la tabla siguiente se muestra el nivel de compatibilidad con el reconocimiento de PPP por monitor ofrecido por diversos marcos de interfaz de usuario de Windows a partir de Windows 10 1703:

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
<th>Plataforma/tecnología</th>
<th>Soporte técnico</th>
<th>Versión del SO.</th>
<th>Ajuste de escala de PPP controlado por</th>
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
<td>Win32/controles comunes sin formato V6 (comctl32.dll)</td>
<td><ul>
<li>Mensajes de notificación de cambio de PPP enviados a todos los HWND</li>
<li>Los activos dibujados por temas se representan correctamente en controles comunes</li>
<li>Escala de PPP automática para cuadros de diálogo</li>
</ul></td>
<td>1703</td>
<td>Application</td>
<td><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">Ejemplo de GitHub</a></td>
</tr>
<tr class="odd">
<td>Windows Forms</td>
<td>Escala de PPP por monitor automática limitada para algunos controles</td>
<td>1703</td>
<td>Marco de interfaz de usuario</td>
<td><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Compatibilidad con PPP alta en Windows Forms</a></td>
</tr>
<tr class="even">
<td>Windows Presentation Framework (WPF)</td>
<td>Las aplicaciones WPF nativas escalarán PPP de WPF hospedadas en otros marcos y otros marcos de trabajo hospedados en WPF no se escalan automáticamente</td>
<td>1607</td>
<td>Marco de interfaz de usuario</td>
<td><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">Ejemplo de GitHub</a></td>
</tr>
<tr class="odd">
<td>GDI</td>
<td>None</td>
<td>N/D</td>
<td>Application</td>
<td>Consulte <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">escala de PPP alta-PPP</a></td>
</tr>
<tr class="even">
<td>GDI+</td>
<td>None</td>
<td>N/D</td>
<td>Application</td>
<td>Consulte <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">escala de PPP alta-PPP</a></td>
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

Para actualizar una aplicación de escritorio existente para controlar el escalado de PPP correctamente, debe actualizarse de forma que, como mínimo, las partes importantes de su interfaz de usuario se actualicen para responder a los cambios de PPP.

La mayoría de las aplicaciones de escritorio se ejecutan en modo de reconocimiento de PPP del sistema. Las aplicaciones con reconocimiento de PPP del sistema normalmente se escalan al ppp de la pantalla principal (la pantalla en la que se encontraba la bandeja del sistema en el momento en que se inició la sesión de Windows). Cuando cambia el PPP, Windows ajustará el mapa de bits de la interfaz de usuario de estas aplicaciones, lo que a menudo resulta que son borrosos. Al actualizar una aplicación compatible con PPP del sistema a reconocimiento de PPP por monitor, el código que controla el diseño de la interfaz de usuario debe actualizarse de forma que se realice no solo durante la inicialización de la aplicación, sino que también siempre que se reciba una notificación de cambio de PPP ([WM \_ DPICHANGED](wm-dpichanged.md) en el caso de Win32). Normalmente, esto implica volver a visitar cualquier suposición en el código que la interfaz de usuario solo debe escalar una vez.

Además, en el caso de la programación de Win32, muchas API de Win32 no tienen ningún contexto de pantalla o PPP, por lo que solo devolverán valores relativos al valor de PPP del sistema. Puede ser útil para grep a través del código con el fin de buscar algunas de estas API y reemplazarlas por variantes con reconocimiento de PPP. Algunas de las API comunes que tienen variantes con reconocimiento de PPP son:



| Versión de PPP única   | Versión de Per-Monitor        |
|----------------------|----------------------------|
| GetSystemMetrics     | GetSystemMetricsForDpi     |
| AdjustWindowRectEx   | AdjustWindowRectExForDpi   |
| SystemParametersInfo | SystemParametersInfoForDpi |
| GetDpiForMonitor     | GetDpiForWindow            |



 

También es una buena idea buscar los tamaños codificados de forma rígida en el código base que suponen un PPP constante y los reemplazan por código que cuenta correctamente para la escala de PPP. A continuación se muestra un ejemplo que incorpora todas estas sugerencias:

### <a name="example"></a>Ejemplo:

En el ejemplo siguiente se muestra un caso de Win32 simplificado de creación de un HWND secundario. La llamada a CreateWindow supone que la aplicación se está ejecutando a 96 PPP y que el tamaño y la posición del botón serán correctos en PPP superior:


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

1.  El código de creación de ventanas PPP escala la posición y el tamaño del HWND secundario para el PPP de su ventana primaria
2.  Responder al cambio de PPP cambiando la posición y el tamaño del HWND secundario
3.  Los tamaños codificados de forma rígida se quitan y reemplazan por código que responde a los cambios de PPP


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



Al actualizar una aplicación compatible con PPP del sistema, algunos de los pasos que debe seguir son los siguientes:

1.  Marque el proceso como reconocimiento de PPP por monitor (V2) mediante un manifiesto de aplicación (u otro método, en función de los marcos de interfaz de usuario utilizados).
2.  Haga que la lógica de diseño de la interfaz de usuario sea reutilizable y muévala del código de inicialización de la aplicación para que se pueda reutilizar cuando se produzca un cambio de PPP (WM \_ DPICHANGED en el caso de la programación de Windows (Win32)).
3.  Invalide cualquier código que asuma que no es necesario actualizar nunca la información sensible a los PPP (PPP, fuentes, tamaños, etc.). Es una práctica muy común almacenar en caché los tamaños de fuente y los valores de PPP en la inicialización del proceso. Al actualizar una aplicación para que sea compatible con PPP por monitor, se deben volver a evaluar los datos con distinción de PPP cada vez que se encuentre un nuevo ppp.
4.  Cuando se produce un cambio de PPP, vuelva a cargar (o vuelva a rasterizar) los recursos de mapa de bits para el nuevo PPP o, opcionalmente, ajuste el mapa de bits a los activos cargados actualmente en el tamaño correcto.
5.  Grep para las API que no son compatibles con PPP Per-Monitor y las reemplazan por Per-Monitor API que reconocen los PPP (si procede). Ejemplo: Reemplace GetSystemMetrics por GetSystemMetricsForDpi.
6.  Pruebe la aplicación en un sistema de varios PPP o múltiples pantallas.
7.  En el caso de las ventanas de nivel superior de la aplicación que no se puedan actualizar a una escala de PPP adecuada, use el escalado de PPP en modo mixto (que se describe a continuación) para permitir que el sistema ajuste los mapas de bits de estas ventanas de nivel superior.

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a>Ajuste de escala de PPP Mixed-Mode (escala de PPP de subproceso)

Al actualizar una aplicación para admitir el reconocimiento de PPP por monitor, a veces puede resultar poco práctico o imposible actualizar cada ventana de la aplicación en un solo paso. Esto puede ser simplemente debido al tiempo y al esfuerzo necesarios para actualizar y probar todas las interfaces de usuario, o porque no posee todo el código de interfaz de usuario que necesita ejecutar (si la aplicación puede cargar una interfaz de usuario de terceros). En estas situaciones, Windows ofrece una manera de facilitar el mundo del reconocimiento por monitor, ya que permite ejecutar algunas de las ventanas de la aplicación (solo de nivel superior) en su modo de reconocimiento de PPP original mientras se centra el tiempo y la actualización de energía de las partes más importantes de la interfaz de usuario.

A continuación se muestra una ilustración del aspecto que podría tener: actualice la interfaz de usuario de la aplicación principal ("ventana principal" en la ilustración) para ejecutar con reconocimiento de PPP por monitor mientras ejecuta otras ventanas en su modo existente ("ventana secundaria").

![diferencias en el escalado de PPP entre los modos de reconocimiento](images/hub-page-illustrations.png)

Antes de la actualización de aniversario de Windows 10 (1607), el modo de reconocimiento de PPP de un proceso era una propiedad de todo el proceso. A partir de la actualización de aniversario de Windows 10, esta propiedad se puede establecer ahora por ventana **de nivel superior** . (Las ventanas **secundarias** deben seguir coincidiendo con el tamaño de escala de su elemento primario). Una ventana de nivel superior se define como una ventana sin elementos primarios. Normalmente, se trata de una ventana "normal" con botones minimizar, maximizar y cerrar. El escenario para el que está diseñado el reconocimiento de PPP de subprocesos es tener una interfaz de usuario secundaria escalada por Windows (mapa de bits ampliado) mientras se centra el tiempo y los recursos en la actualización de la interfaz de usuario principal.

Para habilitar el reconocimiento de PPP de subprocesos, llame a [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) antes y después de cualquier llamada de creación de ventana. La ventana que se crea se asociará con el reconocimiento de PPP que establezca a través de SetThreadDpiAwarenessContext. Use la segunda llamada para restaurar el reconocimiento actual del subproceso s ppp.

Aunque el escalado de PPP de subproceso permite confiar en Windows para que realice parte de la escala de PPP de la aplicación, puede aumentar la complejidad de la aplicación. Es importante que comprenda las desventajas de este enfoque y la naturaleza de las complejidades que presenta. Para obtener más información sobre el reconocimiento de PPP de subprocesos, vea el tema sobre [la escala de PPP en modo mixto y las API que reconocen ppp.](high-dpi-improvements-for-desktop-applications.md)

## <a name="testing-your-changes"></a>Probar los cambios

Después de haber actualizado la aplicación para que sea compatible con los ppp por monitor, es importante validar que la aplicación responde correctamente a los cambios de PPP en un entorno de PPP mixto. Algunos detalles de la prueba incluyen:

1.  Mover ventanas de aplicaciones hacia delante y hacia atrás entre pantallas de distintos valores de PPP
2.  Inicio de la aplicación en presentaciones de distintos valores de PPP
3.  Cambiar el factor de escala para el monitor mientras la aplicación se está ejecutando
4.  Cambiar la presentación que se usa como pantalla principal, _cerrar la sesión de Windows_ y volver a probar la aplicación después de volver a iniciar sesión. Esto es especialmente útil para buscar código que usa dimensiones o tamaños codificados de forma rígida.

## <a name="common-pitfalls-win32"></a>Errores comunes (Win32)

**No usar el rectángulo sugerido proporcionado en WM \_ DPICHANGED**

Cuando Windows envía un mensaje de [**WM \_ DPICHANGED**](wm-dpichanged.md) a la ventana de la aplicación, este mensaje incluye un rectángulo sugerido que debe usar para cambiar el tamaño de la ventana. Es fundamental que la aplicación use este rectángulo para cambiar el tamaño, ya que esto hará lo siguiente:

1.  Asegúrese de que el cursor del mouse permanecerá en la misma posición relativa en la ventana al arrastrar entre las pantallas.
2.  Impedir que la ventana de la aplicación entre en un ciclo recursivo de cambio de PPP en el que un cambio de PPP desencadena un cambio de PPP posterior, que desencadena otro cambio de PPP.

Si tiene requisitos específicos de la aplicación que impiden usar el rectángulo sugerido que Windows proporciona en el mensaje de DPICHANGED de WM \_ , consulte [**WM \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md). Este mensaje se puede usar para dar a Windows un tamaño deseado que le gustaría usar una vez que se ha producido el cambio de PPP, sin dejar de seguir los problemas descritos anteriormente.

**Falta de documentación sobre la virtualización**

Cuando un HWND o un proceso se está ejecutando como PPP no compatible o con PPP del sistema, puede ser un mapa de bits ajustado por Windows. Cuando esto sucede, Windows escala y convierte la información sensible a los PPP de algunas API en el espacio de coordenadas del subproceso que realiza la llamada. Por ejemplo, si un subproceso sin reconocimiento de PPP consulta el tamaño de la pantalla mientras se ejecuta en una pantalla de PPP alta, Windows virtualizará la respuesta proporcionada a la aplicación como si estuviera en unidades de 96 ppp. Como alternativa, cuando un subproceso de reconocimiento de PPP del sistema está interactuando con una pantalla en un PPP diferente del que estaba en uso al iniciar la sesión del usuario actual, Windows redimensiona algunas llamadas de API en el espacio de coordenadas que usaría HWND si se estaba ejecutando en su factor de escala de PPP original.

Al actualizar la aplicación de escritorio a la escala de PPP correctamente, puede resultar difícil saber qué llamadas de API pueden devolver valores virtualizados según el contexto del subproceso. Esta información no está suficientemente documentada por Microsoft. Tenga en cuenta que si llama a cualquier API del sistema a partir de un contexto de subproceso que no sea compatible con el sistema o con PPP, el valor devuelto podría estar virtualizado. Como tal, asegúrese de que el subproceso se está ejecutando en el contexto de PPP que espera al interactuar con la pantalla o las ventanas individuales. Al cambiar temporalmente el contexto de PPP de un subproceso mediante [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), asegúrese de restaurar el contexto anterior cuando haya terminado de evitar que se produzca un comportamiento incorrecto en otra parte de la aplicación.

**Muchas API de Windows no tienen un contexto de PPP**

Muchas API heredadas de Windows no incluyen un contexto de PPP o HWND como parte de su interfaz. Como resultado, los desarrolladores suelen tener que realizar trabajo adicional para controlar el escalado de cualquier información sensible a los PPP, como tamaños, puntos o iconos. Por ejemplo, los desarrolladores que usan [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) deben tener en el mapa de bits los iconos de stretch cargados o usar API alternativas para cargar los iconos de tamaño correcto para el PPP adecuado, como [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).

**Restablecimiento forzado de reconocimiento de PPP en todo el proceso**

En general, el modo de reconocimiento de PPP del proceso no se puede cambiar después de la inicialización del proceso. Sin embargo, Windows puede cambiar forzosamente el modo de reconocimiento de PPP del proceso si intenta romper el requisito de que todos los HWND de un árbol de ventana tienen el mismo modo de reconocimiento de PPP. En todas las versiones de Windows, a partir de Windows 10 1703, no es posible tener diferentes HWND en un árbol HWND que se ejecuten en distintos modos de reconocimiento de PPP. Si intenta crear una relación de elementos primarios y secundarios que interrumpa esta regla, se puede restablecer el reconocimiento de PPP de todo el proceso. Esto se puede activar mediante:

1.  Una llamada a CreateWindow en la que la ventana primaria pasada tiene un modo de reconocimiento de PPP diferente que el subproceso que realiza la llamada.
2.  Una llamada a SetParent en la que las dos ventanas están asociadas a distintos modos de reconocimiento de PPP.

En la tabla siguiente se muestra lo que ocurre si intenta infringir esta regla:



| Operación                 | Windows 8.1                                  | Windows 10 (1607 y versiones anteriores)                | Windows 10 (1703 y versiones posteriores)                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| CreateWindow (en proceso)    | N/D                                          | Los **elementos secundarios heredan** (modo mixto)              | Los **elementos secundarios heredan** (modo mixto)              |
| CreateWindow (Cross-proc) | **Restablecimiento forzado** (del proceso del llamador)       | Los **elementos secundarios heredan** (modo mixto)              | **Restablecimiento forzado** (del proceso del llamador)       |
| SetParent (en proceso)       | N/D                                          | **Restablecimiento forzado** (del proceso actual)        | **Error (error** de \_ Estado no válido \_ )             |
| SetParent (entre procedimientos)    | **Restablecimiento forzado** (del proceso de la ventana secundaria) | **Restablecimiento forzado** (del proceso de la ventana secundaria) | **Restablecimiento forzado** (del proceso de la ventana secundaria) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la API de PPP alta](high-dpi-reference.md)
</dt> <dt>

[Escala de PPP en modo mixto y API que reconocen ppp.](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

