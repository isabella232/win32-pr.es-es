---
description: En la tabla de la cartelera se muestran los controles de la cartelera mostrados en la interfaz de usuario completa.
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: Tabla de la cartelera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001718"
---
# <a name="billboard-table"></a>Tabla de la cartelera

En la tabla de la cartelera se muestran los controles de la [cartelera](billboard-control.md) mostrados en la interfaz de usuario completa.

La tabla de la cartelera tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Valla | [Identificador](identifier.md) | Y   | N        |
| Característica\_ | [Identificador](identifier.md) | N   | N        |
| Acción    | [Identificador](identifier.md) | N   | Y        |
| Ordenación  | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Valla
</dt> <dd>

Nombre del control de la [cartelera](billboard-control.md).

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Ofrecen\_
</dt> <dd>

Una clave externa a la primera columna de la [tabla de características](feature-table.md). La cartelera solo se muestra si se está instalando esta característica.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar
</dt> <dd>

Nombre de una acción. La cartelera se muestra durante el progreso de los mensajes recibidos de esta acción.

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Pide
</dt> <dd>

Si hay más de una cartelera que corresponde a una acción, se muestran en el orden definido por esta columna. Este número no debe ser negativo.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE95](ice95.md)  
</dl>

 

 



