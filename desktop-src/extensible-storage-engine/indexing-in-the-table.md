---
description: 'Más información sobre: indexación en la tabla'
title: Indexación en la tabla
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5d09fde8c5fcdcf2411f6d40c5a3a70912bed27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082245"
---
# <a name="indexing-in-the-table"></a>Indexación en la tabla


_**Se aplica a:** Windows | Windows Server_

## <a name="indexing-in-the-table"></a>Indexación en la tabla

Un índice es un conjunto de columnas de clave que definen un orden persistente de los registros de una tabla. Los registros son entradas de índice en el índice principal. Se pueden definir un índice principal y varios índices secundarios para crear pedidos de datos diferentes en la tabla.

Aunque se pueden definir varios índices, los registros se almacenan físicamente en árboles B + en el orden especificado por el índice principal. El índice principal siempre es un índice clúster y también debe ser único. El índice principal debe declararse antes de la primera actualización de la tabla para conservar la ordenación del índice. Cuando la aplicación no define ningún índice principal, los datos se almacenan en el orden en que se agregan los registros a la tabla. Este índice especial se conoce como índice secuencial.

Los árboles B + independientes se usan para ordenar los registros según el índice secundario. Las entradas de índice del índice secundario contienen punteros a los datos almacenados según el índice principal. Las entradas de índice de los registros del índice principal deben ser únicas porque el índice secundario apunta al registro mediante la clave principal del registro. Los índices secundarios pueden tener o no una restricción de unicidad. Para obtener más información, vea el tema [información general sobre bases de datos](./database-overview.md) .
