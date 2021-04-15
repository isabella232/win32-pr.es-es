---
description: Si usa tipos de datos genéricos en el código, se puede compilar para Unicode simplemente mediante una directiva de preprocesador para definir &\# 0034; Unicode&\# 0034; antes de las \# instrucciones include para los archivos de encabezado.
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: Usar tipos de datos genéricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2604f87b12e86076bed47f509c6398fa8482b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688699"
---
# <a name="using-generic-data-types"></a>Usar tipos de datos genéricos

Si usa tipos de datos genéricos en el código, se puede compilar para [Unicode](unicode.md) simplemente mediante una directiva de preprocesador para definir "Unicode" antes de las instrucciones **\# include** para los archivos de encabezado. Para compilar las páginas de códigos de código para [Windows (ANSI)](code-pages.md), omita la definición de "Unicode". Las nuevas aplicaciones de Windows deben usar Unicode para evitar las incoherencias de las páginas de códigos variadas y simplificar la localización.

Para crear código fuente que se puede compilar para utilizar caracteres Unicode y cadenas, o para usar caracteres y cadenas de páginas de códigos de Windows:

1.  Utilice tipos de datos genéricos, como TCHAR, LPTSTR y LPTCH, para todos los tipos de caracteres y cadenas que se usan para el texto. Para obtener más información sobre los tipos genéricos, vea [tipos de datos de Windows para cadenas](windows-data-types-for-strings.md).
2.  Asegúrese de que los punteros a los búferes de datos que no son de texto o a las matrices de bytes binarias están codificados con tipos de datos como LPBYTE o LPWORD, en lugar del tipo LPTSTR o LPTCH.
3.  Declare explícitamente punteros de tipo indeterminado como punteros void mediante LPVOID, según corresponda.
4.  Hacer independiente del tipo aritmético del puntero. El uso de unidades de tamaño TCHAR produce variables de 2 bytes si se define Unicode y 1 byte si no se ha definido Unicode. El uso de la aritmética de puntero siempre devuelve el número de elementos indicado por el puntero, tanto si los elementos tienen un tamaño de 1 o 2 bytes. La siguiente expresión siempre recupera el número de elementos, independientemente de si se ha definido Unicode.

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    La siguiente expresión determina el número de bytes utilizados.

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    No es necesario cambiar una instrucción como la siguiente, porque el incremento del puntero apunta al siguiente elemento de carácter.

    ```C++
    chNext = *++lpText;
    ```

    

5.  Reemplazar cadenas literales y constantes de caracteres de manifiesto con macros. Cambie las expresiones como las siguientes.

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    Use la macro [**Text**](/windows/desktop/api/Winnt/nf-winnt-text) como se indica a continuación en esta expresión.

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    La macro [**Text**](/windows/desktop/api/Winnt/nf-winnt-text) hace que las cadenas se evalúen como L "cadena" cuando se define Unicode, y como "cadena" en caso contrario. Para facilitar la administración, mueva las cadenas literales a los recursos, especialmente si contienen caracteres que están fuera del intervalo ASCII (de 0x00 a 0x7F) o se exponen en la interfaz de usuario. Para admitir la localización de la aplicación para distintos idiomas nacionales, es muy importante que todas las cadenas de la interfaz de usuario estén en recursos localizables.

6.  Use las versiones genéricas de las funciones de Windows. Para obtener más información, vea [convenciones de los prototipos de función](conventions-for-function-prototypes.md).
7.  Use las versiones genéricas de las funciones de cadena de la biblioteca estándar de C y recuerde definir " \_ Unicode", así como "Unicode", como se describe en [funciones estándar de C](standard-c-functions.md).
8.  Si va a adaptar una aplicación escrita originalmente para páginas de códigos de Windows, Recuerde cambiar cualquier código que se base en 255 como el valor más grande de un carácter.

Al compilar el código que ha escrito tal y como se ha descrito anteriormente, el compilador puede crear versiones de páginas de códigos de Windows y Unicode de la aplicación desde el mismo origen. En función de las definiciones de Unicode, las funciones genéricas se resuelven para generar los mismos archivos binarios que si se escribiera código exclusivamente para Unicode o exclusivamente para páginas de códigos de Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Unicode y juegos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



