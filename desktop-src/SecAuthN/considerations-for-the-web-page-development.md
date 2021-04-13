---
description: El agente de autenticación Web se basa en la parte superior de las mismas tecnologías que Power Internet Explorer en Windows.
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: Consideraciones para el desarrollo de páginas web
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbe7e738616589afc4f7ba4f03d92a12207d189c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360800"
---
# <a name="considerations-for-the-web-page-development"></a>Consideraciones para el desarrollo de páginas web

El agente de autenticación Web se basa en la parte superior de las mismas tecnologías que Power Internet Explorer en Windows. Sin embargo, debido a una finalidad muy especial de este componente, algunas características de Internet Explorer se deshabilitaron o se bloqueaban para una configuración específica. Además, el agente de autenticación Web proporciona un canal de registro de eventos dedicado para ayudar a solucionar problemas con las páginas que procesa.

## <a name="internet-explorer-10-standard-document-mode"></a>Modo de documento estándar de Internet Explorer 10

El agente de autenticación Web muestra todas las páginas en el "modo estándar de IE10". Puede usar las herramientas de desarrollo de Internet Explorer para ver cómo funciona la página en diferentes modos de documento. Para obtener más información sobre la compatibilidad de Internet Explorer 10, vea los temas de MSDN para [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).

## <a name="disabled-and-locked-down-features"></a>Características deshabilitadas y bloqueadas

Varias características de Internet Explorer están completamente deshabilitadas o bloqueadas para valores específicos que no se pueden cambiar en las opciones de Internet del sistema operativo.



| Característica                            | Situación                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| API de caché de aplicaciones ("AppCache") | Disabled                                                                                                                                                                                                        |
| Historial de vínculos                       | Disabled                                                                                                                                                                                                        |
| Archivos temporales                    | habilitado                                                                                                                                                                                                         |
| Cookies                            | Las cookies de sesión están habilitadas. Las cookies persistentes están permitidas, pero están sujetas a la limpieza automática a menos que el agente de autenticación Web esté en modo SSO. Para obtener más información, consulte la sección Inicio de sesión único. |
| BASE de índice                           | Disabled                                                                                                                                                                                                        |
| Almacenamiento DOM                        | Disabled                                                                                                                                                                                                        |
| ActiveX                            | Disabled                                                                                                                                                                                                        |
| Descargas de archivos                     | Disabled                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a>Requisito de HTTPS

La primera dirección URL que utilizará una aplicación para comunicarse con el proveedor en línea debe ser HTTPS.

## <a name="dimension-for-different-window-sizes"></a>Dimensión para distintos tamaños de ventana

Una aplicación de Windows 8 puede aparecer en varios tamaños, como pantalla completa, una ventana cuyo tamaño se ha cambiado o en un acceso, como el acceso compartido. En función del diseño de ventana que aparezca el agente de autenticación Web, el tamaño con el que tienen que trabajar las páginas web podría ser diferente. Para obtener más información, vea el tema [instrucciones para cambiar el tamaño a diseños estrechos](/previous-versions/windows/hh465371(v=win.10)) y el tema [directrices para compartir contenido](/previous-versions/windows/hh465251(v=win.10)) .

La página web debe usar las consultas multimedia de CSS para comprobar el tamaño con el que tiene que trabajar y colocarse en consecuencia. Sin embargo, la página no debe diseñarse en función de los píxeles exactos que se documentan aquí y deben poder escalarse a distintos tamaños. Los tamaños especificados en este documento están sujetos a cambios en futuras versiones del sistema operativo.

Si una página no puede ajustarse a toda la información del espacio asignado (por ejemplo, una larga lista de permisos que una aplicación está solicitando), el agente de autenticación Web proporcionará barras de desplazamiento para permitir al usuario desplazarse por la página según sea necesario. El zoom también lo proporciona el zoom de pinch para dispositivos basados en táctil y Ctrl + rueda del mouse para equipos portátiles y de escritorio.

Para probar distintos factores de escala, use la [aplicación de ejemplo del SDK del agente de autenticación Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) cargada en Microsoft Visual Studio Professional 2012, que permite simular la pantalla completa y cambiar el tamaño de los Estados.

Además de los distintos diseños descritos anteriormente, asegúrese de probar la página en una orientación de pantalla diferente (por ejemplo, vertical y horizontal) y diferentes configuraciones regionales y idiomas, así como con características de accesibilidad, como la opción "hacer todo más grande" activada.

Los diseños disponibles son:

-   [Pantalla completa](#full-screen)
-   [Ventana cuyo tamaño se ha cambiado](#resized)
-   [Vista de acceso](#charm-view)
-   [Vista del selector de archivos](#file-picker-view)

### <a name="full-screen"></a>Pantalla completa

En el diseño de pantalla completa, las dimensiones de la página web son:

-   Ancho: 566 píxeles
-   Alto: alto de la pantalla (depende de la resolución de la pantalla)

En el ejemplo siguiente se muestra la interfaz de usuario del agente de autenticación Web en el diseño de pantalla completa.

![ejemplo de interfaz de usuario del agente de autenticación Web en el diseño de pantalla completa](images/wab-figure2.png)

### <a name="resized"></a>Tamaño

En el caso de una ventana cuyo tamaño se ha cambiado, las dimensiones de la página web pueden ser:

-   Ancho: 260 píxeles
-   Alto: alto de la pantalla (depende de la resolución de la pantalla)

En el ejemplo siguiente se muestra la interfaz de usuario del agente de autenticación Web en una ventana cuyo tamaño se ha cambiado en la Página Web de XBox. Tenga en cuenta que la interfaz de usuario del agente de autenticación Web solo está en el lado derecho de la captura de pantalla.

![ejemplo de interfaz de usuario del agente de autenticación Web en una ventana cuyo tamaño se ha cambiado](images/wab-figure3.png)

### <a name="charm-view"></a>Vista de acceso

En la vista de acceso, las dimensiones de la página web son:

-   Ancho: 566 píxeles
-   Alto: alto de la pantalla (depende de la resolución de la pantalla)

En el ejemplo siguiente se muestra la interfaz de usuario del agente de autenticación Web en la vista de acceso.

![un ejemplo muestra la interfaz de usuario del agente de autenticación Web en la vista de acceso](images/wab-figure4.png)

### <a name="file-picker-view"></a>Vista del selector de archivos

En la vista selector de archivos, las dimensiones de la página web son:

-   Ancho: 566 píxeles
-   Alto: alto de la pantalla (depende de la resolución de la pantalla)

En el ejemplo siguiente se muestra la interfaz de usuario del agente de autenticación Web en la vista del selector de archivos.

![un ejemplo muestra la interfaz de usuario del agente de autenticación Web en la vista del selector de archivos](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a>No hay ventanas nuevas de forma predeterminada

De forma predeterminada, ninguna dirección URL dará como resultado que se abra una nueva ventana, pero en su lugar se mostrará en la ventana agente de autenticación Web. Esto incluye el método de JavaScript Window. Open, el atributo de destino de los hipervínculos o el uso del mecanismo Ctrl + clic para forzar que se abra una nueva ventana. La excepción a esta regla es cuando una página Web declara que un vínculo es seguro para navegar en un explorador, tal como se describe en el destino de personalización de los hipervínculos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicación de ejemplo del SDK del agente de autenticación Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
