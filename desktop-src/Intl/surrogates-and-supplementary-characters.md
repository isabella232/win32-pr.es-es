---
description: Suplentes y caracteres suplementarios
ms.assetid: 0dea39e2-a2b4-47fc-b44a-56af8ba1e346
title: Suplentes y caracteres suplementarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8d6b738955c8b8de4f6cb0ae43c78f86752a928
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171877"
---
# <a name="surrogates-and-supplementary-characters"></a>Suplentes y caracteres suplementarios

Windows aplicaciones suelen usar UTF-16 para representar datos [de caracteres Unicode.](unicode.md) El uso de 16 bits permite la representación directa de 65 536 caracteres únicos, pero este plano multilingüe básico (BMP) no es suficiente para cubrir todos los símbolos usados en lenguajes humanos. La versión 4.1 de Unicode incluye más de 97 000 caracteres, con más de 70 000 caracteres solo para chino.

El estándar Unicode ha establecido 16 "planos" adicionales de caracteres, cada uno del mismo tamaño que bmp. Naturalmente, la mayoría de los puntos de código más allá del BMP aún no tienen caracteres asignados, pero la definición de los planos ofrece a Unicode la posibilidad de definir 1 114 112 caracteres (es decir, 2⁶ 17 caracteres) dentro del intervalo de puntos de código \* U+0000 a U+10FFFF. Para que UTF-16 represente este conjunto de caracteres más grande, el estándar Unicode define "caracteres adicionales".

## <a name="about-supplementary-characters"></a>Acerca de los caracteres adicionales

Un carácter complementario es un carácter situado más allá del BMP y un "suplente" es un valor de código UTF-16. Para UTF-16, se requiere un "par suplente" para representar un único carácter complementario. El primer suplente (alto) es un valor de código de 16 bits en el intervalo U+D800 a U+DBFF. El segundo suplente (bajo) es un valor de código de 16 bits en el intervalo U+DC00 a U+DFFF. Mediante el mecanismo suplente, UTF-16 puede admitir todos los 1114 112 posibles caracteres Unicode. Para obtener más información sobre los caracteres adicionales, suplentes y pares suplentes, consulte [El estándar Unicode](https://www.unicode.org/standard/standard.html).

> [!Note]  
> Windows 2000 presenta compatibilidad con la entrada básica, la salida y la ordenación simple de caracteres adicionales. Sin embargo, no todos los componentes del sistema son compatibles con caracteres adicionales.

 

El sistema operativo admite caracteres adicionales de las maneras siguientes:

-   El formato 12 de la tabla cmap de fuente OpenType admite directamente el código de caracteres de 4 bytes. Para obtener más información, vea la [especificación de fuente OpenType](/typography/opentype/spec/).
-   Windows admite editores de métodos de entrada [(IME) habilitados para suplentes.](../dxtecharts/installing-and-using-input-method-editors.md)
-   La [Windows GDI](../gdi/windows-gdi.md) API admite el formato 12 tablas de cmap en fuentes para que los suplentes se puedan mostrar correctamente.
-   [Uniscribe](uniscribe.md) API admite caracteres adicionales.
-   [Windows controles](../controls/window-controls.md), [incluidos Editar](../controls/edit-controls.md) y [Editar](../controls/rich-edit-controls.md)enriquecido, admiten caracteres adicionales.
-   El motor HTML admite páginas HTML que incluyen caracteres adicionales para mostrar, editar (a través de Outlook Express) y enviar formularios.
-   La tabla de ordenación del sistema operativo admite caracteres adicionales.

## <a name="general-guidelines-for-software-development-using-supplementary-characters"></a>Directrices generales para el desarrollo de software mediante caracteres adicionales

UTF-16 controla los caracteres adicionales como pares suplentes. El sistema operativo procesa un par suplente de forma similar a la forma en que procesa las [marcas de no almacenamiento.](using-nonspacing-characters-and-diacritics.md) En el momento de la presentación, el par suplente se muestra como un glifo por medio de Uniscribe, según lo prescrito por el estándar Unicode.

Windows Vista presenta tres nuevas macros para ayudar a identificar los suplentes y los pares suplentes en cadenas UTF-16. Estos son [**HIGH \_ \_ SURROGATE**](/windows/win32/api/Winnls/nf-winnls-is_high_surrogate), [**IS LOW \_ \_ SURROGATE**](/windows/win32/api/Winnls/nf-winnls-is_low_surrogate)y [**IS \_ SURROGATE \_ PAIR**](/windows/win32/api/Winnls/nf-winnls-is_surrogate_pair).

Las aplicaciones admiten automáticamente caracteres adicionales si admiten Unicode y usan controles del sistema y funciones de API estándar, como [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) y [**DrawText.**](/windows/win32/api/winuser/nf-winuser-drawtext) Por lo tanto, si la aplicación usa controles del sistema estándar o usa llamadas generales [**extTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)-type para mostrar, los caracteres adicionales deben funcionar sin ninguna codificación especial.

Las aplicaciones que implementan su propia compatibilidad de edición mediante el trabajo de posiciones de glifo de una manera personalizada pueden usar Uniscribe para todo el procesamiento de texto. Uniscribe tiene funciones independientes para tratar con el procesamiento de scripts complejos, como la presentación de texto, las pruebas de acceso y el movimiento del cursor. Una aplicación debe llamar a las funciones de Uniscribe específicamente para obtener estas características avanzadas. Tenga en cuenta que las aplicaciones que usan las funciones de Uniscribe son totalmente multilingües, pero esto impone una penalización del rendimiento. Por lo tanto, algunas aplicaciones deben realizar su propio procesamiento de caracteres adicionales.

Dado que el mecanismo suplente para representar caracteres adicionales está bien definido, la aplicación puede incluir código para controlar el procesamiento de texto suplente UTF-16. Cuando la aplicación encuentra un valor UTF-16 separado del intervalo suplente reservado inferior (un suplente bajo) o del intervalo suplente reservado superior (un suplente alto), el valor debe ser la mitad de un par suplente. Por lo tanto, la aplicación puede detectar un par suplente mediante la comprobación de intervalo simple. Si encuentra un valor UTF-16 en el intervalo inferior o superior, debe realizar un seguimiento hacia atrás o hacia delante de un ancho de 16 bits para obtener el resto del carácter. Al escribir la aplicación, tenga en cuenta que [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta) y [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva) se mueven por puntos de código de 16 bits, no por pares suplentes.

> [!Note]  
> Los puntos de código suplente independientes tienen un suplente alto sin un suplente bajo adyacente o viceversa. Estos puntos de código no son válidos y no se admiten. Su comportamiento es indefinido.

 

Si va a desarrollar una fuente o un proveedor de IME, tenga en cuenta que los sistemas operativos XP anteriores a la Windows deshabilitan la compatibilidad con caracteres adicionales de forma predeterminada. Windows XP y versiones posteriores habilitan caracteres adicionales de forma predeterminada. Si proporciona una fuente y un paquete IME que requiere caracteres adicionales, la aplicación debe establecer los siguientes valores del Registro:


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

 

 
