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
# <a name="encapsulated-unions"></a>Uniones encapsuladas

Una Unión contenida en su discriminante en una estructura en es una Unión encapsulada. La Unión encapsulada se indica mediante la presencia de la palabra clave [**Switch**](switch.md) . Este tipo de Unión se denomina así porque el compilador MIDL encapsula automáticamente la Unión y su discriminante en una estructura para su transmisión durante una llamada a procedimiento remoto.

Si falta la etiqueta Union (tipo U1 \_ en el ejemplo anterior), el compilador generará la estructura con el campo de Unión denominado *\_ Union etiquetada*.

La forma de las uniones debe ser la misma en todas las plataformas para garantizar la interconectividad.

Para obtener una descripción del formulario de una Unión encapsulada, consulte [**Union**](union.md).

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

Para obtener información relacionada, vea [tipos base de MIDL](midl-base-types.md), [**Char**](char-idl.md), **\[** [**\_ identificador de contexto**](context-handle.md) **\]** , [**enumeración**](enum.md), **\[** [**primero \_ es**](first-is.md) **\]** , **\[** [**identificador**](handle.md) **\]** , **\[** [**omitir**](ignore.md) **\]** , [**int**](int.md), **\[** [**omitir**](ignore.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**MS \_ Union**](ms-union-attrib.md) **\]** , [uniones no encapsuladas](nonencapsulated-unions.md), **\[** [**ptr**](ptr.md) **\]** , **\[** [**ref**](ref.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** , **\[** [**String**](string.md) **\]** , [**struct**](struct.md), [**Switch**](switch.md), **\[** [**Switch \_ is**](switch-is.md) **\]** , **\[** [**Switch \_ Type**](switch-type.md) **\]** , **\[** [**Transmit \_ as**](transmit-as.md) **\]** , [**Union**](union.md)y **\[** [**Unique**](unique.md)**\]**

 

 




