---
description: El Agente de autenticación web se basa en las mismas tecnologías que Internet Explorer en Windows.
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: Consideraciones para el desarrollo de páginas web
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22932f40d5268059fc30e97817de0b3671cee7447974b038ea4be12eedd76ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883274"
---
# <a name="considerations-for-the-web-page-development"></a>Consideraciones para el desarrollo de páginas web

El Agente de autenticación web se basa en las mismas tecnologías que Internet Explorer en Windows. Sin embargo, debido a un propósito muy especial de este componente, algunas características del Internet Explorer se han deshabilitado o bloqueado para una configuración específica. Además, el Agente de autenticación web proporciona un canal de registro de eventos dedicado para ayudar a solucionar problemas con las páginas que procesa.

## <a name="internet-explorer-10-standard-document-mode"></a>Internet Explorer 10 modo de documento estándar

El Agente de autenticación web muestra todas las páginas del "Modo estándar de IE10". Puede usar las herramientas de desarrollo de Internet Explorer para ver cómo funciona la página en diferentes modos de documento. Para obtener más información sobre Internet Explorer 10 compatibilidad, vea los temas de MSDN [para Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).

## <a name="disabled-and-locked-down-features"></a>Características deshabilitadas y bloqueadas

Varias características de Internet Explorer están completamente deshabilitadas o bloqueadas a valores específicos que no se pueden cambiar en las opciones de Internet del sistema operativo.



| Característica                            | Situación                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| API de caché de aplicaciones ("AppCache") | Disabled                                                                                                                                                                                                        |
| Historial de vínculos                       | Disabled                                                                                                                                                                                                        |
| Archivos temporales                    | habilitado                                                                                                                                                                                                         |
| Cookies                            | Las cookies de sesión están habilitadas. Se permiten cookies persistentes, pero están sujetas a limpieza automática a menos que el Agente de autenticación web esté en modo sso. Para más información, consulte la sección Inicio de sesión único. |
| Base de datos de índice                           | Disabled                                                                                                                                                                                                        |
| Almacenamiento DOM                        | Disabled                                                                                                                                                                                                        |
| ActiveX                            | Disabled                                                                                                                                                                                                        |
| Descargas de archivos                     | Disabled                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a>Requisito https

La primera dirección URL que usará una aplicación para comunicarse con el proveedor en línea debe ser HTTPS.

## <a name="dimension-for-different-window-sizes"></a>Dimensión para diferentes tamaños de ventana

Una Windows 8 aplicación puede aparecer en varios tamaños diferentes, como pantalla completa, una ventana con cambio de tamaño o dentro de un acceso como El acceso compartido. Dependiendo del diseño de ventana que aparezca en el Agente de autenticación web, el tamaño con el que las páginas web tienen que funcionar podría ser diferente. Para obtener más información, vea el tema [Guidelines for resizing to narrow layouts](/previous-versions/windows/hh465371(v=win.10)) (Directrices para cambiar el tamaño a diseños estrechos) y [el tema Guidelines for sharing content (Directrices para compartir contenido).](/previous-versions/windows/hh465251(v=win.10))

La página web debe usar consultas multimedia CSS para comprobar el tamaño con el que tiene que trabajar y arse en consecuencia. Sin embargo, la página no debe diseñarse en función de los píxeles exactos documentados aquí y debe poder escalarse a tamaños diferentes. Los tamaños especificados en este documento están sujetos a cambios en versiones futuras del sistema operativo.

Si una página no puede caber toda la información en el espacio asignado (por ejemplo, una larga lista de permisos que solicita una aplicación), el Agente de autenticación web proporcionará barras de desplazamiento para permitir al usuario desplazarse por la página según sea necesario. El zoom también se proporciona mediante zoom de reducción para dispositivos táctiles y Ctrl + rueda del mouse para equipos portátiles y de escritorio.

Para probar diferentes factores de escalado, use la aplicación de ejemplo [del SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) del Agente de autenticación web cargada en Microsoft Visual Studio Professional 2012, que permite simular la pantalla completa y los estados de cambio de tamaño.

Además de los diferentes diseños documentados anteriormente, asegúrese de probar la página con una orientación de pantalla diferente (por ejemplo, vertical y horizontal) y diferentes configuraciones regionales e idiomas, así como con características de accesibilidad como la opción "Hacer todo más grande" activada.

Los diseños disponibles son:

-   [Pantalla completa](#full-screen)
-   [Ventana con cambio de tamaño](#resized)
-   [Vista de acceso](#charm-view)
-   [Vista del selector de archivos](#file-picker-view)

### <a name="full-screen"></a>Pantalla completa

Para el diseño de pantalla completa, las dimensiones de página web son:

-   Ancho: 566 píxeles
-   Alto: alto de la pantalla (depende de la resolución de la pantalla)

En el ejemplo siguiente se muestra la interfaz de usuario del agente de autenticación web en el diseño de pantalla completa.

![un ejemplo de interfaz de usuario del agente de autenticación web en el diseño de pantalla completa](images/wab-figure2.png)

### <a name="resized"></a>Redimensionada

En el caso de una ventana con cambio de tamaño, las dimensiones de la página web pueden ser:

-   Ancho: 260 píxeles
-   Alto: alto de la pantalla (depende de la resolución de la pantalla)

En el ejemplo siguiente se muestra la interfaz de usuario del Agente de autenticación web en una ventana de cambio de tamaño en la página web de XBox. Tenga en cuenta que la interfaz de usuario del Agente de autenticación web solo está en el lado derecho de la captura de pantalla.

![un ejemplo de interfaz de usuario del agente de autenticación web en una ventana de cambio de tamaño](images/wab-figure3.png)

### <a name="charm-view"></a>Vista de acceso

Para la vista De acceso, las dimensiones de la página web son:

-   Ancho: 566 píxeles
-   Alto: alto de la pantalla (depende de la resolución de la pantalla)

En el ejemplo siguiente se muestra la interfaz de usuario del Agente de autenticación web en la vista De acceso.

![un ejemplo muestra la interfaz de usuario del agente de autenticación web en la vista de acceso](images/wab-figure4.png)

### <a name="file-picker-view"></a>Vista del selector de archivos

Para la vista del selector de archivos, las dimensiones de página web son:

-   Ancho: 566 píxeles
-   Alto: alto de la pantalla (depende de la resolución de la pantalla)

En el ejemplo siguiente se muestra la interfaz de usuario del Agente de autenticación web en la vista del selector de archivos.

![un ejemplo muestra la interfaz de usuario del agente de autenticación web en la vista del selector de archivos](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a>No hay nuevas ventanas de forma predeterminada

De forma predeterminada, ninguna dirección URL dará lugar a que se abra una nueva ventana, pero en su lugar se mostrará dentro de la ventana Agente de autenticación web. Esto incluye el método de JavaScript window.open, el atributo "target" de los hipervínculos o cuando el usuario usa el mecanismo Ctrl+Clic para forzar la apertura de una nueva ventana. La excepción a esta regla es cuando una página web declara un vínculo como seguro para navegar en un explorador, como se describe en El destino de personalización de los hipervínculos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicación de ejemplo del SDK del Agente de autenticación web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
