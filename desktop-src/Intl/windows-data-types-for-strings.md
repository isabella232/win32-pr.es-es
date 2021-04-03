---
description: La mayoría de las operaciones de cadena pueden utilizar la misma lógica para Unicode y para las páginas de códigos de Windows.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Tipos de datos de Windows para cadenas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e24be1024736ce324e040e58f6ac45636a11d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083476"
---
# <a name="windows-data-types-for-strings"></a>Tipos de datos de Windows para cadenas

La mayoría de las operaciones de cadena pueden utilizar la misma lógica para [Unicode](unicode.md) y para [las páginas de códigos de Windows](code-pages.md). La única diferencia es que la unidad básica de operación es un carácter de 16 bits (también conocido como carácter ancho) para Unicode y un carácter de 8 bits para las páginas de códigos de Windows. Los archivos de encabezado de Windows proporcionan varias definiciones de tipos que facilitan la creación de orígenes que se pueden compilar para Unicode o para páginas de códigos de Windows.

Windows admite tres conjuntos de tipos de datos de caracteres y cadenas: un conjunto de definiciones de tipo genérico que se pueden compilar para páginas de códigos Unicode o Windows, y dos conjuntos de definiciones de tipo específicas. Un conjunto de definiciones de tipo específico es para su uso con Unicode y el otro es para su uso con las páginas de códigos de Windows.

Una aplicación que usa tipos de datos genéricos se puede compilar para Unicode simplemente definiendo "Unicode" antes de las instrucciones **\# include** para los archivos de encabezado o durante la compilación. Las nuevas aplicaciones de Windows deben usar Unicode para evitar las incoherencias de las páginas de códigos variadas y para simplificar la localización. Deben escribirse con tipos de datos genéricos y deben definir "Unicode" para compilar estos tipos en tipos Unicode. En los pocos lugares donde una aplicación debe trabajar con datos de caracteres de 8 bits, puede hacer un uso explícito de los tipos de las páginas de códigos de Windows.

La capacidad de compilar los tipos genéricos en tipos de páginas de códigos de Windows existe principalmente para la compatibilidad con aplicaciones heredadas. Para compilar las páginas de códigos de Windows, la aplicación simplemente omite la definición de Unicode.

En el ejemplo siguiente se muestra el método utilizado en los archivos de encabezado de Windows para definir los tres conjuntos de tipos de datos. Para la implementación, vea el archivo de encabezado Winnt. h.


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



La letra "T" de una definición de tipo, por ejemplo, TCHAR o LPTSTR, designa un tipo genérico que se puede compilar para páginas de códigos de Windows o Unicode. La letra "W" de una definición de tipo, por ejemplo, WCHAR o LPWSTR, designa un tipo Unicode. Dado que las páginas de códigos de Windows tienen el formato anterior, tienen definiciones de tipos simples, como CHAR y LPSTR. Para obtener una descripción completa de los tipos de datos de Windows, vea [tipos de datos de Windows](../winprog/windows-data-types.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Unicode en la API de Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
