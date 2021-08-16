---
title: Cadenas (RPC)
description: Tres tipos de cadenas y llamada a procedimiento remoto (RPC).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b15467ed5a1425443cbc5a53cf35aba71725c5db68c542c292af38eb0d238cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924841"
---
# <a name="strings-rpc"></a>Cadenas (RPC)

Hay tres tipos de cadenas que indican las siguientes subcadenas finales en el carácter de formato.



| Tipo                  | Substring |
|-----------------------|-----------|
| Cadena de caracteres      | Cstring   |
| Cadena de caracteres anchos | WSTRING   |
| Estructura con capacidad de cadena | SSTRING   |



 

### <a name="nonconformant-strings"></a>Cadenas no conformes

Un ejemplo de cadena no conformante es una **\[ cadena \]** en una matriz de tamaño fijo.

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

El primer formato describe cadenas comunes, como un **\[ argumento char \]** de \* cadena. Una cadena compatible de tamaño tiene la última descripción.

La descripción de conformidad<> es un descriptor de correlación y tiene 4 o 6 bytes, dependiendo de \_ si [**se usa /robust.**](/windows/desktop/Midl/-robust)

### <a name="structure-strings"></a>Cadenas de estructura

A continuación se muestra una estructura con capacidad de cadena noformista:

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

Estructura compatible con capacidad de cadena:

``` syntax
FC_C_SSTRING 
element_size<1>
```

–o –

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

La última descripción es para una estructura con capacidad de cadena de tamaño.

 

 