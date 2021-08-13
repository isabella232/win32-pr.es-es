---
description: La tabla Binary contiene los datos binarios de elementos como mapas de bits, animaciones e iconos. La tabla binaria también se usa para almacenar datos para acciones personalizadas. Vea Limitaciones de OLE Secuencias.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Tabla binaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a70750193b1dc147a9b2b4cfa01bbea410f0e44b7c03f16bd1c992f118a4f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638809"
---
# <a name="binary-table"></a>Tabla binaria

La tabla Binary contiene los datos binarios de elementos como mapas de bits, animaciones e iconos. La tabla binaria también se usa para almacenar datos para acciones personalizadas. Vea [Limitaciones de OLE Secuencias](ole-limitations-on-streams.md).

La tabla Binary tiene las columnas siguientes.



| Columna | Tipo                         | Key | Nullable |
|--------|------------------------------|-----|----------|
| Nombre   | [Identificador](identifier.md) | Y   | N        |
| data   | [Binario](binary.md)         | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Clave única que identifica los datos binarios concretos. Si los datos binarios son para un control , la clave aparece en la columna Texto del control asociado en la [tabla Control](control-table.md). Esta clave debe ser única entre todos los controles que requieren datos binarios.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Datos
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

 

 



