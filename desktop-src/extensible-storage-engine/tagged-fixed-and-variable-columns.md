---
description: 'Más información sobre: Columnas etiquetadas, fijas y variables'
title: Columnas etiquetadas, fijas y variables
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: af2ab8ece57342f211b0dd4488b6feb25b191c1977ae39038fb61ea56f20d543
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118484753"
---
# <a name="tagged-fixed-and-variable-columns"></a>Columnas etiquetadas, fijas y variables


_**Se aplica a:** Windows | Windows Servidor_

## <a name="tagged-fixed-and-variable-columns"></a>Columnas etiquetadas, fijas y variables

Las columnas etiquetadas, fijas y de longitud variable son los tipos de columna principales admitidos por ESE. Las columnas etiquetadas no están presentes en un registro a menos que los datos se almacenen en la columna y puedan tener una longitud fija o variable. Las columnas etiquetadas también pueden contener más de un valor en un único registro. Las columnas fijas toman la misma cantidad de espacio en cada fila y requieren 1 bit para representar el valor NULL. Las columnas de longitud variable requieren 2 bytes para representar el tamaño y el valor NULL, y ocupan una cantidad variable de espacio en cada registro. Para obtener más información sobre las columnas etiquetadas y fijas, vea la opción Jet_bitColumnTagged y Jet_bitColumnFixed en el miembro **grbit** de la estructura JET_COLUMNDEF utilizada en la llamada [a](./jet-columndef-structure.md) [JetAddColumn](./jetaddcolumn-function.md).

Las columnas de longitud variable están determinadas por el tipo de columna que se establece en el parámetro *coltyp* en la llamada a [JetAddColumn](./jetaddcolumn-function.md). Los siguientes tipos de columna pueden ser fijos o de longitud variable dependiendo de si se Jet_bitColumnFixed la opción de columna:

  - JET_coltypBinary

  - JET_coltypText

  - JET_coltypLongBinary

  - JET_coltypLongText

En general, los datos del registro se almacenan primero con el intervalo fijo, el intervalo variable siguiente y el intervalo etiquetado almacenado en último lugar. En el diagrama siguiente se muestra cómo se almacenan los registros en la tabla. Como se muestra en el diagrama, el intervalo etiquetado puede contener columnas con varios valores.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
