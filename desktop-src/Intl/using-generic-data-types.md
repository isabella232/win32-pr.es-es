---
description: Si usa tipos de datos genéricos en el código, se puede compilar para Unicode simplemente mediante una directiva de preprocesador para definir &\# 0034; UNICODE&\# 0034; antes de las \# instrucciones include para los archivos de encabezado.
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: Usar tipos de datos genéricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2604f87b12e86076bed47f509c6398fa8482b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254865"
---
# <a name="using-generic-data-types"></a>Usar tipos de datos genéricos

Si usa tipos de datos genéricos en el código, se puede compilar para [Unicode](unicode.md) simplemente mediante una directiva de preprocesador para definir "UNICODE" antes de las instrucciones **\# include** para los archivos de encabezado. Para compilar el código de [Windows (ANSI)](code-pages.md), omita la definición de "UNICODE". Las Windows nuevas deben usar Unicode para evitar las incoherencias de páginas de códigos variadas y simplificar la localización.

Para crear código fuente que se pueda compilar para usar caracteres Unicode y cadenas o para usar caracteres y cadenas de Windows páginas de códigos:

1.  Use tipos de datos genéricos, como TCHAR, LPTSTR y LPTCH, para todos los tipos de caracteres y cadenas usados para el texto. Para obtener más información sobre los tipos [genéricos, vea Windows tipos de datos para cadenas](windows-data-types-for-strings.md).
2.  Asegúrese de que los punteros a búferes de datos que no son de texto o matrices de bytes binarios están codificados con tipos de datos como LPBYTE o LPWORD, en lugar del tipo LPTSTR o LPTCH.
3.  Declare punteros de tipo indeterminado explícitamente como punteros void mediante LPVOID según corresponda.
4.  Haga que el tipo aritmético de puntero sea independiente. El uso de unidades de tamaño TCHAR produce variables que son de 2 bytes si se define UNICODE y de 1 byte si unicode no está definido. El uso de aritmética de puntero siempre devuelve el número de elementos indicados por el puntero, independientemente de si los elementos tienen un tamaño de 1 o 2 bytes. La expresión siguiente siempre recupera el número de elementos, independientemente de si se define UNICODE.

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    La expresión siguiente determina el número de bytes usados.

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    No es necesario cambiar una instrucción como la siguiente, porque el incremento de puntero apunta al siguiente elemento de carácter.

    ```C++
    chNext = *++lpText;
    ```

    

5.  Reemplace las cadenas literales y las constantes de caracteres de manifiesto por macros. Cambie expresiones como la siguiente.

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    Use la [**macro TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) como se muestra a continuación en esta expresión.

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    La [**macro TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) hace que las cadenas se evalúen como L"string" cuando se define UNICODE y, en caso contrario, como "cadena". Para facilitar la administración, mueva las cadenas literales a los recursos, especialmente si contienen caracteres fuera del intervalo ASCII (0x00 a 0x7F) o se exponen en la interfaz de usuario. Para admitir la localización de la aplicación para distintos idiomas nacionales, es muy importante que todas las cadenas de interfaz de usuario se puedan encontrar en recursos localizables.

6.  Use las versiones genéricas de las Windows funciones. Para obtener más información, vea [Convenciones para prototipos de función.](conventions-for-function-prototypes.md)
7.  Use las versiones genéricas de las funciones de cadena de la biblioteca estándar de C y recuerde definir "UNICODE" así como "UNICODE", como se describe \_ en Funciones estándar de [C](standard-c-functions.md).
8.  Si va a adaptar una aplicación escrita originalmente para Windows páginas de códigos, recuerde cambiar cualquier código que se base en 255 como el valor más grande para un carácter.

Al compilar código que ha escrito como se ha descrito anteriormente, el compilador puede crear versiones de página de códigos Unicode y Windows de la aplicación desde el mismo origen. En función de las definiciones de UNICODE, las funciones genéricas se resuelven para generar los mismos archivos binarios que si escribiera código exclusivamente para Unicode o exclusivamente para Windows páginas de códigos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Unicode y juegos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



