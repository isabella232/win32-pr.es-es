---
description: 'Más información sobre: columnas etiquetadas, fijas y de variable'
title: Columnas etiquetadas, fijas y de variables
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 3f27237c5f75874f7320f675affe20f3833084b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497405"
---
# <a name="tagged-fixed-and-variable-columns"></a>Columnas etiquetadas, fijas y de variables


_**Se aplica a:** Windows | Windows Server_

## <a name="tagged-fixed-and-variable-columns"></a>Columnas etiquetadas, fijas y de variables

Las columnas etiquetadas, fijas y de longitud variable son los tipos de columna principales admitidos por ESE. Las columnas etiquetadas no están presentes en un registro a menos que los datos se almacenen en la columna y pueden ser de longitud fija o variable. Las columnas etiquetadas también pueden contener más de un valor en un solo registro. Las columnas fijas ocupan la misma cantidad de espacio en cada fila y requieren 1 bit para representar el valor NULL. Las columnas de longitud variable requieren 2 bytes para representar el tamaño y el valor NULL, y ocupan una cantidad variable de espacio en cada registro. Para obtener más información sobre las columnas etiquetadas y fijas, vea la opción Jet_bitColumnTagged y Jet_bitColumnFixed en el miembro **grbit** de la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) utilizada en la llamada a [JetAddColumn](./jetaddcolumn-function.md).

Las columnas de longitud variable se determinan por el tipo de columna que se establece en el parámetro *coltyp* en la llamada a [JetAddColumn](./jetaddcolumn-function.md). Los siguientes tipos de columna pueden ser fijos o de longitud variable, dependiendo de si se establece la opción Jet_bitColumnFixed:

  - JET_coltypBinary

  - JET_coltypText

  - JET_coltypLongBinary

  - JET_coltypLongText

En general, los datos del registro se almacenan primero con el intervalo fijo, el intervalo de variables siguiente y el intervalo etiquetado almacenado en último lugar. En el diagrama siguiente se muestra cómo se almacenan los registros en la tabla. Como se muestra en el diagrama, el intervalo etiquetado puede contener columnas con varios valores.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
