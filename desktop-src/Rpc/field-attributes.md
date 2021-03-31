---
title: Atributos de los campos
description: Atributos de campo (atributos aplicados a los campos de una matriz, estructura, Unión o matriz de caracteres) y llamada a procedimiento remoto (RPC).
ms.assetid: 4508479d-ff0a-4698-94aa-588837032067
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b9421ddf4ea7e7bc4c70af0ecd826e2681875d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995568"
---
# <a name="field-attributes"></a>Atributos de los campos

Los atributos de campo son los atributos que se pueden aplicar a los campos de una matriz, estructura, Unión o matriz de caracteres:

-   **\[**[**omitir**](/windows/desktop/Midl/ignore) **\]** , **\[** [ **el tamaño \_ es**](/windows/desktop/Midl/size-is)**\]**
-   **\[**[**Max \_ es**](/windows/desktop/Midl/max-is)**\]**
-   **\[**[**la longitud \_ es**](/windows/desktop/Midl/length-is)**\]**
-   **\[**[**el primero \_ es**](/windows/desktop/Midl/first-is)**\]**
-   **\[**[**última \_ es**](/windows/desktop/Midl/last-is)**\]**
-   **\[**[**el modificador \_ es**](/windows/desktop/Midl/switch-is)**\]**
-   **\[**[**String@**](/windows/desktop/Midl/string)**\]**
-   [atributos de puntero](three-pointer-types.md)

Por ejemplo, los atributos de campo se utilizan junto con las declaraciones de matriz para especificar el tamaño de la matriz o la parte de la matriz que contiene datos válidos. Esto se hace asociando otro parámetro, un campo de estructura o una expresión constante con la matriz.

El **\[** [](/windows/desktop/Midl/ignore) **\]** atributo Ignore designa los campos de puntero que se van a omitir durante el proceso de cálculo de referencias. Este campo omitido se establece en **null** en el lado del receptor.

MIDL proporciona matrices *compatibles*, *variables* y de *apertura* . Una matriz se llama conforme si sus límites se determinan en tiempo de ejecución. El **\[** [**atributo \_ size**](/windows/desktop/Midl/size-is) **\]** designa el límite superior en el tamaño de asignación de la matriz y el **\[** atributo [**Max \_ is**](/windows/desktop/Midl/max-is) **\]** designa el límite superior en el valor de un índice de matriz válido. Para obtener más información, vea **\[** [**matrices**](arrays.md) **\]** .

Una matriz se denomina variable si sus límites se determinan en tiempo de compilación, pero el intervalo de elementos transmitidos se determina en tiempo de ejecución. Una matriz abierta (también denominada matriz varying compatible) es una matriz cuyo límite superior y el intervalo de elementos transmitidos se determinan en tiempo de ejecución. Para determinar el intervalo de elementos transmitidos de una matriz, la declaración de la matriz debe incluir una **\[** [**longitud \_**](/windows/desktop/Midl/length-is) **\]** , el **\[** [**primero \_ es**](/windows/desktop/Midl/first-is) **\]** o el **\[** atributo [**Last \_**](/windows/desktop/Midl/last-is) **\]** .

El atributo **\[ \_ \] length** designa el número de elementos de matriz que se van a transmitir y el **\[ primero \_ es \]** Attribute designa el índice del primer elemento de la matriz que se va a transmitir. El atributo **\[ Last \_ es \]** el índice del último elemento de la matriz que se va a transmitir.

El **\[** atributo [**Switch \_ es**](/windows/desktop/Midl/switch-is) **\]** Field designa un discriminador Union. Cuando la Unión es un parámetro de procedimiento, el discriminador de Unión debe ser otro parámetro del mismo procedimiento. Cuando la Unión es un campo de una estructura, el discriminador debe ser otro campo de la estructura en el mismo nivel que el campo de Unión. El discriminador debe ser un tipo [**booleano**](/windows/desktop/Midl/boolean), [**Char**](/windows/desktop/Midl/char-idl), [**int**](/windows/desktop/Midl/int)o [**enum**](/windows/desktop/Midl/enum) , o un tipo que se resuelva en uno de estos tipos. Para obtener más información, vea [uniones no encapsuladas](/windows/desktop/Midl/nonencapsulated-unions) y el **\[ modificador \_ es \]**.

El **\[** atributo de campo de [**cadena**](/windows/desktop/Midl/string) **\]** designa que un carácter unidimensional o una matriz de bytes, o un puntero a un carácter o un flujo de bytes terminados en cero, se tratará como una cadena. El atributo String solo se aplica a las matrices y punteros unidimensionales. El tipo de elemento está limitado a [**Char**](/windows/desktop/Midl/char-idl), [**byte**](/windows/desktop/Midl/byte), [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t)o a un tipo con nombre que se resuelve en uno de estos tipos.

Para obtener información sobre el contexto en el que aparecen los atributos de campo, vea [matrices de MIDL](/windows/desktop/Midl/midl-arrays), [estructuras MIDL](/windows/desktop/Midl/midl-structures)y [uniones MIDL](/windows/desktop/Midl/midl-unions).

 

 