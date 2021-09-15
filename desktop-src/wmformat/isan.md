---
title: ISAN
description: El atributo ISAN contiene el número de norma internacional (ISAN) que identifica el contenido.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- Formato de windows Media de ISAN
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dc4a850edc43178deb043143ee8f9b37140507
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466699"
---
# <a name="isan"></a>ISAN

El **atributo ISAN** contiene el número de norma internacional (ISAN) que identifica el contenido.

## <a name="global-constant"></a>Constante global

g \_ wszISAN

## <a name="data-type"></a>Tipo de datos

**CADENA DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Observaciones

ISAN es un estándar internacional para identificar los trabajos del intérprete. Para obtener información sobre ISAN, visite el sitio [web del estándar](https://www.isan.org/).

El objeto del editor de metadatos comprueba la cadena ISAN al establecer este atributo. El formato de cadena aceptable, como se describe en la sección 4.1 de la especificación ISAN, consta de 16 dígitos hexadecimales, separados opcionalmente por espacios en blanco o guiones en segmentos de 4 dígitos. El número con formato debe ir seguido, también opcionalmente, de un espacio o guion, por un carácter de comprobación válido. El carácter de comprobación puede ser un dígito decimal o una letra mayúscula. Consulte el anexo A de la guía del usuario de ISAN para obtener información sobre cómo derivar el número de comprobación.

La cadena ISAN estándar puede estar seguida de la información de versión. Si está presente, la información de versión consta de ocho dígitos hexadecimales seguidos de un número de comprobación. El formato de estos caracteres sigue las mismas reglas que la cadena básica.

## <a name="examples"></a>Ejemplos

Las siguientes son tres cadenas con formato aceptable para un ISAN de ejemplo.


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



La cadena siguiente muestra el formato de un ISAN con información de versión.


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




