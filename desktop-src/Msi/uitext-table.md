---
description: La tabla UIText contiene las versiones localizadas de algunas de las cadenas usadas en la interfaz de usuario. Estas cadenas no forman parte de ninguna otra tabla. La tabla UIText es para las cadenas que no tienen ningún lugar lógico en ninguna otra tabla.
ms.assetid: 2965e3a8-2cbf-4445-963b-ec2040692106
title: UIText Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ab939c9539b95528a574015e45e4f8aeae435b33405d054d8d7ff1756b580
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810335"
---
# <a name="uitext-table"></a>UIText Table

La tabla UIText contiene las versiones localizadas de algunas de las cadenas usadas en la interfaz de usuario. Estas cadenas no forman parte de ninguna otra tabla. La tabla UIText es para las cadenas que no tienen ningún lugar lógico en ninguna otra tabla.

La tabla UIText tiene las columnas siguientes.



| Columna | Tipo                         | Clave | Nullable |
|--------|------------------------------|-----|----------|
| Clave    | [Identificador](identifier.md) | Y   | N        |
| Texto   | [Texto](text.md)             | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave
</dt> <dd>

Clave única que identifica la cadena determinada.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

Versión localizada de la cadena.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Algunos controles usan la tabla UIText como origen de cadenas. Para obtener información sobre qué cadenas son necesarias en esta tabla para cada control determinado, vea los controles individuales en la [Interfaz de usuario referencia](user-interface-reference.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



