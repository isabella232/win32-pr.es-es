---
title: Trabajo con cadenas
description: .
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c74530a1acd0eb94f0d88662924203a8c58116
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149228"
---
# <a name="working-with-strings"></a>Trabajo con cadenas

Windows admite de forma nativa cadenas Unicode para elementos de interfaz de usuario, nombres de archivo, etc. Unicode es la codificación de caracteres preferida, ya que admite todos los juegos de caracteres e idiomas. Windows representa caracteres Unicode mediante la codificación UTF-16, en la que cada carácter se codifica como un valor de 16 bits. Los caracteres UTF-16 se denominan caracteres *anchos* para distinguirlos de caracteres ANSI de 8 bits. El compilador Visual C++ admite el tipo de datos integrado **WCHAR \_ t** para caracteres anchos. El archivo de encabezado Winnt. h también define el siguiente **typedef**.


```C++
typedef wchar_t WCHAR;
```



Verá ambas versiones en el código de ejemplo de MSDN. Para declarar un literal de carácter ancho o un literal de cadena de caracteres anchos, coloque **L** delante del literal.


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



Estas son algunas de las definiciones de tipo relacionadas con cadenas que verá:



| Definición de tipo                   | Definición       |
|---------------------------|------------------|
| **CHAR**                  | `char`           |
| **PSTR** o **LPSTR**     | `char*`          |
| **PCSTR** o **LPCSTR**   | `const char*`    |
| **PWSTR** o **LPWStr**   | `wchar_t*`       |
| **PCWSTR** o **LPCWSTR** | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a>Funciones Unicode y ANSI

Cuando Microsoft presentó la compatibilidad con Unicode en Windows, facilitó la transición proporcionando dos conjuntos paralelos de API: uno para las cadenas ANSI y el otro para las cadenas Unicode. Por ejemplo, hay dos funciones para establecer el texto de la barra de título de una ventana:

-   **SetWindowTextA** toma una cadena ANSI.
-   **SetWindowTextW** toma una cadena Unicode.

Internamente, la versión ANSI traduce la cadena a Unicode. Los encabezados de Windows también definen una macro que se resuelve en la versión Unicode cuando se define el símbolo de preprocesador `UNICODE` o la versión ANSI, en caso contrario.


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



En MSDN, la función se documenta con el nombre [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), aunque es en realidad el nombre de la macro, no el nombre de función real.

Las aplicaciones nuevas siempre deben llamar a las versiones Unicode. Muchos idiomas internacionales requieren Unicode. Si usa cadenas ANSI, no será posible localizar la aplicación. Las versiones ANSI también son menos eficaces, ya que el sistema operativo debe convertir las cadenas ANSI en Unicode en tiempo de ejecución. En función de sus preferencias, puede llamar a las funciones Unicode explícitamente, como **SetWindowTextW**, o usar las macros. El código de ejemplo de MSDN normalmente llama a las macros, pero las dos formas son exactamente equivalentes. La mayoría de las API más recientes de Windows tienen solo una versión Unicode, sin ninguna versión ANSI correspondiente.

## <a name="tchars"></a>TCHARs

De vuelta cuando las aplicaciones necesarias para admitir tanto Windows NT como Windows 95, Windows 98 y Windows me, resultaba útil compilar el mismo código para cadenas ANSI o Unicode, en función de la plataforma de destino. Para este fin, el Windows SDK proporciona macros que asignan cadenas a Unicode o ANSI, dependiendo de la plataforma.



| Macro     | Unicode   | ANSI   |
|-----------|-----------|--------|
| TCHAR     | `wchar_t` | `char` |
| TEXTO ("x") | `L"x"`    | `"x"`  |



 

Por ejemplo, el código siguiente:


```C++
SetWindowText(TEXT("My Application"));
```



se resuelve como uno de los siguientes:


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



Las macros **Text** y **TCHAR** son menos útiles hoy en día, ya que todas las aplicaciones deben usar Unicode. Sin embargo, es posible que los vea en código anterior y en algunos de los ejemplos de código de MSDN.

Los encabezados de las bibliotecas en tiempo de ejecución de C de Microsoft definen un conjunto similar de macros. Por ejemplo, **\_ tcslen** se resuelve como **strlen** si `_UNICODE` no está definido; de lo contrario, se resuelve como **wcslen**, que es la versión con caracteres anchos de **strlen**.


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



Tenga cuidado: algunos encabezados utilizan el símbolo de preprocesador `UNICODE` y otros usan `_UNICODE` con un prefijo de subrayado. Defina siempre ambos símbolos. Visual C++ los establece de forma predeterminada al crear un nuevo proyecto.

## <a name="next"></a>Siguientes

[¿Qué es una ventana?](what-is-a-window-.md)

 

 