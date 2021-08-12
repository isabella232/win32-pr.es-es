---
title: Compatibilidad con contraste alto temas
description: En este tema se compara la compatibilidad con temas de contraste alto en Windows 8 con la de versiones anteriores de Windows y se explica cómo admitir temas de contraste alto en una aplicación Windows 8.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f32c89302daeb7190174a0d6b9e822e1c55d3e530ad29baedd00c5ffdefc97b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670642"
---
# <a name="supporting-high-contrast-themes"></a>Compatibilidad con contraste alto temas

En este tema se compara la compatibilidad con temas de contraste alto en Windows 8 con la de versiones anteriores de Windows y se explica cómo admitir temas de contraste alto en una aplicación Windows 8.

Incluye las secciones siguientes.

-   [Información general sobre la compatibilidad con contraste alto temas](#overview-of-support-for-high-contrast-themes)
-   [Compatibilidad con contraste alto temas en Windows 8 y versiones posteriores](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [Agregar una sección de compatibilidad al manifiesto de aplicación](#adding-a-compatibility-section-to-your-application-manifest)
-   [Detección de contraste alto en versiones anteriores de Windows](#detecting-high-contrast-in-previous-versions-of-windows)
-   [Temas relacionados](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a>Información general sobre la compatibilidad con contraste alto temas

Windows 7 y versiones anteriores admiten dos modelos de tema, incluidos el modelo Windows modelo clásico y los estilos visuales actuales. El Windows modelo clásico se ha conservado a través de Windows 7 principalmente para admitir los distintos temas de contraste alto. Sin embargo, Windows modelo clásico tiene una serie de inconvenientes:

-   No se admiten temas que usan estilos visuales, como Windows Aero. Los usuarios de temas de contraste alto deben usar la interfaz Windows clásica.
-   No se admiten características de interfaz de usuario que se basan en Administrador de ventanas de escritorio (DWM) para ejecutarse, como vistas previas de miniaturas y la lupa de pantalla completa que se introdujo en Windows 7.
-   Los desarrolladores deben mantener dos rutas de acceso de código independientes para admitir los dos modelos de aspectos diferentes.

En Windows 8 y versiones posteriores, los siguientes cambios en el modelo de temas abordan los inconvenientes anteriores:

-   El Windows modelo de modelado clásico ya no se admite, lo que permite a los desarrolladores mantener solo una ruta de acceso de código para las aplicaciones que solo tienen como destino Windows 8.
-   Dado que los estilos visuales y DWM están en Windows 8, los usuarios de contraste alto tienen acceso a características como vistas previas de miniaturas y la lupa de pantalla completa.
-   Los estilos visuales admiten la configuración de los colores de varios elementos de la interfaz de usuario, lo que permite a los usuarios de contraste alto personalizar la interfaz de usuario para adaptarse a las necesidades y preferencias individuales.
-   Windows 8 compatibilidad con aplicaciones existentes diseñadas para usar temas de contraste alto basados en Windows modelo de temas clásicos.

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a>Compatibilidad con contraste alto temas en Windows 8 y versiones posteriores

En Windows 8, dado que los estilos visuales están en modo de contraste alto, la compatibilidad con temas de contraste alto es sencilla siempre que se acomenten las siguientes directrices.

-   Tamaños de fuente y control. Para asegurarse de que la interfaz de usuario sea accesible para los usuarios con discapacidades, establezca los tamaños de fuente según la configuración actual del tema. Establezca el tamaño de los controles como mínimo el tamaño predeterminado.
-   Colores. Evite el uso de colores codificados de forma fuerte. En su lugar, use los colores del sistema porque se basan en el tema actual. El uso de colores personalizados puede interferir con los colores de los temas de contraste alto e invalidarlo.
-   Manifiesto de aplicación. Las aplicaciones diseñadas para trabajar con los nuevos temas de contraste alto deben tener una sección de compatibilidad de aplicaciones definida en su manifiesto que contenga los GUID Windows 8 compatibilidad de aplicaciones. De lo contrario, Windows supone que la aplicación está diseñada para una versión anterior de Windows y representa la interfaz de usuario de la aplicación simulando el modelo de Windows de tema clásico.

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a>Agregar una sección de compatibilidad al manifiesto de aplicación

Un manifiesto de aplicación es un archivo XML que describe los requisitos de una aplicación. La sección de compatibilidad del manifiesto identifica las versiones de Windows compatibles con la aplicación. Los siguientes GUID se usan en la sección de compatibilidad para identificar las distintas versiones de Windows.

| Versión       | GUID                                   |
|---------------|----------------------------------------|
| Windows Vista | {e2011457-1546-43c5-a5fe-008deee3d3f0} |
| Windows 7     | {35138b9a-5d96-4fbd-8e2d-a2440225f93a} |
| Windows 8     | {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} |



 

La sección de compatibilidad puede especificar varias versiones de Windows, pero cada una debe incluirse dentro de su propia `<supportedOS/>` etiqueta. En el ejemplo siguiente se muestra un manifiesto de aplicación que especifica Windows 7 y Windows 8 en la sección de compatibilidad:


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!--The ID below indicates application support for Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>

            <!--The ID below indicates application support for Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        </application>
    </compatibility>
</assembly>
```



Si una aplicación no tiene un manifiesto de compatibilidad, se supone que es una aplicación Windows Vista y no usa controles temas en el área cliente cuando un tema de contraste alto está activo. Además, el comportamiento de algunas funciones de estilos visuales se ve afectado. Por ejemplo, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)e [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) devuelven FALSE, mientras que [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) y [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) devuelven un identificador NULL. Esto es para la compatibilidad, de modo que las aplicaciones creadas antes de Windows 8 todavía puedan representar su interfaz de usuario en el mismo aspecto que el modo de contraste alto de versiones anteriores de Windows donde los estilos visuales no están disponibles.

En Windows 8, la aplicación sigue recibindo las ventajas de la composición de escritorio. Esto significa, por ejemplo, que las aplicaciones de facilidad de uso, como la lupa de pantalla completa, no dependen del estado del manifiesto de una aplicación individual. La aplicación de facilidad de uso sigue funcionando en modo de contraste alto con una aplicación que no se identifica como Windows 8 compatible en su manifiesto.

Las imágenes siguientes muestran un cuadro de diálogo simple en contraste alto en Windows 7.

![hig contrast (cuadro de diálogo)](images/win7-high-contrast.png)

Esta imagen muestra el mismo cuadro de diálogo en contraste alto Windows 8, pero con la compatibilidad Windows 7 especificada en el manifiesto de aplicación:

![Cuadro de diálogo de contraste alto w8](images/win7-compat.png)

Esta imagen muestra el mismo cuadro de diálogo en contraste alto Windows 8, con Windows 8 especificado en el manifiesto de aplicación:

![Cuadro de diálogo de contraste alto w8 con manifiesto](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a>Detección de contraste alto en versiones anteriores de Windows

Las aplicaciones que se ejecutan en versiones anteriores Windows no tienen acceso a los nuevos temas de contraste alto. Si la aplicación necesita ejecutarse en versiones anteriores de , debe incluir compatibilidad para representar la interfaz de usuario en alta contraWindowsst en el modelo de Windows de modelado clásico. La aplicación puede determinar si un tema de contraste alto está activo llamando a la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con la **marca SPI \_ GETHIGHCONTRAST.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Habilitar los estilos visuales](cookbook-overview.md)
</dt> <dt>

[Estilos visuales](themes-overview.md)
</dt> </dl>

 

 