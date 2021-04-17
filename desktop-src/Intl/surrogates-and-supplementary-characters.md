---
description: Suplentes y caracteres suplementarios
ms.assetid: 0dea39e2-a2b4-47fc-b44a-56af8ba1e346
title: Suplentes y caracteres suplementarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8d6b738955c8b8de4f6cb0ae43c78f86752a928
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652413"
---
# <a name="surrogates-and-supplementary-characters"></a>Suplentes y caracteres suplementarios

Normalmente, las aplicaciones Windows usan UTF-16 para representar los datos de caracteres [Unicode](unicode.md) . El uso de 16 bits permite la representación directa de 65.536 caracteres únicos, pero este plano básico multilingüe (BMP) no es lo suficientemente grande como para abarcar todos los símbolos que se usan en los idiomas humanos. La versión 4,1 de Unicode incluye más de 97.000 caracteres, con más de 70.000 caracteres únicamente para chino.

El estándar Unicode ha establecido 16 "planos" adicionales de caracteres, cada uno de los cuales tiene el mismo tamaño que el BMP. Naturalmente, la mayoría de los puntos de código más allá del BMP todavía no tienen caracteres asignados, pero la definición de los planos permite que Unicode sea el potencial para definir 1.114.112 caracteres (es decir, 2 ¹ ⁶ \* 17 caracteres) dentro del intervalo de puntos de código de u + 0000 a u + 10FFFF. En el caso de UTF-16 para representar este conjunto de caracteres más grande, el estándar Unicode define "caracteres adicionales".

## <a name="about-supplementary-characters"></a>Acerca de los caracteres adicionales

Un carácter suplementario es un carácter que se encuentra más allá del BMP y un "suplente" es un valor de código UTF-16. Para UTF-16, se requiere un "par suplente" para representar un único carácter suplementario. El primer suplente (alto) es un valor de código de 16 bits comprendido entre U + D800 y U + DBFF. El segundo suplente (bajo) es un valor de código de 16 bits en el intervalo de U + DC00 a U + DFFF. Mediante el mecanismo suplente, UTF-16 puede admitir todos los caracteres Unicode posibles 1.114.112. Para obtener más información sobre los caracteres adicionales, los suplentes y los pares suplentes, consulte [el estándar Unicode](https://www.unicode.org/standard/standard.html).

> [!Note]  
> Windows 2000 incluye compatibilidad con la entrada básica, la salida y la ordenación simple de caracteres adicionales. Sin embargo, no todos los componentes del sistema son compatibles con los caracteres adicionales.

 

El sistema operativo admite caracteres adicionales de las siguientes maneras:

-   El formato 12 de la tabla CMAP de fuente OpenType es compatible directamente con el código de caracteres de 4 bytes. Para obtener más información, vea la [especificación de fuente OpenType](/typography/opentype/spec/).
-   Windows admite [editores de métodos de entrada (IME)](../dxtecharts/installing-and-using-input-method-editors.md)habilitados para suplentes.
-   La API de [Windows GDI](../gdi/windows-gdi.md) admite el formato 12 tablas de CMAP en fuentes para que los suplentes se puedan mostrar correctamente.
-   La API de [Uniscribe](uniscribe.md) admite caracteres adicionales.
-   [Los controles de Windows](../controls/window-controls.md), incluidos [edición](../controls/edit-controls.md) y [edición enriquecida](../controls/rich-edit-controls.md), admiten caracteres complementarios.
-   El motor HTML admite páginas HTML que incluyen caracteres adicionales para mostrar, editar (a través de Outlook Express) y envío de formularios.
-   La tabla de ordenación del sistema operativo admite caracteres adicionales.

## <a name="general-guidelines-for-software-development-using-supplementary-characters"></a>Directrices generales para el desarrollo de software mediante caracteres adicionales

UTF-16 controla los caracteres complementarios como pares suplentes. El sistema operativo procesa un par suplente de forma similar al modo en que procesa las marcas de no [espacio](using-nonspacing-characters-and-diacritics.md). En el momento de la presentación, el par suplente se muestra como un glifo por medio de Uniscribe, como se indica en el estándar Unicode.

Windows Vista presenta tres nuevas macros para ayudar a identificar los suplentes y los pares suplentes en cadenas UTF-16. Se [**trata de \_ un \_ suplente alto**](/windows/win32/api/Winnls/nf-winnls-is_high_surrogate), [**es un \_ \_ suplente bajo**](/windows/win32/api/Winnls/nf-winnls-is_low_surrogate)y [**es un \_ \_ par suplente**](/windows/win32/api/Winnls/nf-winnls-is_surrogate_pair).

Las aplicaciones admiten automáticamente los caracteres adicionales si admiten Unicode y usan controles del sistema y funciones de la API estándar, como [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) y [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). Por lo tanto, si la aplicación usa controles del sistema estándar o utiliza llamadas generales de tipo [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)para mostrar, los caracteres adicionales deben funcionar sin ninguna codificación especial.

Las aplicaciones que implementan su propia compatibilidad de edición mediante la utilización de las posiciones del glifo de una manera personalizada pueden utilizar unipose para todo el procesamiento de texto. Uniscribe tiene funciones independientes para tratar con el procesamiento de scripts complejos, como la presentación de texto, la prueba de posicionamiento y el movimiento del cursor. Una aplicación debe llamar a las funciones de Uniscribe específicamente para obtener estas características avanzadas. Tenga en cuenta que las aplicaciones que usan las funciones de Uniscribe son totalmente multilingües, pero esto impone una reducción del rendimiento. Por lo tanto, algunas aplicaciones deben realizar su propio procesamiento de caracteres adicionales.

Dado que el mecanismo suplente para representar los caracteres complementarios está bien definido, la aplicación puede incluir código para controlar el procesamiento de texto suplente UTF-16. Cuando la aplicación encuentra un valor UTF-16 separado desde el intervalo suplente menor reservado (un suplente bajo) o el intervalo suplente superior (un suplente alto), el valor debe ser una mitad de un par suplente. Por lo tanto, la aplicación puede detectar un par suplente realizando una comprobación de intervalo simple. Si encuentra un valor UTF-16 en el intervalo inferior o superior, debe realizar un seguimiento del ancho de bit de 1 16 hacia atrás o hacia delante para obtener el resto del carácter. Al escribir la aplicación, tenga en cuenta que [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta) y [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva) se mueven por puntos de código de 16 bits, no por pares suplentes.

> [!Note]  
> Los puntos de código suplente independientes tienen un suplente alto sin un suplente bajo adyacente, o viceversa. Estos puntos de código no son válidos y no se admiten. Su comportamiento es indefinido.

 

Si está desarrollando una fuente o un proveedor de IME, tenga en cuenta que los sistemas operativos anteriores a Windows XP deshabilitan la compatibilidad con caracteres adicionales de forma predeterminada. Windows XP y versiones posteriores habilitan los caracteres complementarios de forma predeterminada. Si proporciona un paquete de fuentes y IME que requiere caracteres adicionales, la aplicación debe establecer los siguientes valores del registro:


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\LanguagePack]
SURROGATE=(REG_DWORD)0x00000002

[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\International\Scripts\42]
IEFixedFontName=[Surrogate Font Face Name]
IEPropFontName=[Surrogate Font Face Name]
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Juegos de caracteres](character-sets.md)
</dt> </dl>

 

 
