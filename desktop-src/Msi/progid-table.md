---
description: La tabla ProgId contiene información sobre los identificadores de programa y los identificadores de programa independientes de la versión que deben generarse como parte del anuncio del producto.
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: Tabla ProgId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293ce3748f691b664d55b0a1158a574472388202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002972"
---
# <a name="progid-table"></a>Tabla ProgId

La tabla ProgId contiene información sobre los identificadores de programa y los identificadores de programa independientes de la versión que deben generarse como parte del anuncio del producto.

La tabla ProgId tiene las columnas siguientes.



| Columna         | Tipo                         | Clave | Nullable |
|----------------|------------------------------|-----|----------|
| ProgId         | [Texto](text.md)             | Y   | N        |
| ProgId ( \_ elemento primario) | [Texto](text.md)             | N   | Y        |
| Las\_        | [GUID](guid.md)             | N   | Y        |
| Descripción    | [Texto](text.md)             | N   | Y        |
| Icono\_         | [Identificador](identifier.md) | N   | Y        |
| IconIndex      | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>Programa
</dt> <dd>

Identificador de programa o identificador de programa independiente de la versión. Los ProgId que aparecen en la tabla ProgId se registran si el CLSID que aparece en la \_ columna clase de esta tabla está programado para ser anunciado o instalado. Cuando se selecciona el ProgId para el registro, todos los ProgId que hacen referencia a esta fila a través de la \_ columna primaria ProgID también se seleccionan para el registro.

</dd> <dt>

<span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId ( \_ elemento primario)
</dt> <dd>

Solo se define para los identificadores de programa independientes de la versión. Este campo es una clave externa en la columna ProgId. Para definir un identificador de programa independiente de la versión, escriba el ProgId correspondiente en la \_ columna primaria ProgID. Cuando se selecciona el ProgId para la instalación, también se seleccionan los ProgId independientes de la versión correspondientes asociados a la \_ columna primaria ProgID para el registro.

</dd> <dt>

<span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Las\_
</dt> <dd>

Una clave externa opcional en la [tabla de clases](class-table.md). Esta columna debe ser null para un ProgId independiente de la versión. Si el \_ valor de clase de un ProgID es null, el ProgID se registra cuando aparece en la columna ProgID de una fila de la [tabla de extensión](extension-table.md) y la extensión tiene al menos un verbo asociado en la [tabla de verbos](verb-table.md). Los ProgId seleccionados para el registro de esta manera no instalan otros ProgId que hagan referencia al ProgId actual a través del \_ valor predeterminado de ProgID.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación
</dt> <dd>

Descripción localizada opcional del identificador de programa asociado.

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icono\_
</dt> <dd>

Una clave externa opcional en la [tabla de iconos](icon-table.md) que especifica el archivo de icono asociado a este ProgID. Esto se escribe en la clave DefaultIcon asociada a este ProgId. Esta columna debe ser null para un ProgId independiente de la versión.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Índice del icono en el archivo de icono. Esta columna debe ser null para un ProgId independiente de la versión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las acciones [RegisterProgIdInfo](registerprogidinfo-action.md) y [UnregisterProgIdInfo](unregisterprogidinfo-action.md) de [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla. Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE89](ice89.md)  
</dl>

 

 



