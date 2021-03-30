---
title: Compatibilidad con temas de contraste alto
description: En este tema se compara la compatibilidad con los temas de contraste alto de Windows 8 con la de versiones anteriores de Windows y se explica cómo se admiten los temas de contraste alto en una aplicación de Windows 8.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2068d64b585f302f578296c9e156895c23b9bce9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904839"
---
# <a name="supporting-high-contrast-themes"></a>Compatibilidad con temas de contraste alto

En este tema se compara la compatibilidad con los temas de contraste alto de Windows 8 con la de versiones anteriores de Windows y se explica cómo se admiten los temas de contraste alto en una aplicación de Windows 8.

Incluye las siguientes secciones.

-   [Información general de la compatibilidad con temas de contraste alto](#overview-of-support-for-high-contrast-themes)
-   [Compatibilidad con temas de contraste alto en Windows 8 y versiones posteriores](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [Agregar una sección de compatibilidad al manifiesto de aplicación](#adding-a-compatibility-section-to-your-application-manifest)
-   [Detección de contraste alto en versiones anteriores de Windows](#detecting-high-contrast-in-previous-versions-of-windows)
-   [Temas relacionados](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a>Información general de la compatibilidad con temas de contraste alto

Windows 7 y versiones anteriores admiten dos modelos de ti, incluido el modelo clásico de Windows heredado y los estilos visuales actuales. El modelo clásico de Windows se ha mantenido a través de Windows 7 principalmente para admitir los diversos temas de contraste alto. Sin embargo, el modelo clásico de Windows tiene varias desventajas:

-   No se admiten temas que usan estilos visuales, como Windows Aero. Los usuarios de los temas de contraste alto deben usar la interfaz de usuario clásica de Windows.
-   No se admiten las características de la interfaz de usuario que se basan en Administrador de ventanas de escritorio (DWM) para ejecutarse, como las vistas previas en miniatura y el ampliador de pantalla completa que se presentó en Windows 7.
-   Los desarrolladores deben mantener dos rutas de acceso de código independientes para admitir los dos modelos de cada una de ellas.

En Windows 8 y versiones posteriores, los siguientes cambios en el modelo de los procedimientos abordan los inconvenientes anteriores:

-   Ya no se admite el modelo de ti clásico de Windows, lo que permite a los desarrolladores mantener solo una ruta de acceso al código para las aplicaciones destinadas solo a Windows 8.
-   Dado que los estilos visuales y DWM están activados en Windows 8, los usuarios de alto contraste tienen acceso a características como las vistas previas de miniaturas y el ampliador de pantalla completa.
-   Los estilos visuales admiten la configuración de los colores de varios elementos de la interfaz de usuario, lo que permite a los usuarios de contraste alto personalizar la interfaz de usuario para adaptarse a las necesidades y preferencias individuales.
-   Windows 8 incluye compatibilidad con las aplicaciones existentes que están diseñadas para usar temas de contraste alto basados en el modelo de temas clásicos de Windows.

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a>Compatibilidad con temas de contraste alto en Windows 8 y versiones posteriores

En Windows 8, dado que los estilos visuales están activados en el modo de contraste alto, la compatibilidad con los temas de contraste alto es sencilla siempre y cuando se tengan en cuentan las siguientes directrices.

-   Tamaños de fuente y control. Para asegurarse de que la interfaz de usuario es accesible para los usuarios con discapacidades, establezca tamaños de fuente según la configuración de tema actual. Establezca el tamaño de los controles para que sea al menos el tamaño predeterminado.
-   Colorea. Evite el uso de colores codificados de forma rígida. En su lugar, use los colores del sistema porque se basan en el tema actual. El uso de colores personalizados puede interferir con los colores de los temas de contraste alto y reemplazarlos.
-   Manifiesto de aplicación. Las aplicaciones diseñadas para trabajar con los nuevos temas de contraste alto deben tener definida una sección de compatibilidad de aplicaciones en su manifiesto que contenga los GUID de compatibilidad de Windows 8. De lo contrario, Windows supone que la aplicación está diseñada para una versión anterior de Windows y representa la interfaz de usuario de la aplicación mediante la simulación del modelo de los Windows clásico.

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a>Agregar una sección de compatibilidad al manifiesto de aplicación

Un manifiesto de aplicación es un archivo XML que describe los requisitos de una aplicación. La sección de compatibilidad del manifiesto identifica las versiones de Windows compatibles con la aplicación. En la sección compatibilidad se usan los siguientes GUID para identificar las distintas versiones de Windows.

| Versión       | GUID                                   |
|---------------|----------------------------------------|
| Windows Vista | {e2011457-1546-43c5-a5fe-008deee3d3f0} |
| Windows 7     | {35138b9a-5d96-4fbd-8e2d-a2440225f93a} |
| Windows 8     | {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} |



 

La sección de compatibilidad puede especificar varias versiones de Windows, pero cada una debe estar contenida dentro de su propia `<supportedOS/>` etiqueta. En el ejemplo siguiente se muestra un manifiesto de aplicación que especifica Windows 7 y Windows 8 en la sección de compatibilidad:


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



Si una aplicación no tiene un manifiesto de compatibilidad, se supone que es una aplicación de Windows Vista y no usa controles con temas en el área cliente cuando está activo un tema de contraste alto. Además, el comportamiento de algunas funciones de estilos visuales se ve afectado. Por ejemplo, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)y [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) devuelven false, mientras que [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) y [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) devuelven un identificador nulo. Esto es para la compatibilidad con la compatibilidad, de modo que las aplicaciones compiladas antes de Windows 8 todavía pueden representar su interfaz de usuario en el mismo aspecto que el modo de contraste alto de las versiones anteriores de Windows en las que los estilos visuales no están disponibles.

En Windows 8, la aplicación sigue recibiendo las ventajas de la composición del escritorio. Esto significa, por ejemplo, que las aplicaciones de facilidad de uso, como el ampliador de pantalla completa, no dependen del estado del manifiesto de una aplicación individual. La aplicación de facilidad de uso sigue funcionando en el modo de contraste alto con una aplicación que no se identifica como compatible con Windows 8 en su manifiesto.

En las imágenes siguientes se muestra un cuadro de diálogo simple en contraste alto en Windows 7.

![cuadro de diálogo contraste de hig](images/win7-high-contrast.png)

En esta imagen se muestra el mismo cuadro de diálogo en contraste alto en Windows 8, pero con la compatibilidad de Windows 7 especificada en el manifiesto de aplicación:

![W8 cuadro de diálogo contraste alto](images/win7-compat.png)

En esta imagen se muestra el mismo cuadro de diálogo en contraste alto en Windows 8, con Windows 8 especificado en el manifiesto de aplicación:

![W8 cuadro de diálogo de contraste alto con manifiesto](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a>Detección de contraste alto en versiones anteriores de Windows

Las aplicaciones que se ejecutan en versiones anteriores de Windows no tienen acceso a los nuevos temas de contraste alto. Si la aplicación necesita ejecutarse en versiones anteriores de, debe incluir la compatibilidad para representar la interfaz de usuario en alta contraWindowsst en el modelo de Windows clásico. La aplicación puede determinar si un tema de contraste alto está activo mediante una llamada a la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con la marca **SPI \_ GETHIGHCONTRAST** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Habilitar los estilos visuales](cookbook-overview.md)
</dt> <dt>

[Estilos visuales](themes-overview.md)
</dt> </dl>

 

 