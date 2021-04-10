---
description: 'Más información acerca de: columnas'
title: Columnas
TOCTitle: Columns
ms:assetid: bc16ca4c-e3c9-43db-ac16-284d7cc0926d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294073(v=EXCHG.10)
ms:contentKeyID: 32765688
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 86f7d2bbb3925434ddbfff52e987b6e408af9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155053"
---
# <a name="columns"></a>Columnas


_**Se aplica a:** Windows | Windows Server_

## <a name="columns"></a>Columnas

Una tabla se puede crear con un conjunto inicial de columnas mediante una llamada a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o sin un conjunto inicial de columnas llamando a [JetCreateTable](./jetcreatetable-function.md). Las tablas de ESE pueden contener hasta 127 columnas de longitud fija, 128 columnas de longitud variable y 64.993 columnas etiquetadas. Las columnas se identifican por su nombre e identificador y se pueden agregar dinámicamente a la tabla con [JetAddColumn](./jetaddcolumn-function.md). Las columnas se crean con un tipo de datos específico y un conjunto opcional de atributos, por ejemplo, si la columna tiene una longitud fija o si puede ser NULL o no.

El tipo de una columna determina los datos que se pueden almacenar en la columna y muchas de las propiedades de la columna, incluido su orden de indexación. ESE es compatible con una amplia gama de tipos de columna, con un tamaño de entre 1 y 2 GB (2146483647 caracteres ASCII o 1073741823 caracteres Unicode). Para obtener una lista completa de los tipos de datos de columna admitidos por ESE, vea el tema [JET_COLTYP](./jet-coltyp.md) . En los temas siguientes se tratan algunos de los tipos de columnas admitidos por ESE:

  - [Columnas etiquetadas, fijas y de variables](./tagged-fixed-and-variable-columns.md)

  - [Columnas de versión, incremento automático y custodia](./version-auto-increment-and-escrow-columns.md)

  - [Columnas de valor largo](./long-value-columns.md)

  - [Columnas dispersas con varios valores](./multi-valued-sparse-columns.md)

  - [Columnas definidas por el usuario](./user-defined-columns.md)

  - [Usar columnas en una tabla](./using-columns-in-a-table.md)
