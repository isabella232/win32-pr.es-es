---
description: La \_ tabla SummaryInformation es una tabla especial que se usa con El flujo de información de resumen. Puede obtener o establecer el flujo de información de resumen de una base de datos Windows Installer mediante la exportación o importación de un archivo de archivo de texto denominado \_ SummaryInformation.idt.
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803b89223db8b6fc8074336109221a8300f7c1ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159295"
---
# <a name="_summaryinformation"></a>\_SummaryInformation

La \_ tabla SummaryInformation es una tabla especial que se usa con [la secuencia de información de resumen](summary-information-stream.md). Puede obtener o establecer el flujo de información de resumen de una base [](text-archive-files.md) de datos Windows Installer mediante la exportación o importación de un archivo de archivo de texto denominado \_ SummaryInformation.idt.

El archivo .idt de una tabla \_ SummaryInformation exportada tiene el formato siguiente.

-   La primera fila contiene los nombres de columna de tabla separados por pestañas: PropertyId y Value. Consulte el [tema Summary Information Stream Property Set](summary-information-stream-property-set.md) (Conjunto de propiedades de flujo de información de resumen) para obtener una lista de las propiedades y sus identificadores (PID).
-   La segunda fila contiene las definiciones de columna separadas por pestañas. Las definiciones de columna se especifican de la misma manera que en el formato de archivo de archivo .idt [básico](archive-file-format.md). La columna PropertyId puede ser un entero corto que no acepta valores NULL. La columna Valor puede ser una cadena localizable de 255 caracteres que no acepta valores NULL.
-   La tercera fila es el nombre de la tabla y el nombre de la columna de clave principal separados por pestañas: \_ SummaryInformation y PropertyId.
-   Las filas restantes del archivo representan el PID y el valor asociado, separados por tabulaciones. Fecha y hora en \_ ResumenInformación tienen el formato: YYYY/MM/DD hh::mm::ss. Por ejemplo, 1999/03/22 15:25:45.

A continuación se muestra un ejemplo del flujo [de información de resumen](summary-information-stream.md) de una base de datos en formato .idt.

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

Cuando se usa [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) o el método [Import](database-import.md) del objeto [**Database**](database-object.md) para importar una tabla de archivo de texto denominada SummaryInformation en una base de datos del instalador, se escribe la secuencia "05SummaryInformation" en la base de \_ datos.

 

 



