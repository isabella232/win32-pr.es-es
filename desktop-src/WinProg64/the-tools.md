---
title: Herramientas
description: En este tema se describen las herramientas disponibles para que la aplicación esté lista para 64 bits. Windows 10 está disponible para procesadores basados en x64 y ARM64.
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- Guía de programación de 64 Windows de programación de 64 Windows programación, herramientas
- herramientas de programación de Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87fb315200ae32eb1e1441ed330be49aa02d669
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581305"
---
# <a name="the-tools"></a>Herramientas

En este tema se describen las herramientas disponibles para que la aplicación esté lista para 64 bits. Windows 10 está disponible para procesadores basados en x64 y ARM64.

## <a name="include-files"></a>Archivos de inclusión

Los elementos de API son prácticamente idénticos entre las máquinas virtuales de 32 y 64 Windows. Los Windows de encabezado se han modificado para que se puedan usar para código de 32 y 64 bits. Los nuevos tipos y macros de 64 bits se definen en un nuevo archivo de encabezado, Basetsd.h, que se encuentra en el conjunto de archivos de encabezado incluidos por Windows.h. Basetsd.h incluye las nuevas definiciones de tipo de datos para ayudar a que el tamaño de palabra del código fuente se haga independiente.

## <a name="new-data-types"></a>Nuevos tipos de datos

Los Windows de encabezado contienen nuevos tipos de datos. Estos tipos son principalmente para la compatibilidad de tipos con los tipos de datos de 32 bits. Los nuevos tipos proporcionan exactamente el mismo tipo que los tipos existentes, a la vez que proporcionan compatibilidad con la máquina de 64 Windows. Para obtener más información, [vea Los nuevos tipos de datos o](the-new-data-types.md) el archivo de encabezado Basetsd.h.

## <a name="predefined-macros"></a>Macros predefinidas

El compilador define las macros siguientes para identificar la plataforma.



| Macro   | Significado                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| \_WIN64 | Una plataforma de 64 bits. Esto incluye x64 y ARM64.                                                        |
| \_WIN32 | Una plataforma de 32 bits. El compilador de 64 bits también define este valor para la compatibilidad con versiones anteriores.<br/> |
| \_WIN16 | Una plataforma de 16 bits                                                                                           |



 

Las macros siguientes son específicas de la arquitectura.



| Macro      | Significado                |
|------------|------------------------|
| \_M \_ IA64  | Plataforma Intel Itanium |
| \_M \_ IX86  | Plataforma x86           |
| \_M \_ X64   | Plataforma x64           |
| \_M \_ ARM64 | Plataforma ARM64         |



 

No use estas macros excepto con código específico de la arquitectura; en su lugar, use \_ WIN64, \_ WIN32 y \_ WIN16 siempre que sea posible.

## <a name="helper-functions"></a>Funciones del asistente

Las siguientes funciones insertadas (definidas en Basetsd.h) pueden ayudarle a convertir valores de un tipo a otro de forma segura.

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
> **IntToPtr** sign-extends the **int** value, **UIntToPtr** zero-extends the **unsigned int** value, **LongToPtr** sign-extends the **long** value, and **ULongToPtr** zero-extends the **unsigned long** value.

 

## <a name="64-bit-compiler"></a>Compilador de 64 bits

Los compiladores de 64 bits se pueden usar para identificar el truncamiento de punteros, las conversión de tipos incorrectas y otros problemas específicos de 64 bits.

La primera vez que se ejecuta el compilador, probablemente generará muchas advertencias de truncamiento de puntero o de error de coincidencia de tipos, como las siguientes:

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

Use estas advertencias como guía para que el código sea más sólido. Es un procedimiento recomendado eliminar todas las advertencias, especialmente las advertencias de truncamiento de punteros.

## <a name="64-bit-compiler-switches-and-warnings"></a>Advertencias y modificadores del compilador de 64 bits

Tenga en cuenta que este compilador habilita el modelo de datos LLP64.

Hay una opción de advertencia para ayudar a portear a LLP64. El modificador -Wp64 -W3 habilita las advertencias siguientes:

-   C4305: Advertencia de truncamiento. Por ejemplo, "return": truncamiento de "unsigned int64" a "long".
-   C4311: Advertencia de truncamiento. Por ejemplo, "type cast": truncamiento del puntero de "int \* \_ ptr64" a "int".
-   C4312: Conversión a advertencia de tamaño mayor. Por ejemplo, "type cast": conversión de "int" a "int \* \_ ptr64" de mayor tamaño.
-   C4318: Pasar longitud cero. Por ejemplo, pasar constante cero como longitud a la **función memset.**
-   C4319: Operador Not. Por ejemplo, "~": cero que extiende "unsigned long" a "unsigned \_ int64" de mayor tamaño.
-   C4313: Llamada a la **familia printf** de funciones con especificadores y argumentos de tipo de conversión en conflicto. Por ejemplo, "printf": "%p" en cadena de formato entra en conflicto con el argumento 2 de tipo " \_ int64". Otro ejemplo es la llamada printf("%x", valor de puntero); esto provoca un truncamiento de \_ los 32 bits superiores. La llamada correcta es printf("%p", valor de \_ puntero).
-   C4244: igual que la advertencia existente C4242. Por ejemplo, "return": conversión de " \_ int64" a "unsigned int", posible pérdida de datos.

## <a name="64-bit-linker-and-libraries"></a>Vinculador y bibliotecas de 64 bits

Para compilar aplicaciones, use el vinculador y las bibliotecas que proporciona Windows SDK. La mayoría de las bibliotecas de 32 bits tienen una versión correspondiente de 64 bits, pero algunas bibliotecas heredadas solo están disponibles en versiones de 32 bits. El código que llama a estas bibliotecas no se vinculará cuando la aplicación se haya creado para archivos de 64 Windows.

 

 





