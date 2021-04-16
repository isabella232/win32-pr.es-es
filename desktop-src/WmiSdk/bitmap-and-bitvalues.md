---
description: Es un entero vinculado a una propiedad con los calificadores BitMap y BitValue.
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: Calificadores BitMap y BitValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60dd6b4ad5866ddc79c960316757700bc5fbb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652555"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a><span data-ttu-id="7e0c4-103">Calificadores BitMap y BitValue</span><span class="sxs-lookup"><span data-stu-id="7e0c4-103">BitMap and BitValue Qualifiers</span></span>

<span data-ttu-id="7e0c4-104">Un mapa de bits es un entero vinculado a una propiedad con los calificadores **Bitmap** y **BitValue** .</span><span class="sxs-lookup"><span data-stu-id="7e0c4-104">A bitmap is an integer linked to a property with the **BitMap** and **BitValue** qualifiers.</span></span> <span data-ttu-id="7e0c4-105">Cada bit del valor de la propiedad actúa como un índice en la matriz de valores de la lista **BitValue** .</span><span class="sxs-lookup"><span data-stu-id="7e0c4-105">Each bit of the property value acts as an index into the array of values in the **BitValue** list.</span></span> <span data-ttu-id="7e0c4-106">Dado que varios bits en el valor de la propiedad pueden ser "ON" al mismo tiempo, se puede usar un valor de propiedad único para indicar varios valores simultáneos.</span><span class="sxs-lookup"><span data-stu-id="7e0c4-106">Because multiple bits in the property value can be "on" at the same time, it is possible to use a single property value to indicate multiple concurrent values.</span></span>

<span data-ttu-id="7e0c4-107">Por ejemplo, en el siguiente ejemplo de código MOF se establece la propiedad **filetype** como con los calificadores **Bitmap** y **BitValues** .</span><span class="sxs-lookup"><span data-stu-id="7e0c4-107">For example, the following MOF code example establishes the **FileType** property as having the **BitMap** and **BitValues** qualifiers.</span></span> <span data-ttu-id="7e0c4-108">Además, establece que el bit de orden inferior (bit 0) corresponde al valor "Read Only".</span><span class="sxs-lookup"><span data-stu-id="7e0c4-108">It further establishes that the low-order bit (bit 0) corresponds to the value "Read Only".</span></span> <span data-ttu-id="7e0c4-109">El siguiente bit (bit 1) corresponde a "Hidden", y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="7e0c4-109">The next bit (bit 1) corresponds to "Hidden", and so on.</span></span> <span data-ttu-id="7e0c4-110">(No todos los bits deben ser significativos.</span><span class="sxs-lookup"><span data-stu-id="7e0c4-110">(Not all bits must be significant.</span></span> <span data-ttu-id="7e0c4-111">En este sistema de ocho bits, los dos bits de orden superior, 6 y 7, no tienen importancia.)</span><span class="sxs-lookup"><span data-stu-id="7e0c4-111">In this eight-bit system, the two high-order bits, 6 and 7, have no significance.)</span></span>

``` syntax
[BitMap("0","1","2","3","4","5"),
 BitValues("Read Only",
           "Hidden",
           "System",
           "Volume Label",
           "Subdirectory",
           "Archive")]
byte FileType;
```

<span data-ttu-id="7e0c4-112">Si la propiedad **filetype** informa del valor 7 (bits 0000 0111), el archivo es "Read Only", "System" y "Hidden".</span><span class="sxs-lookup"><span data-stu-id="7e0c4-112">If the **FileType** property reports the value 7 (bits 0000 0111), the file is "Read Only", "System", and "Hidden".</span></span> <span data-ttu-id="7e0c4-113">Si la propiedad **filetype** informa del valor 18 (0X12, bits 0001 0010), se trata de un subdirectorio oculto.</span><span class="sxs-lookup"><span data-stu-id="7e0c4-113">If the **FileType** property reports the value 18 (0x12, bits 0001 0010), it is a hidden subdirectory.</span></span>

<span data-ttu-id="7e0c4-114">Hay dos tipos diferentes de mapas de bits que usan código MOF:</span><span class="sxs-lookup"><span data-stu-id="7e0c4-114">There are two different types of bitmaps using MOF code:</span></span>

-   <span data-ttu-id="7e0c4-115">Bits significativos consecutivos que empiezan por el bit de orden inferior (bit 0)</span><span class="sxs-lookup"><span data-stu-id="7e0c4-115">Consecutive significant bits beginning with the low-order bit (bit 0)</span></span>

    <span data-ttu-id="7e0c4-116">Puede definir una matriz de valores de bit sin especificar explícitamente los bits significativos si los bits significativos comienzan con el bit de orden inferior (bit 0) y progresan hacia arriba sin interrupción a través de todos los elementos de la matriz **BitValue** .</span><span class="sxs-lookup"><span data-stu-id="7e0c4-116">You can define an array of bit values without explicitly specifying the significant bits if the significant bits begin with the low-order bit (bit 0) and progress upward without interruption through all items in the **BitValue** array.</span></span> <span data-ttu-id="7e0c4-117">El siguiente ejemplo de código MOF realiza la misma función que en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="7e0c4-117">The following MOF code example performs the same function as the previous example.</span></span>

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   <span data-ttu-id="7e0c4-118">Bit significativo precedido por un bit no significativo</span><span class="sxs-lookup"><span data-stu-id="7e0c4-118">Significant bit preceded by a non-significant bit</span></span>

    <span data-ttu-id="7e0c4-119">Si el bit de orden inferior es insignificante o la secuencia de bits significativos no es continua, debe especificar los calificadores **Bitmap** y **BitValues** .</span><span class="sxs-lookup"><span data-stu-id="7e0c4-119">If the low-order bit is insignificant, or the sequence of significant bits is not continuous, you must specify both the **BitMap** and **BitValues** qualifiers.</span></span> <span data-ttu-id="7e0c4-120">En el siguiente ejemplo de código MOF se muestra una situación en la que el bit de orden inferior no es significativo y hay un hueco en la secuencia de bits significativos.</span><span class="sxs-lookup"><span data-stu-id="7e0c4-120">The following MOF code example shows a situation in which the low-order bit is not significant and there is a gap in the sequence of significant bits.</span></span>

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    <span data-ttu-id="7e0c4-121">En este caso, el establecimiento del bit de orden inferior (bit 0) no tiene importancia y se omite.</span><span class="sxs-lookup"><span data-stu-id="7e0c4-121">In this case, setting the low-order bit (bit 0) has no significance and is ignored.</span></span> <span data-ttu-id="7e0c4-122">Sin embargo, la configuración de bit 1 (0X2) indica que este mensaje de correo electrónico está marcado para seguimiento, el valor bit 4 (0x8) indica que se debe enviar una confirmación de entrega al remitente cuando el mensaje de correo electrónico ha llegado al buzón del destinatario y el valor de bit 5 (0x10) especifica que se debe enviar una confirmación de lectura al remitente cuando el destinatario Abra el mensaje de correo.</span><span class="sxs-lookup"><span data-stu-id="7e0c4-122">However, setting bit 1 (0x2) indicates that this email message is flagged for follow up, setting bit 4 (0x8) indicates that a delivery receipt should be sent to the sender when the email message has arrived at the recipient's mailbox, and setting bit 5 (0x10) specifies that a read receipt should be sent to the sender when the email message is opened by the recipient.</span></span> <span data-ttu-id="7e0c4-123">Al establecer los tres bits significativos (0x1A), se especifican las tres condiciones del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7e0c4-123">Setting all three significant bits (0x1A) specifies all three conditions for the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e0c4-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e0c4-124">Remarks</span></span>

<span data-ttu-id="7e0c4-125">A **la hora** de decidir si usar los / calificadores de valores **BitValues** o **ValueMap** /  , determine si alguno de los valores que se indican podría producirse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="7e0c4-125">In deciding whether to use the **BitMap**/**BitValues** or **ValueMap**/**Values** qualifiers, determine whether any of the values being indicated could occur concurrently.</span></span> <span data-ttu-id="7e0c4-126">Si pueden existir varios valores simultáneos, debe usar el **mapa de bits** / **BitValues**.</span><span class="sxs-lookup"><span data-stu-id="7e0c4-126">If multiple concurrent values can exist, you must use **BitMap**/**BitValues**.</span></span> <span data-ttu-id="7e0c4-127">Si todos los valores son mutuamente excluyentes, debe usar los  / calificadores de **valores** ValueMap.</span><span class="sxs-lookup"><span data-stu-id="7e0c4-127">If all the values are mutually exclusive, you should use the **ValueMap**/**Values** qualifiers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e0c4-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e0c4-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e0c4-129">Valores de ValueMap y calificadores de valor</span><span class="sxs-lookup"><span data-stu-id="7e0c4-129">ValueMap and Value Qualifiers</span></span>](value-map.md)
</dt> </dl>

 

 



