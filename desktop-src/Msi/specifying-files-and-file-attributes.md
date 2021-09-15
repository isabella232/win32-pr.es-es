---
description: La instalación y eliminación de cada archivo viene determinada por el Windows instalador que controla el archivo.
ms.assetid: 6f84bf57-2c68-4f37-b9cd-eee3a657e7cd
title: Especificar archivos y atributos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719dacbc434d47b4074a183e67edb02a88cb3c90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473934"
---
# <a name="specifying-files-and-file-attributes"></a>Especificar archivos y atributos de archivo

La instalación y eliminación de cada archivo viene determinada por el [Windows instalador que](windows-installer-components.md) controla el archivo. Una vez especificada la agrupación de recursos en componentes, se puede agregar información de atributos de archivo a la base de datos de instalación. En esta sección, agregará información de archivo a la base de datos de instalación para el Bloc de notas ejemplo. Vea el grupo [Tablas de archivos](file-tables-group.md).

Los archivos del ejemplo Bloc de notas no se comprimen. Consulte [Orígenes comprimidos y sin comprimir para](compressed-and-uncompressed-sources.md) obtener información sobre cómo agregar archivos de archivo a paquetes. Este ejemplo no contiene información de control de versiones de archivos. Para obtener más información sobre el control de versiones de archivos, vea [Reglas de control de](file-versioning-rules.md) versiones de archivos y Control de versiones de archivos [predeterminado.](default-file-versioning.md)

Use el editor de bases de datos para MNP2000.msi y escriba los datos siguientes en la tabla File vacía.

[Tabla de archivos](file-table.md)



| Archivo         | Componente\_ | FileName     | FileSize | Versión | Idioma | Atributos | Secuencia |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Béisbol    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | Concierto     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | Baile       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | Fútbol    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Ayuda        | Help.txt     | 1000     |         |          | 0          | 1        |
| January.txt  | January     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Bloc de notas     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Bloc de notas     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[Continuar](specifying-source-media.md)

 

 



