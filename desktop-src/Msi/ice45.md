---
description: ICE45 valida que las columnas de campo de bits de la base de datos no establezcan ningún bit reservado en 1.
ms.assetid: 43fa5e9c-2059-4217-8f8e-c194e37f238a
title: ICE45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0651d94c296ae14f66b562841c3c4e2bca7b8e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276509"
---
# <a name="ice45"></a>ICE45

ICE45 valida que las columnas de campo de bits de la base de datos no establezcan ningún bit reservado en 1.

Los bits reservados no proporcionan ninguna funcionalidad en las versiones actuales del instalador, pero pueden en versiones futuras. Deben establecerse en 0 para ser compatibles con versiones futuras de Windows Installer.

## <a name="result"></a>Resultado

ICE45 envía un mensaje de error si alguna de las tablas siguientes contiene un campo de bits con un bit reservado establecido en un valor de 1.

-   [Tabla BBControl](bbcontrol-table.md)
-   [Tabla de cuadro de diálogo](dialog-table.md)
-   [Tabla de características](feature-table.md)
-   [Tabla de archivos](file-table.md)
-   [Tabla MoveFile](movefile-table.md)
-   [Tabla ModuleConfiguration](moduleconfiguration-table.md)
-   [Tabla ODBCDataSource](odbcdatasource-table.md)
-   [Tabla de revisión](patch-table.md)
-   [Tabla RemoveFile](removefile-table.md)
-   [Tabla ServiceControl](servicecontrol-table.md)
-   [Tabla ServiceInstall](serviceinstall-table.md)
-   [Tabla de TextStyle](textstyle-table.md)

ICE45 envía uno de dos mensajes de advertencia si la [tabla de control](control-table.md) contiene un campo de bits con un bit reservado establecido en un valor de 1.

## <a name="example"></a>Ejemplo

ICE45 notifica el siguiente error para el ejemplo que se muestra.

``` syntax
Row 'File1' in table 'File' has bits set in the 'Attributes' 
    column that are reserved. They must be 0 to ensure 
    compatibility with future installer versions.
```

ICE45 notifica la siguiente advertencia para el ejemplo que se muestra.

``` syntax
Row 'Dialog1.Edit2' in table 'Control' has bits set in the 'Attribute' 
    column that are reserved. They should be 0 to ensure compatibility 
    with future installer versions.
```

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Atributos |
|-------|------------|
| Archivo1 | 128        |



 

[Tabla de control](control-table.md) (parcial)



| Diálogo  | Control | Atributos |
|---------|---------|------------|
| Dialog1 | Edit1   | 2 097 152    |
| Dialog1 | Edit2   | 1 048 576    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



