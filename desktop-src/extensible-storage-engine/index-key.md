---
description: 'Más información acerca de: clave de índice'
title: Clave de índice
TOCTitle: Index Key
ms:assetid: 104bdb1c-71ac-44f4-bbda-c553131aaad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269188(v=EXCHG.10)
ms:contentKeyID: 32765491
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: eff0812f363fa83d133ab087140d415d8e2dbad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558093"
---
# <a name="index-key"></a>Clave de índice


_**Se aplica a:** Windows | Windows Server_

## <a name="index-key"></a>Clave de índice

Se crea un índice sobre los datos de la tabla con [JetCreateIndex](./jetcreateindex-function.md) o varios índices, que se pueden crear simultáneamente con [JetCreateIndex2](./jetcreateindex2-function.md) mediante la estructura de [JET_INDEXCREATE](./jet-indexcreate-structure.md) . El índice se define en términos de una matriz de columnas, en orden de prioridad. Esta matriz de columnas también se denomina clave de índice. La clave de índice se puede definir como índice principal cuando se establece la opción JET_bitIndexPrimary en el parámetro *grbit* de [JetCreateIndex](./jetcreateindex-function.md) o [JET_INDEXCREATE](./jet-indexcreate-structure.md). La clave de índice es una cadena terminada en NULL de tokens terminados en null, tal y como se muestra en el ejemplo siguiente:

\+Col1 \\ 0-Col2 \\ 0 + Col3 \\ 0 \\ 0

La clave del ejemplo se puede usar para crear un índice en tres columnas de la tabla. Cada columna especificada en el índice se conoce como "segmento de índice" o "columna de clave". El segmento de índice puede ser ascendente o descendente en cuanto a su contribución de ordenación. En el ejemplo anterior, el nombre de la primera columna del índice es col1. El objeto + indica que col1 está indexado en orden ascendente. El – antes de Col2 indica que está indexado en orden descendente.

Cuando las columnas condicionales están presentes en el índice, la estructura de [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) se usa para indicar cómo se indexan. Una columna condicional se puede usar para controlar la presencia o ausencia de una entrada de índice en un índice basándose en el valor de la columna condicional correspondiente sin afectar al criterio de ordenación del índice. Una columna condicional puede incluir o excluir una entrada de índice del índice si el valor de esa columna condicional es NULL para el registro correspondiente.

De forma predeterminada, el tamaño máximo de la clave de índice viene determinado por la constante JET_cbKeyMost, que siempre ha sido 255 bytes de datos normalizados (bytes de datos, incluida la sobrecarga de indización). A partir de Windows Vista, el tamaño máximo de la clave de índice se puede establecer con la estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) . El tamaño máximo de la clave de índice corresponde al tamaño de página de la base de datos. Para habilitar un tamaño de clave máximo personalizado, especifique la opción Jet_bitIndexKeyMost en el miembro grbits de [JET_INDEXCREATE](./jet-indexcreate-structure.md)y establezca el miembro **cbKeyMost** en uno de los siguientes valores:

  - JET_cbKeyMost2KBytePage: cuando el tamaño de la página de la base de datos es de 2048 bytes, el tamaño máximo de la clave de índice puede estar entre 255 bytes como mínimo y 500 bytes como máximo.

  - JET_cbKeyMost4KBytePage: cuando el tamaño de la página de la base de datos es de 4096 bytes, el tamaño máximo de la clave de índice puede estar entre 255 bytes como mínimo y 1000 bytes como máximo.

  - JET_cbKeyMost8KBytePage: cuando el tamaño de la página de la base de datos es de 8196 bytes, el tamaño máximo de la clave de índice puede estar entre 255 bytes como mínimo y 2000 bytes como máximo.

En el ejemplo del diagrama siguiente se muestra una tabla que contiene información de los empleados. La tabla tiene seis columnas, cada una de las cuales define un atributo de empleado específico. Un registro de la tabla contiene los valores de un empleado, como el nombre del empleado en la columna 1 y el ID. de empleado en la columna 2. Un índice principal creado para esta tabla organiza los datos según el nombre del empleado en primer lugar y el ID. de empleado. El nombre y el identificador se indizan en orden ascendente. Por ejemplo, un registro que contenga el nombre Johnson y el ID. de empleado 12345 se enumerarán antes de un registro con un nombre de empleado Jones y un identificador de 10000. Todos los registros de Jones se almacenan juntos en la tabla, con sus identificadores de empleado en orden ascendente, tal como se muestra en la tabla.

![ESE_Documentation_IndexTable](images/Gg269188.ESE_Documentation_IndexTable(EXCHG.10).gif "ESE_Documentation_IndexTable")

La clave del índice principal debe ser única, pero las claves del índice secundario pueden ser duplicados. Por ejemplo, si se crea un índice con el apellido y hay dos personas con Stevens en la base de datos, ESE devuelve un error de Jet_errKeyDuplicate de [JetUpdate](./jetupdate-function.md) o [JetUpdate2](./jetupdate2-function.md), cuando la aplicación intenta insertar el segundo "Stevens". Cuando la clave real es mayor que el tamaño de clave máximo, se trunca la clave. La búsqueda y la unicidad de los efectos de truncamiento de clave y deben ser administrados por la aplicación. Por ejemplo, si "Stevens" y "Stevenson" se almacenaron en un índice por encima del apellido y el tamaño máximo de la clave era demasiado pequeño para almacenar la parte "ON" de "Stevenson", el truncamiento de claves daría lugar a que el motor de base de datos declarara que "Stevens" y "Stevenson" son duplicados aunque no lo sean. La aplicación debe estar preparada para controlar los casos como este durante la búsqueda y la actualización si la definición del índice y los valores de columna que indexa son tales que el truncamiento de claves es una posibilidad. A partir de Windows Vista, las aplicaciones pueden especificar la opción Jet_bitIndexDisallowTruncation en [JET_INDEXCREATE](./jet-indexcreate-structure.md) o [JetMakeKey](./jetmakekey-function.md). Si se especifica este marcador, se producirá un error en cualquier actualización del índice que dé lugar a una clave truncada con JET_errKeyTruncated. De lo contrario, las claves se truncarán de forma silenciosa. Esto permitirá que la aplicación funcione sin preocuparse por los artefactos causados por el truncamiento de clave que se ha descrito anteriormente.
