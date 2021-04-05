---
description: Una página web Personaliza la interfaz de usuario (UI) con el título, el icono y el color del encabezado mediante etiquetas de metadatos definidas en la Página Web.
ms.assetid: 6F1E0B2E-E013-4C5B-86A4-0AF8606D0C12
title: Cómo personalizar los elementos de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19314f8e4c5d4944a500a0eef3aa0f75cd231b12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911881"
---
# <a name="how-to-customize-the-ui-elements"></a>Cómo personalizar los elementos de la interfaz de usuario

Una página web Personaliza la interfaz de usuario (UI) con el título, el icono y el color del encabezado mediante etiquetas de metadatos definidas en la Página Web. Los desarrolladores web pueden usar <meta> etiquetas HTML para mostrar la personalidad y la marca del proveedor en la interfaz de usuario del agente de autenticación Web. Además, los desarrolladores pueden dirigir acciones de usuario más complicadas, por ejemplo, el registro y la recuperación de contraseñas. El concepto es muy similar a la característica de sitios anclados de Windows Internet Explorer 9 y Windows 7.

Además de personalizar la interfaz de usuario en torno al área de la página web, la página web también debe aprovechar las ventajas de los estilos de los controles de Windows 8, estar habilitado para tocar y permitir que los vínculos se abran en el explorador cuando corresponda.

A continuación se ofrece un ejemplo de una página web que ha sacado provecho del modelo de personalización del agente de autenticación Web. ![elementos de la interfaz de usuario del agente de autenticación Web](images/wab-figure7.png)

## <a name="instructions"></a>Instrucciones

### <a name="step-1-customize-the-icon"></a>Paso 1: personalizar el icono

La página web puede proporcionar un icono mediante una etiqueta meta mswebdialog-logo.

``` syntax
<meta name="mswebdialog-logo" content="https://www.contoso.com/logo.png"/>
```

El contenido es una dirección URL que puede ser una página relativa o absoluta. El esquema de la dirección URL puede ser HTTP o HTTPS. El formato del archivo debe ser PNG o JPG. El tamaño de la imagen debe ser de 30 x 30 píxeles. Si la imagen tiene un tamaño diferente, el sistema operativo la reducirá o reducirá horizontalmente para ajustarse al espacio de 30 x 30. La imagen debe diseñarse para que se represente correctamente cuando se escale hasta un 140% y un 180% para tener en cuenta pantallas de mayor resolución. Para probar distintos factores de escala, use la [aplicación de ejemplo del SDK del agente de autenticación Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) cargada en Visual Studio 11, que permite simular diferentes resoluciones y factores de escalado mediante las ventanas del dispositivo del modo de diseño.

### <a name="step-2-customize-the-title-text"></a>Paso 2: personalizar el texto del título

La página web puede proporcionar el título mediante la etiqueta meta mswebdialog-title.

``` syntax
<meta name="mswebdialog-title" content="Contoso Social"/>
```

El título debe ser corto y debe reflejar la marca del proveedor (por ejemplo, contoso).

### <a name="step-3-customize-the-header-color"></a>Paso 3: personalizar el color del encabezado

La página web puede proporcionar el color que representa la identidad de marca que se va a usar para el encabezado del cuadro de diálogo mediante la etiqueta meta mswebdialog-header-color.

``` syntax
<meta name="mswebdialog-header-color" content="#1267DF"/>
```

El color puede ser cualquier valor especificado aquí. Sin embargo, el agente de autenticación Web omitirá cualquier valor de canal alfa. Con este color específicamente y con los colores usados en la página en general, se recomienda seguir los mismos colores que se usan en la aplicación de Windows 8 del proveedor si dicha aplicación existe.

> [!Note]  
> Los iconos y colores se almacenan en caché por servidor en el cliente una vez que se analizan las etiquetas META. Borre la memoria caché del cliente antes de iniciar la interfaz de usuario para que los cambios surtan efecto. Para ello, modifique la siguiente configuración del registro.

 

``` syntax
// Registry location under HKLM used for setting various AuthHost parameters.
#define AUTH_HOST_LOCAL_MACHINE_REGPATH \
    L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Image File Execution Options\\authhost.exe"
// MaxAge to use for downloading logo images
#define AUTH_HOST_LOGO_IMAGE_MAX_AGE_SECONDS_REG_VALUE_NAME \
    L"LogoImageMaxAgeSeconds"
// 24 hours
#define AUTH_HOST_LOGO_IMAGE_MAX_AGE_SECONDS_DEFAULT        \
    (24 * 60 * 60)
```

Una vez que se descarga un icono, no se vuelve a recoger durante 24 horas. Para probar con imágenes de logotipo, establezca la clave de registro anterior con un valor inferior.

### <a name="step-4-customize-the-web-page"></a>Paso 4: personalizar la página web

Además de personalizar la interfaz de usuario en torno a la página web, los desarrolladores también deben crear páginas web sin problemas e integradas con la experiencia general de Windows 8. Esto incluye el uso de los estilos recomendados, asegurándose de que las páginas web funcionan bien con dispositivos táctiles habilitados y que abren determinadas páginas web en el explorador Web.

-   Aplicación de estilos

    Se recomienda encarecidamente usar el estilo recomendado aquí para crear una experiencia de usuario más coherente en las páginas web del agente de autenticación Web y en otros componentes de la interfaz de usuario de Windows 8. La página web debe usar un fondo blanco y sin bordes. Los botones como login o CANCEL se deben colocar en la esquina inferior derecha y usar el mismo color que el encabezado. Por último, dado que el agente de autenticación Web proporciona un botón atrás, considere la posibilidad de eliminar por completo un botón Cancelar de la Página Web.

-   Habilitar Touch

    La página web se debe diseñar teniendo en cuenta una interacción del usuario basada en el toque. Para obtener más información sobre el diseño de Touch en Windows 8, vea el tema [diseño de interacción táctil](https://msdn.microsoft.com/library/Hh465415(v=Win.10).aspx) .

-   Personalizar el destino de los hipervínculos

    El agente de autenticación Web es excelente para entregar páginas web que requieren una única acción del usuario, como las páginas de autorización de inicio de sesión o OAuth. Sin embargo, para flujos de usuarios más complejos, como la creación de cuentas, la recuperación de una contraseña perdida o olvidada, la visualización de declaraciones de privacidad, etc., donde se espera que el usuario invierta algún tiempo en entender y completar el flujo, se recomienda que estas páginas se inicien en el explorador preferido del usuario para permitir la navegación completa y la exploración. El agente de autenticación Web de forma predeterminada no permite abrir nuevas ventanas del explorador desde una página web (consulte la sección no hay ventanas nuevas de forma predeterminada para obtener más detalles). Sin embargo, mediante el uso de la etiqueta meta, `mswebdialog-newwindowurl` la página web puede declarar qué direcciones URL deben abrirse en el explorador.

    `mswebdialog-newwindowurl`Permite que la página web especifique una dirección URL o parte de la dirección URL que utilizará el agente de autenticación Web para buscar coincidencias (coincidencia de cadena izquierda) en cada vez que se le pida que abra una dirección URL en una nueva ventana mediante el atributo de destino o el método window. Open (). Si hay una coincidencia, la dirección URL se abrirá en el explorador predeterminado del usuario. Si no hay ninguna coincidencia, el agente de autenticación Web navegará a la propia dirección URL (comportamiento predeterminado). Por ejemplo:`<meta name="mswebdialog-newwindowurl" content="https://www.contoso.com/privacy"/>`

    En el caso de esta etiqueta meta, el agente de autenticación Web abrirá el https://www.contoso.com/privacy/policy.html en el explorador, pero se desplazará directamente a https://www.contoso.com/termsofuse.html . Tenga en cuenta que los vínculos que no intentan abrir en una nueva ventana (por ejemplo, los vínculos que no usan el método window. Open () o el atributo de destino) no se ven afectados por esta etiqueta meta. El contenido es una dirección URL que puede ser una página relativa o absoluta. El esquema de la dirección URL puede ser HTTP o HTTPS. Debe definir `mswebdialog-newwindowurl` etiquetas meta que cubran los vínculos que no formen parte del flujo de usuario principal, como las declaraciones de privacidad, los formularios de registro, etc. Si admite el inicio de sesión con un proveedor de autenticación de terceros (por ejemplo, los proveedores de OpenID), asegúrese de mantener esas interacciones dentro del agente de autenticación Web. Para habilitar todos los vínculos de la página como seguros para abrirlos en el explorador, use la sintaxis de estrella, como, `  <meta name="mswebdialog-newwindowurl" content="*"/>` tenga en cuenta que " \* " solo se puede usar de forma exclusiva y no puede combinarse con otra dirección URL, por ejemplo, " https://www.contoso.com/\ *" no es una sintaxis válida.

### <a name="step-5-rules-applied-to-all-meta-tags"></a>Paso 5: reglas aplicadas a todas las etiquetas meta

Cuando el agente de autenticación Web procesa etiquetas meta, se aplican las siguientes reglas:

-   El efecto de la etiqueta meta se conservará en todas las páginas del mismo dominio de segundo nivel (por ejemplo, contoso.com), a menos que se encuentre otra etiqueta meta con el mismo nombre pero con contenido diferente.
-   Si se encuentran varias etiquetas meta con el mismo nombre en la misma página, el agente de autenticación Web elegirá solo una de ellas y omitirá el resto. La etiqueta meta específica que se elige no está definida.
    > [!Note]  
    > Esta regla no se aplica a la `mswebdialog-newwindowurl` etiqueta meta que permite varias instancias de la misma página.

     

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones para el desarrollo de páginas web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Aplicación de ejemplo del SDK del agente de autenticación Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
