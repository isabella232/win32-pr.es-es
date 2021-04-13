---
description: 'Más información sobre: información general sobre bases de datos'
title: Información general sobre bases de datos
TOCTitle: Database Overview
ms:assetid: 6e4ebfab-8bd2-4fcf-9d91-2148a693596c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269290(v=EXCHG.10)
ms:contentKeyID: 32765582
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 473ffc7f11b3688f0f0904ae15a366ef7d6812d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564621"
---
# <a name="database-overview"></a>Información general sobre bases de datos


_**Se aplica a:** Windows | Windows Server_

## <a name="database-overview"></a>Información general sobre bases de datos

La base de datos ESE es un método de acceso secuencial indizado (ISAM) para almacenar y recuperar datos. Una base de datos ESE se almacena en un único archivo y consta de una o varias tablas definidas por el usuario. Los datos se organizan en los registros de la tabla con una o más columnas definidas por el usuario. Los índices que se crean proporcionan una organización diferente para todo el conjunto o un subconjunto de registros de la tabla. Mediante la API de ESE, las aplicaciones pueden crear cursores que naveguen por los registros de la base de datos en diferentes pedidos secuenciales. Los elementos de la tabla se definen a continuación:

  - **Columna**: la columna es un campo de la tabla que almacena un tipo de información específico. Las columnas pueden ser fijas o de longitud variable, dependiendo del tipo de datos almacenado en ellas. Algunas columnas, como las columnas etiquetadas, no ocupan espacio cuando son **nulas** o establecen el valor predeterminado, y pueden contener varios valores.

  - **Registros**: un registro es una colección de valores de columnas que tienen una identidad única, tal como la define la clave principal.

  - **Index**: el índice es una colección de columnas de clave que definen un orden almacenado de registros en la tabla. El índice clúster, o principal, define el orden en el que se almacenan los registros en la tabla. Se pueden definir varios índices para especificar diferentes ordenaciones de recorrido a través de los registros de la tabla. Un índice también puede limitar el conjunto de registros visibles en función de criterios simples como la presencia o ausencia de un valor de columna de clave determinado en el registro.

  - **Cursor**: el cursor indica el registro actual de la tabla y navega a los registros de la tabla utilizando el índice actual. El cursor también contiene información sobre el estado de la actualización preparada actualmente.

En cualquier momento se pueden agregar o quitar columnas e índices de la tabla. Aunque se pueden definir varios índices, los datos de la tabla se almacenan físicamente y se agrupan lógicamente de acuerdo con la definición del índice principal en un árbol B +. Cada índice secundario se almacena en un árbol B + independiente que solo contiene punteros lógicos a los datos reales que se almacenan en la tabla principal. Si no se define ningún índice, los registros de la tabla se almacenan en un árbol B + en el orden de inserción y se conocen como índice secuencial.

El diagrama siguiente es un ejemplo de cómo se almacenan los datos de la tabla en un árbol B + según el índice principal. El índice principal es para el nombre y el identificador, y se crea un índice secundario para el número de oficina del empleado. Las entradas del índice secundario se almacenan en un árbol B + independiente que solo contiene punteros a los registros almacenados en la tabla principal. Por ejemplo, el número de Office 12348 en la tabla secundaria está relacionado con el registro 3 de la tabla principal. El registro 3 contiene los valores de columna para el empleado en Office 12348. Para obtener más información, vea el tema [indexación en la tabla](./indexing-in-the-table.md) .

![ESE_Documentation_tableandrow2](images/Gg269290.ESE_Documentation_tableandrow2(EXCHG.10).gif "ESE_Documentation_tableandrow2")
