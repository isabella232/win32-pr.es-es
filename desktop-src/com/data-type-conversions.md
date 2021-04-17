---
title: Conversiones de tipos de datos
description: Conversiones de tipos de datos
ms.assetid: 54688ee9-2dd7-466b-b278-13d6f9d1e6ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8135a3fb86fda9ac9ab9666ec42991a8d04d9e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705040"
---
# <a name="data-type-conversions"></a>Conversiones de tipos de datos

Cada lenguaje de programación define determinados tipos y contenedores para los datos. La mayoría de estos tipos de datos, especialmente los primitivos, se asignan fácilmente a otros lenguajes de programación. Sin embargo, algunos tipos de datos no tienen ningún equivalente en otro lenguaje y no se pueden convertir.

Para obtener información específica acerca de los tipos de datos que el lenguaje de programación no reconoce, vea los temas siguientes:

-   [Traducir a C++](translating-to-c--.md)
-   [Trasladar a Visual Basic](translating-to-visual-basic.md)
-   [Traducir a Java](translating-to-java.md)

En la tabla siguiente se enumeran las conversiones entre los lenguajes de programación para tipos de datos comunes.



| C++                                     | Visual Basic             | Java                               | Contiene                                                                                       |
|-----------------------------------------|--------------------------|------------------------------------|------------------------------------------------------------------------------------------------|
| **signed char**<br/>              | No compatible<br/> | **byte**<br/>                | entero de 1 byte con signo <br/> (VT \_ I1, \[ T \] )<br/>                                   |
| **unsigned char**<br/>            | **Byte**<br/>      | No compatible<br/>           | entero de 1 byte sin signo <br/> (VT \_ UI1, \[ V \] \[ T \] \[ \] \[ S \] )<br/>                 |
| **unsigned char**<br/>            | **Carácter**<br/> | **char**<br/>                | carácter Unicode de 2 bytes <br/> (VT \_ UI2, \[ T \] \[ P \] )<br/>                          |
| **short**<br/>                    | **Entero**<br/>   | **short**<br/>               | entero de 2 bytes con signo <br/> (VT \_ I2, \[ V \] \[ T \] \[ \] \[ S \] )<br/>                    |
| **unsigned short**<br/>           | No compatible<br/> | No compatible<br/>           | entero de 2 bytes sin signo <br/> (VT \_ UI2, \[ T \] \[ P \] )<br/>                           |
| **int**<br/>                      | **Long**<br/>      | **int**<br/>                 | entero de 4 bytes con signo <br/> (VT \_ I4, \[ V \] \[ T \] \[ \] \[ S \] )<br/>                    |
| **unsigned int**<br/>             | No compatible<br/> | No compatible<br/>           | entero de 4 bytes sin signo <br/> (VT \_ UI4, \[ T \] \[ P \] )<br/>                           |
| **\_\_Int64**<br/>                | No compatible<br/> | **long**<br/>                | entero de 8 bytes con signo <br/> (VT \_ I8, \[ T \] \[ P \] )<br/>                              |
| **unsigned \_ \_ Int64**<br/>       | No compatible<br/> | No compatible<br/>           | entero de 8 bytes sin signo <br/> (VT \_ UI8, \[ T \] \[ P \] )<br/>                           |
| **float**<br/>                    | **Single**<br/>    | **float**<br/>               | número de punto flotante de 4 bytes <br/> (VT \_ R4, \[ V \] \[ T \] \[ \] \[ S \] )<br/>             |
| **double**<br/>                   | **Double**<br/>    | **double**<br/>              | número de punto flotante de 8 bytes <br/> (VT \_ R8, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>             |
| **UTILICEN**<br/>                     | **String**<br/>    | **Java. lang. String**<br/>    | Cadena de automatización <br/> (VT \_ BSTR, \[ V \] \[ T \] \[ \] \[ S \] )<br/>                      |
| **BOOLEANO**<br/>                     | **Boolean**<br/>   | **boolean**<br/>             | Boolean <br/> (VT \_ BOOL, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                                |
| **VARIANTE**<br/>                  | **Variante**<br/>   | **com. ms. com. Variant**<br/>  | VARIANTE DEL EXTREMO\* <br/> (VT \_ VARIANTE, \[ V \] \[ T \] \[ \] \[ S \] )<br/>                       |
| [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)<br/> | **object**<br/>    | **com. ms. com. IUnknown**<br/> | Puntero de interfaz IDispatch <br/> (VT \_ ENVÍO, \[ V \] \[ T \] \[ \] \[ S \] )<br/>        |
| **DATE**<br/>                     | **Date**<br/>      | **com. ms. com. Variant**<br/>  | Fecha <br/> (VT \_ FECHA, \[ V \] \[ T \] \[ \] \[ S \] )<br/>                                   |
| **CURRENCY**<br/>                 | **Moneda**<br/>  | **com. ms. com. Variant**<br/>  | Moneda <br/> (VT \_ CY, \[ v \] \[ t \] \[ \] \[ \] o VT \_ decimal, \[ v \] \[ t \] \[ s \] )<br/> |



 

Para obtener información sobre los valores de VARTYPE y cómo usarlos, vea el tema [tipos de datos y estructuras de IDispatch](/previous-versions/ms221600(v=vs.100)).

Las conversiones de tipos de datos entre los lenguajes de scripting son más sencillas que las de los lenguajes de programación. JScript y JavaScript admiten los mismos tipos de datos y VBScript solo admite un tipo de datos único, **Variant**. Por lo tanto, todos los tipos de datos de JScript y JavaScript se convierten en tipos **variantes** cuando se convierten en VBScript. Al convertir VBScript en JScript o JavaScript, los tipos de **variante** se convierten en números, cadenas, valores booleanos, etc.

 

