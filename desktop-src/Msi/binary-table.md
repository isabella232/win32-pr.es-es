---
description: La tabla binaria contiene los datos binarios de elementos tales como mapas de bits, animaciones e iconos. La tabla binaria también se utiliza para almacenar datos para las acciones personalizadas. Vea limitaciones de OLE en secuencias.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Tabla binaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4069c7e684e7d90c94b4b04f3d5839058f3570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667015"
---
# <a name="binary-table"></a>Tabla binaria

La tabla binaria contiene los datos binarios de elementos tales como mapas de bits, animaciones e iconos. La tabla binaria también se utiliza para almacenar datos para las acciones personalizadas. Vea [limitaciones de OLE en secuencias](ole-limitations-on-streams.md).

La tabla binaria tiene las columnas siguientes.



| Columna | Tipo                         | Clave | Nullable |
|--------|------------------------------|-----|----------|
| Nombre   | [Identificador](identifier.md) | Y   | N        |
| Datos   | [Binario](binary.md)         | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Una clave única que identifica los datos binarios concretos. Si los datos binarios son para un control, la clave aparece en la columna de texto del control asociado en la [tabla de control](control-table.md). Esta clave debe ser única entre todos los controles que requieren datos binarios.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Data
</dt> <dd>

Datos binarios sin formato.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE29](ice29.md)  
</dl>

 

 



