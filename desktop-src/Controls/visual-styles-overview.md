---
title: Información general sobre los estilos visuales
description: En este tema se describen los estilos visuales e identifica Windows componentes que los admiten. También se explican los pasos que debe seguir para usar estilos visuales en las aplicaciones.
ms.assetid: 5B5D7BB6-684F-478D-BF5F-B8D18BBCFF2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 237ac858e1a60e615a6af177728102fb7e6ea1737a3a2d94d93091264b02121a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077738"
---
# <a name="visual-styles-overview"></a>Información general sobre los estilos visuales

En este tema se describen los estilos visuales e identifica Windows componentes que los admiten. También se explican los pasos que debe seguir para usar estilos visuales en las aplicaciones. Este tema incluye las siguientes secciones:

-   [Themes and Visual Styles](#themes-and-visual-styles)
-   [Componentes de estilos visuales](#visual-styles-components)
-   [Requisitos de la aplicación para admitir estilos visuales](#application-requirements-for-supporting-visual-styles)
-   [Temas relacionados](#related-topics)

## <a name="themes-and-visual-styles"></a>Themes and Visual Styles

Windows incluye varias características que permiten a los usuarios adaptar la interfaz de usuario para adaptarse a sus necesidades y preferencias individuales. Estas características incluyen temas, que se introdujeron en Microsoft Plus. para Windows 95. Un tema es una colección de configuraciones seleccionable por el usuario que incluye papel tapiz, cursores, fuentes, sonidos e iconos. A continuación se den algunas características de los temas.

-   La configuración del tema se especifica en los archivos .theme que tienen un formato similar a win.ini archivos.
-   Un proveedor de software independiente (ISV) puede crear y distribuir un archivo .theme con un producto.
-   En versiones anteriores a Windows Vista, los archivos de tema se muestran en la pestaña Tema del panel de control Mostrar. En Windows Vista y versiones posteriores, los temas se muestran en el panel de control Personalización.

Para obtener más información sobre los archivos .theme, vea [Theme File Format](themesfileformat-overview.md).

Un estilo visual es una especificación que define la apariencia del Windows controles comunes. Los estilos visuales están asociados a temas; Es decir, un archivo .theme contiene una sección que especifica el estilo visual que se aplicará cuando el tema concreto esté activo. Las siguientes son algunas características de los estilos visuales.

-   Los usuarios pueden cambiar el estilo visual en cualquier momento seleccionando un tema diferente.
-   Debe usar la API de estilos visuales para aplicar el estilo visual activo actualmente a los controles personalizados o dibujados por el propietario de la aplicación, si los hay.
-   La información que define un estilo visual se almacena en un archivo .msstyles. Microsoft no admite la creación de archivos .msstyles.


En la ilustración siguiente se muestra un cuadro de diálogo simple con una barra de tareas, en un escritorio de Windows 7 que usa el tema Windows Avión sin transparencia. Dado que la aplicación no está configurada para usar estilos visuales, los botones aparecen igual independientemente de la configuración del tema.

![captura de pantalla de un cuadro de diálogo con botones que no usan transparencia](images/tb-wostyles.png)

Por el contrario, en la ilustración siguiente se muestra el mismo cuadro de diálogo en el mismo escritorio, pero esta vez la aplicación se ha configurado para que funcione con estilos visuales. Observe la apariencia diferente de los botones en el área de cliente. Los botones tienen un aspecto diferente porque el sistema ha aplicado los estilos visuales definidos en el tema DeEr.

![captura de pantalla de un cuadro de diálogo con botones que usan transparencia](images/tb-withstyles.png)

En el ejemplo siguiente se muestra un cuadro de diálogo similar en un Windows 8 escritorio. En Windows 8, los estilos visuales siempre están on, por lo que Windows 8 aplicaciones obtenerlos "de forma gratuita".

![captura de pantalla de un cuadro de diálogo simple en el escritorio de Windows 8](images/tb-win8.png)

## <a name="visual-styles-components"></a>Componentes de estilos visuales

Los estilos visuales son compatibles con los componentes siguientes:

-   Versión 6 o posterior de la biblioteca de control común (ComCtl32.dll)
-   Api de estilos visuales implementada en UxTheme.dll
-   Servicio de temas
-   Uno o varios archivos de definición de estilo visual (.msstyles)

La API de estilos visuales depende de un servicio del sistema denominado Temas. La biblioteca de controles común consulta el servicio Themes para obtener información relacionada con el estilo y, hasta Windows 7, usa el servicio para representar controles en el estilo visual actual.

En Windows 8 y versiones posteriores, la API de estilos visuales sigue funcionando si el servicio Temas está desactivado. Esto significa que los controles comunes y el área no cliente de las ventanas seguirán teniendo estilos visuales cuando el servicio Temas esté desactivado. Las Windows 8 que todavía requieren el servicio Temas incluyen:

-   Cambiar el estilo visual, normalmente a través de la **página Personalización** del **equipo Configuración**.
-   Optimizaciones de rendimiento implicadas en la conmutación de usuarios, el cierre de sesión, el apagado y el uso compartido entre sesiones de usuario.

La API de estilos visuales obtiene información de estilo del archivo .msstyles asociado al tema seleccionado actualmente. El archivo .msstyles contiene un conjunto de métricas, fuentes, colores y mapas de bits que definen un estilo visual.

## <a name="application-requirements-for-supporting-visual-styles"></a>Requisitos de la aplicación para admitir estilos visuales

Para usar estilos visuales, la aplicación debe ejecutarse en un sistema operativo que ComCtl32.dll versión 6 o posterior. Si desea que la aplicación use ComCtl32.dll versión 6, debe agregar un manifiesto de aplicación o una directiva del compilador para especificar que se debe usar la versión 6 si está disponible. Para obtener información sobre cómo crear un manifiesto de aplicación que permita a la aplicación usar estilos visuales, vea [Habilitar estilos visuales.](cookbook-overview.md)

En el caso de los controles comunes, no es necesario realizar ninguna otra acción para asegurarse de que los controles se muestran en el estilo visual preferido del usuario.

Si la aplicación contiene controles personalizados o dibujados por el propietario, debe usar la API de estilos visuales para recuperar información sobre el estilo visual activo actualmente y para dibujar los controles en ese estilo.

Para Windows versiones anteriores a Windows 8, las aplicaciones normalmente necesitan proporcionar dos rutas de acceso de código independientes para dibujar controles personalizados y dibujados por el propietario. Una ruta de acceso de código dibuja los controles cuando un tema que usa estilos visuales está activo y otra ruta de acceso de código dibuja los controles cuando el tema clásico de Windows o un tema de contraste alto está activo. En Windows 8, sin embargo, los estilos visuales siempre están on, por lo que no se necesitan rutas de acceso de código de tema independientes. Las aplicaciones que se manifiestan para Windows 8 obtienen un alto contraste de los theming "de forma gratuita". Para obtener más información, [vea Supporting contraste alto Themes](supporting-high-contrast-themes.md).

Para obtener más información sobre, vea Usar estilos visuales con controles personalizados [y Owner-Drawn y](using-visual-styles.md) Referencia de estilos [visuales.](uxctl-ref.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estilos visuales](themes-overview.md)
</dt> </dl>

 

 




