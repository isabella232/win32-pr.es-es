---
description: 'Más información sobre: Introducción a la base de datos'
title: Introducción a la base de datos
TOCTitle: Database Overview
ms:assetid: 6e4ebfab-8bd2-4fcf-9d91-2148a693596c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269290(v=EXCHG.10)
ms:contentKeyID: 32765582
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: c0b90e1faec861c995c5f9f789af9b4dda68cfb68c704c6ace6d3b367a2e209f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976365"
---
# <a name="database-overview"></a>Introducción a la base de datos


_**Se aplica a:** Windows | Windows Servidor_

## <a name="database-overview"></a>Introducción a la base de datos

La base de datos ESE es un método de acceso secuencial indexado (ISAM) para almacenar y recuperar datos. Una base de datos ese se almacena en un único archivo y consta de una o varias tablas definidas por el usuario. Los datos se organizan en registros de la tabla con una o varias columnas definidas por el usuario. Los índices que se crean proporcionan una organización diferente para todo el conjunto o un subconjunto de registros de la tabla. Mediante la API de ESE, las aplicaciones pueden crear cursores que navegan por los registros de la base de datos en distintos pedidos secuenciales. Los elementos de la tabla se definen a continuación:

  - **Columna:** la columna es un campo de la tabla que almacena un tipo específico de información. Las columnas pueden ser fijas o de longitud variable, dependiendo del tipo de datos almacenado en ellas. Algunas columnas, como las columnas etiquetadas, no toman espacio **cuando son NULL** o se establecen en el valor predeterminado, y pueden contener varios valores.

  - **Registros:** un registro es una colección de valores de columnas que tienen una identidad única definida por la clave principal.

  - **Índice:** el índice es una colección de columnas de clave que definen una ordenación almacenada de los registros de la tabla. El índice clúster, o principal, define el orden en el que se almacenan los registros dentro de la tabla. Se pueden definir varios índices para especificar diferentes ordenaciones de recorrido a través de los registros de la tabla. Un índice también puede limitar el conjunto de registros visibles en función de criterios simples, como la presencia o ausencia de un valor de columna de clave determinado en el registro.

  - **Cursor:** el cursor indica el registro actual de la tabla y navega a los registros de la tabla mediante el índice actual. El cursor también contiene información sobre el estado de la actualización preparada actualmente.

Las columnas y los índices se pueden agregar o quitar de la tabla en cualquier momento. Aunque se pueden definir varios índices, los datos de la tabla se almacenan físicamente y se agrupan lógicamente en clústeres según la definición del índice principal en un árbol B+. Cada índice secundario se almacena en un árbol B+ independiente que solo contiene punteros lógicos a los datos reales almacenados en la tabla principal. Si no se define ningún índice, los registros de la tabla se almacenan en un árbol B+ en el orden de inserción y se conocen como índice secuencial.

El diagrama siguiente es un ejemplo de cómo se almacenan los datos de la tabla en un árbol B+ según el índice principal. El índice principal es para Nombre e Identificador, y se crea un índice secundario para el número de oficina del empleado. Las entradas del índice secundario se almacenan en un árbol B+ independiente que solo contiene punteros a los registros almacenados en la tabla principal. Por ejemplo, el número de oficina 12348 de la tabla secundaria está relacionado con el registro 3 de la tabla principal. El registro 3 contiene los valores de columna del empleado en la oficina 12348. Para obtener más información, vea [el tema Indexación en la](./indexing-in-the-table.md) tabla .

![ESE_Documentation_tableandrow2](images/Gg269290.ESE_Documentation_tableandrow2(EXCHG.10).gif "ESE_Documentation_tableandrow2")
