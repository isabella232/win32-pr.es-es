---
description: En la tabla Deón se enumeran los controles Deserción que se muestran en la interfaz de usuario completa.
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: Tabla de Destinos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd96773e738efa14e47411f6059869e31651ea09a20dc42e0fe531eb12a12c71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105385"
---
# <a name="billboard-table"></a>Tabla de Destinos

En la tabla Deserción se enumeran [los controles de Controls](billboard-control.md) que se muestran en la interfaz de usuario completa.

La tabla Deón tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Cartelera | [Identificador](identifier.md) | Y   | N        |
| Característica\_ | [Identificador](identifier.md) | N   | N        |
| Acción    | [Identificador](identifier.md) | N   | Y        |
| Ordenación  | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Cartelera
</dt> <dd>

Nombre del [control Deón](billboard-control.md).

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Característica\_
</dt> <dd>

Clave externa de la primera columna de la [tabla De características](feature-table.md). El cuadro de diálogo solo se muestra si se está instalando esta característica.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Acción
</dt> <dd>

Nombre de una acción. El cuadro de diálogo se muestra durante los mensajes de progreso recibidos de esta acción.

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordenar
</dt> <dd>

Si hay más de un cuadro correspondiente a una acción, se muestran en el orden definido por esta columna. Este número no debe ser negativo.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE95](ice95.md)  
</dl>

 

 



