---
description: La mayoría de las operaciones de cadena pueden usar la misma lógica para Unicode y Windows páginas de códigos.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Tipos de datos de Windows para cadenas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2bef3dc98b7b8649b6cb0fc5bd9450c6f22c8b2bb6e3345790dab0dd24587f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146818"
---
# <a name="windows-data-types-for-strings"></a>Tipos de datos de Windows para cadenas

La mayoría de las operaciones de cadena pueden usar la misma lógica [para Unicode](unicode.md) y para Windows páginas [de códigos](code-pages.md). La única diferencia es que la unidad básica de operación es un carácter de 16 bits (también conocido como carácter ancho) para Unicode y un carácter de 8 bits para Windows páginas de códigos. Los Windows de encabezado proporcionan varias definiciones de tipo que hacen que sea fácil crear orígenes que se puedan compilar para Unicode o para Windows páginas de códigos.

Windows admite tres conjuntos de tipos de datos de caracteres y cadenas: un conjunto de definiciones de tipos genéricos que se pueden compilar para páginas de códigos Unicode o Windows y dos conjuntos de definiciones de tipos específicas. Un conjunto de definiciones de tipos específicos es para su uso con Unicode y el otro es para su uso Windows páginas de códigos.

Una aplicación que usa tipos de datos genéricos se puede compilar para Unicode simplemente definiendo "UNICODE" antes de las instrucciones **\# include** para los archivos de encabezado o durante la compilación. Las Windows nuevas deben usar Unicode para evitar las incoherencias de páginas de códigos variadas y simplificar la localización. Deben escribirse con tipos de datos genéricos y deben definir "UNICODE" para compilar estos tipos en tipos Unicode. En los pocos lugares donde una aplicación debe funcionar con datos de caracteres de 8 bits, puede hacer un uso explícito de los tipos para Windows páginas de códigos.

La capacidad de compilar los tipos genéricos en tipos para Windows páginas de códigos existe principalmente para admitir aplicaciones heredadas. Para compilar para Windows de código, la aplicación simplemente omite la definición unicode.

En el ejemplo siguiente se muestra el método utilizado en los Windows de encabezado para definir los tres conjuntos de tipos de datos. Para la implementación, consulte el archivo de encabezado Winnt.h.


```C++
// Generic types

#ifdef UNICODE
    typedef wchar_t TCHAR;
#else
    typedef unsigned char TCHAR;
#endif

typedef TCHAR *LPTSTR, *LPTCH;

// 8-bit character specific

typedef unsigned char CHAR;
typedef CHAR *LPSTR, *LPCH;

// Unicode specific (wide characters)

typedef unsigned wchar_t WCHAR;
typedef WCHAR *LPWSTR, *LPWCH;
```



La letra "T" de una definición de tipo, por ejemplo, TCHAR o LPTSTR, designa un tipo genérico que se puede compilar para páginas de códigos Windows o Unicode. La letra "W" en una definición de tipo, por ejemplo, WCHAR o LPWSTR, designa un tipo Unicode. Dado Windows páginas de códigos son de la forma anterior, tienen definiciones de tipo simples, como CHAR y LPSTR. Para obtener una descripción completa de los tipos de datos en Windows, [vea Windows Data Types](../winprog/windows-data-types.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Unicode en la API de Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
