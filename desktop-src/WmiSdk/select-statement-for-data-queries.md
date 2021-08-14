---
description: Describa la instrucción SELECT para una consulta de datos.
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: Instrucción SELECT para consultas de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fec0526c5e5d47a74d6e165726222f9e521bd7102072e5a4b79e960f8dae19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315953"
---
# <a name="select-statement-for-data-queries"></a>Instrucción SELECT para consultas de datos

Puede usar una variedad de instrucciones SELECT para consultar información. Las instrucciones pueden ser instrucciones básicas o pueden ser más restrictivas para restringir el conjunto de resultados que se devuelve de la consulta.

El ejemplo siguiente es una instrucción SELECT básica que se usa para consultar datos.


```sql
SELECT * FROM Class
```



Esta instrucción devuelve instancias de la clase especificada y cualquiera de sus subclases. Se incluyen todas las propiedades definidas por el usuario y del sistema para las clases. Si una propiedad del sistema no es relevante para una consulta determinada, contiene **NULL.**

Puede usar varias técnicas para reducir el ancho de banda necesario para recuperar el conjunto de resultados, si la ejecución de la consulta genera demasiada sobrecarga y el usuario solo está interesado en un subconjunto de las propiedades. En primer lugar, las consultas pueden reemplazar el asterisco por las propiedades deseadas.

En el ejemplo siguiente se muestra cómo consultar propiedades específicas.


```sql
SELECT property_1, property_2, property_3 FROM class
```



El conjunto de resultados incluye todas las propiedades del sistema y las propiedades no del sistema especificadas.

Otra técnica para restringir el ámbito del conjunto de resultados de una consulta es usar la [**\_ \_ propiedad del sistema CLASS.**](wmi-system-properties.md) De forma predeterminada, las consultas devuelven todas las instancias de la clase especificada y sus subclases. Puede usar la propiedad del sistema **\_ \_ CLASS** para solicitar solo instancias de la clase especificada, excepto sus subclases.

En el ejemplo siguiente se muestra cómo usar la [**\_ \_ propiedad del**](wmi-system-properties.md) sistema CLASS en una cláusula WHERE.


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



También puede usar la propiedad del sistema [**\_ \_ CLASS**](wmi-system-properties.md) para restringir el conjunto de resultados a instancias de subclases concretas.

En el ejemplo siguiente se muestra cómo restringir el conjunto de resultados a instancias de subclases concretas.


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> Si construye una consulta con una ruta de acceso no válida para un objeto incrustado, la consulta no devuelve un error ni ningún resultado.

 

En el ejemplo siguiente se devuelve una instancia de **MainClass**, suponiendo que existe una instancia de **MainClass** que contiene el objeto **incrustado EmbedObj** con una propiedad **P \_ Uint32** que es igual a "70011".


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



En el ejemplo siguiente no se devuelve ningún resultado y no se devuelve un error, suponiendo que el objeto **incrustado EmbedObj** en la instancia de **MainClass** no tiene una propiedad **INVALID**.


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



