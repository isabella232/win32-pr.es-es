---
description: La tabla de accesos directos y las tablas relacionadas de la base de datos de instalación contienen información necesaria para instalar accesos directos. Vea el grupo tablas información de programas y editar accesos directos del instalador.
ms.assetid: 0f3adf78-e650-414f-b85d-b53b986eafda
title: Especificar accesos directos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29edf10a51827880a67826320d7f8415e70ea52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677673"
---
# <a name="specifying-shortcuts"></a>Especificar accesos directos

La [tabla de accesos directos](shortcut-table.md) y las tablas relacionadas de la base de datos de instalación contienen información necesaria para instalar accesos directos. Vea el [Grupo tablas información de programas](program-information-tables-group.md) y [Editar accesos directos del instalador](editing-installer-shortcuts.md).

En esta sección se agrega información que especifica los accesos directos anunciados y no anunciados para el ejemplo de Bloc de notas.

Utilice el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la tabla de accesos directos.

[Tabla de acceso directo](shortcut-table.md)



| Acceso directo  | Directorio\_ | Nombre         | Componente\_ | Destino             | Argumentos | Descripción | Tecla de acceso rápido | Icono\_         | IconIndex | ShowCmd | WkDir |
|-----------|-------------|--------------|-------------|--------------------|-----------|-------------|--------|----------------|-----------|---------|-------|
| sBaseball | MENUDIR     | Baseball.txt | Baloncesto    | Baloncesto           |           |             |        | \_icon.exe Orca |           |         |       |
| sConcert  | MENUDIR     | Concert.txt  | Concierto     | \[\#Concert.txt\]  |           |             |        |                |           |         |       |
| sDance    | MENUDIR     | Dance.txt    | Dance       | \[\#Dance.txt\]    |           |             |        |                |           |         |       |
| sFootball | MENUDIR     | Football.txt | Balón    | \[\#Football.txt\] |           |             |        |                |           |         |       |
| sHelp     | MENUDIR     | Help.txt     | Ayuda        | \[\#Help.txt\]     |           |             |        |                |           |         |       |
| sJanuary  | MENUDIR     | January.txt  | January     | \[\#January.txt\]  |           |             |        |                |           |         |       |
| sNewYears | MENUDIR     | NewYears.txt | NewYears    | \[\#NewYears.txt\] |           |             |        |                |           |         |       |
| sNotepad  | MENUDIR     | Redpark.exe  | Bloc de notas     | \[\#Redpark.exe\]  |           |             |        |                |           |         |       |
| sReadme   | MENUDIR     | Readme.txt   | Bloc de notas     | \[\#Readme.txt\]   |           |             |        |                |           |         |       |



 

La instalación de ejemplo debe habilitar la instalación de un acceso directo anunciado para la característica béisbol. Esto requiere especificar una clave para la tabla de iconos en la \_ columna icono de la tabla de acceso directo. Para los fines de este ejemplo, puede copiar el icono del editor de base de datos Orca proporcionado con el SDK de Windows Installer. Exporte la [tabla de iconos](icon-table.md) de Orca.msi y, a continuación, combine esta tabla en la base de datos de MNP2000.msi mediante Orca u otra herramienta de combinación. Orca también crea un directorio denominado Icon en el directorio que contiene MNP2000.msi y agrega el archivo de datos binarios de icono Orca \_icon.exe. ibd. Vea la columna de datos en la tabla de iconos. La tabla de iconos completada debe tener el siguiente aspecto cuando se ve en orca.

[Tabla de iconos](icon-table.md)



| Nombre           | Datos            |
|----------------|-----------------|
| \_icon.exe Orca | \[Binary Data\] |



 

[Continuar](specifying-properties.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Editar accesos directos del instalador](editing-installer-shortcuts.md)
</dt> </dl>

 

 



