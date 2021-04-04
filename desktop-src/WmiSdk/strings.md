---
title: Cadenas MOF
description: Una cadena es un tipo de datos que contiene una cadena de caracteres que normalmente pretende ser texto legible.
ms.assetid: 08a07184-6d23-4988-a3de-e5bfc3e177f8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1427accbdb3a4dae0240563656785968d4bd075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908563"
---
# <a name="mof-strings"></a>Cadenas MOF

Una cadena es un tipo de datos que contiene una cadena de caracteres que normalmente pretende ser texto legible. MOF describe dos tipos de cadenas que se usan para contener uno o varios caracteres. MOF también tiene una serie de reglas que describen el uso de comillas dentro de una cadena.

En la tabla siguiente se enumeran los tipos de datos de cadena para MOF.



| Tipo de datos  | Tipo de automatización | Descripción                                                                            |
|------------|-----------------|----------------------------------------------------------------------------------------|
| **char16** | **I2 de VT \_**      | Carácter Unicode de 16 bits único en formato de juego de caracteres universal 2 (UCS-2)<br/> |
| **string** | **VT \_ BSTR**    | Cadena de caracteres Unicode<br/>                                                    |



 

Utilice las siguientes directrices al escribir cadenas para MOF:

-   Incluya las constantes de un solo carácter entre comillas simples.

    Si no usa comillas simples con constantes de caracteres individuales, debe usar la representación entera del valor de carácter Unicode. Opcionalmente, puede especificar el carácter literalmente con la \\ secuencia de escape x del estándar C de American National Standards Institute (ANSI), como se muestra a continuación:

    ``` syntax
    char16  TestChar1 = '\x4133';
    char16  Testchar2 = 'A';
    ```

    Dado que MOF se basa en Unicode, también puede especificar valores de 16 bits.

    Tenga en cuenta que las constantes de un solo carácter en formato ANSI C están entre comillas dobles.

-   Rodear cadenas de caracteres entre comillas dobles.

    ``` syntax
    DTime    = "19940107140332.000000-300";
    ```

-   Concatene cadenas de Comillas consecutivas con uno o más espacios en blanco.

    ``` syntax
    DString = "This" "becomes a long string";
    ```

-   Use una secuencia de escape que empiece por una barra diagonal inversa para insertar comillas en una cadena.

    ``` syntax
    DMyString = "This is an \"embedded quote\" example."
    ```

En el ejemplo siguiente se describe cómo inicializar las propiedades de cadena y un parámetro de cadena:

``` syntax
class  StringDataClass
{
    [key]  String    Dstring;
    DateTime         DTime;
    char16           CharVal1;
    char16           CharVal2;
    sint32 DiskMethod ([in, Id(0)] string Description = "Disk 1");
};

instance of StringDataClass
{
    Dstring = "this can go on for " " some time"
       " before it is complete";
    DTime    = "19940107140332.000000-300";
    CharVal1 = '\x16';
    CharVal2 = '\x32';
};
```

 

 




