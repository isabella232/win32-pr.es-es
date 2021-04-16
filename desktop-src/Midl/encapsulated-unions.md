---
title: Uniones encapsuladas
description: Una Unión contenida en su discriminante en una estructura en es una Unión encapsulada.
ms.assetid: d32c18b4-b2f6-4ce2-94fe-a495a3c15d14
keywords:
- tipos de datos MIDL, uniones encapsuladas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4489a043ff3690ddb31a8acccf359dcd76940aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685608"
---
# <a name="encapsulated-unions"></a><span data-ttu-id="03b05-104">Uniones encapsuladas</span><span class="sxs-lookup"><span data-stu-id="03b05-104">Encapsulated Unions</span></span>

<span data-ttu-id="03b05-105">Una Unión contenida en su discriminante en una estructura en es una Unión encapsulada.</span><span class="sxs-lookup"><span data-stu-id="03b05-105">A union that is contained with its discriminant in a structure within is an encapsulated union.</span></span> <span data-ttu-id="03b05-106">La Unión encapsulada se indica mediante la presencia de la palabra clave [**Switch**](switch.md) .</span><span class="sxs-lookup"><span data-stu-id="03b05-106">The encapsulated union is indicated by the presence of the [**switch**](switch.md) keyword.</span></span> <span data-ttu-id="03b05-107">Este tipo de Unión se denomina así porque el compilador MIDL encapsula automáticamente la Unión y su discriminante en una estructura para su transmisión durante una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="03b05-107">This type of union is so named because the MIDL compiler automatically encapsulates the union and its discriminant in a structure for transmission during a remote procedure call.</span></span>

<span data-ttu-id="03b05-108">Si falta la etiqueta Union (tipo U1 \_ en el ejemplo anterior), el compilador generará la estructura con el campo de Unión denominado *\_ Union etiquetada*.</span><span class="sxs-lookup"><span data-stu-id="03b05-108">If the union tag is missing (U1\_TYPE in the example above), the compiler will generate the structure with the union field named *tagged\_union*.</span></span>

<span data-ttu-id="03b05-109">La forma de las uniones debe ser la misma en todas las plataformas para garantizar la interconectividad.</span><span class="sxs-lookup"><span data-stu-id="03b05-109">The shape of unions must be the same across platforms to ensure interconnectivity.</span></span>

<span data-ttu-id="03b05-110">Para obtener una descripción del formulario de una Unión encapsulada, consulte [**Union**](union.md).</span><span class="sxs-lookup"><span data-stu-id="03b05-110">For a description of the form of an encapsulated union, see [**union**](union.md).</span></span>

## <a name="examples"></a><span data-ttu-id="03b05-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="03b05-111">Examples</span></span>

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

<span data-ttu-id="03b05-112">Para obtener información relacionada, vea [tipos base de MIDL](midl-base-types.md), [**Char**](char-idl.md), **\[** [**\_ identificador de contexto**](context-handle.md) **\]** , [**enumeración**](enum.md), **\[** [**primero \_ es**](first-is.md) **\]** , **\[** [**identificador**](handle.md) **\]** , **\[** [**omitir**](ignore.md) **\]** , [**int**](int.md), **\[** [**omitir**](ignore.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**MS \_ Union**](ms-union-attrib.md) **\]** , [uniones no encapsuladas](nonencapsulated-unions.md), **\[** [**ptr**](ptr.md) **\]** , **\[** [**ref**](ref.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** , **\[** [**String**](string.md) **\]** , [**struct**](struct.md), [**Switch**](switch.md), **\[** [**Switch \_ is**](switch-is.md) **\]** , **\[** [**Switch \_ Type**](switch-type.md) **\]** , **\[** [**Transmit \_ as**](transmit-as.md) **\]** , [**Union**](union.md)y **\[** [**Unique**](unique.md)**\]**</span><span class="sxs-lookup"><span data-stu-id="03b05-112">For related information, see [MIDL Base Types](midl-base-types.md), [**char**](char-idl.md), **\[**[**context\_handle**](context-handle.md)**\]**, [**enum**](enum.md), **\[**[**first\_is**](first-is.md)**\]**, **\[**[**handle**](handle.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, [**int**](int.md), **\[**[**ignore**](ignore.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**ms\_union**](ms-union-attrib.md)**\]**, [Nonencapsulated Unions](nonencapsulated-unions.md), **\[**[**ptr**](ptr.md)**\]**, **\[**[**ref**](ref.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**, **\[**[**string**](string.md)**\]**, [**struct**](struct.md), [**switch**](switch.md), **\[**[**switch\_is**](switch-is.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**, [**union**](union.md), and **\[**[**unique**](unique.md)**\]**</span></span>

 

 




