---
description: El SDK Windows proporciona prototipos de función en versiones genéricas, Windows de códigos y Unicode.
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: Convenciones para Prototipos de función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd37171ed4cd1f0f00267b935ec57f17ef2957514b63d770efdc851b9c08bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746145"
---
# <a name="conventions-for-function-prototypes"></a>Convenciones para Prototipos de función

El SDK Windows proporciona prototipos de función en versiones genéricas, [Windows de códigos y](code-pages.md) [Unicode.](unicode.md) Los prototipos se pueden compilar para generar prototipos Windows de página de códigos o prototipos Unicode. Los tres prototipos se de abordan en este tema y se ilustran con ejemplos de código para la [**función SetWindowText.**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)

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



El preprocesador expande la macro en la página Windows de códigos o en el nombre de la función Unicode. La letra "A" (ANSI) o "W" (Unicode) se agrega al final del nombre de función genérica, según corresponda. A continuación, el archivo de encabezado proporciona dos prototipos específicos, uno para Windows páginas de códigos y otro para Unicode, como se muestra en los ejemplos siguientes.


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



Como se explica Windows tipos de datos para [cadenas](windows-data-types-for-strings.md), el prototipo de función genérica usa el tipo de datos LPCTSTR para el parámetro text. Sin embargo, el prototipo de la página de códigos de Windows utiliza el tipo LPCSTR, y el prototipo Unicode utiliza LPCWSTR.

Para todas las características con argumentos de texto, las aplicaciones deben utilizar normalmente los prototipos genéricos de la función. Si una aplicación define "UNICODE" antes de las instrucciones **\# include** para los archivos de encabezado o durante la compilación, las instrucciones se compilarán en funciones Unicode.

> [!Note]  
> Las Windows nuevas aplicaciones deben usar Unicode para evitar las incoherencias de páginas de códigos variadas y facilitar la localización. Deben escribirse con funciones genéricas y deben definir UNICODE para compilar las funciones en funciones Unicode. En los pocos lugares en los que una aplicación debe trabajar con datos de caracteres de 8 bits, puede hacer un uso explícito de las funciones para Windows páginas de códigos.

 

La aplicación debe utilizar siempre un prototipo genérico de la función con cadena y tipos de caracteres genéricos. Todos los nombres de funciones que terminen con una “W” mayúscula utilizan Unicode, es decir, carácter, parámetros anchos. Algunas funciones solo existen en versiones Unicode y solo se pueden usar con los tipos de datos adecuados. Por ejemplo, [**LCIDToLocaleName y**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) solo tienen versiones Unicode.

La sección Requisitos de la documentación de referencia de cada función Unicode y juego de caracteres proporciona información sobre las versiones de función implementadas por sistemas operativos compatibles. Si se incluye una línea que empieza por "Unicode", la función tiene versiones independientes de Unicode Windows de página de códigos.

> [!Note]  
> Cuando una función tiene un parámetro de longitud para una cadena de caracteres, la longitud debe documentarse como un recuento de valores TCHAR en la cadena. Este tipo de datos hace referencia a bytes Windows de página de códigos de la función o palabras de 16 bits para versiones Unicode. Sin embargo, las funciones que requieren o devuelven punteros a bloques de memoria sin tipo, como la [**función GlobalAlloc,**](/windows/win32/api/winbase/nf-winbase-globalalloc) suelen tener un tamaño en bytes, independientemente del prototipo que se utilice. Si la asignación de memoria sin tipo es para una cadena, la aplicación debe multiplicar el número de caracteres por sizeof(TCHAR). Para obtener información adicional, vea [Usar tipos de datos genéricos.](using-generic-data-types.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Unicode en la API de Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
