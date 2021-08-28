---
title: Modo de contraste alto
description: Modo de contraste alto
ms.assetid: 817F2BBD-3744-4D34-927F-EBF9F7894CC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a288447dda8d3a76278ad695459d2c15598b328
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883892"
---
# <a name="high-contrast-mode"></a>Modo de contraste alto

## <a name="platforms"></a>Plataformas

 **Clientes:** Windows 8  
**Servidores:** Windows Server 2012  



## <a name="description"></a>Descripción

En versiones Windows sistemas operativos, el modo de contraste alto se limitaba a los temas que se ejecutaban en temas clásicos, que no tenían un estilo visual. En Windows 8 y Windows Server 2012, el modo clásico se ha quitado y reemplazado por temas de contraste alto con estilo visual. Una de las principales ventajas de este cambio es la eliminación de una ruta de acceso de código independiente para las aplicaciones que se ejecutan en modo clásico.

Los desarrolladores deben seguir teniendo en cuenta cómo el modo de contraste alto puede afectar a su aplicación y cómo desarrollar una aplicación realmente independiente del estilo. Esto es importante porque, aunque el uso incorrecto o la suposición de los colores del tema pueden hacer que las aplicaciones se comporten correctamente bajo un estilo visual como Aero, esas mismas aplicaciones responden incorrectamente en contraste alto. Por ejemplo, en Aero, el texto siempre es negro y el color de resaltado es un azul claro. Sin embargo, en negro de contraste alto, el color de resaltado es negro. Si asume texto negro, como ha sido el caso en muchas aplicaciones de cuadro antes de Windows 8, y usa el valor predeterminado del sistema para el resaltado, el usuario verá texto negro sobre un fondo negro. En estas situaciones, es necesario comprender cómo usar los temas y las métricas del sistema correctamente para que la aplicación se vea correcta en todos los estilos.

## <a name="manifestations"></a>Manifestaciones

-   El uso de lesa no está habilitado en el área cliente de las aplicaciones que no contienen una Windows 8 &lt; supportedOS &gt; en su manifiesto de aplicación. Por lo tanto, las aplicaciones deben representar el área de cliente mediante la ruta de acceso del código necesaria para representar en modo de contraste alto del tema clásico.
-   La temas no está habilitada en las áreas cliente y no cliente de las aplicaciones en temas de contraste alto. Tampoco está habilitado en aplicaciones que no contienen una etiqueta supportedOS de Windows 8 en su manifiesto de aplicación y que se dibujan en el área no cliente de una ventana mediante la &lt; &gt; API DwnIsCompositionEnabled(). Toda la aplicación se representa en el modo de contraste alto del tema clásico.
-   Las aplicaciones que agregan compatibilidad con Windows 8 en su manifiesto, pero no usan estilos visuales para la representación, es decir, codifican de forma hardcode colores o imágenes en sus aplicaciones, podrían no representarse correctamente en temas de contraste alto. Es posible que el texto sea difícil de leer o que las imágenes no aparezcan como deberían en el modo de contraste alto.

## <a name="mitigation"></a>Mitigación

Se ha escrito que los colores de texto de los temas de contraste alto son compatibles con las directrices de accesibilidad de Microsoft. Se mantiene una relación de contraste alto 14:1 entre primer plano y fondo. Si los colores habilitados de forma predeterminada no son adecuados para un usuario final determinado, se pueden personalizar fácilmente a través de la configuración del panel de control para "Color de ventana" en esos temas de contraste alto.

Estos componentes de la interfaz de usuario son personalizables en temas de contraste alto:

-   Color de fondo de la ventana
-   Color del texto
-   Color de hipervínculos
-   Texto deshabilitado
-   Colores de primer plano y fondo de texto seleccionados
-   Colores de primer plano y fondo del título de la ventana activa
-   Colores de primer plano y fondo del título de la ventana inactiva
-   Colores de primer plano y fondo de los botones

## <a name="solution"></a>Solución

Si se observa un comportamiento inesperado en aplicaciones en temas de contraste alto, una de estas soluciones podría ayudar:

-   **Manifiesto de una aplicación para Windows 8:**

    Las aplicaciones que no contienen la Windows 8 supportedOS en el manifiesto de aplicación tendrán sus áreas cliente &lt; &gt; representados sin un tema. Todas las aplicaciones en cuadro deben contener esta entrada en el manifiesto de aplicación. Agregue el valor 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38 GUID para Windows 8.

-   **Uso de estilos visuales con las URI dibujadas por el propietario:**

    Los controles dibujados por el propietario deben seguir las instrucciones de [MSDN para](/windows/desktop/Controls/using-visual-styles) representar correctamente los elementos y estados de control, incluido el texto. Los desarrolladores no deben confiar en el texto o el color de fondo especificados en un contexto de dispositivo para poder usar métodos que no son UxTheme para la representación. En el caso de que no haya ninguna parte de tema para el [](/windows/desktop/api/winuser/nf-winuser-getsyscolor) control en cuestión, use GetThemeSysColor con la métrica adecuada y dibuje el texto mediante métodos GDI estándar. Si ninguna de las llamadas a UxTheme es adecuada, use el método GetSysColor para obtener la métrica adecuada.

-   **Selección del color del texto:**

    No use un color de texto codificado de forma rígida, incluso si se supone que se ve bien en todos los escenarios comunes. Los temas de envío se crean de una manera que admite una alta visibilidad con las métricas asociadas. Por ejemplo, COLOR HIGHLIGHTTEXT está pensado para usarse con COLOR HIGHLIGHT como fondo y COLOR WINDOWTEXT está pensado para usarse con \_ \_ COLOR WINDOW como \_ \_ fondo. Si hay excepciones a estas asociaciones, trabaje con ellas en las partes del tema y las definiciones de estado, y no en el código. Al diseñar las UI de contraste alto, es fundamental que la interfaz de usuario sea independiente del tema de contraste alto aplicado actualmente, ya que los usuarios de contraste alto pueden personalizar sus colores.

-   **Respuesta al evento \_ ThemeChange de WM:**

    Si la aplicación almacena en caché los colores recuperados del tema o aplica colores de forma no estándar, agregue un controlador de mensajes para WM THEMECHANGE que recalcula los valores de color almacenados y vuelve a dibujar la interfaz de \_ usuario.

-   **Escritura de una aplicación WWA de contraste alto:**

    Las aplicaciones web no tienen acceso a las API de UxTheme, pero deben escribirse con las métricas del sistema actuales como base para la interfaz de usuario. Hay algunos recursos que los desarrolladores de WWA pueden aprovechar para garantizar una aplicación compatible con contraste alto:

    -   La especificación de color CSS de [W3C](https://www.w3.org/TR/css3-color/) especifica la sintaxis para usar métricas del sistema en lugar de colores específicos
    -   Se agrega compatibilidad con consultas multimedia de contraste alto a Internet Explorer 10
    -   Los WWA pueden aprovechar el método IAccessibilityCapabilities::get HighContrast() para comprobar el \_ estado de contraste alto.

    Windows Las aplicaciones de la Tienda no tienen muchos de los mismos problemas con las partes del tema que están presentes en las aplicaciones de Windows clásicas, pero sigue siendo necesario garantizar el cumplimiento de alto contraste. De forma predeterminada, Internet Explorer algunos estilos definidos por el usuario y los reemplaza por valores compatibles con contraste alto. Por ejemplo, se omiten las propiedades CSS background-image, background y color.

    Si no desea que Internet Explorer o ignore las propiedades establecidas y se ha asegura de que la interfaz de usuario es compatible con contraste alto, puede establecer la nueva propiedad CSS M3 –ms-high-contrast: off en un elemento primario.

-   **Escritura de una aplicación de la Tienda Windows contraste alto:**

    Windows La aplicación store debe usar la clase [SystemColors](/dotnet/api/system.windows.systemcolors) para determinar el color adecuado de los elementos de la interfaz de usuario, teniendo en cuenta que determinados colores de métricas del sistema están diseñados para usarse juntos, como SystemColors.WindowColor y SystemColors.WindowTextColor. Esto facilita una experiencia de contraste alto superior.

-   **Detectar correctamente el contraste alto en versiones anteriores de Windows:**

    Las aplicaciones que se ejecutan en versiones anteriores de Windows no tienen acceso a los nuevos temas de contraste alto, incluso si el manifiesto especifica compatibilidad con la versión de Windows en cuestión. Por lo tanto, puede ser necesario insertar rutas de acceso de código adicionales para controlar la representación en el entorno clásico usado en versiones anteriores de Windows. La presencia de contraste alto en este caso debe comprobarse llamando a la función [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con la marca \_ SPI GETHIGHCONTRAST. Esta es la única manera admitida de comprobar la presencia de contraste alto.

## <a name="tests"></a>Pruebas

Al probar una aplicación, asegúrese de que se representa correctamente en todos los temas que incluye Windows 8: Aero, Basic, contraste alto 1, contraste alto 2, contraste alto Black y contraste alto White. Asegúrese de que el texto es claramente visible y fácil de leer en los temas de contraste alto.

## <a name="resources"></a>Recursos

-   [Clases, partes y estados](../controls/aero-style-classes-parts-and-states.md) de estilo Aero (el nuevo tema básico y los temas de contraste alto también usan estos estados)
-   [Partes y estados comunes a todos los estilos visuales](../controls/parts-and-states.md)
-   [Usar estilos visuales con controles personalizados y Owner-Drawn personalizados](../controls/using-visual-styles.md)
-   [Función GetSysColor](/windows/win32/api/winuser/nf-winuser-getsyscolor)
-   [W3C CSS Color Module Level 3](https://www.w3.org/TR/css3-color/)
-   [SystemColors (clase)](/dotnet/api/system.windows.systemcolors?view=netcore-3.1)
-   [Función SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
-   [Accesibilidad de Microsoft](https://www.microsoft.com/enable/)

 

 
