---
title: Atributos de los campos
description: Atributos de campo (atributos aplicados a campos de una matriz, estructura, unión o matriz de caracteres) y llamada a procedimiento remoto (RPC).
ms.assetid: 4508479d-ff0a-4698-94aa-588837032067
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6d14bab0cf14710e91fceb466111c4af32d3d2828e4b7bdacc9494fa27b7d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930004"
---
# <a name="field-attributes"></a>Atributos de los campos

Los atributos de campo son los atributos que se pueden aplicar a los campos de una matriz, estructura, unión o matriz de caracteres:

-   **\[**[**ignore**](/windows/desktop/Midl/ignore) **\]** , el tamaño **\[** [ **\_ es**](/windows/desktop/Midl/size-is)**\]**
-   **\[**[**max \_ is**](/windows/desktop/Midl/max-is)**\]**
-   **\[**[**length \_ es**](/windows/desktop/Midl/length-is)**\]**
-   **\[**[**en \_ primer lugar es**](/windows/desktop/Midl/first-is)**\]**
-   **\[**[**el \_ último es**](/windows/desktop/Midl/last-is)**\]**
-   **\[**[**switch \_ es**](/windows/desktop/Midl/switch-is)**\]**
-   **\[**[**Cadena**](/windows/desktop/Midl/string)**\]**
-   [atributos de puntero](three-pointer-types.md)

Por ejemplo, los atributos de campo se usan junto con declaraciones de matriz para especificar el tamaño de la matriz o la parte de la matriz que contiene datos válidos. Para ello, se asocia otro parámetro, un campo de estructura o una expresión constante a la matriz.

El **\[** [**atributo ignore**](/windows/desktop/Midl/ignore) **\]** designa los campos de puntero que se omitirán durante el proceso de serialización. Este campo omitido se establece en **NULL en** el lado receptor.

MIDL proporciona *matrices compatibles,* *variables* *y* abiertas. Una matriz se denomina conforme si sus límites se determinan en tiempo de ejecución. El **\[** [**atributo size \_ is**](/windows/desktop/Midl/size-is) designa el límite superior en el tamaño de asignación de la matriz y el atributo max is designa el límite superior en el valor de un índice de **\]** **\[** [**\_**](/windows/desktop/Midl/max-is) **\]** matriz válido. Para obtener más información, vea **\[** [**matrices**](arrays.md) **\]** .

Se llama a una matriz variable si sus límites se determinan en tiempo de compilación, pero el intervalo de elementos transmitidos se determina en tiempo de ejecución. Una matriz abierta (también denominada matriz variable compatible) es una matriz cuyo límite superior y el intervalo de elementos transmitidos se determinan en tiempo de ejecución. Para determinar el intervalo de elementos transmitidos de una matriz, la declaración de matriz debe incluir una longitud **\[** [**\_ es**](/windows/desktop/Midl/length-is), el primero **\]** **\[** [**\_ es**](/windows/desktop/Midl/first-is) **\]** o el último es **\[** [**\_ el**](/windows/desktop/Midl/last-is) **\]** atributo .

La **\[ longitud \_ es \]** atributo que designa el número de elementos de matriz que se transmitirán y el primer atributo **\[ \_ es \]** designa el índice del primer elemento de matriz que se va a transmitir. El **\[ último atributo \_ is \]** designa el índice del último elemento de matriz que se va a transmitir.

El **\[** [**modificador es \_ un**](/windows/desktop/Midl/switch-is) **\]** atributo de campo que designa un discriminador de unión. Cuando la unión es un parámetro de procedimiento, el discriminador de unión debe ser otro parámetro del mismo procedimiento. Cuando la unión es un campo de una estructura, el discriminador debe ser otro campo de la estructura en el mismo nivel que el campo de unión. El discriminador debe ser [**un tipo booleano**](/windows/desktop/Midl/boolean), [**char**](/windows/desktop/Midl/char-idl), [**int**](/windows/desktop/Midl/int)o [**enum,**](/windows/desktop/Midl/enum) o un tipo que se resuelva en uno de estos tipos. Para obtener más información, vea [Nonencapsulated Unions](/windows/desktop/Midl/nonencapsulated-unions) y **\[ switch \_ is \]**.

El atributo de campo de cadena designa que un carácter unidimensional o una matriz de bytes, o un puntero a un carácter o secuencia de bytes terminados en cero, se trate **\[** [](/windows/desktop/Midl/string) **\]** como una cadena. El atributo string solo se aplica a matrices unidimensionales y punteros. El tipo de elemento se limita a [**char**](/windows/desktop/Midl/char-idl), [**byte**](/windows/desktop/Midl/byte), [**wchar \_ t**](/windows/desktop/Midl/wchar-t)o un tipo con nombre que se resuelve en uno de estos tipos.

Para obtener información sobre el contexto en el que aparecen los atributos de campo, vea [MidL Arrays](/windows/desktop/Midl/midl-arrays), [MIDL Structures](/windows/desktop/Midl/midl-structures)y [MIDL Unions](/windows/desktop/Midl/midl-unions).

 

 