---
description: Las palabras clave ALL BITWISE y SOME BITWISE se usan para probar los bits en un tipo entero.
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: TODO BIT A BIT Y ALGO BIT A BIT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac133e04eae78fe9b943c1e354d9e4dcf451640ad60be1883eecc938ec1d418a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594725"
---
# <a name="all-bitwise-and-some-bitwise"></a>TODO BIT A BIT Y ALGO BIT A BIT

Las **palabras clave ALL BITWISE** y SOME **BITWISE** se usan para probar los bits en un tipo entero. Si todos los bits establecidos en una propiedad coinciden con la máscara, **ALL BITWISE** es true. Si al menos uno de los bits establecidos en una propiedad coincide con la máscara, **SOME BITWISE** es true.

Los operadores se pueden aplicar tanto a propiedades escalares (de un solo valor) como a propiedades vectoriales (de varios valores). En el ejemplo de código siguiente se muestra cómo probar los valores de propiedad **con ALL BITWISE** y **SOME BITWISE**.


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a>Operadores de comparación

Los operadores de comparación admitidos para las pruebas BITWISE se enumeran en la tabla siguiente.



| Operadores de comparación | Descripción  |
|---------------------|--------------|
| =                   | Igual a     |
| != o <>      | No es igual a |



 

La lógica de las pruebas BITWISE se muestra en la tabla siguiente.



| Operador de prueba y comparación BITWISE | Lógica                   |
|--------------------------------------|-------------------------|
| = ALL BIT A BIT                        | Property & Mask = Mask  |
| = ALGO BIT A BIT                       | Property & Mask != 0    |
| <> TODO BIT A BIT                 | Máscara & propiedades != Mask |
| <> BIT A BIT                | Máscara & propiedades = 0     |



 

En la siguiente tabla truth se usan valores binarios y hexadecimales de ejemplo para restablecer la lógica de las pruebas BITWISE.



| Propiedad en binario (hexadecimal) | Máscara en binario (hexadecimal) | Property & Mask = binary (hexadecimal) | = ALGO BIT A BIT | = ALL BIT A BIT |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| 0001 (0x1)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0001 (0x1)               | 0011 (0x3)           | 0001 (0x1)                     | Verdadero           | Falso         |
| 0011 (0x3)               | 0001 (0x1)           | 0001 (0x1)                     | True           | True          |
| 0010 (0x2)               | 0001 (0x1)           | 0000 (0x0)                     | Falso          | False         |
| 11110000 (0xF0)          | 00000011 (0x03)      | 00000000 (0x00)                | Falso          | False         |
| 11110010 (0xF2)          | 11110010 (0xF2)      | 11110010 (0xF2)                | True           | True          |
| 11110010 (0xF2)          | 00000011 (0x03)      | 00000010 (0x02)                | Verdadero           | Falso         |



 

## <a name="example"></a>Ejemplo

A continuación se muestra un ejemplo **del predicado ALL BITWISE.**


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



