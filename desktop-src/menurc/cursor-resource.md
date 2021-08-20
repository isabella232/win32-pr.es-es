---
title: Recurso CURSOR
description: Define un mapa de bits que define la forma del cursor en la pantalla o un cursor animado.
ms.assetid: c087abca-5502-4625-8c9b-464e1718571f
keywords:
- Menús de recursos CURSOR y otros recursos
topic_type:
- apiref
api_name:
- CURSOR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc993317d154a3b769f071b7c7187a2cf71d188dd7e73ac834bbec4874c89f91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687922"
---
# <a name="cursor-resource"></a>Recurso CURSOR

Define un mapa de bits que define la forma del cursor en la pantalla o un cursor animado.

``` syntax
nameID CURSOR filename
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nombre único o entero de 16 bits sin signo que identifica el recurso.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Nombre*
</dt> <dd>

Nombre del archivo que contiene el recurso. El nombre debe ser un nombre de archivo válido; debe ser una ruta de acceso completa si el archivo no está en el directorio de trabajo actual. La ruta de acceso debe ser una cadena entre comillas.

</dd> </dl>

Algunos atributos también se admiten por compatibilidad con versiones anteriores. Para más información, consulte [Atributos de recursos comunes.](common-resource-attributes.md)

## <a name="remarks"></a>Comentarios

Los recursos de icono y cursor pueden contener más de una imagen.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se definen dos recursos de cursor; uno por nombre (cursor1) y el otro por número (2):

``` syntax
cursor1 CURSOR "bullseye.cur"
2       CURSOR "d:\\cursor\\arrow.cur" 
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de cursores](./using-cursors.md)
</dt> </dl>

 

 