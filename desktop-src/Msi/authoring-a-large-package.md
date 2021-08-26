---
description: Use esta guía para crear un paquete Windows Installer que contenga más de 32767 archivos.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Creación de un paquete grande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d55f7933fe600bd6c0db0705328f18d7eae2f55e3463e3ea03be8118229eca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996885"
---
# <a name="authoring-a-large-package"></a>Creación de un paquete grande

Use esta guía para crear un paquete Windows Installer que contenga más de 32767 archivos.

Si el Windows Installer contiene más de 32767 archivos, debe cambiar el esquema de la base de datos para aumentar el límite de las columnas siguientes:

-   Columna Sequence de la [tabla File](file-table.md).
-   Columna LastSequence de la [tabla Media](media-table.md).
-   Columna Sequence de la [tabla Patch](patch-table.md).

Para obtener más información, vea [Formato de definición de columna](column-definition-format.md).

**Para aumentar el límite de una columna de base de datos**

1.  Exporte la tabla a un archivo .idt. Para obtener más información, [ veaMsidb.exe](msidb-exe.md), [Exportar archivos](export-files.md)e Importar [y exportar](importing-and-exporting.md).
2.  Edite el archivo .idt para cambiar el tipo de columna de i2 a i4, o de I2 a I4.
3.  Exporte [ \_ la tabla Validation](-validation-table.md) a un archivo .idt.
4.  Edite el archivo .idt para cambiar los valores de la columna MaxValue de la tabla [ \_ Validation](-validation-table.md) para adaptarse a los anchos de columna aumentados.
5.  Vuelva a importar los archivos .idt en la base de datos.

Tenga en cuenta que las transformaciones y revisiones no se pueden crear entre dos paquetes con tipos de columna diferentes.

 

 



