---
description: 'Más información sobre: Clave de índice'
title: Clave de índice
TOCTitle: Index Key
ms:assetid: 104bdb1c-71ac-44f4-bbda-c553131aaad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269188(v=EXCHG.10)
ms:contentKeyID: 32765491
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: eff0812f363fa83d133ab087140d415d8e2dbad3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965804"
---
# <a name="index-key"></a>Clave de índice


_**Se aplica a:** Windows | Windows Servidor_

## <a name="index-key"></a>Clave de índice

Se crea un índice sobre los datos de la tabla con [JetCreateIndex](./jetcreateindex-function.md) o se pueden crear varios índices simultáneamente [con JetCreateIndex2](./jetcreateindex2-function.md) mediante la [JET_INDEXCREATE](./jet-indexcreate-structure.md) datos. El índice se define en términos de una matriz de columnas, en orden de precedencia. Esta matriz de columnas también se denomina clave de índice. La clave de índice se puede definir como índice principal cuando la opción JET_bitIndexPrimary está establecida en el parámetro *grbit* de [JetCreateIndex](./jetcreateindex-function.md) [o JET_INDEXCREATE](./jet-indexcreate-structure.md). La clave de índice es una cadena terminada en NULL de tokens terminados en NULL, como se muestra en el ejemplo siguiente:

\+Col1 \\ 0-Col2 \\ 0+Col3 \\ 0 \\ 0

La clave del ejemplo se puede usar para crear un índice en tres columnas de la tabla. Cada columna especificada en el índice se conoce como "segmento de índice" o "columna de clave". El segmento de índice puede ser ascendente o descendente en términos de su contribución de ordenación. En el ejemplo anterior, el nombre de la primera columna del índice es Col1. + indica que Col1 está indexado en orden ascendente. : antes de Col2 indica que está indexado en orden descendente.

Cuando las columnas condicionales están presentes en el índice, [la JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) estructura se usa para indicar cómo se indexa. Una columna condicional se puede usar para controlar la presencia o ausencia de una entrada de índice en un índice en función del valor de la columna condicional correspondiente sin afectar al criterio de ordenación del índice. Una columna condicional puede incluir o excluir una entrada de índice del índice si el valor de esa columna condicional es NULL para el registro correspondiente.

De forma predeterminada, el tamaño máximo de la clave de índice lo da la constante JET_cbKeyMost que siempre ha sido 255 bytes de datos normalizados (bytes de datos, incluida la sobrecarga de indexación). A partir Windows Vista, el tamaño máximo de la clave de índice se puede establecer con [la JET_INDEXCREATE](./jet-indexcreate-structure.md) estructura. El tamaño máximo de la clave de índice corresponde al tamaño de página de la base de datos. Para habilitar un tamaño de clave máximo personalizado, especifique la opción Jet_bitIndexKeyMost en el miembro grbits de [JET_INDEXCREATE](./jet-indexcreate-structure.md)y establezca el **miembro cbKeyMost** en uno de los valores siguientes:

  - JET_cbKeyMost2KBytePage: cuando el tamaño de página de la base de datos es de 2048 bytes, el tamaño máximo de clave de índice puede estar entre 255 bytes como mínimo y 500 bytes como máximo.

  - JET_cbKeyMost4KBytePage: cuando el tamaño de página de la base de datos es de 4096 bytes, el tamaño máximo de clave de índice puede estar entre 255 bytes como mínimo y 1000 bytes como máximo.

  - JET_cbKeyMost8KBytePage: cuando el tamaño de página de la base de datos es de 8196 bytes, el tamaño máximo de clave de índice puede estar entre 255 bytes como mínimo y 2000 bytes como máximo.

En el ejemplo del diagrama siguiente se muestra una tabla que contiene información de empleados. La tabla tiene 6 columnas, cada una de las que define un atributo de empleado específico. Un registro de la tabla contiene valores para un empleado, como el nombre del empleado en la columna 1 y el identificador de empleado en la columna 2. Un índice principal creado para esta tabla organiza primero los datos según el nombre del empleado y el identificador de empleado en segundo lugar. Tanto el nombre como el identificador se indexa en orden ascendente. Por ejemplo, un registro que contiene el nombre Jones y el identificador de empleado 12345 se mostrará antes que un registro con un nombre de empleado Jones y un identificador de 10 000. Todos los registros de Jones se almacenan juntos en la tabla, con sus IDs de empleado en orden ascendente, como se muestra en la tabla.

![ESE_Documentation_IndexTable](images/Gg269188.ESE_Documentation_IndexTable(EXCHG.10).gif "ESE_Documentation_IndexTable")

La clave del índice principal debe ser única, pero las claves del índice secundario pueden ser duplicadas. Por ejemplo, si se crea un índice sobre los apellidos y hay dos personas con Steves en la base de datos, ese devuelve un error Jet_errKeyDuplicate de [JetUpdate](./jetupdate-function.md) o [JetUpdate2](./jetupdate2-function.md), cuando la aplicación intenta insertar el segundo "Stephens". Cuando la clave real es mayor que el tamaño máximo de clave, la clave se trunca. La búsqueda y la unidad de los efectos de truncamiento clave y deben administrarse mediante la aplicación. Por ejemplo, si "Steves" y "Steveson" se almacenaron en un índice sobre el apellido y el tamaño máximo de la clave era demasiado pequeño para almacenar la parte "on" de "Stephenson", el truncamiento de la clave daría lugar a que el motor de base de datos declarara que "Steves" y "Steveson" son duplicados aunque no lo estén. La aplicación debe estar preparada para controlar casos como este durante la búsqueda y actualización si la definición del índice y los valores de columna que indexa son tales que el truncamiento de claves es una posibilidad. A partir Windows Vista, las aplicaciones pueden especificar la Jet_bitIndexDisallowTruncation en [JET_INDEXCREATE](./jet-indexcreate-structure.md) [o JetMakeKey](./jetmakekey-function.md). Si se especifica esta marca, se producirá un error en cualquier actualización del índice que provocaría un error en una clave truncada JET_errKeyTruncated. De lo contrario, las claves se truncarán en modo silencioso. Esto permitirá que la aplicación funcione sin preocuparse por los artefactos causados por el truncamiento de claves que se describieron anteriormente.
