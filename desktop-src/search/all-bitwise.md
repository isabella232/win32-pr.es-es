---
description: ALL bit a bit y algunas palabras clave bit a bit se usan para probar los bits en un tipo entero.
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: ALL bit a bit y SOME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709db4829f5b620bcb14e0b4261fac7e7d9a6f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540654"
---
# <a name="all-bitwise-and-some-bitwise"></a>ALL bit a bit y SOME

**All bit a bit** y algunas palabras clave **bit a bit** se usan para probar los bits en un tipo entero. Si todos los bits establecidos en una propiedad coinciden con la máscara, **All bit a bit** es true. Si al menos uno de los bits establecidos en una propiedad coincide con la máscara, **algún bit a bit** es true.

Los operadores se pueden aplicar tanto a las propiedades escalares (de valor único) como a las propiedades de vector (varios valores). En el ejemplo de código siguiente se muestra cómo se prueban los valores de propiedad con **todos los** **bits y bit a bit.**


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a>Operadores de comparación

En la tabla siguiente se enumeran los operadores de comparación admitidos para las pruebas bit a bit.



| Operadores de comparación | Descripción  |
|---------------------|--------------|
| =                   | Igual a     |
| ! = o <>      | No es igual a |



 

En la tabla siguiente se muestra la lógica de las pruebas bit a bit.



| Operador de comparación y prueba bit a bit | Lógica                   |
|--------------------------------------|-------------------------|
| = ALL BIT A BIT                        | Propiedad & Máscara = máscara  |
| = ALGUNOS BITS                       | Propiedad & máscara! = 0    |
| <> TODOS LOS BITS                 | Propiedad & Mask! = Mask |
| <> ALGUNOS BITS                | Propiedad & máscara = 0     |



 

La siguiente tabla de verdad usa valores binarios y hexadecimales de ejemplo para demostrar la lógica de las pruebas bit a bit.



| Propiedad en binario (hex) | Máscara en binario (hex) | Propiedad & máscara = binaria (hexadecimal) | = ALGUNOS BITS | = ALL BIT A BIT |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| 0001 (0x1)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0001 (0x1)               | 0011 (0X3)           | 0001 (0x1)                     | True           | False         |
| 0011 (0X3)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0010 (0X2)               | 0001 (0x1)           | 0000 (0X0)                     | False          | False         |
| 11110000 (0xF0)          | 00000011 (0x03)      | 00000000 (0x00)                | False          | False         |
| 11110010 (0xF2)          | 11110010 (0xF2)      | 11110010 (0xF2)                | True           | True          |
| 11110010 (0xF2)          | 00000011 (0x03)      | 00000010 (0x02)                | True           | False         |



 

## <a name="example"></a>Ejemplo

El siguiente es un ejemplo del predicado **bit a bit All** .


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



