---
title: Información general sobre los estilos visuales
description: En este tema se describen los estilos visuales y se identifican los componentes de Windows que los admiten. También se explican los pasos que debe seguir para usar estilos visuales en las aplicaciones.
ms.assetid: 5B5D7BB6-684F-478D-BF5F-B8D18BBCFF2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5663730c752fbf16c4f229a031eafa0c65bb9dbb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488560"
---
# <a name="visual-styles-overview"></a>Información general sobre los estilos visuales

En este tema se describen los estilos visuales y se identifican los componentes de Windows que los admiten. También se explican los pasos que debe seguir para usar estilos visuales en las aplicaciones. Este tema incluye las siguientes secciones:

-   [Themes and Visual Styles](#themes-and-visual-styles)
-   [Componentes de estilos visuales](#visual-styles-components)
-   [Requisitos de la aplicación para admitir estilos visuales](#application-requirements-for-supporting-visual-styles)
-   [Temas relacionados](#related-topics)

## <a name="themes-and-visual-styles"></a>Themes and Visual Styles

Windows incluye varias características que permiten a los usuarios adaptar la interfaz de usuario para adaptarse a sus necesidades y preferencias individuales. Estas características incluyen temas, que se introdujeron en Microsoft Plus. para Windows 95. Un tema es una colección seleccionable por el usuario de valores que incluye papel tapiz, cursores, fuentes, sonidos e iconos. A continuación se muestran algunas características de los temas.

-   La configuración del tema se especifica en los archivos. theme que tienen un formato similar a win.ini archivos.
-   Un fabricante de software independiente (ISV) puede crear y distribuir un archivo. theme con un producto.
-   En las versiones anteriores a Windows Vista, los archivos de tema se muestran en la pestaña tema del panel de control de pantalla. En Windows Vista y versiones posteriores, los temas se muestran en el panel de control de personalización.

Para obtener más información acerca de los archivos. theme, consulte [formato de archivo de tema](themesfileformat-overview.md).

Un estilo visual es una especificación que define la apariencia de los controles comunes de Windows. Los estilos visuales están asociados a los temas; es decir, un archivo. theme contiene una sección que especifica el estilo visual que se aplicará cuando el tema determinado esté activo. A continuación se muestran algunas características de los estilos visuales.

-   Los usuarios pueden cambiar el estilo visual en cualquier momento seleccionando otro tema.
-   Debe usar la API de estilos visuales para aplicar el estilo visual actualmente activo a los controles personalizados o dibujados por el propietario de la aplicación, si los hay.
-   La información que define un estilo visual se almacena en un archivo. msstyles. Microsoft no admite la creación de archivos. msstyles.


En la ilustración siguiente se muestra un cuadro de diálogo simple con una barra de tareas, en un escritorio de Windows 7 que usa el tema Aero de Windows sin transparencia. Dado que la aplicación no está configurada para usar estilos visuales, los botones aparecen de la misma forma independientemente de la configuración del tema.

![captura de pantalla de un cuadro de diálogo con botones que no usan transparencia](images/tb-wostyles.png)

En cambio, en la siguiente ilustración se muestra el mismo cuadro de diálogo en el mismo escritorio, pero esta vez la aplicación se ha configurado para trabajar con estilos visuales. Tenga en cuenta la apariencia diferente de los botones del área cliente. Los botones tienen un aspecto diferente porque el sistema ha aplicado los estilos visuales que se definen en el tema de Aero.

![captura de pantalla de un cuadro de diálogo con botones que usan transparencia](images/tb-withstyles.png)

En el ejemplo siguiente se muestra un cuadro de diálogo similar en un escritorio de Windows 8. En Windows 8, los estilos visuales están siempre activados, por lo que las aplicaciones de Windows 8 lo obtienen "gratis".

![captura de pantalla de un cuadro de diálogo simple en el escritorio de Windows 8](images/tb-win8.png)

## <a name="visual-styles-components"></a>Componentes de estilos visuales

Los estilos visuales son compatibles con los siguientes componentes:

-   Versión 6 o posterior de la biblioteca de controles comunes (ComCtl32.dll)
-   La API de estilos visuales implementada en UxTheme.dll
-   Servicio de temas
-   Uno o varios archivos de definición de estilo visual (. msstyles)

La API de estilos visuales depende de un servicio de sistema denominado themes. La biblioteca de controles comunes consulta el servicio de temas para obtener información relacionada con el estilo y, hasta Windows 7, usa el servicio para representar controles en el estilo visual actual.

En Windows 8 y versiones posteriores, la API de estilos visuales sigue funcionando si el servicio themes está desactivado. Esto significa que los controles comunes y el área no cliente de Windows seguirán teniendo estilos visuales cuando el servicio themes esté desactivado. Las características de Windows 8 que siguen requiriendo el servicio temas incluyen:

-   Cambiar el estilo visual, normalmente a través de la página **Personalización** de **configuración de PC**.
-   Optimizaciones de rendimiento implicadas en el cambio de usuarios, el cierre de sesión, el apagado y el uso compartido entre sesiones de usuario.

La API de estilos visuales obtiene información de estilo del archivo. msstyles asociado al tema seleccionado actualmente. El archivo. msstyles contiene un conjunto de métricas, fuentes, colores y mapas de bits que definen un estilo visual

## <a name="application-requirements-for-supporting-visual-styles"></a>Requisitos de la aplicación para admitir estilos visuales

Para usar estilos visuales, la aplicación debe ejecutarse en un sistema operativo que contenga ComCtl32.dll versión 6 o posterior. Si desea que la aplicación use ComCtl32.dll versión 6, debe agregar un manifiesto de aplicación o una directiva de compilador para especificar que se debe usar la versión 6 Si está disponible. Para obtener información sobre cómo crear un manifiesto de aplicación que permita a la aplicación usar estilos visuales, vea [habilitar estilos visuales](cookbook-overview.md).

En el caso de los controles comunes, no es necesario realizar ninguna otra acción para asegurarse de que los controles se muestran en el estilo visual preferido del usuario.

Si la aplicación contiene controles personalizados o dibujados por el propietario, debe usar la API de estilos visuales para recuperar información sobre el estilo visual activo actual y para dibujar los controles de ese estilo.

En el caso de las versiones de Windows anteriores a Windows 8, las aplicaciones normalmente necesitan proporcionar dos rutas de acceso de código independientes para dibujar controles personalizados y dibujados por el propietario. Una ruta de código dibuja los controles cuando un tema que utiliza estilos visuales está activo y otra ruta de acceso de código dibuja los controles cuando el tema clásico de Windows o un tema de contraste alto están activos. En Windows 8, sin embargo, los estilos visuales están siempre activados, por lo que no es necesario separar las rutas de acceso del código. Las aplicaciones que se manifiestan para Windows 8 obtienen un alto contraste "gratis". Para obtener más información, consulte [compatibilidad con temas de contraste alto](supporting-high-contrast-themes.md).

Para obtener más información sobre, vea [usar estilos visuales con controles personalizados y Owner-Drawn](using-visual-styles.md) y [referencia de estilos visuales](uxctl-ref.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estilos visuales](themes-overview.md)
</dt> </dl>

 

 




