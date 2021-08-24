---
description: La instalación y eliminación de cada archivo viene determinada por el componente Windows instalador que controla el archivo.
ms.assetid: 6f84bf57-2c68-4f37-b9cd-eee3a657e7cd
title: Especificar archivos y atributos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdb63bf2779ddc5730013bad06b382c168a62bab5e897d5d621f7a65644e445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893735"
---
# <a name="specifying-files-and-file-attributes"></a>Especificar archivos y atributos de archivo

La instalación y eliminación de cada archivo viene determinada por el [componente Windows instalador que](windows-installer-components.md) controla el archivo. Una vez especificada la agrupación de recursos en componentes, se puede agregar información de atributos de archivo a la base de datos de instalación. En esta sección, agregará información de archivo a la base de datos de instalación para el Bloc de notas ejemplo. Vea el grupo [Tablas de archivos](file-tables-group.md).

Los archivos de la Bloc de notas ejemplo no se comprimen. Consulte [Orígenes comprimidos y sin comprimir para](compressed-and-uncompressed-sources.md) obtener información sobre cómo agregar archivos de archivador a paquetes. Este ejemplo no contiene información de control de versiones de archivos. Para obtener más información sobre el control de versiones de archivos, vea [Reglas de control](file-versioning-rules.md) de versiones de archivos y Control de versiones de archivos [predeterminado.](default-file-versioning.md)

Use el editor de base de datos para MNP2000.msi y escriba los datos siguientes en la tabla File vacía.

[Tabla de archivos](file-table.md)



| Archivo         | Componente\_ | FileName     | FileSize | Versión | Lenguaje | Atributos | Secuencia |
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

 

 



