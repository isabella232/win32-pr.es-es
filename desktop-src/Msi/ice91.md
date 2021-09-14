---
description: ICE91 envía una advertencia si un archivo, .ini o un archivo de acceso directo está instalado en un directorio solo por usuario.
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f5723369c21894817dacbc1755430a31f17199
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074512"
---
# <a name="ice91"></a>ICE91

ICE91 envía una advertencia si un archivo, .ini o un archivo de acceso directo está instalado en un directorio solo por usuario. Estas advertencias son inofensivas si el paquete [](installation-context.md) solo se usa para la instalación en el contexto de instalación por usuario y nunca se usa para las instalaciones por máquina.

Los archivos, .ini archivos o accesos directos en directorios solo por usuario se instalan en un perfil de usuario determinado. Incluso si el usuario establece la propiedad [**ALLUSERS**](allusers.md) para instalaciones por equipo, los archivos, los archivos .ini o los accesos directos de los directorios solo por usuario no se copian en el perfil "Todos los usuarios" y no están disponibles para otros usuarios. Los directorios solo por usuario no varían con la **propiedad ALLUSERS.** A continuación se muestra una lista de los directorios solo por usuario:

-   AppDataFolder
-   FavoritesFolder
-   NetFolderFolder
-   PersonalFolder
-   PrintFolderFolder
-   RecentFolder
-   SendToFolder
-   MyPicturesFolder
-   LocalAppDataFolder

## <a name="result"></a>Resultado

ICE91 publica las advertencias siguientes.



| Advertencia de ICE91                                                                                                                                                                                                                            | Descripción                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| El archivo ' 1 ' se instalará en el directorio por usuario ' 2 ' que no varía en \[ \] función del valor \[ \] [**ALLUSERS.**](allusers.md) Este archivo no se copiará en el perfil de cada usuario, aunque se desee una instalación por máquina.     | El archivo se instala en un directorio solo por usuario. No se instala en el perfil de cada usuario durante una instalación por máquina.      |
| IniFile ' 1 ' se instalará en el directorio por usuario ' 2 ' que no varía en función \[ \] del valor \[ \] [**ALLUSERS.**](allusers.md) Este archivo no se copiará en el perfil de cada usuario, aunque se desee una instalación por máquina.  | El .ini se instala en un directorio solo por usuario. No se instala en el perfil de cada usuario durante una instalación por máquina. |
| El acceso directo ' 1 ' se instalará en el directorio por usuario ' 2 ' que no varía en \[ \] función del valor \[ \] [**ALLUSERS.**](allusers.md) Este archivo no se copiará en el perfil de cada usuario, aunque se desee una instalación por máquina. | El acceso directo se instala en un directorio solo por usuario. No se instala en el perfil de cada usuario durante una instalación por máquina.  |



 

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



 

[Tabla de](component-table.md) componentes (parcial) (parcial) (parcial) (parcial)



| Componente | Directorio\_ |
|-----------|-------------|
| C1        | MyDir       |



 

[Tabla IniFile](inifile-table.md)



| IniFile  | DirProperty |
|----------|-------------|
| IniFile1 | MyIniDir    |



 

[Tabla de métodos abreviados](shortcut-table.md)



| Acceso directo  | Directorio\_   |
|-----------|---------------|
| Acceso directo1 | MyShortcutDir |



 

[Tabla de directorios](directory-table.md)



| Directorio     | Elemento primario \_ del directorio  |
|---------------|--------------------|
| MyDir         | FavoritesFolder    |
| MyIniDir      | LocalAppDataFolder |
| MyShortcutDir | PersonalFolder     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



