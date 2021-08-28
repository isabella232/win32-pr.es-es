---
description: Una página web personaliza la interfaz de usuario (UI) con el título, el icono y el color del encabezado mediante etiquetas de metadatos definidas en la página web.
ms.assetid: 6F1E0B2E-E013-4C5B-86A4-0AF8606D0C12
title: Cómo personalizar los elementos de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a99e8e7da789653226db40763116472eb065df0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884556"
---
# <a name="how-to-customize-the-ui-elements"></a>Cómo personalizar los elementos de la interfaz de usuario

Una página web personaliza la interfaz de usuario (UI) con el título, el icono y el color del encabezado mediante etiquetas de metadatos definidas en la página web. Los desarrolladores web pueden usar etiquetas meta HTML para mostrar la personalidad y la marca del proveedor en la interfaz de usuario del Agente de &lt; &gt; autenticación web. Además, los desarrolladores pueden dirigir acciones de usuario más complejas, por ejemplo, registrarse y recuperar contraseñas. El concepto es muy similar a la característica Sitios anclados de Windows Internet Explorer 9 y Windows 7.

Además de personalizar la interfaz de usuario en torno al área de página web, la página web también debe aprovechar los estilos de los controles Windows 8, estar habilitada para la entrada táctil y permitir que los vínculos se abran en el explorador cuando corresponda.

A continuación se muestra un ejemplo de una página web que ha aprovechado el modelo de personalización del Agente de autenticación web. ![Elementos de la interfaz de usuario del agente de autenticación web](images/wab-figure7.png)

## <a name="instructions"></a>Instrucciones

### <a name="step-1-customize-the-icon"></a>Paso 1: Personalizar el icono

La página web puede proporcionar un icono mediante una etiqueta metamswebdialog-logo.

``` syntax
<meta name="mswebdialog-logo" content="https://www.contoso.com/logo.png"/>
```

El contenido es una dirección URL que puede ser relativa o absoluta. El esquema de la dirección URL puede ser HTTP o HTTPS. El formato del archivo debe ser PNG o JPG. El tamaño de la imagen debe ser de 30 x 30 píxeles. Si la imagen tiene un tamaño diferente, el sistema operativo la escalará verticalmente para ajustarse al espacio de 30 x 30. La imagen debe diseñarse para representarse correctamente cuando se escala hasta un 140 % y un 180 % para tener en cuenta pantallas de mayor resolución. Para probar diferentes factores de escalado, use la aplicación de ejemplo [del SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) del Agente de autenticación web cargada en Visual Studio 11, que permite simular diferentes resoluciones y factores de escalado mediante las ventanas Dispositivo del modo de diseño.

### <a name="step-2-customize-the-title-text"></a>Paso 2: Personalizar el texto del título

La página web puede proporcionar el título mediante la etiqueta meta mswebdialog-title.

``` syntax
<meta name="mswebdialog-title" content="Contoso Social"/>
```

El título debe ser corto y debe reflejar la marca del proveedor (por ejemplo, Contoso).

### <a name="step-3-customize-the-header-color"></a>Paso 3: Personalizar el color del encabezado

La página web puede proporcionar el color que representa su identidad de marca que se usará para el encabezado del cuadro de diálogo mediante la etiqueta meta mswebdialog-header-color.

``` syntax
<meta name="mswebdialog-header-color" content="#1267DF"/>
```

El color puede ser cualquier valor especificado aquí. Sin embargo, el Agente de autenticación web omitirá cualquier valor de canal alfa. Con este color específicamente y con los colores usados en la página en general, se recomienda seguir los mismos colores que se usan en la aplicación de Windows 8 proveedor si existe dicha aplicación.

> [!Note]  
> Los iconos y colores se almacenan en caché por servidor en el cliente una vez que se analizan las etiquetas META. Borre la caché del cliente antes de iniciar la interfaz de usuario para que los cambios sumen efecto. Para ello, modifique la siguiente configuración del Registro.

 

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

Una vez descargado un icono, no se vuelve a seleccionar durante 24 horas. Para probar con imágenes de logotipo, establezca la clave reg anterior con un valor inferior.

### <a name="step-4-customize-the-web-page"></a>Paso 4: Personalizar la página web

Además de personalizar la interfaz de usuario en torno a la página web, los desarrolladores también deben crear páginas web que sean perfectas e integradas con la experiencia general Windows 8 web. Esto incluye el uso de estilos recomendados, asegurarse de que las páginas web funcionan bien con dispositivos táctiles y abrir determinadas páginas web en el explorador web.

-   Aplicación de estilos

    Se recomienda encarecidamente usar el estilo recomendado aquí para crear una experiencia de usuario más coherente en las páginas web del Agente de autenticación web y otros componentes de interfaz de usuario de Windows 8. La página web debe usar un fondo blanco y ningún borde. Los botones como Inicio de sesión o Cancelar deben colocarse en la esquina inferior derecha y usar el mismo color que el encabezado. Por último, dado que el Agente de autenticación web proporciona botón Atrás, considere la posibilidad de eliminar completamente un botón Cancelar de la página web.

-   Habilitación de la táctil

    La página web debe diseñarse pensando en una interacción táctil del usuario. Para obtener más información sobre el diseño para la interacción táctil Windows 8, vea el tema Sobre el [diseño de interacción táctil.](https://msdn.microsoft.com/library/Hh465415(v=Win.10).aspx)

-   Personalización del destino de los hipervínculos

    El Agente de autenticación web es excelente para entregar páginas web que requieren una sola acción de usuario, como páginas de autorización de OAuth o de inicio de sesión. Sin embargo, para flujos de usuario más complejos, como la creación de cuentas, la recuperación de una contraseña perdida u olvidada, la presentación de declaraciones de privacidad, etc., donde se espera que el usuario invierta algún tiempo en comprender y completar el flujo, se recomienda que estas páginas se inician en el explorador preferido del usuario para admitir la navegación completa y la exploración de alcance. De forma predeterminada, el Agente de autenticación web no permite abrir nuevas ventanas del explorador desde una página web (consulte la sección No hay nuevas ventanas de forma predeterminada para obtener más detalles). Sin embargo, mediante la etiqueta meta, la página web puede `mswebdialog-newwindowurl` declarar qué direcciones URL deben abrirse en el explorador.

    permite a la página web especificar una dirección URL o parte de la dirección URL que el Agente de autenticación web usará para hacer coincidir (coincidencia de cadena izquierda) cada vez que se le pida que abra una dirección URL en una nueva ventana mediante el atributo de destino o el método `mswebdialog-newwindowurl` window.open(). Si hay una coincidencia, la dirección URL se abrirá en el explorador predeterminado del usuario. Si no hay ninguna coincidencia, el Agente de autenticación web navegará a la propia dirección URL (comportamiento predeterminado). Por ejemplo:`<meta name="mswebdialog-newwindowurl" content="https://www.contoso.com/privacy"/>`

    En el caso de esta metaetiqueta, el Agente de autenticación web abrirá en el https://www.contoso.com/privacy/policy.html explorador, pero navegará directamente a https://www.contoso.com/termsofuse.html . Tenga en cuenta que los vínculos que no intentan abrirse en una nueva ventana (por ejemplo, los vínculos que no usan el atributo de destino o el método window.open() ) no se ven afectados por esta metaetiqueta. El contenido es una dirección URL que puede ser relativa o absoluta. El esquema de la dirección URL puede ser HTTP o HTTPS. Debe definir etiquetas meta para cubrir los vínculos que no forman parte del flujo de usuario principal, como declaraciones de `mswebdialog-newwindowurl` privacidad, formularios de registro, entre otros. Si admite el inicio de sesión con un proveedor de autenticación de terceros (por ejemplo, proveedores de OpenID), asegúrese de mantener esas interacciones dentro del Agente de autenticación web. Para habilitar todos los vínculos de la página como seguros para que se abran en el explorador, use la sintaxis de estrella, como , tenga en cuenta que " " solo se puede usar exclusivamente y no se puede combinar con otra dirección URL, por ejemplo, " *" no es una sintaxis `  <meta name="mswebdialog-newwindowurl" content="*"/>` \* https://www.contoso.com/\ válida.

### <a name="step-5-rules-applied-to-all-meta-tags"></a>Paso 5: Reglas aplicadas a todas las etiquetas meta

Cuando el Agente de autenticación web procesa etiquetas meta, se aplican las siguientes reglas:

-   El efecto de la metaetiqueta se conservará en todas las páginas del mismo dominio de segundo nivel (por ejemplo, contoso.com) a menos que se encuentre otra metaetiqueta con el mismo nombre pero con contenido diferente.
-   Si se encuentran varias metaetiquetas con el mismo nombre en la misma página, el Agente de autenticación web elegirá solo una de ellas e ignorará el resto. La metaetiqueta específica que se elige no está definida.
    > [!Note]  
    > Esta regla no se aplica a la `mswebdialog-newwindowurl` metaetiqueta que permite varias instancias en la misma página.

     

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones para el desarrollo de páginas web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Aplicación de ejemplo del SDK del Agente de autenticación web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
