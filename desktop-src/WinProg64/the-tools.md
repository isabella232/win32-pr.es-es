---
title: Las herramientas
description: En este tema se describen las herramientas disponibles para su uso a fin de que la aplicación esté preparada para 64 bits. Windows 10 está disponible para procesadores basados en x64 y en ARM64.
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, herramientas
- herramientas de programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87fb315200ae32eb1e1441ed330be49aa02d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418992"
---
# <a name="the-tools"></a>Las herramientas

En este tema se describen las herramientas disponibles para su uso a fin de que la aplicación esté preparada para 64 bits. Windows 10 está disponible para procesadores basados en x64 y en ARM64.

## <a name="include-files"></a>Archivos de inclusión

Los elementos de la API son prácticamente idénticos entre las ventanas 32 y 64 bits. Los archivos de encabezado de Windows se han modificado de modo que se puedan usar para el código de 32 y 64 bits. Los nuevos tipos de 64 bits y macros se definen en un nuevo archivo de encabezado, Basetsd. h, que se encuentra en el conjunto de archivos de encabezado incluidos en Windows. h. Basetsd. h incluye las nuevas definiciones de tipos de datos para ayudar a que el código fuente tenga un tamaño de texto independiente.

## <a name="new-data-types"></a>Nuevos tipos de datos

Los archivos de encabezado de Windows contienen nuevos tipos de datos. Estos tipos son principalmente para la compatibilidad de tipos con los tipos de datos de 32 bits. Los nuevos tipos proporcionan exactamente el mismo tipo que los tipos existentes, al mismo tiempo que proporcionan compatibilidad para Windows de 64 bits. Para obtener más información, vea [los nuevos tipos de datos](the-new-data-types.md) o el archivo de encabezado Basetsd. h.

## <a name="predefined-macros"></a>Macros predefinidas

El compilador define las macros siguientes para identificar la plataforma.



| Macro   | Significado                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| \_WIN64 | Plataforma de 64 bits. Esto incluye tanto x64 como ARM64.                                                        |
| \_32 | Plataforma de 32 bits. Este valor también lo define el compilador de 64 bits para la compatibilidad con versiones anteriores.<br/> |
| \_WIN16 | Una plataforma de 16 bits                                                                                           |



 

Las macros siguientes son específicas de la arquitectura.



| Macro      | Significado                |
|------------|------------------------|
| \_M \_ ia64  | Plataforma Intel Itanium |
| \_M \_ IX86  | plataforma x86           |
| \_M \_ x64   | plataforma x64           |
| \_M \_ ARM64 | Plataforma ARM64         |



 

No utilice estas macros excepto con código específico de la arquitectura, en su lugar, use \_ WIN64, \_ Win32 y \_ WIN16 siempre que sea posible.

## <a name="helper-functions"></a>Funciones del asistente

Las siguientes funciones insertadas (definidas en Basetsd. h) pueden ayudarle a convertir los valores de un tipo a otro de forma segura.

``` syntax
void            * Handle64ToHandle( const void * POINTER_64 h ) 
void * POINTER_64 HandleToHandle64( const void *h )
long              HandleToLong(     const void *h )
unsigned long     HandleToUlong(    const void *h )
void            * IntToPtr(         const int i )
void            * LongToHandle(     const long h )
void            * LongToPtr(        const long l )
void            * Ptr64ToPtr(       const void * POINTER_64 p )
int               PtrToInt(         const void *p )
long              PtrToLong(        const void *p )
void * POINTER_64 PtrToPtr64(       const void *p )
short             PtrToShort(       const void *p )
unsigned int      PtrToUint(        const void *p )
unsigned long     PtrToUlong(       const void *p )
unsigned short    PtrToUshort(      const void *p )
void            * UIntToPtr(        const unsigned int ui )
void            * ULongToPtr(       const unsigned long ul )
```

> [!WARNING]
> El signo de **IntToPtr** extiende el valor **int** , **UIntToPtr** cero: extiende el valor **int sin signo** , **LongToPtr** el signo y extiende el valor **Long** , y **ULongToPtr** cero extiende el valor **Long sin signo** .

 

## <a name="64-bit-compiler"></a>compilador de 64 bits

Los compiladores de 64 bits se pueden usar para identificar el truncamiento de punteros, conversiones de tipos incorrectas y otros problemas específicos de 64 bits.

Cuando se ejecuta el compilador por primera vez, es probable que genere muchas advertencias de truncamiento de puntero o de falta de coincidencia de tipos, como las siguientes:

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

Use estas advertencias como guía para hacer que el código sea más sólido. Se recomienda eliminar todas las advertencias, especialmente las advertencias de truncamiento de puntero.

## <a name="64-bit-compiler-switches-and-warnings"></a>Advertencias y modificadores de compilador de 64 bits

Tenga en cuenta que este compilador habilita el modelo de datos LLP64.

Existe una opción de advertencia para ayudar a migrar a LLP64. El modificador-Wp64-W3 habilita las siguientes advertencias:

-   C4305: ADVERTENCIA de truncamiento. Por ejemplo, "Return": truncamiento de "unsigned Int64" a "Long".
-   C4311: ADVERTENCIA de truncamiento. Por ejemplo, "tipo de conversión": truncamiento de puntero de "int \* \_ ptr64" a "int".
-   C4312: conversión a una advertencia de mayor tamaño. Por ejemplo, "tipo de conversión": conversión de "int" a "int \* \_ ptr64" de mayor tamaño.
-   C4318: pasando longitud cero. Por ejemplo, pasar la constante Zero como longitud a la función **memset** .
-   C4319: operador not. Por ejemplo, "~": extensión de cero "unsigned Long" a "Int64 sin signo \_ " de mayor tamaño.
-   C4313: llamar a la familia de funciones **printf** con especificadores y argumentos de tipo de conversión conflictivos. Por ejemplo, "printf": "% p" en la cadena de formato entra en conflicto con el argumento 2 de tipo " \_ Int64". Otro ejemplo es la llamada a printf ("% x", el valor del puntero \_ ); esto provoca un truncamiento de los 32 bits superiores. La llamada correcta es printf ("% p", valor de puntero \_ ).
-   C4244: igual que el C4242 de advertencia existente. Por ejemplo, "Return": conversión de " \_ Int64" a "int sin signo", posible pérdida de datos.

## <a name="64-bit-linker-and-libraries"></a>Enlazador y bibliotecas de 64 bits

Para compilar aplicaciones, use el enlazador y las bibliotecas proporcionadas por el Windows SDK. La mayoría de las bibliotecas de 32 bits tienen una versión de 64 bits correspondiente, pero algunas bibliotecas heredadas solo están disponibles en las versiones de 32 bits. El código que llama a estas bibliotecas no se vinculará cuando la aplicación se compile para Windows de 64 bits.

 

 





