---
title: Recurso MESSAGETABLE
description: Define el identificador y el archivo del recurso de tabla de mensajes de una aplicación. Las tablas de mensajes son recursos de cadena especiales que se usan en el registro de eventos y con la función FormatMessage. El archivo contiene una tabla de mensajes binarios generada por el compilador de mensajes, MC.EXE.
ms.assetid: c379cfff-23bf-4750-8d7a-d5c3c6783921
keywords:
- Menús de recursos MESSAGETABLE y otros recursos
topic_type:
- apiref
api_name:
- MESSAGETABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378860e10ab6da929147e13a8120ee169204276e3c609b20176c22df9de15dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886725"
---
# <a name="messagetable-resource"></a>Recurso MESSAGETABLE

Define el identificador y el archivo del recurso de tabla de mensajes de una aplicación. Las tablas de mensajes son recursos de cadena especiales que se usan en el registro de eventos y con la [**función FormatMessage.**](/windows/desktop/api/winbase/nf-winbase-formatmessage) El archivo contiene una tabla de mensajes binarios generada por el compilador de mensajes, MC.EXE.

El compilador de mensajes también genera un archivo de script de recursos que contiene las instrucciones **MESSAGETABLE** que necesita para incluir los recursos de la tabla de mensajes en el archivo de recursos compilado. Use la [**\# directiva include**](-include.md) para incluir este script de recursos en el script de recursos principal.

``` syntax
nameID MESSAGETABLE filename
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nombre único o un valor entero de 16 bits sin signo que identifica el recurso.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Nombre*
</dt> <dd>

Nombre del archivo que contiene el recurso. El nombre debe ser un nombre de archivo válido; debe ser una ruta de acceso completa si el archivo no está en el directorio de trabajo actual.

</dd> </dl>

Algunos atributos también se admiten para la compatibilidad con versiones anteriores. Para obtener más información, vea [Atributos de recursos comunes](common-resource-attributes.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se define **un recurso MESSAGETABLE:**

``` syntax
1  MESSAGETABLE MSG00409.bin
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 