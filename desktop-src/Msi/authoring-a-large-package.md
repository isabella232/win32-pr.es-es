---
description: Use esta instrucción para crear un paquete de Windows Installer que contenga más de 32767 archivos.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Crear un paquete grande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca09c427336e4ca8a17fd8ebdf803f52ebe6c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667036"
---
# <a name="authoring-a-large-package"></a>Crear un paquete grande

Use esta instrucción para crear un paquete de Windows Installer que contenga más de 32767 archivos.

Si el paquete de Windows Installer contiene más de 32767 archivos, debe cambiar el esquema de la base de datos para aumentar el límite de las columnas siguientes:

-   Columna de secuencia de la [tabla de archivos](file-table.md).
-   La columna LastSequence de la [tabla de medios](media-table.md).
-   La columna Sequence de la [tabla patch](patch-table.md).

Para obtener más información, vea [formato de definición de columna](column-definition-format.md).

**Para aumentar el límite de una columna de base de datos**

1.  Exporte la tabla a un archivo. IDT. Para obtener más información, vea [Msidb.exe](msidb-exe.md), [exportar archivos](export-files.md)e [importar y exportar](importing-and-exporting.md).
2.  Edite el archivo. IDT para cambiar el tipo de columna de i2 a I4 o de i2 a I4.
3.  Exporte la tabla de [ \_ validación](-validation-table.md) a un archivo. IDT.
4.  Edite el archivo. IDT para cambiar los valores de la columna MaxValue de la tabla de [ \_ validación](-validation-table.md) para que quepan los mayores anchos de columna.
5.  Vuelva a importar los archivos. IDT en la base de datos.

Tenga en cuenta que las transformaciones y revisiones no se pueden crear entre dos paquetes con tipos de columna diferentes.

 

 



