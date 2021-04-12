---
title: Cadenas (RPC)
description: Tres tipos de cadenas y llamada a procedimiento remoto (RPC).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207e20b1c343ded17b5d62db2321bee380463f20
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359282"
---
# <a name="strings-rpc"></a>Cadenas (RPC)

Hay tres tipos de cadenas que se indican mediante las siguientes subcadenas finales en el carácter de formato.



| Tipo                  | Substring |
|-----------------------|-----------|
| Cadena de caracteres      | CSTRING   |
| Cadena de caracteres anchos | WSTRING   |
| Estructura que permite cadenas | SSTRING   |



 

### <a name="nonconformant-strings"></a>Cadenas no compatibles

Un ejemplo de cadena no conforme es una **\[ cadena \]** en una matriz de tamaño fijo.

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a>Cadenas compatibles

``` syntax
FC_C_CSTRING | FC_C_WSTRING
FC_PAD 
```

-o bien-

``` syntax
FC_C_CSTRING | FC_C_WSTRING 
FC_STRING_SIZED 
conformance_description<> 
```

El primer formato describe cadenas comunes, como un argumento de carácter de **\[ \] cadena** \* . Una cadena compatible con tamaño tiene la última Descripción.

La descripción del cumplimiento \_<> es un descriptor de correlación y tiene 4 o 6 bytes dependiendo de si se usa [**/Robust**](/windows/desktop/Midl/-robust) .

### <a name="structure-strings"></a>Cadenas de estructura

La siguiente es una estructura que permite la cadena no conforme:

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

Estructura compatible con cadenas compatibles:

``` syntax
FC_C_SSTRING 
element_size<1>
```

de

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

La última Descripción es para una estructura que permita la cadena con el tamaño.

 

 