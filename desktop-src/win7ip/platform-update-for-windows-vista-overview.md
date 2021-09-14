---
title: Acerca de la actualización de plataforma para Windows Vista
description: Proporciona información general sobre la actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008 y sus características.
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Actualización de plataforma para Windows Server 2008
- Actualización de plataforma para Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bcd3e94f8784ce3d060a8e56c0b089a065d288
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359589"
---
# <a name="about-platform-update-for-windows-vista"></a>Acerca de la actualización de plataforma para Windows Vista

La actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008 son actualizaciones del sistema operativo del usuario final que admiten el uso de tecnologías de Windows 7 seleccionadas en versiones anteriores del sistema operativo Windows. Las actualizaciones incluyen un conjunto de bibliotecas en tiempo de ejecución que permiten a los desarrolladores de aplicaciones tener como destino las versiones actuales, Windows 7 y Windows Server 2008 R2, así como versiones anteriores, Windows Vista y Windows Server 2008.

## <a name="summary-of-supported-api-by-technology"></a>Resumen de la API admitida por tecnología

Cada tecnología compatible con la actualización de plataforma para Windows Vista y la actualización de plataforma para las actualizaciones de Windows Server 2008 incluye un conjunto de API que se puede usar en una aplicación que tiene como destino la versión anterior de Windows.

Para obtener más información sobre el uso de las API admitidas por las actualizaciones de una aplicación que tiene como destino versiones anteriores de Windows, vea [Developing Application for Previous Versions of Windows](developing-applications-for-previous-versions-of-windows.md).

> [!Note]  
> Es posible que algunas API asociadas a una tecnología no sean compatibles y el comportamiento, el rendimiento o los requisitos de algunas API admitidas pueden variar en Windows versiones. Para más información sobre la API admitida para una tecnología específica, haga clic en el vínculo de una de las tablas de resumen para ir a la sección sobre esa tecnología.

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a>Tecnologías admitidas con la actualización de plataforma para Windows Vista

Para más información sobre la API admitida para una tecnología específica, haga clic en el vínculo de una de las tablas de resumen para ir a la sección sobre esa tecnología.

Las tecnologías que se admiten para Windows Vista y Windows XP con la actualización de plataforma para Windows Vista se muestran en la tabla siguiente.

| Tecnología                                                                                    | Windows Vista | Windows XP |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [API de automatización de Windows](#windows-automation-api)                                             | Sí           | Sí        |
| [Windows Gráficos, imágenes y biblioteca XPS](#windows-graphics-imaging-and-xps-library)        | Sí           | No         |
| [Windows Cinta de opciones y biblioteca del Administrador de animaciones](#windows-ribbon-and-animation-manager-library) | Sí           | No         |
| [Windows Plataforma de dispositivos portátiles](#windows-portable-devices-platform)                       | Sí           | No         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a>Tecnologías compatibles con la actualización de plataforma para Windows Server 2008

Para más información sobre la API admitida para una tecnología específica, haga clic en el vínculo de una de las tablas de resumen para ir a la sección sobre esa tecnología.

Las tecnologías que se admiten para Windows Server 2008 y Windows Server 2003 con la actualización de plataforma para Windows Server 2008 se muestran en la tabla siguiente.

| Tecnología                                                                                    | Windows Server 2008 | Windows Server 2003 |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [API de automatización de Windows](#windows-automation-api)                                             | Sí                 | Sí                 |
| [Windows Gráficos, imágenes y biblioteca XPS](#windows-graphics-imaging-and-xps-library)        | Sí                 | No                  |
| [Windows Cinta de opciones y biblioteca del Administrador de animaciones](#windows-ribbon-and-animation-manager-library) | Sí                 | No                  |
| [Windows Plataforma de dispositivos portátiles](#windows-portable-devices-platform)                       | No                  | No                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a>Descripciones de la API admitida por la tecnología

Para más información sobre la API admitida para una tecnología específica, haga clic en el vínculo de una de las tablas de resumen para ir a la sección sobre esa tecnología.

-   [API de automatización de Windows](#windows-automation-api)
-   [Windows Gráficos, imágenes y biblioteca XPS](#windows-graphics-imaging-and-xps-library)
-   [Windows Cinta de opciones y biblioteca del Administrador de animaciones](#windows-ribbon-and-animation-manager-library)
-   [Windows Plataforma de dispositivos portátiles](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a>API de automatización de Windows

Windows Automation API 3.0 es un conjunto de archivos DLL y elementos de API que permiten a los productos de tecnología de asistencia (AT) proporcionar un mejor acceso al equipo para las personas que tienen dificultades físicas o cognitivas, discapacidades o discapacidades. Además, dado que Windows Automation API 3.0 permite que las aplicaciones accedan y manipulen los elementos de la interfaz de usuario (UI) de otras aplicaciones, es una tecnología ideal para implementar herramientas de prueba automatizadas.

Microsoft Active Accessibility (MSAA) y Automatización de la interfaz de usuario son similares en que proporcionan un medio para exponer y recopilar información sobre los controles y elementos de la interfaz de usuario para admitir la accesibilidad de la interfaz de usuario y la automatización de pruebas de software. Automatización de la interfaz de usuario es una Windows implementación de la especificación Automatización de la interfaz de usuario datos. Es una tecnología más reciente que aborda muchas de las limitaciones de MSAA.

Para obtener más información sobre Windows Automation API 3.0, [vea Windows Automation API: Overview .](/windows/desktop/WinAuto/windows-automation-api-overview)

La actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008 admiten las siguientes Windows Automation API 3.0:

-   [Microsoft Active Accessibility (MSAA)](#microsoft-active-accessibility-msaa)
-   [Automatización de la interfaz de usuario](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Ediciones aptas para las actualizaciones

La actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008 habilitan la compatibilidad con Windows Automation API 3.0 en las ediciones de Windows que se muestran en la tabla siguiente.



<table>
<thead>
<tr class="header">
<th>Versión de Windows</th>
<th>Ediciones aptas para actualización</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter con SP2 (x86)<br />
Home Basic con SP2 (x86 y amd64)<br />
Inicio Premium con SP2 (x86 y amd64)<br />
Negocio con SP2 (x86 y amd64)<br />
Enterprise con SP2 (x86 y amd64)<br />
Ultimate con SP2 (x86 y amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows XP</td>
<td><dl> Windows XP Home with SP3 (x86)<br />
Windows XP Professional con SP3 (x86)<br />
</dl></td>
</tr>
<tr class="odd">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 con SP2 (x86 y amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2003</td>
<td><dl> Windows Server 2003 con SP2 (x86 y amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a>Microsoft Active Accessibility (MSAA)

Microsoft Active Accessibility (MSAA) es una tecnología heredada que se introdujo por primera vez con Windows 95. Se trata de un conjunto de API que mejora la forma en que los productos de tecnología de asistencia (AT) funcionan con aplicaciones que se ejecutan en Microsoft Windows. La API proporciona interfaces de programación y métodos para exponer información sobre los elementos de la interfaz de usuario.

Para obtener más información sobre Microsoft Active Accessibility, vea [Información general técnica.](/windows/desktop/WinAuto/technical-overview)

### <a name="supported-microsoft-active-accessibility-api-elements"></a>Elementos Microsoft Active Accessibility API admitidos

Todas las API se admiten en versiones anteriores de Windows que son aptas para la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008.

### <a name="ui-automation"></a>Automatización de la interfaz de usuario

Automatización de la interfaz de usuario es una tecnología más reciente que implementa la especificación Automatización de la interfaz de usuario y aborda muchas de las limitaciones de Microsoft Active Accessibility. Es un conjunto de API que proporciona acceso mediante programación a los elementos de la interfaz de usuario de las aplicaciones. La API proporcionada ayuda a los productos de assistive Technology y a las herramientas de prueba automatizadas a acceder, identificar y manipular los elementos de interfaz de usuario estándar y personalizados de una aplicación.

Para obtener más información sobre Automatización de la interfaz de usuario, [consulte Windows Automation API: Automatización de la interfaz de usuario](../winauto/entry-uiauto-win32.md).

### <a name="supported-ui-automation-api-elements"></a>Elementos Automatización de la interfaz de usuario API admitidos

Todas las API se admiten en versiones anteriores de Windows que son aptas para la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008.

### <a name="running-ui-automation-on-previous-windows-versions"></a>Ejecución de Automatización de la interfaz de usuario en versiones Windows anteriores

Debido a las diferencias en la forma en que los controles comunes y los controles estándar de Windows se implementan en diferentes versiones de Windows, puede haber ligeras diferencias en la información que recuperan los servidores proxy de Automatización de la interfaz de usuario para estos controles de una versión a otra.

### <a name="windows-graphics-imaging-and-xps-library"></a>Windows Gráficos, imágenes y biblioteca XPS

La actualización de plataforma para Windows Vista admite las siguientes API Windows 7 de la biblioteca de Windows Gráficos, Creación de imágenes y XPS:

-   [Direct2D](#direct2d)
-   [Direct3D](#direct3d)
-   [DirectWrite](#directwrite)
-   [Packaging](#packaging)
-   [Windows Imaging Component](#windows-imaging-component)
-   [Documento XPS](#xps-document)
-   [XPS Print](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Ediciones aptas para las actualizaciones

La actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008 habilitan la compatibilidad con gráficos, imágenes y biblioteca XPS de Windows en las ediciones de Windows que se muestran en la tabla siguiente.



<table>
<thead>
<tr class="header">
<th>Versión de Windows</th>
<th>Ediciones aptas para actualización</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter con SP2 (x86)<br />
Home Basic con SP2 (x86 y amd64)<br />
Inicio Premium con SP2 (x86 y amd64)<br />
Negocio con SP2 (x86 y amd64)<br />
Enterprise con SP2 (x86 y amd64)<br />
Ultimate con SP2 (x86 y amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 con SP2 (x86 y amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="direct2d"></a>Direct2D

Direct2D API es una nueva API de gráficos 2D de modo inmediato acelerada por hardware que proporciona un alto rendimiento y una representación de alta calidad para geometría 2D, mapas de bits y texto. La API de Direct2D está diseñada para interoperar bien con código existente que usa GDI, GDI+ o Direct3D.

Para obtener más información sobre Direct2D, vea [Acerca de Direct2D.](/windows/desktop/Direct2D/direct2d-overview)

### <a name="supported-direct2d-api-elements"></a>Elementos de API de Direct2D admitidos

Todas las API se admiten en versiones anteriores de Windows que son aptas para la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008.

### <a name="running-direct2d-on-previous-windows-versions"></a>Ejecución de Direct2D en versiones Windows anteriores

Si falta el controlador WDDM 1.1 en Windows Vista, el rendimiento de la interoperabilidad de Direct2D/GDI se degrada.

### <a name="direct3d"></a>Direct3D

La actualización de plataforma para Windows Vista proporciona compatibilidad con la superficie de BGRA para las rutas de acceso de código Direct3D10 y Direct3D10.1. Direct3D10Level9 permite que la funcionalidad de Direct3D10 funcione en hardware de Direct3D9. Direct3D WARP10 es un rasterizador de software de rendimiento para aplicaciones Direct3D10. Direct3D11, la versión más reciente de Direct3D, proporciona nuevas funcionalidades, como compatibilidad mejorada con multithreading, teselación, funcionalidad DirectCompute y vinculación dinámica del sombreador.

Si crea aplicaciones que usan Direct3D, se requiere el [SDK de DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .

Para obtener más información sobre Direct3D, [vea Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/default.aspx) .

### <a name="supported-direct3d-api-elements"></a>Elementos de API de Direct3D admitidos

Todas las API se admiten en versiones anteriores de Windows que son aptas para la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008.

### <a name="directwrite"></a>DirectWrite

La API DirectWrite es una nueva API de texto que proporciona varias capas de funcionalidad, incluido el diseño de texto, el procesamiento de scripts, la representación de glifos y el sistema de fuentes. DirectWrite usa fuentes OpenType y representación clearType de subpíxeles para mejorar la experiencia de texto proporcionada por las aplicaciones. La representación de texto se acelera por hardware cuando se usa con Direct2D.

Para obtener más información sobre DirectWrite, vea [Introducing DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).

### <a name="supported-directwrite-api-elements"></a>Elementos DirectWrite API admitidos

Todas las API se admiten en versiones anteriores de Windows que son aptas para la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008.

### <a name="running-directwrite-on-previous-windows-versions"></a>Ejecución de DirectWrite en versiones Windows anteriores

Los siguientes problemas de comportamiento pueden afectar al uso de DirectWrite API en versiones Windows anteriores:

-   Es posible que los scripts Windows 7 no se represente completamente correctamente en versiones Windows anteriores.
-   Las configuraciones regionales no disponibles en Windows versiones anteriores se resales al comportamiento predeterminado.
-   ClearType Tuner no está disponible en versiones Windows anteriores.
-   La interoperabilidad de GDI tiene un mayor costo de memoria en algunos escenarios en versiones Windows anteriores.

### <a name="packaging"></a>Packaging

La actualización de plataforma para Windows Vista admite un subconjunto limitado de las API de empaquetado necesarias para realizar tareas con document API XPS en aplicaciones no administradas.

Para obtener más información sobre las API de empaquetado, consulte Información [general de Packaging API.](/previous-versions/windows/desktop/opc/packaging-api-overview)

### <a name="supported-packaging-api-elements"></a>Elementos de API de empaquetado admitidos

Solo se admiten las siguientes interfaces de empaquetado:

-   IOpcUri
-   IOpcPartUri
-   IOpcFactory (solo se admiten los métodos siguientes)
    -   CreatePackageRootUri
    -   CreatePartUri
    -   CreateStreamOnFile

Las API de empaquetado compatibles se pueden usar para crear secuencias a través de archivos, así como para crear e interactuar con el URI basado en paquetes.

### <a name="running-packaging-api-on-previous-windows-versions"></a>Ejecución de Packaging API en versiones Windows anteriores

El comportamiento y el rendimiento de los métodos y interfaces de empaquetado admitidos son los mismos en todas las plataformas admitidas.

Si una aplicación intenta crear instancias o llamar a un método o interfaz de empaquetado no admitidos, se producirá un error en el intento. Si la llamada es a un método [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) no compatible, se devolverá el código de error E \_ NOTIMPL.

### <a name="windows-imaging-component"></a>Windows Imaging Component

Las nuevas características de Windows Imaging Component (WIC) incluyen seguridad mejorada, compatibilidad con un color alto y una mejor interoperabilidad de metadatos. Además, el componente de creación de imágenes de Windows amplía su cumplimiento de estándares al proporcionar compatibilidad con la descodación progresiva de imágenes, características PNG expandida, metadatos GIF, , actualizaciones de fotos de HD y metadatos que abarcan segmentos APPn.

Para obtener más información sobre el Windows de creación de imágenes, vea el Windows información general del [componente de creación de imágenes.](/windows/desktop/wic/-wic-about-windows-imaging-codec)

### <a name="supported-wic-api-elements"></a>Elementos de LA API de WIC admitidos

Todas las API se admiten en versiones anteriores de Windows que son aptas para la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008.

### <a name="xps-document"></a>Documento XPS

Las API de documentos XPS admiten la creación, modificación y guardado de documentos XPS en aplicaciones no administradas

Para obtener más información sobre las API de documentos XPS, consulte la Guía [de programación de documentos XPS.](/previous-versions//dd372978(v=vs.85))

### <a name="supported-xps-document-api-elements"></a>Elementos de la API de documentos XPS admitidos

Solo las [interfaces xps digital signatures](/previous-versions/windows/desktop/dd372947(v=vs.85)) no se admiten en las versiones de sistema operativo de nivel inferior.

### <a name="xps-print"></a>XPS Print

Las API de impresión XPS admiten la impresión de documentos XPS desde Windows basadas en aplicaciones.

Para obtener más información sobre las API de impresión XPS, consulte [XpsPrint API](/windows/desktop/printdocs/xpsprint-api).

### <a name="supported-xps-print-api-elements"></a>Elementos de LA API de impresión XPS admitidos

Todas las API se admiten en versiones anteriores de Windows que son aptas para la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008.

### <a name="windows-ribbon-and-animation-manager-library"></a>Windows Cinta de opciones y biblioteca del Administrador de animaciones

La actualización de plataforma para Windows Vista admite las siguientes API Windows 7 desde la cinta Windows y Biblioteca de animaciones:

-   [Windows Marco de la cinta de opciones](#windows-ribbon-and-animation-manager-library)
-   [Windows Administrador de animaciones](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Ediciones aptas para las actualizaciones

La actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008 habilitan la compatibilidad con la cinta de opciones y la biblioteca del Administrador de animaciones de Windows en las ediciones de Windows que se muestran en la tabla siguiente.



<table>
<thead>
<tr class="header">
<th>Versión de Windows</th>
<th>Ediciones aptas para actualización</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter con SP2 (x86)<br />
Home Basic con SP2 (x86 y amd64)<br />
Inicio Premium con SP2 (x86 y amd64)<br />
Negocio con SP2 (x86 y amd64)<br />
Enterprise con SP2 (x86 y amd64)<br />
Ultimate con SP2 (x86 y amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 con SP2 (x86 y amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="windows-ribbon-framework"></a>Windows Marco de la cinta de opciones

El marco Windows cinta de opciones (cinta) es un completo sistema de presentación de comandos que proporciona una alternativa moderna a los menús en capas, las barras de herramientas y los paneles de tareas de las aplicaciones Windows tradicionales.

El marco es una colección de API de Microsoft Win32 que proporcionan una serie de nuevas funcionalidades de interfaz de usuario para desarrolladores de Windows e incluye la cinta de opciones y un sistema de menú contextual.

Para obtener más información sobre el marco de la cinta de opciones, vea [Introducing the Windows Ribbon Framework](../windowsribbon/windowsribbon-introduction.md).

### <a name="supported-ribbon-framework-api-elements"></a>Elementos de API de Ribbon Framework admitidos

Todas las API se admiten en versiones anteriores de Windows que son aptas para la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008.

### <a name="windows-animation-manager"></a>Windows Administrador de animaciones

El Windows animation manager (Windows Animation) es una interfaz de programación que admite la animación de elementos visuales de Windows aplicaciones. Windows La animación está diseñada para simplificar el desarrollo y el mantenimiento de secuencias de animación y para permitir a los desarrolladores implementar animaciones coherentes e intuitivas. Windows La animación se puede usar con cualquier plataforma gráfica, como Direct2D, Direct3D o GDI+.

Windows Animation es una API COM de un solo subproceso que proporciona todo lo que un desarrollador necesita para crear, administrar y controlar la animación de la interfaz de usuario.

Para obtener más información sobre Windows Animation Manager, vea [Introducing Windows Animation](/windows/desktop/UIAnimation/introducing-windows-animation-manager).

### <a name="supported-animation-manager-api-elements"></a>Elementos de API de Animation Manager admitidos

Todas las API se admiten en versiones anteriores de Windows que son aptas para la actualización de plataforma para Windows Vista o la actualización de plataforma para Windows Server 2008.

### <a name="windows-portable-devices-platform"></a>Windows Plataforma de dispositivos portátiles

La actualización de plataforma para Windows Vista admite las Windows 7 a la plataforma Windows dispositivos portátiles (WPD). Esta característica permite a los equipos comunicarse con dispositivos de almacenamiento y medios conectados. WPD proporciona una manera flexible y sólida de que los equipos se comuniquen con cámaras digitales, reproductores de música, teléfonos móviles y muchos otros tipos de dispositivos conectados.

Para obtener más información sobre Windows dispositivos portátiles, [vea Windows Portable Devices](/windows-hardware/drivers/portable/) ( https://docs.microsoft.com/windows-hardware/drivers/portable/) .

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Ediciones aptas para las actualizaciones

La actualización de plataforma para Windows Vista y la actualización de plataforma para Windows Server 2008 habilitan la compatibilidad con dispositivos portátiles (WPD) de Windows en las ediciones de Windows que se muestran en la tabla siguiente.



<table>
<thead>
<tr class="header">
<th>Versión de Windows</th>
<th>Ediciones aptas para actualización</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter con SP2 (x86)<br />
Home Basic con SP2 (x86 y amd64)<br />
Inicio Premium con SP2 (x86 y amd64)<br />
Negocio con SP2 (x86 y amd64)<br />
Enterprise con SP2 (x86 y amd64)<br />
Ultimate con SP2 (x86 y amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a>Elementos de API de WPD admitidos

En la tabla siguiente se identifican las características que se admiten para las versiones Windows 7, Windows Vista y Windows Vista con la actualización de plataforma para las versiones de Windows Vista del sistema operativo Windows.

| Característica WPD                    | Windows 7 | Windows Vista | Windows Vista con actualización de plataforma para Windows Vista |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| MTP a través de USB                   | Sí       | Sí           | Sí                                                  |
| MTP a través de IP                    | Sí       | Sí           | Sí                                                  |
| MTP sobre Bluetooth             | Sí       | No            | Sí                                                  |
| WPD y MTP Device Services    | Sí       | No            | Sí                                                  |
| Automatización de WPD                 | Sí       | No            | No                                                   |
| Multi-function/Multi-transport | Sí       | No            | No                                                   |
| Device Stage (puede estar en inglés)                   | Sí       | No            | No                                                   |
| Plataforma de sincronización de dispositivos           | Sí       | No            | No                                                   |



 

Para las ediciones de Windows 7 y Windows Vista que no tienen Microsoft Reproductor de Windows Media instalado de forma predeterminada (las ediciones N y KN), debe instalar el SDK de [Windows Media Format 11]( ../audio-and-video.md) ( para habilitar la funcionalidad https://msdn.microsoft.com/windows/bb190326.aspx) de WPD. Para obtener más información, [vea el Knowledge Base](https://support.microsoft.com/kb/953693) ( , que se publicó originalmente como una resolución para Windows https://go.microsoft.com/fwlink/p/?linkid=158715) Vista.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Actualización de plataforma para Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Temas de introducción**
</dt> <dt>

[Acerca de la actualización de plataforma para Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Knowledge Base sobre la actualización de plataforma para Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 