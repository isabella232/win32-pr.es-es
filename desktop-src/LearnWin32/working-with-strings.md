---
title: Trabajo con cadenas
description: Trabajo con cadenas
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4661c6b07a267d90e0fca05d04354c018be04527
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110973"
---
# <a name="working-with-strings"></a>Trabajo con cadenas

Windows admite de forma nativa cadenas Unicode para elementos de interfaz de usuario, nombres de archivo, etc. Unicode es la codificación de caracteres preferida, ya que admite todos los idiomas y conjuntos de caracteres. Windows representa caracteres Unicode mediante la codificación UTF-16, en la que cada carácter se codifica como un valor de 16 bits. Los caracteres UTF-16 se *denominan caracteres anchos,* para distinguirlos de los caracteres ANSI de 8 bits. El Visual C++ admite el tipo de datos **integrado wchar \_ t para** caracteres anchos. El archivo de encabezado WinNT.h también define la definición **de tipo siguiente.**


```C++
typedef wchar_t WCHAR;
```



Verá ambas versiones en código de ejemplo de MSDN. Para declarar un literal de caracteres anchos o un literal de cadena de caracteres anchos, coloque **L** delante del literal.


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



Estas son algunas otras definiciones de tipos relacionadas con cadenas que verá:



| Definición de tipo                   | Definición       |
|---------------------------|------------------|
| **CHAR**                  | `char`           |
| **PSTR** o **LPSTR**     | `char*`          |
| **PCSTR** o **LPCSTR**   | `const char*`    |
| **PWSTR** o **LPWSTR**   | `wchar_t*`       |
| **PCWSTR** o **LPCWSTR** | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a>Funciones Unicode y ANSI

Cuando Microsoft introdujo la compatibilidad con Unicode en Windows, se facilitaba la transición proporcionando dos conjuntos paralelos de API, uno para cadenas ANSI y otro para cadenas Unicode. Por ejemplo, hay dos funciones para establecer el texto de la barra de título de una ventana:

-   **SetWindowTextA toma** una cadena ANSI.
-   **SetWindowTextW toma** una cadena Unicode.

Internamente, la versión ANSI traduce la cadena a Unicode. Los encabezados de Windows también definen una macro que se resuelve en la versión Unicode cuando se define el símbolo de preprocesador o la versión ANSI en caso `UNICODE` contrario.


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



En MSDN, la función se documenta con el nombre [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), aunque ese es realmente el nombre de la macro, no el nombre real de la función.

Las nuevas aplicaciones siempre deben llamar a las versiones Unicode. Muchos idiomas del mundo requieren Unicode. Si usa cadenas ANSI, será imposible encontrar la aplicación. Las versiones ANSI también son menos eficaces, ya que el sistema operativo debe convertir las cadenas ANSI a Unicode en tiempo de ejecución. Según sus preferencias, puede llamar explícitamente a las funciones Unicode, como **SetWindowTextW,** o usar las macros . El código de ejemplo de MSDN normalmente llama a las macros, pero las dos formas son exactamente equivalentes. La mayoría de las API más recientes de Windows solo tienen una versión Unicode, sin la versión ANSI correspondiente.

## <a name="tchars"></a>TCHAR

Cuando las aplicaciones necesitaban admitir Windows NT, así como Windows 95, Windows 98 y Windows Me, resultaba útil compilar el mismo código para cadenas ANSI o Unicode, en función de la plataforma de destino. Con este fin, el Windows SDK proporciona macros que asignan cadenas a Unicode o ANSI, en función de la plataforma.



| Macro     | Unicode   | ANSI   |
|-----------|-----------|--------|
| TCHAR     | `wchar_t` | `char` |
| TEXT("x") | `L"x"`    | `"x"`  |



 

Por ejemplo, el código siguiente:


```C++
SetWindowText(TEXT("My Application"));
```



se resuelve en uno de los siguientes elementos:


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



Las **macros TEXT** y **TCHAR** son menos útiles hoy en día, porque todas las aplicaciones deben usar Unicode. Sin embargo, es posible que los vea en código anterior y en algunos de los ejemplos de código de MSDN.

Los encabezados de las bibliotecas en tiempo de ejecución de Microsoft C definen un conjunto similar de macros. Por ejemplo, **\_ tcslen** se resuelve como **strlen** si no está definido; de lo contrario, se resuelve como wcslen , que es la versión de caracteres `_UNICODE` anchos **de strlen**. 


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



Tenga cuidado: algunos encabezados usan el símbolo de preprocesador `UNICODE` y otros usan con un prefijo de `_UNICODE` subrayado. Defina siempre ambos símbolos. Visual C++ establece ambos de forma predeterminada al crear un proyecto.

## <a name="next"></a>Siguientes

[¿Qué es una ventana?](what-is-a-window-.md)

 

 
