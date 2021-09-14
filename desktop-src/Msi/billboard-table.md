---
description: En la tabla Deserción se enumeran los controles Desenlazados que se muestran en la interfaz de usuario completa.
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: Tabla de Paneles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158987"
---
# <a name="billboard-table"></a>Tabla de Paneles

En la tabla Deserción se enumeran [los controles Desenlazados](billboard-control.md) que se muestran en la interfaz de usuario completa.

La tabla Descándalo tiene las columnas siguientes.



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

Nombre del [control Deón.](billboard-control.md)

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Característica\_
</dt> <dd>

Clave externa de la primera columna de la [tabla Feature](feature-table.md). La pantalla solo se muestra si se está instalando esta característica.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Acción
</dt> <dd>

Nombre de una acción. El cuadro de diálogo se muestra durante los mensajes de progreso recibidos de esta acción.

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordenar
</dt> <dd>

Si hay más de una marca de pantalla correspondiente a una acción, se muestran en el orden definido por esta columna. Este número no debe ser negativo.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE95](ice95.md)  
</dl>

 

 



