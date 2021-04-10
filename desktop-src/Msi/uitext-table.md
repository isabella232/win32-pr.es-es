---
description: La tabla UIText contiene las versiones localizadas de algunas de las cadenas usadas en la interfaz de usuario. Estas cadenas no forman parte de ninguna otra tabla. La tabla UIText es para las cadenas que no tienen ninguna posición lógica en ninguna otra tabla.
ms.assetid: 2965e3a8-2cbf-4445-963b-ec2040692106
title: Tabla UIText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5fe8bbdec694511103636508d229ab0d2e40afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153737"
---
# <a name="uitext-table"></a>Tabla UIText

La tabla UIText contiene las versiones localizadas de algunas de las cadenas usadas en la interfaz de usuario. Estas cadenas no forman parte de ninguna otra tabla. La tabla UIText es para las cadenas que no tienen ninguna posición lógica en ninguna otra tabla.

La tabla UIText tiene las columnas siguientes.



| Columna | Tipo                         | Clave | Nullable |
|--------|------------------------------|-----|----------|
| Clave    | [Identificador](identifier.md) | Y   | N        |
| Texto   | [Texto](text.md)             | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave
</dt> <dd>

Una clave única que identifica la cadena determinada.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Negrita
</dt> <dd>

Versión localizada de la cadena.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Algunos controles usan la tabla UIText como origen de cadenas. Para obtener información sobre qué cadenas son necesarias en esta tabla para cada control concreto, vea los controles individuales en la referencia de la [interfaz de usuario](user-interface-reference.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



