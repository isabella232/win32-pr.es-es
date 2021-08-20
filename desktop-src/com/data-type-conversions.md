---
title: Conversiones de tipos de datos
description: Conversiones de tipos de datos
ms.assetid: 54688ee9-2dd7-466b-b278-13d6f9d1e6ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a978126cd6cb9beaf718c3d6013d86d9efa7b58c50f8d75a7cae79dc5c1543
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919615"
---
# <a name="data-type-conversions"></a>Conversiones de tipos de datos

Cada lenguaje de programación define determinados tipos y contenedores para los datos. La mayoría de estos tipos de datos, especialmente los primitivos, se asignan fácilmente a otros lenguajes de programación. Sin embargo, algunos tipos de datos no tienen ningún equivalente en otro idioma y no se pueden convertir.

Para obtener información específica sobre los tipos de datos no reconocidos por el lenguaje de programación, vea los temas siguientes:

-   [Traducción a C++](translating-to-c--.md)
-   [Traducción a Visual Basic](translating-to-visual-basic.md)
-   [Traducción a Java](translating-to-java.md)

En la tabla siguiente se enumeran las conversiones entre lenguajes de programación para tipos de datos comunes.



| C++                                     | Visual Basic             | Java                               | Contiene                                                                                       |
|-----------------------------------------|--------------------------|------------------------------------|------------------------------------------------------------------------------------------------|
| **signed char**<br/>              | No compatible<br/> | **byte**<br/>                | Entero con signo de 1 byte <br/> (VT) \_ I1, \[ T \] )<br/>                                   |
| **unsigned char**<br/>            | **Byte**<br/>      | No compatible<br/>           | Entero sin signo de 1 byte <br/> (VT) \_ UI1, \[ V T P S \] \[ \] \[ \] \[ \] )<br/>                 |
| **unsigned char**<br/>            | **Carácter**<br/> | **char**<br/>                | Carácter Unicode de 2 bytes <br/> (VT) \_ UI2, \[ T \] \[ P \] )<br/>                          |
| **short**<br/>                    | **Entero**<br/>   | **short**<br/>               | Entero de 2 bytes con signo <br/> (VT) \_ I2, \[ V T P S \] \[ \] \[ \] \[ \] )<br/>                    |
| **unsigned short**<br/>           | No compatible<br/> | No compatible<br/>           | Entero sin signo de 2 bytes <br/> (VT) \_ UI2, \[ T \] \[ P \] )<br/>                           |
| **int**<br/>                      | **Long**<br/>      | **int**<br/>                 | Entero de 4 bytes con signo <br/> (VT) \_ I4, \[ V T P S \] \[ \] \[ \] \[ \] )<br/>                    |
| **unsigned int**<br/>             | No compatible<br/> | No compatible<br/>           | Entero sin signo de 4 bytes <br/> (VT) \_ UI4, \[ T \] \[ P \] )<br/>                           |
| **\_\_int64**<br/>                | No compatible<br/> | **long**<br/>                | Entero de 8 bytes con signo <br/> (VT) \_ I8, \[ T \] \[ P \] )<br/>                              |
| **unsigned \_ \_ int64**<br/>       | No compatible<br/> | No compatible<br/>           | Entero de 8 bytes sin signo <br/> (VT) \_ UI8, \[ T \] \[ P \] )<br/>                           |
| **float**<br/>                    | **Single**<br/>    | **float**<br/>               | Número de punto flotante de 4 bytes <br/> (VT) \_ R4, \[ V T P S \] \[ \] \[ \] \[ \] )<br/>             |
| **double**<br/>                   | **Double**<br/>    | **double**<br/>              | Número de punto flotante de 8 bytes <br/> (VT) \_ R8, \[ V T P S \] \[ \] \[ \] \[ \] )<br/>             |
| **Bstr**<br/>                     | **String**<br/>    | **java.lang.String**<br/>    | Cadena de Automation <br/> (VT) \_ BSTR, \[ V T P S \] \[ \] \[ \] \[ \] )<br/>                      |
| **Bool**<br/>                     | **Boolean**<br/>   | **boolean**<br/>             | Boolean <br/> (VT) \_ BOOL, \[ V T P S \] \[ \] \[ \] \[ \] )<br/>                                |
| **Variante**<br/>                  | **Variante**<br/>   | **com.ms.com.Variant**<br/>  | VARIANT FAR\* <br/> (VT) \_ VARIANT, \[ V T P S \] \[ \] \[ \] \[ \] )<br/>                       |
| [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)<br/> | **object**<br/>    | **com.ms.com.IUnknown**<br/> | Puntero de interfaz IDispatch <br/> (VT) \_ DISPATCH, \[ V T P S \] \[ \] \[ \] \[ \] )<br/>        |
| **DATE**<br/>                     | **Fecha**<br/>      | **com.ms.com.Variant**<br/>  | Date <br/> (VT) \_ DATE, \[ V T P S \] \[ \] \[ \] \[ \] )<br/>                                   |
| **CURRENCY**<br/>                 | **Moneda**<br/>  | **com.ms.com.Variant**<br/>  | Moneda <br/> (VT) \_ CY, \[ V T P S o VT \] \[ \] \[ \] \[ \] \_ DECIMAL, V T \[ S \] \[ \] \[ \] )<br/> |



 

Para obtener información sobre los valores VARTYPE y cómo usarlos, vea el tema [IDispatch Data Types and Structures](/previous-versions/ms221600(v=vs.100)).

Las conversiones de tipos de datos entre lenguajes de scripting son más sencillas que las de los lenguajes de programación. JScript y JavaScript admiten los mismos tipos de datos, y VBScript solo admite un tipo de datos único, **Variant**. Por lo tanto, todos JScript de datos de JavaScript y se convierten en **tipos Variant** cuando se convierten a VBScript. Al convertir VBScript a JScript o JavaScript, los tipos **Variant** se convierten en números, cadenas, valores booleanos, y así sucesivamente.

 

