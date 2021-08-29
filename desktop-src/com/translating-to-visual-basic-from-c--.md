---
title: Traducción a Visual Basic desde C++
description: Traducción a Visual Basic desde C++
ms.assetid: fce7ea25-cb24-4cc4-8f36-0e8aed2f3ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2514c2428ff69b6cffa550a3976119b36e100c0f7eb30b05e8ae7beb40193194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372805"
---
# <a name="translating-to-visual-basic-from-c"></a>Traducción a Visual Basic desde C++

Con el lenguaje de programación C++, los desarrolladores pueden acceder directamente a la memoria que almacena una variable determinada. Los punteros de memoria proporcionan este acceso directo. En Visual Basic, los punteros se controlan por usted. Por ejemplo, un parámetro declarado como puntero a un **valor int** en C++ es equivalente a un parámetro declarado en Visual Basic como un **entero ByRef** **.**

Un parámetro que se declara **como cadena** en Visual Basic se declara como puntero a **un BSTR** en C++. Establecer un puntero de cadena en **NULL** en C++ equivale a establecer la cadena en la **constante vbNullString** en Visual Basic. Pasar una cadena de longitud cero ("") a una función diseñada para recibir **NULL** no funciona, ya que pasa un puntero a una cadena de longitud cero en lugar de a un puntero de cero.

C++ admite contenedores de datos, es decir, estructuras y uniones, que no tienen equivalentes en las primeras versiones de Visual Basic. Por esta razón, los objetos COM normalmente encapsulan información que normalmente se almacena en estructuras y uniones en clases de objeto. Sin embargo, algunos objetos COM pueden contener estructuras, lo que hace que algunas partes de los métodos o la funcionalidad del objeto no sean accesibles para Visual Basic.

Algunos tipos de datos de C++ no se admiten Visual Basic, por ejemplo, tipos sin signo y **tipos HWND.** Los métodos que aceptan o devuelven estos tipos de datos no están disponibles en Visual Basic.

Visual Basic tipos de datos compatibles con Automation como sus tipos de datos internos. Por lo tanto, los tipos de datos de C++ compatibles con Automation también son compatibles con Visual Basic. Es posible que los tipos de datos que no son compatibles con Automation no se puedan convertir a Visual Basic.

En la tabla siguiente se enumeran los tipos de datos admitidos por Visual Basic y sus **equivalentes VARTYPE.** **VARTYPE es** una enumeración que enumera los tipos de variantes de Automation.



| Tipo de datos en Visual Basic  | EQUIVALENTE DE VARTYPE                |
|-------------------------|-----------------------------------|
| **Entero**<br/>  | 16 bits, firmado, VT \_ I2<br/> |
| **Long**<br/>     | 32 bits, firmado, VT \_ I4<br/> |
| **Fecha**<br/>     | FECHA \_ DE VT<br/>               |
| **Moneda**<br/> | VT \_ CY<br/>                 |
| **Object**<br/>   | \*VT \_ DISPATCH<br/>         |
| **String**<br/>   | VT \_ BSTR<br/>               |
| **Boolean**<br/>  | VT \_ BOOL<br/>               |
| **Moneda**<br/> | VT \_ DECIMAL<br/>            |
| **Single**<br/>   | VT \_ R4<br/>                 |
| **Double**<br/>   | VT \_ R8<br/>                 |
| **Decimal**<br/>  | VT \_ DECIMAL<br/>            |
| **Byte**<br/>     | VT \_ DECIMAL<br/>            |
| **Variante**<br/>  | VT \_ VARIANT<br/>            |



 

Todos los parámetros Visual Basic, a menos que estén etiquetados con la palabra clave **ByVal**, se pasan por referencia (como punteros) en lugar de por valor.

C++ y Visual Basic difieren ligeramente en cómo representan las propiedades. En C++, las propiedades se representan como un conjunto de funciones de accessor, una que establece el valor de propiedad y otra que recupera el valor de propiedad. En Visual Basic, las propiedades se representan como un único elemento que se puede usar para recuperar o establecer el valor de propiedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducción a Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 





