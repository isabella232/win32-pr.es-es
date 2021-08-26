---
description: La tabla ProgId contiene información sobre los identificadores de programa y los identificadores de programa independientes de la versión que se deben generar como parte del anuncio del producto.
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: Tabla ProgId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbed8baea9bd8421757cf2e31f0ba06679db3394c95f732537a7e230c02b5ee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042065"
---
# <a name="progid-table"></a>Tabla ProgId

La tabla ProgId contiene información sobre los identificadores de programa y los identificadores de programa independientes de la versión que se deben generar como parte del anuncio del producto.

La tabla ProgId tiene las columnas siguientes.



| Columna         | Tipo                         | Clave | Nullable |
|----------------|------------------------------|-----|----------|
| ProgId         | [Texto](text.md)             | Y   | N        |
| ProgId \_ (elemento primario) | [Texto](text.md)             | N   | Y        |
| Clase\_        | [GUID](guid.md)             | N   | Y        |
| Descripción    | [Texto](text.md)             | N   | Y        |
| Icono\_         | [Identificador](identifier.md) | N   | Y        |
| IconIndex      | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>Progid
</dt> <dd>

El identificador de programa o el identificador de programa independiente de la versión. Los ProgIds enumerados en la tabla ProgId se registran si el CLSID que aparece en la columna Clase de esta tabla está programado para anunciarse \_ o instalarse. Cuando el ProgId está seleccionado para el registro, también se seleccionan para el registro todos los ProgId que hacen referencia a esta fila a través de la columna ProgId \_ Parent.

</dd> <dt>

<span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId \_ (elemento primario)
</dt> <dd>

Se define solo para los iD de programa independientes de la versión. Este campo es una clave externa en la columna ProgId. Para definir un identificador de programa independiente de la versión, escriba el ProgId correspondiente en la columna \_ ProgId Parent . Cuando se selecciona el ProgId para la instalación, también se seleccionan para el registro los ProgId independientes de la versión correspondientes asociados a través de la columna ProgId \_ Parent.

</dd> <dt>

<span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Clase\_
</dt> <dd>

Clave externa opcional en la [tabla Class](class-table.md). Esta columna debe ser Null para un ProgId independiente de la versión. Si el valor class de un ProgId es null, el ProgId se registra cuando aparece en la columna ProgId de una fila de la tabla Extension y la extensión tiene al menos un verbo asociado a él en la \_ [tabla Verbo](verb-table.md). [](extension-table.md) Los ProgId seleccionados para el registro de esta manera no instalan otros ProgId que hacen referencia al ProgId actual a través del valor predeterminado de \_ ProgId.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descripción
</dt> <dd>

Descripción localizada opcional del identificador de programa asociado.

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icono\_
</dt> <dd>

Clave externa opcional en la [tabla Icon](icon-table.md) que especifica el archivo de icono asociado a este ProgId. Esto se escribe en la clave DefaultIcon asociada a este ProgId. Esta columna debe ser Null para un ProgId independiente de la versión.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Índice de icono en el archivo de icono. Esta columna debe ser Null para un ProgId independiente de la versión.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las [acciones RegisterProgIdInfo](registerprogidinfo-action.md) y [UnregisterProgIdInfo](unregisterprogidinfo-action.md) de las tablas de secuencia [*procesan*](s-gly.md) la información de esta tabla. Para obtener información sobre el *uso de tablas de secuencia,* vea Usar una tabla de [secuencia.](using-a-sequence-table.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE89](ice89.md)  
</dl>

 

 



