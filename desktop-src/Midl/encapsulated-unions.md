---
title: Uniones encapsuladas
description: Una unión contenida con su discriminador en una estructura dentro de es una unión encapsulada.
ms.assetid: d32c18b4-b2f6-4ce2-94fe-a495a3c15d14
keywords:
- tipos de datos MIDL, uniones encapsuladas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4489a043ff3690ddb31a8acccf359dcd76940aa7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159606"
---
# <a name="encapsulated-unions"></a>Uniones encapsuladas

Una unión contenida con su discriminador en una estructura dentro de es una unión encapsulada. La unión encapsulada se indica mediante la presencia de la palabra clave [**switch.**](switch.md) Este tipo de unión se denomina así porque el compilador MIDL encapsula automáticamente la unión y su discriminador en una estructura para su transmisión durante una llamada a procedimiento remoto.

Si falta la etiqueta de unión (U1 TYPE en el ejemplo anterior), el compilador generará la estructura con el campo de unión \_ denominado *unión \_ etiquetada.*

La forma de las uniones debe ser la misma en todas las plataformas para garantizar la interconectividad.

Para obtener una descripción del formato de una unión encapsulada, vea [**unión**](union.md).

## <a name="examples"></a>Ejemplos

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

Para obtener información relacionada, vea [MidL Base Types](midl-base-types.md), [**char**](char-idl.md), context **\[** [**\_ handle**](context-handle.md) **\]** , [**enum**](enum.md), first **\[** [**\_ is**](first-is.md) **\]** , handle , **\[** [](handle.md) **\]** **\[** [**ignore**](ignore.md) **\]** , [**int**](int.md), **\[** [**ignore**](ignore.md) **\]** , last **\[** [**\_ is**](last-is.md) **\]** , length **\[** [**\_ is**](length-is.md) **\]** , max **\[** [**\_ is**](max-is.md) **\]** , **\[** [**ms \_ union**](ms-union-attrib.md) **\]** , [Nonencapsulated Unions](nonencapsulated-unions.md), **\[** [**ptr**](ptr.md) **\]** , **\[** [**ref**](ref.md), **\]** size **\[** [**\_ is**](size-is.md) **\]** , **\[** [**string**](string.md) **\]** , [**struct**](struct.md), switch , [**switch**](switch.md) **\[** [**\_ is**](switch-is.md) **\]** , switch **\[** [**\_ type**](switch-type.md) **\]** , transmit **\[** [**\_ as**](transmit-as.md) **\]** , [**union**](union.md), and **\[** [**unique**](unique.md)**\]**

 

 




