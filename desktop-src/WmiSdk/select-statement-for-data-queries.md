---
description: Describir la instrucción SELECT para una consulta de datos.
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: Instrucción SELECT para consultas de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06905cfd9ef5e55022b3fc2275ed705a670a0ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706081"
---
# <a name="select-statement-for-data-queries"></a>Instrucción SELECT para consultas de datos

Puede utilizar una serie de instrucciones SELECT para consultar información. Las instrucciones pueden ser instrucciones básicas o pueden ser más restrictivas para restringir el conjunto de resultados que se devuelve de la consulta.

El ejemplo siguiente es una instrucción SELECT básica que se utiliza para consultar datos.


```sql
SELECT * FROM Class
```



Esta instrucción devuelve instancias de la clase especificada y cualquiera de sus subclases. Se incluyen todas las propiedades del sistema y definidas por el usuario para las clases. Si una propiedad del sistema no es relevante para una consulta determinada, contiene **null**.

Puede usar varias técnicas para reducir el ancho de banda necesario para recuperar el conjunto de resultados, si la ejecución de la consulta produce demasiada sobrecarga y el usuario solo está interesado en un subconjunto de las propiedades. En primer lugar, las consultas pueden reemplazar el asterisco por las propiedades deseadas.

En el ejemplo siguiente se muestra cómo consultar propiedades específicas.


```sql
SELECT property_1, property_2, property_3 FROM class
```



El conjunto de resultados incluye todas las propiedades del sistema y las propiedades que no son del sistema especificadas.

Otra técnica para limitar el ámbito del conjunto de resultados de una consulta es usar la propiedad del sistema de [**\_ \_ clase**](wmi-system-properties.md) . De forma predeterminada, las consultas devuelven todas las instancias de la clase especificada y sus subclases. Puede usar la propiedad System de **\_ \_ clase** para solicitar solo las instancias de la clase especificada, excluidas sus subclases.

En el ejemplo siguiente se muestra cómo usar la propiedad System de [**\_ \_ clase**](wmi-system-properties.md) en una cláusula WHERE.


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



También puede usar la propiedad System de [**\_ \_ clase**](wmi-system-properties.md) para restringir el conjunto de resultados a las instancias de subclases determinadas.

En el ejemplo siguiente se muestra cómo restringir el conjunto de resultados a instancias de subclases determinadas.


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> Si crea una consulta con una ruta de acceso no válida para un objeto incrustado, la consulta no devuelve ningún error ni ningún resultado.

 

En el ejemplo siguiente se devuelve una instancia de **mainclass**, suponiendo que existe una instancia de **mainclass** que contiene el objeto incrustado **EmbedObj** con una propiedad **P \_ Uint32** que es igual a "70011".


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



En el ejemplo siguiente no se devuelve ningún resultado y no se devuelve un error, suponiendo que el objeto incrustado **EmbedObj** en la instancia de **MainClass** no tiene una propiedad no **válida**.


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



