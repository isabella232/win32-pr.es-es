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
# <a name="mof-strings"></a><span data-ttu-id="622c0-103">Cadenas MOF</span><span class="sxs-lookup"><span data-stu-id="622c0-103">MOF strings</span></span>

<span data-ttu-id="622c0-104">Una cadena es un tipo de datos que contiene una cadena de caracteres que normalmente pretende ser texto legible.</span><span class="sxs-lookup"><span data-stu-id="622c0-104">A string is a data type that contains a string of characters usually intended as human-readable text.</span></span> <span data-ttu-id="622c0-105">MOF describe dos tipos de cadenas que se usan para contener uno o varios caracteres.</span><span class="sxs-lookup"><span data-stu-id="622c0-105">MOF describes two types of strings, which use to hold single or multiple characters.</span></span> <span data-ttu-id="622c0-106">MOF también tiene una serie de reglas que describen el uso de comillas dentro de una cadena.</span><span class="sxs-lookup"><span data-stu-id="622c0-106">MOF also has a series of rules describing the use of quotes within a string.</span></span>

<span data-ttu-id="622c0-107">En la tabla siguiente se enumeran los tipos de datos de cadena para MOF.</span><span class="sxs-lookup"><span data-stu-id="622c0-107">The following table lists the string data types for MOF.</span></span>



| <span data-ttu-id="622c0-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="622c0-108">Data type</span></span>  | <span data-ttu-id="622c0-109">Tipo de automatización</span><span class="sxs-lookup"><span data-stu-id="622c0-109">Automation type</span></span> | <span data-ttu-id="622c0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="622c0-110">Description</span></span>                                                                            |
|------------|-----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="622c0-111">**char16**</span><span class="sxs-lookup"><span data-stu-id="622c0-111">**char16**</span></span> | <span data-ttu-id="622c0-112">**I2 de VT \_**</span><span class="sxs-lookup"><span data-stu-id="622c0-112">**VT\_I2**</span></span>      | <span data-ttu-id="622c0-113">Carácter Unicode de 16 bits único en formato de juego de caracteres universal 2 (UCS-2)</span><span class="sxs-lookup"><span data-stu-id="622c0-113">Single 16-bit Unicode character in Universal Character Set 2 (UCS-2) format</span></span><br/> |
| <span data-ttu-id="622c0-114">**string**</span><span class="sxs-lookup"><span data-stu-id="622c0-114">**string**</span></span> | <span data-ttu-id="622c0-115">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="622c0-115">**VT\_BSTR**</span></span>    | <span data-ttu-id="622c0-116">Cadena de caracteres Unicode</span><span class="sxs-lookup"><span data-stu-id="622c0-116">Unicode character string</span></span><br/>                                                    |



 

<span data-ttu-id="622c0-117">Utilice las siguientes directrices al escribir cadenas para MOF:</span><span class="sxs-lookup"><span data-stu-id="622c0-117">Use the following guidelines when writing strings for MOF:</span></span>

-   <span data-ttu-id="622c0-118">Incluya las constantes de un solo carácter entre comillas simples.</span><span class="sxs-lookup"><span data-stu-id="622c0-118">Surround single-character constants with single quotes.</span></span>

    <span data-ttu-id="622c0-119">Si no usa comillas simples con constantes de caracteres individuales, debe usar la representación entera del valor de carácter Unicode.</span><span class="sxs-lookup"><span data-stu-id="622c0-119">If you do not use single quotes with single character constants, you must use the integer representation of the Unicode character value.</span></span> <span data-ttu-id="622c0-120">Opcionalmente, puede especificar el carácter literalmente con la \\ secuencia de escape x del estándar C de American National Standards Institute (ANSI), como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="622c0-120">Optionally, you could specify the character literally with the \\x escape sequence from the American National Standards Institute (ANSI) C standard, as shown:</span></span>

    ``` syntax
    char16  TestChar1 = '\x4133';
    char16  Testchar2 = 'A';
    ```

    <span data-ttu-id="622c0-121">Dado que MOF se basa en Unicode, también puede especificar valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="622c0-121">Because MOF is based on Unicode, you can also specify 16-bit values.</span></span>

    <span data-ttu-id="622c0-122">Tenga en cuenta que las constantes de un solo carácter en formato ANSI C están entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="622c0-122">Be aware that single-character constants in ANSI C format are surrounded by double quotes.</span></span>

-   <span data-ttu-id="622c0-123">Rodear cadenas de caracteres entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="622c0-123">Surround character strings with double quotes.</span></span>

    ``` syntax
    DTime    = "19940107140332.000000-300";
    ```

-   <span data-ttu-id="622c0-124">Concatene cadenas de Comillas consecutivas con uno o más espacios en blanco.</span><span class="sxs-lookup"><span data-stu-id="622c0-124">Concatenate successive quote strings with one or more white spaces.</span></span>

    ``` syntax
    DString = "This" "becomes a long string";
    ```

-   <span data-ttu-id="622c0-125">Use una secuencia de escape que empiece por una barra diagonal inversa para insertar comillas en una cadena.</span><span class="sxs-lookup"><span data-stu-id="622c0-125">Use an escape sequence beginning with a backslash to embed quotes into a string.</span></span>

    ``` syntax
    DMyString = "This is an \"embedded quote\" example."
    ```

<span data-ttu-id="622c0-126">En el ejemplo siguiente se describe cómo inicializar las propiedades de cadena y un parámetro de cadena:</span><span class="sxs-lookup"><span data-stu-id="622c0-126">The following example describes how to initialize string properties and a string parameter:</span></span>

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

 

 




