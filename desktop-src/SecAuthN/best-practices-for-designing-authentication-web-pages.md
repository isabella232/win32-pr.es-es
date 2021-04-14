---
description: En este tema se describen los procedimientos recomendados para diseñar páginas web que utilizan el agente de autenticación Web para iniciar sesión.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Procedimientos recomendados para diseñar páginas web de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6360e313b49a69c16aebf532911bcdf562f9a4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360472"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a>Procedimientos recomendados para diseñar páginas web de autenticación

En este tema se describen los procedimientos recomendados para diseñar páginas web que utilizan el agente de autenticación Web para iniciar sesión.

-   [Uso de metaetiquetas](#use-of-metatags)
-   [Uso del estilo CSS de Windows 8](#use-of-windows-8-css-styling)
-   [Uso de color y temas](#use-of-color-and-themes)
-   [Alineación](#alignment)
-   [Diseñar para ajustar](#designing-for-snap)
-   [Diseño para una experiencia de inicio de sesión rápida y fluida](#designing-for-a-fast-and-fluid-login-experience)
-   [Consideraciones sobre la seguridad](#security-considerations)
-   [Temas relacionados](#related-topics)

## <a name="use-of-metatags"></a>Uso de metaetiquetas

Mediante el uso de metatags, el proveedor "Contoso social" puede especificar el título, el icono y el color del encabezado. En el archivo HTML de ejemplo (WebAuthLogin.html), esto se hace mediante el código siguiente.


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



Esto permite a Windows integrar la presencia del proveedor de forma destacada en el encabezado de la interfaz de usuario, tal y como se resalta en el cuadro rojo de la captura de pantalla siguiente. ![Página de inicio de sesión que muestra el encabezado de Contoso en la interfaz de usuario](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a>Uso del estilo CSS de Windows 8

La hoja de estilos UI-Light. CSS proporcionada es la hoja de estilos de Windows 8 que usan las aplicaciones de la tienda Windows. Define el estilo de la aplicación de la tienda Windows para controles estándar y tipográficos, como botones, cuadros de texto, hipervínculos y casillas para asegurarse de que son cómodos. Al diseñar y personalizar páginas de autorización web para Windows 8, se recomienda usar esta hoja de estilos tal cual y actualizarla según sea necesario, siempre y cuando la página web siga los procedimientos recomendados de su forma.

Por ejemplo, si tiene una hoja de estilos especial para el aspecto de los hipervínculos en la página web, es conveniente asegurarse de que el estilo que proporcione es táctil, de la misma manera que los hipervínculos estándar de Windows 8. Esto es esencial para la base del consumidor que usa Windows 8 en sus dispositivos táctiles.

## <a name="use-of-color-and-themes"></a>Uso de color y temas

Este ejemplo muestra un uso exhaustivo del color de varias maneras diferentes.

-   Fondo blanco de la Página Web. Como puede ver en la captura de pantalla anterior, la página web se hospeda en una superficie blanca que abarca el ancho de la pantalla. Para asegurarse de que la página web se integra con la superficie, se recomienda que la página web tenga un fondo blanco.
-   Colorear controles según el color de la marca. El archivo CSS Theme-colors. CSS proporciona estilos para invalidar los colores estándar de los controles de la hoja de estilos UI-Light para que coincidan con los de los controles y el color del encabezado. Por ejemplo, en la siguiente captura de pantalla, los botones e hipervínculos toman los colores derivados del color de encabezado. ![captura de pantalla de los botones y el texto con el mismo color que el encabezado](images/wab-figure11.png)
-   Color de encabezado. El uso del color de la marca de Contoso en el encabezado crea una personalidad unificada para la marca del proveedor dentro de la interfaz de usuario del sistema.

## <a name="alignment"></a>Alignment

La propia página web no tiene relleno a la izquierda o a la derecha para permitir la alineación tipográfica con el título en el encabezado de la izquierda y el icono del encabezado de la derecha.

También observará que los botones siempre están alineados en la parte inferior derecha de la página web (y alineados a la derecha con el icono del encabezado). Esta es la práctica recomendada, ya que los usuarios de Windows 8 estarán acostumbrados a flujos de diálogo similares con botones en la parte inferior derecha.

## <a name="designing-for-snap"></a>Diseñar para ajustar

En la imagen siguiente, puede ver las páginas inicio de sesión y permisos en el estado de ajuste.

![vista de ajuste de la pantalla de inicio de sesión ](images/wab-figure12.png) . ![vista de ajuste de la página permisos ](images/wab-figure13.png)

En el archivo de ejemplo UI-webauth. CSS, puede ver el uso de consultas multimedia que optimizan el diseño de la página para el estado de ajuste basado en el ancho disponible para la Página Web. El fragmento de código incluido en el ámbito siguiente implementa CSS adaptados para el estado de ajuste.


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



En Windows 8, el ancho del estado de ajuste es de 320 píxeles. La página web-auth ocupa 260 píxeles en la interfaz de usuario anterior. Estamos usando un valor de ancho máximo con un margen suficiente, por lo que el código de consulta de medios del proveedor no se enlaza al ancho exacto del estado de ajuste.

En la personalización de la aplicación para la vista de ajuste, es importante que el usuario no pierda ningún contexto que tenga en las otras vistas de la experiencia de autenticación Web (vistas completa, de relleno o de acceso), pero es importante volver a estructurar el diseño y la jerarquía de los elementos de la página para que la información necesaria para conservar el contexto sea visible e interactiva. Hemos llamado a algunos ejemplos de la forma en la que el ejemplo realiza la finalización de la página web para el estado de ajuste.

-   Por ejemplo, para la página de inicio de sesión en el estado de ajuste, la propiedad ancho del campo de texto de entrada (tal y como se especifica en UI-Light. CSS) se ha invalidado y se ha establecido como valor numérico más pequeño, por lo que el campo de texto no se recorta horizontalmente.
-   Como otro ejemplo, en el estado de ajuste, el tamaño de fuente de los encabezados H1 y H2 se reduce a 20 PT y 11 pt de 42 PT y 20 PT, respectivamente. Esto se realiza de acuerdo con la rampa de tipos de Windows 8 y optimiza el texto para que sea más compacto en la ventanilla modificada.
-   Como otro ejemplo, observe que los tamaños de los iconos de la página permisos son más pequeños (Comparar con la página vista completa anterior). De nuevo, esto se hace para conservar el contexto, al mismo tiempo que se intercambian los recursos de diseño para que la ventanilla cambiada sea más óptima.

## <a name="designing-for-a-fast-and-fluid-login-experience"></a>Diseño para una experiencia de inicio de sesión rápida y fluida

En la primera parte del diseño de esta página web, nos estiraremos de que una de las cosas en las que es mejor esta página es una experiencia de inicio de sesión rápida y fluida. Por lo tanto, la interfaz de usuario más destacada en el flujo es el campo de nombre de usuario y contraseña en la página de inicio de sesión para una experiencia rápida de entrada de credenciales. Aunque hemos identificado que hay otros escenarios comunes, como la recuperación de contraseñas y la referencia a declaraciones de privacidad, la experiencia enriquecida de la web es un lugar mejor para esas experiencias. En el caso de todos los flujos no relacionados con la experiencia de autenticación Web segura, se recomienda navegar por el usuario al explorador. Esto se muestra en el archivo HTML de ejemplo (WebAuthLogin.html) de la siguiente manera: `<meta name="mswebdialog-newwindowurl" content="*" />` se abren todas las páginas web vinculadas a desde la página inicio de sesión o permisos en el explorador predeterminado del usuario, donde el usuario puede completar estos flujos y volver a la aplicación para iniciar sesión.

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

En los artículos siguientes se proporcionan instrucciones para escribir código de C++ seguro.

-   [Prácticas recomendadas de seguridad para C++](/cpp/security/security-best-practices-for-cpp)
-   [Patterns & prácticas guía de seguridad para aplicaciones](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones para el desarrollo de páginas web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Preguntas más frecuentes sobre el agente de autenticación Web](faq-for-web-authentication-broker.md)
</dt> <dt>

[Aplicación de ejemplo del SDK del agente de autenticación Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
