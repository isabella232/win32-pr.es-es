---
description: En este tema se describen los procedimientos recomendados para diseñar páginas web que usan el Agente de autenticación web para iniciar sesión.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Procedimientos recomendados para diseñar páginas web de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80fbf38c0e020cad342331d67278818b56ce331ff39434aefd726dea52bae1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883621"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a>Procedimientos recomendados para diseñar páginas web de autenticación

En este tema se describen los procedimientos recomendados para diseñar páginas web que usan el Agente de autenticación web para iniciar sesión.

-   [Uso de metatags](#use-of-metatags)
-   [Uso del estilo Windows 8 CSS](#use-of-windows-8-css-styling)
-   [Uso de colores y temas](#use-of-color-and-themes)
-   [Alineación](#alignment)
-   [Diseño para ajustar](#designing-for-snap)
-   [Diseño para una experiencia de inicio de sesión rápida y fluida](#designing-for-a-fast-and-fluid-login-experience)
-   [Consideraciones sobre la seguridad](#security-considerations)
-   [Temas relacionados](#related-topics)

## <a name="use-of-metatags"></a>Uso de metatags

Mediante metatags, el proveedor "Contoso Social" puede especificar el título, el icono y el color del encabezado. En el archivo HTML de ejemplo (WebAuthLogin.html), esto se realiza mediante el código siguiente.


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



Esto permite Windows la presencia del proveedor de forma destacada en el encabezado de la interfaz de usuario, tal como se resalta en el cuadro rojo de la captura de pantalla siguiente. ![página de inicio de sesión que muestra el encabezado contoso en la interfaz de usuario](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a>Uso del estilo Windows 8 CSS

La hoja de estilos ui-light.css proporcionada es la hoja Windows 8 estilo que usan las Windows Store. Define el estilo Windows store para la tipografía y los controles estándar, como botones, cuadros de texto, hipervínculos y casillas para asegurarse de que son táctiles. Al diseñar y personalizar páginas de autorización web para Windows 8, le recomendamos que use esta hoja de estilos tal y como está y la actualice según sea necesario siempre que la página web siga los procedimientos recomendados a su manera.

Por ejemplo, si tiene una hoja de estilos especial para el aspecto que deben tener los hipervínculos en la página web, es bueno tener cuidado para asegurarse de que el estilo que proporcione sea descriptivo al toque de la misma manera que los hipervínculos estándar Windows 8. Esto es esencial para la base de consumidores mediante Windows 8 en sus dispositivos táctiles.

## <a name="use-of-color-and-themes"></a>Uso de colores y temas

En este ejemplo se muestra un uso cuidadoso del color de varias maneras diferentes.

-   Fondo blanco de la página web. Como puede ver en la captura de pantalla anterior, la página web se hospeda dentro de una superficie blanca que abarca el ancho de la pantalla. Para asegurarse de que la página web se integra con la superficie, se recomienda que la página web tenga un fondo blanco.
-   Controles de coloración basados en el color de la marca. El archivo CSS theme-colors.css proporciona estilo para invalidar los colores estándar de los controles de la hoja de estilos de la interfaz de usuario ligera para que coincidan con el tema de los controles con el color del encabezado. Por ejemplo, en la siguiente captura de pantalla, los botones y los hipervínculos toman colores derivados del color del encabezado. ![captura de pantalla de los botones y el texto con el mismo color que el encabezado](images/wab-figure11.png)
-   Color del encabezado. El uso del color de marca de Contoso en el encabezado crea una personalidad unificada para la marca del proveedor dentro de la interfaz de usuario del sistema.

## <a name="alignment"></a>Alignment

La propia página web no tiene relleno a la izquierda ni a la derecha para permitir la alineación tipográfica con el título del encabezado de la izquierda y el icono en el encabezado de la derecha.

También observará que los botones siempre están alineados de abajo a la derecha en la página web (y alineados a la derecha con el icono del encabezado). Este es el procedimiento recomendado, ya Windows 8 usuarios estarán acostumbrados a flujos de diálogo similares con botones en la parte inferior derecha.

## <a name="designing-for-snap"></a>Diseño para ajustar

En la imagen siguiente, puede ver las páginas de inicio de sesión y permisos en estado de ajuste.

![vista snap de la pantalla de inicio de sesión ](images/wab-figure12.png) . ![vista de instantánea de la página de permisos ](images/wab-figure13.png)

En el archivo de ejemplo ui-webauth.css, puede ver el uso de consultas multimedia que optimizan el diseño de la página para ajustar el estado en función del ancho disponible para la página web. El fragmento de código incluido en el ámbito siguiente implementa CSS adaptado para el estado de ajuste.


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



En Windows 8, el ancho del estado de ajuste es de 320 píxeles. La página de autenticación web ocupa 260 píxeles en la interfaz de usuario anterior. Estamos usando un valor de ancho máximo con margen suficiente, por lo que el código de consulta multimedia del proveedor no está enlazado al ancho exacto del estado de ajuste.

Al personalizar la aplicación para la vista de ajuste, es importante que el usuario no pierda ningún contexto que tenga en las otras vistas de la experiencia de autenticación web (vistas completa, de relleno o de acceso), pero es útil volver a estructurar el diseño y la jerarquía de los elementos de la página para que la información necesaria para conservar el contexto sea visible e interactiva. Hemos llamado a algunos ejemplos de cómo el ejemplo adapta la página web para el estado de ajuste.

-   Por ejemplo, para la página de inicio de sesión en estado de ajuste, la propiedad width del campo de texto de entrada (como se especifica en ui-light.css) se ha invalidado y se ha establecido como un valor numérico más pequeño, de modo que el campo de texto no se recorta horizontalmente.
-   Como otro ejemplo, en estado de ajuste, el tamaño de fuente de los encabezados h1 y h2 se reduce a 20 pt y 11 pt de 42 pt y 20 pt respectivamente. Esto se hace de acuerdo con la rampa de Windows 8 y optimiza el texto para que sea más compacto en la ventanilla modificada.
-   Como otro ejemplo, observe que los tamaños de los iconos de la página de permisos son más pequeños (compare con la página de vista completa anterior). De nuevo, esto se hace para conservar el contexto, al mismo tiempo que se intercambian los recursos de diseño para los más óptimos para la ventanilla cambiada.

## <a name="designing-for-a-fast-and-fluid-login-experience"></a>Diseño para una experiencia de inicio de sesión rápida y fluida

Al principio del diseño de esta página web, nos hemos puesto en peligro en el hecho de que una de las cosas en las que esta página es mejor es una experiencia de inicio de sesión rápida y fluida. Por lo tanto, la interfaz de usuario más destacada en el flujo es el campo nombre de usuario y contraseña de la página de inicio de sesión para una experiencia rápida de entrada de credenciales. Aunque hemos identificado que hay otros escenarios comunes, como la recuperación de contraseñas y la referencia a declaraciones de privacidad, la experiencia enriquecencia de la web es un lugar mejor para esas experiencias. Para todos los flujos no relacionados con la experiencia de autenticación web segura, se recomienda navegar al usuario al explorador. Esto se muestra en el archivo HTML de ejemplo (WebAuthLogin.html) como se indica a continuación: se abren todas las páginas web vinculadas a desde la página de inicio de sesión o permisos en el explorador predeterminado del usuario, donde el usuario puede completar estos flujos y, a continuación, volver a la aplicación para iniciar `<meta name="mswebdialog-newwindowurl" content="*" />` sesión.

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

En los artículos siguientes se proporcionan instrucciones para escribir código C++ seguro.

-   [Procedimientos recomendados de seguridad para C++](/cpp/security/security-best-practices-for-cpp)
-   [Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones para el desarrollo de páginas web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Preguntas más frecuentes sobre el Agente de autenticación web](faq-for-web-authentication-broker.yml)
</dt> <dt>

[Aplicación de ejemplo del SDK del Agente de autenticación web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
