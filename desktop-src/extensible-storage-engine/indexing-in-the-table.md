---
description: 'Más información sobre: Indexación en la tabla'
title: Indexación en la tabla
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 8bfc5054e5fd2b2f13747b0b5729987b9f81d5c21aa2faf38385b11e757f6763
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721455"
---
# <a name="indexing-in-the-table"></a>Indexación en la tabla


_**Se aplica a:** Windows | Windows Servidor_

## <a name="indexing-in-the-table"></a>Indexación en la tabla

Un índice es un conjunto de columnas de clave que definen una ordenación persistente de los registros de una tabla. Los registros son entradas de índice en el índice principal. Se puede definir un índice principal y varios índices secundarios para crear diferentes pedidos de datos en la tabla.

Aunque se pueden definir varios índices, los registros se almacenan físicamente en árboles B+ en el orden especificado por el índice principal. El índice principal siempre es un índice clúster y también debe ser único. El índice principal debe declararse antes de la primera actualización de tabla para conservar la ordenación del índice. Cuando la aplicación no define ningún índice principal, los datos se almacenan en el orden en que se agregan registros a la tabla. Este índice especial se conoce como índice secuencial.

Los árboles B+ independientes se usan para ordenar los registros según el índice secundario. Las entradas de índice del índice secundario contienen punteros a los datos almacenados según el índice principal. Las entradas de índice de los registros del índice principal deben ser únicas porque el índice secundario apunta al registro mediante la clave principal del registro. Los índices secundarios pueden tener o no una restricción de unidad. Para obtener más información, vea el tema [Información general de la base de](./database-overview.md) datos.
