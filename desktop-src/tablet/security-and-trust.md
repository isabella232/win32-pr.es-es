---
description: .NET Framework tiene un modelo de seguridad que trata las aplicaciones de manera diferente dependiendo de su origen.
ms.assetid: 37fa870a-6f38-44ae-943e-27697f6b9fba
title: Seguridad y confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e3039f8aa93c2ae563a918177462cd09a217af
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105649319"
---
# <a name="security-and-trust"></a>Seguridad y confianza

.NET Framework tiene un modelo de seguridad que trata las aplicaciones de manera diferente dependiendo de su origen. Los archivos ejecutables y ensamblados que son del equipo de un usuario suelen ejecutarse con plena confianza; los mismos ejecutables y ensamblados que se ejecutan a través de Internet normalmente se ejecutan con confianza parcial. Esto es para evitar que el código malintencionado lea o modifique la información a la que no debería tener acceso, como los archivos locales, los elementos del portapapeles y otros recursos. Si un ejecutable llama a un ensamblado, que a su vez llama a otro ensamblado que requiere cierto nivel de confianza, se aplica el nivel de confianza más bajo de todos los componentes de la cadena. Sin embargo, un administrador de un equipo puede establecer permisos específicos que invalidan los permisos predeterminados.

Una introducción al modelo de seguridad se proporciona en [controles seguros Light-Weight Client-Side](/archive/msdn-magazine/2002/january/dhtml-and-net-host-secure-lightweight-client-side-controls-in-microsoft-internet-explorer)y puede obtener más información sobre el modelo de seguridad en la [seguridad de acceso del código en la práctica](/previous-versions/msp-n-p/ff648663(v=pandp.10)). Puede encontrar una buena introducción sobre la seguridad de las bibliotecas (que es especialmente importante para los objetos de [**UserControl**](/uwp/api/Windows.UI.Xaml.Controls.UserControl?view=winrt-19041) en una página web) en el [uso de bibliotecas de código de confianza parcial](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconusinglibrariesfrompartiallytrustedcode.asp)y otra información de seguridad sobre controles administrados en [escribir controles administrados seguros](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconwritingsecuremanagedcontrols.asp%3fframe%3dtrue).

## <a name="permissions"></a>Permisos

La mayoría de los objetos y miembros administrados de la API de tecnologías de Tablet PC tienen dos requisitos:

-   La ejecución siempre es obligatoria.
-   Se requiere FullTrust cuando se produce la acción de seguridad [InheritanceDemand](/previous-versions/windows/) . Esto significa que se requiere plena confianza cuando una clase derivada hereda una clase o invalida un método del SDK de Tablet PC.

En la tabla siguiente se enumeran las clases y los miembros que requieren permisos adicionales. Los permisos para una clase determinada también se aplican a todos sus miembros que no aparecen en esta tabla.



| Clase o método                                                                       | Permisos                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                                  | [UIPermissionClipboard. AllClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Ink. ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                                    | [UIPermissionClipboard. OwnClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Ink. ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                                  | [UIPermissionClipboard. AllClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**InkCollector**](inkcollector-class.md)                                            | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| InkCollector (IntPtr)                                                                  | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) y [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| InkCollector. Handle                                                                   | [UIPermissionWindow. allcargador](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) y [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) (vea la nota a continuación)<br/> |
| InkEdit                                                                               | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [InkOverlay](/previous-versions/ms552322(v=vs.100))                                   | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| InkOverlay (IntPtr)                                                                    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) y SecurityPermissionFlag. UnmanagedCode<br/>                                                                 |
| [InkOverlay. Handle](/previous-versions/ms833109(v=msdn.10))                      | [UIPermissionWindow. allcargador](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1) y [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) (vea la nota a continuación)<br/> |
| [InkPicture](/previous-versions/aa514604(v=msdn.10))                                   | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| [PenInputPanel](/previous-versions/aa514041(v=msdn.10))                             | Vea la nota siguiente.<br/>                                                                                                                                                                                     |
| [**InkRenderer**](inkrenderer-class.md)                                              | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw), [ **DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)        | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) y [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| Renderer. InkSpaceToPixel (IntPtr, Point), renderer. InkSpaceToPixel (IntPtr, Point \[ \] )    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) y [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| Renderer. PixelToInkSpace (IntPtr, Point), renderer. PixelToInkSpace (IntPtr, Point \[ \] )    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) y [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))                                      | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| DynamicRenderer (IntPtr)                                                               | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) y [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**RealTimeStylus**](realtimestylus-class.md)                                        | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| RealTimeStylus (IntPtr), RealTimeStylus (IntPtr, Boolean), RealTimeStylus (IntPtr, tableta) | [UIPermissionWindow. allcargador](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) y [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>                  |



 

> [!Note]  
> Por lo general, es preferible utilizar un control en lugar de un identificador (IntPtr) para los constructores, ya que los controles requieren menos permisos. Del mismo modo, es preferible usar un objeto gráfico en lugar de un identificador para representador [. Draw](/previous-versions/ms828488(v=msdn.10)), [renderer. InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) y [renderer. PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)).

 

> [!Note]  
> Las propiedades [InkCollector. Handle](/previous-versions/ms836504(v=msdn.10)) y [InkOverlay. Handle](/previous-versions/ms833109(v=msdn.10)) no requieren el permiso [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) si el identificador es para un control Windows Forms, pero sí para otras ventanas.

 

> [!Note]  
> En el caso de la clase [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , los siguientes métodos y propiedades requieren [SecurityPermissionFlag. AllFlags](/previous-versions/windows/): PenInputPanel (IntPtr), [AttachedEditWindow](/previous-versions/ms582240(v=vs.100)), [busy](/previous-versions/ms571975(v=vs.100)), [CommitPendingInput](/previous-versions/ms569650(v=vs.100)), [CurrentPanel](/previous-versions/ms571976(v=vs.100)), [DefaultPanel](/previous-versions/ms571977(v=vs.100)), [EnableTsf](/previous-versions/ms569656(v=vs.100)), [Factoid](/previous-versions/ms571978(v=vs.100)), [height](/previous-versions/ms571979(v=vs.100)), [HorizontalOffset](/previous-versions/ms571980(v=vs.100)), [InputFailed](/previous-versions/ms567738(v=vs.100)), [left](/previous-versions/ms571981(v=vs.100)), [moveTo](/previous-versions/ms569667(v=vs.100)), [PanelChanged](/previous-versions/ms567741(v=vs.100)), [PanelMoving](/previous-versions/ms567748(v=vs.100)), [Refresh](/previous-versions/ms569778(v=vs.100)), [Top](/previous-versions/ms571982(v=vs.100)), [VerticalOffset](/previous-versions/ms571983(v=vs.100)), [visible](/previous-versions/ms571984(v=vs.100)), [VisibleChanged](/previous-versions/ms567754(v=vs.100))y [width](/previous-versions/ms571985(v=vs.100)).

 

## <a name="other-considerations"></a>Otras consideraciones

Otras consideraciones de seguridad conocidas son:

-   Se requiere Microsoft Internet Explorer 6 o una versión posterior para que los controles Web funcionen correctamente. Con Internet Explorer 5,5, solo se cargan los controles administrados iniciales; no se pueden cargar controles adicionales dinámicamente en tiempo de ejecución.
-   Si usa Windows XP Service Pack 2 (SP2) y CLR 1.0, tener controles Web en Internet Explorer requiere agregar el sitio como un sitio de confianza, incluso si se encuentran en la zona de intranet. Sin embargo, cuando lo haga, ya no se ejecutarán en la zona de sitios de confianza, aunque se ejecuten en la zona de intranet. Este problema se ha corregido con CLR 1.1.

 

 