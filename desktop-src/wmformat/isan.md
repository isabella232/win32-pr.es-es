---
title: ISAN
description: El atributo ISAN contiene el número audiovisual estándar internacional (ISAN) que identifica el contenido.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- Formato de Windows Media de ISAN
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dc4a850edc43178deb043143ee8f9b37140507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420361"
---
# <a name="isan"></a>ISAN

El atributo **ISAN** contiene el número audiovisual estándar internacional (ISAN) que identifica el contenido.

## <a name="global-constant"></a>Constante global

g \_ wszISAN

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

ISAN es un estándar internacional para identificar trabajos audiovisuales. Para obtener información acerca de ISAN, visite el [sitio web](https://www.isan.org/)del estándar.

El objeto editor de metadatos comprueba la cadena de ISAN al establecer este atributo. El formato de cadena aceptable, como se describe en la sección 4,1 de la especificación de ISAN, consta de 16 dígitos hexadecimales, separados por espacios en blanco o guiones en segmentos de 4 dígitos. Se debe seguir el número con formato, opcionalmente separado por un espacio o un guión, mediante un carácter de comprobación válido. El carácter de verificación puede ser un dígito decimal o una letra mayúscula. Consulte el anexo a de la guía de usuario de ISAN para obtener información sobre cómo derivar el número de marca.

La cadena de ISAN estándar puede ir seguida de la información de versión. Si está presente, la información de versión consta de ocho dígitos hexadecimales seguidos de un número de comprobación. El formato de estos caracteres sigue las mismas reglas que la cadena básica.

## <a name="examples"></a>Ejemplos

A continuación se muestran tres cadenas con formato aceptable para un ejemplo de ISAN.


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



La cadena siguiente muestra el formato de un ISAN con información de versión.


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




