---
title: Modo de contraste alto
description: Modo de contraste alto
ms.assetid: 817F2BBD-3744-4D34-927F-EBF9F7894CC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8c53d3e92bb97dd9e2f5fa34bad9f901920cc7
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794206"
---
# <a name="high-contrast-mode"></a>Modo de contraste alto

## <a name="platforms"></a>Plataformas

 **Clientes** : Windows 8  
**Servidores** : Windows Server 2012  



## <a name="description"></a>Descripción

En los sistemas operativos Windows anteriores, el modo de alto contraste estaba limitado a los temas que se ejecutaban en temas clásicos, que no tenían un estilo visual. En Windows 8 y Windows Server 2012, el modo clásico se ha quitado y se ha reemplazado por temas de contraste alto de estilo visual. Una de las principales ventajas de este cambio es la eliminación de una ruta de acceso de código independiente para las aplicaciones que se ejecutan en modo clásico.

Los desarrolladores todavía deben instruirse en cómo el modo de alto contraste puede afectar a su aplicación y cómo desarrollar una aplicación realmente independiente del estilo. Esto es importante porque aunque el uso o suposición incorrectos de los colores del tema puede hacer que las aplicaciones se comporten correctamente con un estilo visual como Aero, esas mismas aplicaciones responden incorrectamente en contraste alto. Por ejemplo, en Aero, el texto siempre es negro y el color de resaltado es azul claro. Sin embargo, en negro de contraste alto, el color de resaltado es negro. Si asume texto en negro, como en muchas aplicaciones integradas anteriores a Windows 8, y usa el valor predeterminado del sistema para el resaltado, el usuario verá el texto en negro en un fondo negro. En estas situaciones, es necesario saber cómo usar los temas y las métricas del sistema correctamente para que la aplicación tenga un aspecto correcto en todos los estilos.

## <a name="manifestations"></a>Manifestaciones

-   La tarea no está habilitada en el área cliente de las aplicaciones que no contienen una <supportedOS> etiqueta de Windows 8 en el manifiesto de la aplicación. Por lo tanto, las aplicaciones deben representar el área cliente, mediante la ruta de acceso del código requerida para representar en el modo de alto contraste del tema clásico.
-   Los temas no están habilitados en las áreas cliente y no cliente de las aplicaciones en los temas de contraste alto. Tampoco está habilitado en las aplicaciones que no contienen una etiqueta de Windows 8 en el manifiesto de la <supportedOS> aplicación y que se dibujan en el área no cliente de una ventana mediante la API DwnIsCompositionEnabled (). Toda la aplicación se representa en el modo de alto contraste del tema clásico.
-   Las aplicaciones que agregan compatibilidad con Windows 8 en su manifiesto, pero no usan estilos visuales para la representación, es decir, codifican colores o imágenes en sus aplicaciones, es posible que no se representen correctamente en los temas de contraste alto. Es posible que el texto sea difícil de leer o de que las imágenes no aparezcan como deberían en el modo de contraste alto.

## <a name="mitigation"></a>Mitigación

Los colores de texto de los temas de contraste alto se han creado para cumplir con las directrices de accesibilidad de Microsoft. Mantenemos una relación de contraste alto de 14:1 entre el primer plano y el fondo. Si los colores que están habilitados de forma predeterminada no son adecuados para un usuario final determinado, se pueden personalizar fácilmente a través de la configuración del panel de control para "color de ventana" en esos temas de contraste alto.

Estos componentes de interfaz de usuario se pueden personalizar en los temas de contraste alto:

-   Color de fondo de la ventana
-   Color del texto
-   Color de hipervínculos
-   Texto deshabilitado
-   Colores de fondo y de primer plano del texto seleccionado
-   Colores de primer plano y de fondo del título de la ventana activa
-   Colores de primer plano y de fondo del título de la ventana inactiva
-   Colores de primer plano y de fondo del botón

## <a name="solution"></a>Solución

Si se detecta un comportamiento inesperado en las aplicaciones de los temas de contraste alto, una de estas soluciones podría ser útil:

-   **Manifiesto de una aplicación para Windows 8:**

    Las aplicaciones que no contienen la <supportedOS> etiqueta de Windows 8 en el manifiesto de la aplicación tendrán sus áreas de cliente representadas sin un tema. Todas las aplicaciones de la caja deben contener esta entrada en el manifiesto de la aplicación. Agregue el valor de GUID de 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38 para Windows 8.

-   **Usar estilos visuales con las interfaces de usuario dibujadas por el propietario:**

    Los controles dibujados por el propietario deben seguir las instrucciones de [MSDN](/windows/desktop/Controls/using-visual-styles) para representar correctamente las partes y los Estados de control, incluido el texto. Los desarrolladores no deben confiar en el texto o el color de fondo especificado en un contexto de dispositivo con el fin de usar métodos no UxTheme para la representación. En caso de que no haya ninguna parte del tema para el control en cuestión, use GetThemeSysColor con la [métrica adecuada](/windows/desktop/api/winuser/nf-winuser-getsyscolor) y dibuje el texto mediante métodos GDI estándar. Si ninguna de las llamadas a UxTheme es adecuada, use el método GetSysColor para obtener la métrica adecuada.

-   **Selección del color del texto:**

    No use un color de texto codificado, aunque se supone que es correcto en todos los escenarios comunes. Los temas de envío se crean de forma que admita una alta visibilidad con las métricas asociadas. Por ejemplo, \_ el color HIGHLIGHTTEXT está pensado para usarse con \_ el resaltado de color como fondo y el color \_ WINDOWTEXT está pensado para usarse con \_ la ventana de color como fondo. Si hay excepciones a estas asociaciones, trabaje con ellas en las partes del tema y en las definiciones de estado y no en el código. Al diseñar ius de contraste alto, es fundamental que la interfaz de usuario sea independiente del tema de contraste alto aplicado actualmente, ya que los usuarios de contraste alto pueden personalizar sus colores.

-   **Responder al evento de ThemeChange de WM \_ :**

    Si la aplicación almacena en caché los colores recuperados del tema o aplica colores de un modo no estándar, agregue un controlador de mensajes para WM \_ THEMECHANGE que recalcule los valores de color almacenados y vuelva a dibujar la interfaz de usuario.

-   **Escritura de una aplicación WWA de alto contraste:**

    Las aplicaciones web no tienen acceso a las API de UxTheme, pero todavía se deben escribir con las métricas actuales del sistema como base para la interfaz de usuario. Hay algunos recursos que los desarrolladores de WWA pueden aprovechar para garantizar una aplicación compatible con el alto contraste:

    -   La [especificación de color CSS de W3C](https://www.w3.org/TR/css3-color/) especifica la sintaxis para usar las métricas del sistema en lugar de los colores específicos
    -   Se ha agregado compatibilidad con las consultas de medios de contraste alto a Internet Explorer 10.
    -   WWAs puede aprovechar el método IAccessibilityCapabilities:: get \_ HighContrast () para comprobar el estado de contraste alto

    Las aplicaciones de la tienda Windows no tienen muchos de los mismos problemas con las partes del tema que se encuentran en las aplicaciones clásicas de Windows, pero sigue siendo necesario garantizar el cumplimiento de alto contraste. De forma predeterminada, Internet Explorer omite determinados estilos definidos por el usuario y los reemplaza por valores que cumplen con el alto contraste. Por ejemplo, se omiten las propiedades background-image, Background y color de CSS.

    Si no desea que Internet Explorer ignore las propiedades que establezca y asegúrese de que la interfaz de usuario es compatible con contraste alto, puede establecer la nueva propiedad de CSS M3: MS-High-Contrast: OFF en un elemento primario.

-   **Escribir una aplicación de la tienda Windows de alto contraste:**

    La aplicación de la tienda Windows debe usar la clase [SystemColors](/dotnet/api/system.windows.systemcolors) para determinar el color correcto del elemento de la interfaz de usuario, teniendo en cuenta que ciertos colores de métrica del sistema están diseñados para usarse conjuntamente, como SystemColors. WindowColor y SystemColors. WindowTextColor. Esto facilita una experiencia de alto contraste superior.

-   **Detectar correctamente el contraste alto en versiones anteriores de Windows:**

    Las aplicaciones que se ejecutan en versiones anteriores de Windows no tienen acceso a los nuevos temas de contraste alto incluso si el manifiesto especifica compatibilidad con la versión de Windows en cuestión. Como tal, podría ser necesario insertar rutas de acceso de código adicionales para controlar la representación en el entorno clásico usado en versiones anteriores de Windows. La presencia de contraste alto en este caso debe comprobarse mediante una llamada a la función [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con la \_ marca SPI GETHIGHCONTRAST. Esta es la única manera admitida de comprobar la presencia de contraste alto.

## <a name="tests"></a>Pruebas

Al probar una aplicación, asegúrese de que se representa correctamente en todos los temas incluidos en Windows 8: Aero, básico, contraste alto 1, contraste alto 2, contraste alto negro y contraste alto blanco. Asegúrese de que el texto es claramente visible y fácil de leer en los temas de contraste alto.

## <a name="resources"></a>Recursos

-   [Clases, elementos y Estados de estilo de Aero](../controls/aero-style-classes-parts-and-states.md) (el nuevo tema básico y los temas de contraste alto también usan estos Estados)
-   [Partes y Estados comunes a todos los estilos visuales](../controls/parts-and-states.md)
-   [Usar estilos visuales con controles personalizados y Owner-Drawn](../controls/using-visual-styles.md)
-   [GetSysColor (función)](/windows/win32/api/winuser/nf-winuser-getsyscolor)
-   [Nivel 3 del módulo de color CSS de W3C](https://www.w3.org/TR/css3-color/)
-   [SystemColors (clase)](/dotnet/api/system.windows.systemcolors?view=netcore-3.1)
-   [SystemParametersInfo (función)](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
-   [Accesibilidad de Microsoft](https://www.microsoft.com/enable/)

 

 