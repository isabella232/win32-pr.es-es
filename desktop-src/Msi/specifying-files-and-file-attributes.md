---
description: La instalación y eliminación de cada archivo viene determinada por el componente de Windows Installer que controla el archivo.
ms.assetid: 6f84bf57-2c68-4f37-b9cd-eee3a657e7cd
title: Especificar archivos y atributos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719dacbc434d47b4074a183e67edb02a88cb3c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677674"
---
# <a name="specifying-files-and-file-attributes"></a>Especificar archivos y atributos de archivo

La instalación y eliminación de cada archivo viene determinada por el [componente de Windows Installer](windows-installer-components.md) que controla el archivo. Una vez que se ha especificado la agrupación de recursos en componentes, se puede agregar información de atributos de archivo a la base de datos de instalación. En esta sección, agregará información de archivo a la base de datos de instalación del ejemplo de Bloc de notas. Vea el [Grupo tablas de archivos](file-tables-group.md).

Los archivos del ejemplo de Bloc de notas están descomprimidos. Vea [orígenes comprimidos y sin comprimir](compressed-and-uncompressed-sources.md) para obtener información sobre cómo agregar archivos. cab a paquetes. Este ejemplo no contiene información de versión del archivo. Para obtener más información sobre el control de versiones de archivos, vea [reglas de control](file-versioning-rules.md) de versiones de archivos y control de [versiones de archivo predeterminado](default-file-versioning.md).

Utilice el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la tabla de archivos vacía.

[Tabla de archivos](file-table.md)



| Archivo         | Componente\_ | FileName     | FileSize | Versión | Idioma | Atributos | Secuencia |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Baloncesto    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | Concierto     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | Dance       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | Balón    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Ayuda        | Help.txt     | 1000     |         |          | 0          | 1        |
| January.txt  | January     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Bloc de notas     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Bloc de notas     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[Continuar](specifying-source-media.md)

 

 



