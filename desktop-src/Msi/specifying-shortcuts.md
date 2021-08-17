---
description: La tabla de métodos abreviados y las tablas relacionadas de la base de datos de instalación contiene la información necesaria para instalar accesos directos. Vea El grupo de tablas de información del programa y los métodos abreviados del instalador de edición.
ms.assetid: 0f3adf78-e650-414f-b85d-b53b986eafda
title: Especificar accesos directos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67b43a104ee05b3711ac98395098acf9393faab8e046296e58d93df4d6b9218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624689"
---
# <a name="specifying-shortcuts"></a>Especificar accesos directos

La [tabla de métodos abreviados](shortcut-table.md) y las tablas relacionadas de la base de datos de instalación contiene la información necesaria para instalar accesos directos. Vea El grupo [de tablas de información del programa y](program-information-tables-group.md) los [métodos abreviados del instalador de edición](editing-installer-shortcuts.md).

En esta sección agregará información que especifica los accesos directos anunciados y no anunciados para el Bloc de notas ejemplo.

Use el editor de bases de datos para MNP2000.msi y escriba los datos siguientes en la tabla Acceso directo.

[Tabla de métodos abreviados](shortcut-table.md)



| Acceso directo  | Directorio\_ | Nombre         | Componente\_ | Destino             | Argumentos | Descripción | Tecla de acceso rápido | Icono\_         | IconIndex | ShowCmd | WkDir |
|-----------|-------------|--------------|-------------|--------------------|-----------|-------------|--------|----------------|-----------|---------|-------|
| sBaseball | MENUDIR     | Baseball.txt | Béisbol    | Béisbol           |           |             |        | orca \_icon.exe |           |         |       |
| sConcert  | MENUDIR     | Concert.txt  | Concierto     | \[\#Concert.txt\]  |           |             |        |                |           |         |       |
| sDance    | MENUDIR     | Dance.txt    | Baile       | \[\#Dance.txt\]    |           |             |        |                |           |         |       |
| sFootball | MENUDIR     | Football.txt | Fútbol    | \[\#Football.txt\] |           |             |        |                |           |         |       |
| sHelp     | MENUDIR     | Help.txt     | Ayuda        | \[\#Help.txt\]     |           |             |        |                |           |         |       |
| sJanuary  | MENUDIR     | January.txt  | January     | \[\#January.txt\]  |           |             |        |                |           |         |       |
| sNewYears | MENUDIR     | NewYears.txt | NewYears    | \[\#NewYears.txt\] |           |             |        |                |           |         |       |
| sNotepad  | MENUDIR     | Redpark.exe  | Bloc de notas     | \[\#Redpark.exe\]  |           |             |        |                |           |         |       |
| sReadme   | MENUDIR     | Readme.txt   | Bloc de notas     | \[\#Readme.txt\]   |           |             |        |                |           |         |       |



 

La instalación de ejemplo debe habilitar la instalación de un acceso directo anunciado para la característica de béisbol. Esto requiere especificar una clave para la tabla Icono en la columna \_ Icono de la tabla Acceso directo. Para los fines de este ejemplo, puede copiar el icono del editor de bases de datos de Orca proporcionado con el SDK Windows Installer. Exporte [la tabla Icono Orca.msi](icon-table.md) y, a continuación, combine esta tabla en la base de datos MNP2000.msi mediante Orca u otra herramienta de combinación. Orca también crea un directorio denominado Icon en el directorio que MNP2000.msi y agrega el archivo de datos binarios icono o \_icon.exe.ibd. Vea la columna Datos en la tabla Icono. La tabla icono completada debe tener el siguiente aspecto cuando se vea en Orca.

[Tabla de iconos](icon-table.md)



| Nombre           | Datos            |
|----------------|-----------------|
| orca \_icon.exe | \[Binary Data\] |



 

[Continuar](specifying-properties.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Editar métodos abreviados del instalador](editing-installer-shortcuts.md)
</dt> </dl>

 

 



