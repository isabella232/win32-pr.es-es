---
description: El Windows SDK proporciona prototipos de función en las versiones genérica, de la página de códigos de Windows y Unicode.
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: Convenciones para Prototipos de función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951860f72870dcbbcb88572f379e39dc843ecb11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910122"
---
# <a name="conventions-for-function-prototypes"></a>Convenciones para Prototipos de función

El Windows SDK proporciona prototipos de función en las versiones genérica, de la [Página de códigos de Windows](code-pages.md)y [Unicode](unicode.md) . Los prototipos se pueden compilar para generar prototipos de páginas de códigos de Windows o prototipos Unicode. Los tres prototipos se describen en este tema y se muestran en los ejemplos de código para la función [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) .

A continuación se muestra un ejemplo de un prototipo genérico:


```C++
BOOL SetWindowText(
  HWND hwnd,
  LPCTSTR lpText
);
```



El archivo de encabezado proporciona el nombre de función genérico implementado como una macro.


```C++
#ifdef UNICODE
#define SetWindowText SetWindowTextW
#else
#define SetWindowText SetWindowTextA
#endif // !UNICODE
```



El preprocesador expande la macro en la página de códigos de Windows o en el nombre de la función Unicode. La letra "A" (ANSI) o "W" (Unicode) se agrega al final del nombre de la función genérica, según corresponda. A continuación, el archivo de encabezado proporciona dos prototipos específicos, uno para las páginas de códigos de Windows y otro para Unicode, tal y como se muestra en los ejemplos siguientes.


```C++
BOOL SetWindowTextA(
  HWND hwnd,
  LPCSTR lpText
);
```




```C++
BOOL SetWindowTextW(
  HWND hwnd,
  LPCWSTR lpText
);
```



Como se explica en [tipos de datos de Windows para cadenas](windows-data-types-for-strings.md), el prototipo de función genérica usa el tipo de datos LPCTSTR para el parámetro text. Sin embargo, el prototipo de la página de códigos de Windows utiliza el tipo LPCSTR, y el prototipo Unicode utiliza LPCWSTR.

Para todas las características con argumentos de texto, las aplicaciones deben utilizar normalmente los prototipos genéricos de la función. Si una aplicación define "Unicode" antes de las instrucciones **\# include** para los archivos de encabezado o durante la compilación, las instrucciones se compilarán en funciones Unicode.

> [!Note]  
> Las nuevas aplicaciones de Windows deben usar Unicode para evitar las incoherencias de las distintas páginas de códigos y para facilitar la localización. Deben escribirse con funciones genéricas y deben definir Unicode para compilar las funciones en funciones Unicode. En los pocos lugares donde una aplicación debe trabajar con datos de caracteres de 8 bits, puede hacer el uso explícito de las funciones para las páginas de códigos de Windows.

 

La aplicación debe utilizar siempre un prototipo genérico de la función con cadena y tipos de caracteres genéricos. Todos los nombres de funciones que terminen con una “W” mayúscula utilizan Unicode, es decir, carácter, parámetros anchos. Algunas funciones solo existen en las versiones Unicode y solo se pueden usar con los tipos de datos adecuados. Por ejemplo, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) y [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) solo tienen versiones Unicode.

La sección de requisitos de la documentación de referencia de cada función de Unicode y de juego de caracteres proporciona información sobre las versiones de funciones implementadas por los sistemas operativos compatibles. Si se incluye una línea que empieza por "Unicode", la función tiene versiones independientes de la página de códigos de Windows y Unicode.

> [!Note]  
> Cuando una función tiene un parámetro de longitud para una cadena de caracteres, la longitud debe documentarse como un recuento de los valores TCHAR de la cadena. Este tipo de datos hace referencia a los bytes de las versiones de la página de códigos de Windows de la función o de las palabras de 16 bits para las versiones Unicode. Sin embargo, las funciones que requieren o devuelven punteros a bloques de memoria sin tipo, como la función [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) , generalmente toman un tamaño en bytes, independientemente del prototipo que se use. Si la asignación de memoria sin tipo es para una cadena, la aplicación debe multiplicar el número de caracteres por sizeof (TCHAR). Para obtener más información, vea [usar tipos de datos genéricos](using-generic-data-types.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Unicode en la API de Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
