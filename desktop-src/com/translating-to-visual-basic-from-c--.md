---
title: Trasladar a Visual Basic de C++
description: Trasladar a Visual Basic de C++
ms.assetid: fce7ea25-cb24-4cc4-8f36-0e8aed2f3ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba519cbdb0305fe3a2eae4cc8e658fdde1eac3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656287"
---
# <a name="translating-to-visual-basic-from-c"></a>Trasladar a Visual Basic de C++

Mediante el lenguaje de programación C++, los desarrolladores pueden acceder directamente a la memoria que almacena una variable determinada. Los punteros de memoria proporcionan este acceso directo. En Visual Basic, los punteros se controlan automáticamente. Por ejemplo, un parámetro declarado como un puntero a un **int** en C++ es equivalente a un parámetro declarado en Visual Basic como un  **entero** de ByRef.

Un parámetro declarado **como String** en Visual Basic se declara como un puntero a un **BSTR** en C++. Establecer un puntero de cadena en **null** en C++ es equivalente a establecer la cadena en la constante **vbNullString** en Visual Basic. Pasar una cadena de longitud cero ("") a una función diseñada para recibir **null** no funciona, ya que pasa un puntero a una cadena de longitud cero en lugar de un puntero cero.

C++ admite contenedores de datos, es decir, estructuras y uniones, que no tienen ningún equivalente en versiones anteriores de Visual Basic. Por esta razón, los objetos COM normalmente encapsulan información que normalmente se almacena en estructuras y uniones en clases de objeto. Sin embargo, algunos objetos COM pueden contener estructuras, lo que hace que no se pueda tener acceso a partes de los métodos o la funcionalidad del objeto para Visual Basic.

Algunos tipos de datos de C++ no se admiten en Visual Basic, por ejemplo tipos sin signo y tipos **hWnd** . Los métodos que aceptan o devuelven estos tipos de datos no están disponibles en Visual Basic.

Visual Basic usa tipos de datos compatibles con la automatización como sus tipos de datos internos. Por lo tanto, los tipos de datos de C++ que son compatibles con la automatización también son compatibles con Visual Basic. Es posible que los tipos de datos que no son compatibles con la automatización no se puedan convertir en Visual Basic.

En la tabla siguiente se enumeran los tipos de datos admitidos por Visual Basic y sus equivalentes de **VARTYPE** . **VARTYPE** es una enumeración que enumera los tipos de variante de automatización.



| Tipo de datos en Visual Basic  | Equivalente de VARTYPE                |
|-------------------------|-----------------------------------|
| **Entero**<br/>  | I2 de 16 bits, con signo y VT \_<br/> |
| **Long**<br/>     | 32 bits, con signo, VT \_ I4<br/> |
| **Date**<br/>     | fecha de VT \_<br/>               |
| **Moneda**<br/> | VT \_ CY<br/>                 |
| **Object**<br/>   | \*distribución de VT \_<br/>         |
| **String**<br/>   | VT \_ BSTR<br/>               |
| **Boolean**<br/>  | VT \_ bool<br/>               |
| **Moneda**<br/> | VT \_ decimal<br/>            |
| **Single**<br/>   | VT \_ R4<br/>                 |
| **Double**<br/>   | VT \_ R8<br/>                 |
| **Decimal**<br/>  | VT \_ decimal<br/>            |
| **Byte**<br/>     | VT \_ decimal<br/>            |
| **Variante**<br/>  | VT ( \_ variante)<br/>            |



 

Todos los parámetros de Visual Basic, a menos que se etiqueten con la palabra clave **ByVal**, se pasan por referencia (como punteros) en lugar de por valor.

C++ y Visual Basic difieren ligeramente en la forma en que representan las propiedades. En C++, las propiedades se representan como un conjunto de funciones de descriptor de acceso, una que establece el valor de propiedad y otra que recupera el valor de propiedad. En Visual Basic, las propiedades se representan como un único elemento que se puede utilizar para recuperar o establecer el valor de la propiedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trasladar a Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 





