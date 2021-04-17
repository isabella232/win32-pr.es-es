---
description: ICE91 publica una advertencia si un archivo, archivo. ini o archivo de acceso directo se instala en un directorio solo por usuario.
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f5723369c21894817dacbc1755430a31f17199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652945"
---
# <a name="ice91"></a>ICE91

ICE91 publica una advertencia si un archivo, archivo. ini o archivo de acceso directo se instala en un directorio solo por usuario. Estas advertencias son inocuas si el paquete solo se usa para la instalación en el [contexto de instalación](installation-context.md) por usuario y nunca se usa para las instalaciones por máquina.

Los archivos, los archivos. ini o los accesos directos de los directorios de solo usuario se instalan en el perfil de un usuario determinado. Incluso si el usuario establece la propiedad [**AllUsers**](allusers.md) para las instalaciones por equipo, los archivos, los archivos. ini o los accesos directos de los directorios de solo usuario no se copian en el perfil "todos los usuarios" y no están disponibles para otros usuarios. Los directorios solo por usuario no varían con la propiedad **AllUsers** . A continuación se muestra una lista de los directorios solo por usuario:

-   AppDataFolder
-   FavoritesFolder
-   NetHoodFolder
-   PersonalFolder
-   PrintHoodFolder
-   RecentFolder
-   SendToFolder
-   MyPicturesFolder
-   LocalAppDataFolder

## <a name="result"></a>Resultado

ICE91 expone las siguientes advertencias.



| ADVERTENCIA de ICE91                                                                                                                                                                                                                            | Descripción                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| El archivo ' \[ 1 \] ' se instalará en el directorio por usuario ' \[ 2 \] ', que no varía según el valor de [**AllUsers**](allusers.md) . Este archivo no se copiará en el perfil de cada usuario, incluso si se desea una instalación por máquina.     | El archivo se instala en un directorio solo por usuario. No se instala en el perfil de cada usuario durante una instalación por máquina.      |
| El IniFile ' \[ 1 \] ' se instalará en el directorio por usuario ' \[ 2 \] ', que no varía según el valor de [**AllUsers**](allusers.md) . Este archivo no se copiará en el perfil de cada usuario, incluso si se desea una instalación por máquina.  | El archivo. ini se instala en un directorio solo por usuario. No se instala en el perfil de cada usuario durante una instalación por máquina. |
| El acceso directo ' \[ 1 \] ' se instalará en el directorio por usuario ' \[ 2 ', \] que no varía según el valor de [**AllUsers**](allusers.md) . Este archivo no se copiará en el perfil de cada usuario, incluso si se desea una instalación por máquina. | El acceso directo se instala en un directorio solo por usuario. No se instala en el perfil de cada usuario durante una instalación por máquina.  |



 

## <a name="example"></a>Ejemplo

ICE91 notifica las siguientes advertencias para el ejemplo:

``` syntax
The file 'File1' will be installed to the per user directory 'MyPicturesFolder' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The IniFile 'IniFile1' will be installed to the per user directory 'MyIniDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The shortcut 'Shortcut1' will be installed to the per user directory 'MyShortcutDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.
```

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ |
|-------|-------------|
| Archivo1 | C1          |



 

[Tabla de componentes](component-table.md) (parcial) (parcial) (parcial) (parcial)



| Componente | Directorio\_ |
|-----------|-------------|
| C1        | MyDir       |



 

[Tabla IniFile](inifile-table.md)



| IniFile  | DirProperty |
|----------|-------------|
| IniFile1 | MyIniDir    |



 

[Tabla de acceso directo](shortcut-table.md)



| Acceso directo  | Directorio\_   |
|-----------|---------------|
| Shortcut1 | MyShortcutDir |



 

[Tabla de directorio](directory-table.md)



| Directorio     | Directorio \_ primario  |
|---------------|--------------------|
| MyDir         | FavoritesFolder    |
| MyIniDir      | LocalAppDataFolder |
| MyShortcutDir | PersonalFolder     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



