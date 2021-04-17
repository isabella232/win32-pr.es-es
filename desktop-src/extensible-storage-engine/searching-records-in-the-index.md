---
description: Más información acerca de cómo buscar registros en el índice
title: Buscar registros en el índice
TOCTitle: Searching Records in the Index
ms:assetid: 9141b1d6-81b6-49ad-a5d4-2409fe0d511a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269342(v=EXCHG.10)
ms:contentKeyID: 32765631
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 89a4ffe1f1c13280f236442ae218580fa5699741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687673"
---
# <a name="searching-records-in-the-index"></a>Buscar registros en el índice


_**Se aplica a:** Windows | Windows Server_

## <a name="searching-records-in-the-index"></a>Buscar registros en el índice

Las claves de búsqueda se crean para buscar una entrada única o un conjunto de entradas en un índice. Las claves de búsqueda solo se pueden construir para las columnas de clave del índice y pueden contener uno o más valores de columna. La clave de búsqueda se construye con una sola llamada o una serie de llamadas a [JetMakeKey](./jetmakekey-function.md), y se puede recuperar con [JetRetrieveKey](./jetretrievekey-function.md) mediante JET_bitRetrieveCopy. Una vez construida la clave de búsqueda, se puede usar para desplace el cursor al registro del índice.

Existen tres métodos para buscar registros en una tabla:

1.  Busque una sola entrada de índice. Para ello, cree la clave de búsqueda con [JetMakeKey](./jetmakekey-function.md)y, a continuación, desplácese a ese registro con [JetSeek](./jetseek-function.md).

2.  Busque en el índice registro por registro. Los registros se pueden atravesar un registro cada vez llamando a [JetMove](./jetmove-function.md). El cursor puede moverse al primer registro del índice especificando JET_MoveFirst en el parámetro *cRow* de [JetMove](./jetmove-function.md). Del mismo modo, el cursor puede moverse hacia delante, hacia atrás o hasta la última entrada del índice.

3.  Buscar en un conjunto de registros. Para ello, establezca un intervalo de entradas de índice en buscar y, a continuación, desplácese por los registros secuencialmente. Para obtener más información, vea la sección [Buscar en un conjunto de registros]() de este tema.

### <a name="searching-through-a-set-of-records"></a>Buscar en un conjunto de registros

En este diagrama se muestra el cursor que se desplaza por un intervalo de entradas de índice definidas por llamadas a [JetSeek](./jetseek-function.md) y [JetSetIndexRange](./jetsetindexrange-function.md).

Utilice el procedimiento siguiente para buscar en un conjunto de registros de un índice.

### <a name="to-search-a-set-of-records-in-an-index"></a>Para buscar en un conjunto de registros de un índice

1.  Cree la clave de búsqueda para el primer registro del conjunto de registros que se va a buscar con [JetMakeKey](./jetmakekey-function.md).

2.  Mueva el cursor al registro indicado en la clave de búsqueda con [JetSeek](./jetseek-function.md).

3.  Cree otra clave de búsqueda para la última entrada de índice en el intervalo con [JetMakeKey](./jetmakekey-function.md).

4.  Establezca el intervalo de índice con [JetSetIndexRange](./jetsetindexrange-function.md) mediante la clave creada en el paso 3.

5.  Llame a [JetMove](./jetmove-function.md) para moverse secuencialmente a través de cada registro en el intervalo de índice, tal como se muestra en el diagrama siguiente.

![ESE_Documentation_IndexRange](images/Gg269342.ESE_Documentation_IndexRange(EXCHG.10).gif "ESE_Documentation_IndexRange")

El cursor del diagrama aquí solo puede desplazarse por el intervalo de índices establecido en la llamada a [JetSetIndexRange](./jetsetindexrange-function.md). Si la aplicación intenta desplace el cursor más allá del intervalo de índices, ESE devuelve un error de Jet_errNoCurrentRecord de la llamada a [JetMove](./jetmove-function.md). Tenga en cuenta que cualquier tipo de navegación con este cursor que no sea el que se desplaza al Registro siguiente o anterior cancelará el intervalo de índices. Vea [JetSetIndexRange](./jetsetindexrange-function.md) para obtener más información.

El tipo de datos especificado en el parámetro *pvData* para [JetMakeKey](./jetmakekey-function.md) debe coincidir con el tipo de datos y las propiedades especificados para la columna. Por ejemplo, al llamar a [JetMakeKey](./jetmakekey-function.md) con "Ben Miller" especificado en el parámetro *pvData* para un tipo de columna JET_coltypText es una coincidencia de tipo de datos válida. Si desea crear una clave de búsqueda para buscar entre los nombres "Ben Miller" y "Max Stevens" en un índice, mueva el cursor al registro con el nombre "Ben Miller" llamando a [JetSeek](./jetseek-function.md). Llame a [JetMakeKey](./jetmakekey-function.md) una segunda vez y especifique un puntero a una cadena que contenga el nombre "Max Stevens". El intervalo de índice se establece para limitar el cursor y desplazarse entre los nombres "Ben Miller" y "Max Stevens" en la llamada a [JetSetIndexRange](./jetsetindexrange-function.md).
