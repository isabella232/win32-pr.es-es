---
description: La \_ tabla SummaryInformation es una tabla especial que se usa con la secuencia de información de resumen. Puede obtener o establecer la secuencia de información de Resumen de una base de datos Windows Installer mediante la exportación o importación de un archivo de almacenamiento de texto denominado \_ SummaryInformation. IDT.
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803b89223db8b6fc8074336109221a8300f7c1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652637"
---
# <a name="_summaryinformation"></a>\_SummaryInformation

La \_ tabla SummaryInformation es una tabla especial que se usa con la [secuencia de información de Resumen](summary-information-stream.md). Puede obtener o establecer la secuencia de información de Resumen de una base de datos Windows Installer mediante la exportación o importación de un [archivo de almacenamiento de texto](text-archive-files.md) denominado \_ SummaryInformation. IDT.

El archivo. IDT de una \_ tabla SummaryInformation exportada tiene el formato siguiente.

-   La primera fila contiene los nombres de columna de tabla separados por tabulaciones: PropertyId y Value. Vea el tema conjunto de propiedades de [flujo de información de Resumen](summary-information-stream-property-set.md) para obtener una lista de las propiedades y sus identificadores (PID).
-   La segunda fila contiene las definiciones de columna separadas por tabulaciones. Las definiciones de columna se especifican de la misma manera que en el [formato de archivo de almacenamiento](archive-file-format.md)Basic. IDT. La columna PropertyId puede ser un entero corto que no acepta valores NULL. La columna valor puede ser una cadena localizable que no acepta valores NULL 255 caracteres de longitud.
-   La tercera fila es el nombre de la tabla y el nombre de la columna de clave principal separados por tabulaciones: \_ SummaryInformation y PropertyId.
-   Las filas restantes del archivo representan el PID y el valor asociado, separados por tabulaciones. La fecha y la hora de \_ SummaryInformation tienen el formato: AAAA/MM/DD HH:: mm:: SS. Por ejemplo, 1999/03/22 15:25:45.

El siguiente es un ejemplo de la [secuencia de información de Resumen](summary-information-stream.md) de una base de datos en formato. IDT.

``` syntax
PropertyId   Value
i2  l255
_SummaryInformation PropertyId
1   1252
2   Installation Database
3   Internal Quick Test
4   Microsoft Corporation
5   Installer,MSI,Database
6   Installer Internal Release Quick Test
7   Intel;1033
9   {00000002-0001-0000-0000-624474736554}
12  1999/06/21
14  110
15  1
18  Windows Installer
```

Cuando se usa [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) o el método [Import](database-import.md) del objeto [**Database**](database-object.md) para importar una tabla de archivo de texto denominada \_ SummaryInformation en una base de datos del instalador, se escribe la secuencia "05SummaryInformation" en la base de datos.

 

 



