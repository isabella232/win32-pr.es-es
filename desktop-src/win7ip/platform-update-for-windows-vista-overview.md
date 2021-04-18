---
title: Acerca de la actualización de la plataforma para Windows Vista
description: Proporciona información general sobre la actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 y sus características.
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Actualización de la plataforma para Windows Server 2008
- Actualización de la plataforma para Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bcd3e94f8784ce3d060a8e56c0b089a065d288
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105707639"
---
# <a name="about-platform-update-for-windows-vista"></a>Acerca de la actualización de la plataforma para Windows Vista

La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 son actualizaciones del sistema operativo del usuario final que admiten el uso de las tecnologías de Windows 7 seleccionadas en versiones anteriores del sistema operativo Windows. Las actualizaciones incluyen un conjunto de bibliotecas en tiempo de ejecución que permiten a los desarrolladores de aplicaciones tener como destino las versiones actuales, Windows 7 y Windows Server 2008 R2, así como las versiones anteriores, Windows Vista y Windows Server 2008.

## <a name="summary-of-supported-api-by-technology"></a>Resumen de API admitidas por tecnología

Cada tecnología compatible con la actualización de la plataforma para Windows Vista y la actualización de la plataforma para las actualizaciones de Windows Server 2008 incluye un conjunto de API que se puede usar en una aplicación que tiene como destino la versión anterior de Windows.

Para obtener más información sobre el uso de las API admitidas por las actualizaciones en una aplicación que tiene como destino versiones anteriores de Windows, consulte [desarrollo de aplicaciones para versiones anteriores de Windows](developing-applications-for-previous-versions-of-windows.md).

> [!Note]  
> Algunas API que están asociadas a una tecnología pueden no admitirse y el comportamiento, el rendimiento o los requisitos de algunas de las API admitidas pueden variar en función de las versiones de Windows. Para obtener más información sobre la API admitida para una tecnología específica, haga clic en el vínculo de una de las tablas de resumen para ir a la sección sobre esa tecnología.

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a>Tecnologías compatibles con la actualización de la plataforma para Windows Vista

Para obtener más información sobre la API admitida para una tecnología específica, haga clic en el vínculo de una de las tablas de resumen para ir a la sección sobre esa tecnología.

En la tabla siguiente se muestran las tecnologías compatibles con Windows Vista y Windows XP con la actualización de la plataforma para Windows Vista.

| Technology                                                                                    | Windows Vista | Windows XP |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [API de automatización de Windows](#windows-automation-api)                                             | Sí           | Sí        |
| [Biblioteca de gráficos de Windows, de imágenes y XPS](#windows-graphics-imaging-and-xps-library)        | Sí           | No         |
| [Cinta de Windows y biblioteca del administrador de animaciones](#windows-ribbon-and-animation-manager-library) | Sí           | No         |
| [Plataforma de dispositivos portátiles de Windows](#windows-portable-devices-platform)                       | Sí           | No         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a>Tecnologías compatibles con la actualización de la plataforma para Windows Server 2008

Para obtener más información sobre la API admitida para una tecnología específica, haga clic en el vínculo de una de las tablas de resumen para ir a la sección sobre esa tecnología.

En la tabla siguiente se muestran las tecnologías compatibles con Windows Server 2008 y Windows Server 2003 con la actualización de la plataforma para Windows Server 2008.

| Technology                                                                                    | Windows Server 2008 | Windows Server 2003 |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [API de automatización de Windows](#windows-automation-api)                                             | Sí                 | Sí                 |
| [Biblioteca de gráficos de Windows, de imágenes y XPS](#windows-graphics-imaging-and-xps-library)        | Sí                 | No                  |
| [Cinta de Windows y biblioteca del administrador de animaciones](#windows-ribbon-and-animation-manager-library) | Sí                 | No                  |
| [Plataforma de dispositivos portátiles de Windows](#windows-portable-devices-platform)                       | No                  | No                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a>Descripciones de API admitidas por tecnología

Para obtener más información sobre la API admitida para una tecnología específica, haga clic en el vínculo de una de las tablas de resumen para ir a la sección sobre esa tecnología.

-   [API de automatización de Windows](#windows-automation-api)
-   [Biblioteca de gráficos de Windows, de imágenes y XPS](#windows-graphics-imaging-and-xps-library)
-   [Cinta de Windows y biblioteca del administrador de animaciones](#windows-ribbon-and-animation-manager-library)
-   [Plataforma de dispositivos portátiles de Windows](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a>API de automatización de Windows

Windows Automation API 3,0 es un conjunto de archivos dll y elementos de API que permiten a los productos de tecnología de asistencia (AT) proporcionar un mejor acceso al equipo para usuarios que tienen dificultades físicas o cognitivas, deficiencias o discapacidades. Además, dado que la API de Windows Automation 3,0 permite a las aplicaciones tener acceso a los elementos de la interfaz de usuario (UI) de otras aplicaciones y manipularlos, es una tecnología ideal para implementar herramientas de pruebas automatizadas.

Microsoft Active Accessibility (MSAA) y la automatización de la interfaz de usuario son similares en que ambos proporcionan un medio para exponer y recopilar información sobre los elementos y controles de la interfaz de usuario para admitir la automatización de la prueba de software y la accesibilidad de la interfaz de usuario. La automatización de la interfaz de usuario es una implementación de Windows de la especificación de UI Automation. Se trata de una tecnología más reciente que aborda muchas de las limitaciones de MSAA.

Para obtener más información sobre la API de Windows Automation 3,0, consulte [API de Windows Automation: información general](/windows/desktop/WinAuto/windows-automation-api-overview).

La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 admiten la siguiente API de automatización de Windows 3,0:

-   [Microsoft Active Accessibility (MSAA)](#microsoft-active-accessibility-msaa)
-   [Automatización de la interfaz de usuario](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a>Ediciones de Windows válidas para las actualizaciones

La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 habilitan la compatibilidad con la API de Windows Automation 3,0 en las ediciones de Windows que se muestran en la tabla siguiente.



<table>
<thead>
<tr class="header">
<th>Versión de Windows</th>
<th>Ediciones válidas para la actualización</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter con SP2 (x86)<br />
Home Basic con SP2 (x86 y AMD64)<br />
Home Premium con SP2 (x86 y AMD64)<br />
Empresa con SP2 (x86 y AMD64)<br />
Enterprise con SP2 (x86 y AMD64)<br />
Ultimate con SP2 (x86 y AMD64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows XP</td>
<td><dl> Windows XP Home con SP3 (x86)<br />
Windows XP Professional con SP3 (x86)<br />
</dl></td>
</tr>
<tr class="odd">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 con SP2 (x86 y AMD64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2003</td>
<td><dl> Windows Server 2003 con SP2 (x86 y AMD64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a>Microsoft Active Accessibility (MSAA)

Microsoft Active Accessibility (MSAA) es una tecnología heredada que se presentó por primera vez con Windows 95. Es un conjunto de API que mejora la forma en que los productos de tecnología de asistencia (AT) funcionan con las aplicaciones que se ejecutan en Microsoft Windows. La API proporciona interfaces y métodos de programación para exponer información sobre los elementos de la interfaz de usuario.

Para obtener más información acerca de Microsoft Active Accessibility, consulte la [información técnica](/windows/desktop/WinAuto/technical-overview).

### <a name="supported-microsoft-active-accessibility-api-elements"></a>Elementos de la API de Microsoft Active Accessibility admitidos

Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.

### <a name="ui-automation"></a>Automatización de la interfaz de usuario

La automatización de la interfaz de usuario es una tecnología más reciente que implementa la especificación de automatización de la interfaz de usuario y aborda muchas de las limitaciones de Microsoft Active Accessibility. Es un conjunto de API que proporciona acceso mediante programación a los elementos de la interfaz de usuario de las aplicaciones. La API proporcionada ayuda a los productos de tecnología de asistencia y a las herramientas de pruebas automatizadas a obtener acceso, identificar y manipular los elementos de interfaz de usuario estándar y personalizados de una aplicación.

Para obtener más información sobre la automatización de la interfaz de usuario, consulte [API de automatización de Windows: UI Automation](../winauto/entry-uiauto-win32.md).

### <a name="supported-ui-automation-api-elements"></a>Elementos de API de automatización de la interfaz de usuario admitidos

Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.

### <a name="running-ui-automation-on-previous-windows-versions"></a>Ejecutar automatización de la interfaz de usuario en versiones anteriores de Windows

Debido a las diferencias en la forma en que los controles comunes y los controles estándar de Windows se implementan en distintas versiones de Windows, pueden existir ligeras diferencias en la información que los proxies de automatización de la interfaz de usuario recuperan para estos controles de una versión a otra.

### <a name="windows-graphics-imaging-and-xps-library"></a>Biblioteca de gráficos de Windows, de imágenes y XPS

La actualización de la plataforma para Windows Vista admite las siguientes API de Windows 7 de la biblioteca de gráficos, imágenes y XPS de Windows:

-   [Direct2D](#direct2d)
-   [Direct3D](#direct3d)
-   [DirectWrite](#directwrite)
-   [Packaging](#packaging)
-   [Windows Imaging Component](#windows-imaging-component)
-   [Documento XPS](#xps-document)
-   [Impresión XPS](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a>Ediciones de Windows válidas para las actualizaciones

La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 habilitan la compatibilidad con gráficos, imágenes y biblioteca XPS de Windows en las ediciones de Windows que se muestran en la tabla siguiente.



<table>
<thead>
<tr class="header">
<th>Versión de Windows</th>
<th>Ediciones válidas para la actualización</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter con SP2 (x86)<br />
Home Basic con SP2 (x86 y AMD64)<br />
Home Premium con SP2 (x86 y AMD64)<br />
Empresa con SP2 (x86 y AMD64)<br />
Enterprise con SP2 (x86 y AMD64)<br />
Ultimate con SP2 (x86 y AMD64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 con SP2 (x86 y AMD64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="direct2d"></a>Direct2D

La API de Direct2D es una nueva API de gráficos 2D de modo inmediato y con aceleración de hardware que proporciona alto rendimiento y representación de alta calidad para la geometría 2D, los mapas de bits y el texto. La API de Direct2D está diseñada para interoperar bien con el código existente que usa GDI, GDI+ o Direct3D.

Para obtener más información sobre Direct2D, consulte [acerca de direct2d](/windows/desktop/Direct2D/direct2d-overview).

### <a name="supported-direct2d-api-elements"></a>Elementos compatibles de la API de Direct2D

Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.

### <a name="running-direct2d-on-previous-windows-versions"></a>Ejecutar Direct2D en versiones anteriores de Windows

Si falta el controlador WDDM 1,1 en Windows Vista, el rendimiento de la interoperabilidad de Direct2D/GDI disminuye.

### <a name="direct3d"></a>Direct3D

La actualización de la plataforma para Windows Vista proporciona compatibilidad con la superficie de BGRA para las rutas de acceso de código de Direct3D10 y Direct3D 10.1. Direct3D10Level9 permite que la funcionalidad de Direct3D10 funcione en el hardware de Direct3D9. Direct3D WARP10 es un rasterizador de software con rendimiento para aplicaciones de Direct3D10. Direct3D 11, la versión más reciente de Direct3D, proporciona nuevas funcionalidades, como compatibilidad mejorada con multithreading, Teselación, funcionalidad de DirectCompute y vinculación dinámica de sombreador.

Si crea aplicaciones que usan Direct3D, el [SDK de DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) es obligatorio).

Para obtener más información sobre Direct3D, vea [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/default.aspx) .

### <a name="supported-direct3d-api-elements"></a>Elementos compatibles de la API de Direct3D

Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.

### <a name="directwrite"></a>DirectWrite

La API de DirectWrite es una nueva API de texto que proporciona varios niveles de funcionalidad, como el diseño de texto, el procesamiento de scripts, la representación de glifos y el sistema de fuentes. DirectWrite usa fuentes OpenType y representación de ClearType de subpíxeles para mejorar la experiencia de texto que proporcionan las aplicaciones. La representación de texto se acelera por hardware cuando se usa con Direct2D.

Para obtener más información sobre DirectWrite, consulte [Introducción a directwrite](/windows/desktop/DirectWrite/introducing-directwrite).

### <a name="supported-directwrite-api-elements"></a>Elementos compatibles de la API de DirectWrite

Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.

### <a name="running-directwrite-on-previous-windows-versions"></a>Ejecución de DirectWrite en versiones anteriores de Windows

Los siguientes problemas de comportamiento pueden afectar al uso de la API de DirectWrite en versiones anteriores de Windows:

-   Es posible que los scripts nuevos en Windows 7 no se representen correctamente en las versiones anteriores de Windows.
-   Las configuraciones regionales que no están disponibles en versiones anteriores de Windows revierten al comportamiento predeterminado.
-   El sintonizador ClearType no está disponible en versiones anteriores de Windows.
-   La interoperabilidad de GDI tiene un costo de memoria mayor en algunos escenarios en versiones anteriores de Windows.

### <a name="packaging"></a>Packaging

La actualización de la plataforma para Windows Vista admite un subconjunto limitado de las API de empaquetado que se necesitan para realizar tareas con la API de documentos XPS en aplicaciones no administradas.

Para obtener más información sobre las API de empaquetado, consulte la [Introducción a la API de empaquetado](/previous-versions/windows/desktop/opc/packaging-api-overview).

### <a name="supported-packaging-api-elements"></a>Elementos de la API de empaquetado compatibles

Solo se admiten las siguientes interfaces de empaquetado:

-   IOpcUri
-   IOpcPartUri
-   IOpcFactory (solo se admiten los siguientes métodos)
    -   CreatePackageRootUri
    -   CreatePartUri
    -   CreateStreamOnFile

Las API de empaquetado compatibles se pueden usar para crear transmisiones a través de archivos, así como para crear e interactuar con el URI basado en paquetes.

### <a name="running-packaging-api-on-previous-windows-versions"></a>Ejecutar la API de empaquetado en versiones anteriores de Windows

El comportamiento y el rendimiento de las interfaces de empaquetado y métodos admitidos son los mismos en todas las plataformas compatibles.

Si una aplicación intenta crear una instancia o llamar a un método o una interfaz de empaquetado no admitidos, se producirá un error en el intento. Si la llamada se realiza a un método [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) no compatible, se \_ devolverá el código de error E NOTIMPL.

### <a name="windows-imaging-component"></a>Windows Imaging Component

Entre las nuevas características del componente de creación de imágenes de Windows (WIC) se incluyen la seguridad mejorada, la compatibilidad con alto color y una mejor interoperabilidad de metadatos. Además, el componente de creación de imágenes de Windows amplía su compatibilidad con estándares proporcionando compatibilidad para descodificación progresiva de imágenes, características de PNG expandidas, metadatos GIF, actualizaciones fotográficas de HD y metadatos que abarcan segmentos APPn.

Para obtener más información sobre el componente de creación de imágenes de Windows, vea [información general](/windows/desktop/wic/-wic-about-windows-imaging-codec)sobre el componente de creación de imágenes de Windows.

### <a name="supported-wic-api-elements"></a>Elementos de la API de WIC compatibles

Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.

### <a name="xps-document"></a>Documento XPS

Las API de documentos XPS admiten la creación, modificación y guardado de documentos XPS en aplicaciones no administradas.

Para obtener más información acerca de las API de documentos XPS, consulte la [Guía de programación de documentos XPS.](/previous-versions//dd372978(v=vs.85))

### <a name="supported-xps-document-api-elements"></a>Elementos compatibles de la API de documento XPS

Solo las interfaces de [firmas digitales XPS](/previous-versions/windows/desktop/dd372947(v=vs.85)) no se admiten en las versiones de sistema operativo de nivel inferior.

### <a name="xps-print"></a>Impresión XPS

Las API de impresión XPS admiten la impresión de documentos XPS desde aplicaciones basadas en Windows.

Para obtener más información acerca de las API de impresión XPS, consulte la [API de XpsPrint](/windows/desktop/printdocs/xpsprint-api).

### <a name="supported-xps-print-api-elements"></a>Elementos admitidos de la API de impresión XPS

Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.

### <a name="windows-ribbon-and-animation-manager-library"></a>Cinta de Windows y biblioteca del administrador de animaciones

La actualización de la plataforma para Windows Vista admite las siguientes API de Windows 7 desde la cinta de Windows y la biblioteca de animaciones:

-   [Marco de cinta de Windows](#windows-ribbon-and-animation-manager-library)
-   [Administrador de animaciones de Windows](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a>Ediciones de Windows válidas para las actualizaciones

La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 habilitan la compatibilidad con la cinta y la biblioteca del administrador de animaciones de Windows en las ediciones de Windows que se muestran en la tabla siguiente.



<table>
<thead>
<tr class="header">
<th>Versión de Windows</th>
<th>Ediciones válidas para la actualización</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter con SP2 (x86)<br />
Home Basic con SP2 (x86 y AMD64)<br />
Home Premium con SP2 (x86 y AMD64)<br />
Empresa con SP2 (x86 y AMD64)<br />
Enterprise con SP2 (x86 y AMD64)<br />
Ultimate con SP2 (x86 y AMD64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 con SP2 (x86 y AMD64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="windows-ribbon-framework"></a>Marco de cinta de Windows

El marco de cinta de Windows (cinta) es un sistema de presentación de comandos enriquecido que proporciona una alternativa moderna a los menús, las barras de herramientas y los paneles de tareas de las aplicaciones Windows tradicionales.

El marco de trabajo es una colección de API de Microsoft Win32 que proporciona un host de nuevas capacidades de interfaz de usuario para los desarrolladores de Windows e incluye la cinta de opciones y un sistema de menús contextuales.

Para obtener más información sobre el marco de la cinta de opciones, vea [Introducción al marco de cinta de Windows](../windowsribbon/windowsribbon-introduction.md).

### <a name="supported-ribbon-framework-api-elements"></a>Elementos de API del marco de cinta admitidos

Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.

### <a name="windows-animation-manager"></a>Administrador de animaciones de Windows

El administrador de animaciones de Windows (animación de Windows) es una interfaz de programación que admite la animación de elementos visuales de aplicaciones Windows. La animación de Windows está diseñada para simplificar el desarrollo y el mantenimiento de las secuencias de animación y para permitir que los desarrolladores implementen animaciones coherentes e intuitivas. La animación de Windows se puede usar con cualquier plataforma de gráficos, como Direct2D, Direct3D o GDI+.

Windows Animation es una API de un solo subproceso que proporciona todo lo que un desarrollador necesita para crear, administrar y controlar la animación de la interfaz de usuario.

Para obtener más información sobre el administrador de animaciones de Windows, vea Introducción a la [animación de Windows](/windows/desktop/UIAnimation/introducing-windows-animation-manager).

### <a name="supported-animation-manager-api-elements"></a>Elementos de API del administrador de animaciones admitidos

Todas las API se admiten en versiones anteriores de Windows que son válidas para la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008.

### <a name="windows-portable-devices-platform"></a>Plataforma de dispositivos portátiles de Windows

La actualización de la plataforma para Windows Vista es compatible con las extensiones de Windows 7 para la plataforma de dispositivos portátiles de Windows (WPD). Esta característica permite que los equipos se comuniquen con los medios y dispositivos de almacenamiento conectados. WPD proporciona una forma flexible y robusta de que los equipos se comuniquen con cámaras digitales, reproductores de música, teléfonos móviles y muchos otros tipos de dispositivos conectados.

Para obtener más información acerca de los dispositivos portátiles de Windows, consulte [dispositivos portátiles de Windows](/windows-hardware/drivers/portable/) ( https://docs.microsoft.com/windows-hardware/drivers/portable/) .

### <a name="windows-editions-eligible-for-the-updates"></a>Ediciones de Windows válidas para las actualizaciones

La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 habilitan la compatibilidad con dispositivos portátiles de Windows (WPD) en las ediciones de Windows que se muestran en la tabla siguiente.



<table>
<thead>
<tr class="header">
<th>Versión de Windows</th>
<th>Ediciones válidas para la actualización</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter con SP2 (x86)<br />
Home Basic con SP2 (x86 y AMD64)<br />
Home Premium con SP2 (x86 y AMD64)<br />
Empresa con SP2 (x86 y AMD64)<br />
Enterprise con SP2 (x86 y AMD64)<br />
Ultimate con SP2 (x86 y AMD64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a>Elementos compatibles de la API de WPD

En la tabla siguiente se identifican las características compatibles con las versiones de Windows 7, Windows Vista y Windows Vista con actualización de plataforma para Windows Vista del sistema operativo Windows.

| Característica de WPD                    | Windows 7 | Windows Vista | Windows Vista con actualización de plataforma para Windows Vista |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| MTP a través de USB                   | Sí       | Sí           | Sí                                                  |
| MTP a través de IP                    | Sí       | Sí           | Sí                                                  |
| MTP a través de Bluetooth             | Sí       | No            | Sí                                                  |
| WPD y servicios de dispositivos MTP    | Sí       | No            | Sí                                                  |
| Automatización de WPD                 | Sí       | No            | No                                                   |
| Múltiples funciones/transporte múltiple | Sí       | No            | No                                                   |
| Device Stage (puede estar en inglés)                   | Sí       | No            | No                                                   |
| Plataforma de sincronización de dispositivos           | Sí       | No            | No                                                   |



 

En el caso de las ediciones de Windows 7 y Windows Vista que no tienen Microsoft Windows Media Player instalado de forma predeterminada (las ediciones N y KN), debe instalar el [SDK de Windows Media Format 11]( ../audio-and-video.md) ( https://msdn.microsoft.com/windows/bb190326.aspx) para habilitar la funcionalidad de WPD). Para obtener más información, vea el [artículo de Knowledge Base](https://support.microsoft.com/kb/953693) ( https://go.microsoft.com/fwlink/p/?linkid=158715) , que se publicó originalmente como una solución para Windows Vista).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Actualización de la plataforma para Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Temas de introducción**
</dt> <dt>

[Acerca de la actualización de la plataforma para Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Artículo de Knowledge Base acerca de la actualización de la plataforma para Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 