---
description: ICE91 envía una advertencia si un archivo, .ini o un archivo de acceso directo está instalado en un directorio solo por usuario.
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd67c714701baecee50fdeb460323bd25c0a164040bbc751a65cb43a6c99eb44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315255"
---
# <a name="ice91"></a>ICE91

ICE91 envía una advertencia si un archivo, .ini o un archivo de acceso directo está instalado en un directorio solo por usuario. Estas advertencias son inofensivas si el paquete [](installation-context.md) solo se usa para la instalación en el contexto de instalación por usuario y nunca se usa para las instalaciones por equipo.

Los archivos, .ini archivos o accesos directos en directorios solo por usuario se instalan en el perfil de un usuario determinado. Incluso si el usuario establece la propiedad [**ALLUSERS**](allusers.md) para instalaciones por equipo, los archivos, los archivos .ini o los accesos directos de los directorios solo por usuario no se copian en el perfil "Todos los usuarios" y no están disponibles para otros usuarios. Los directorios solo por usuario no varían con la **propiedad ALLUSERS.** A continuación se muestra una lista de los directorios solo por usuario:

-   AppDataFolder
-   FavoritosCarpeta
-   NetFolder
-   PersonalFolder
-   PrintFolder
-   RecentFolder
-   SendToFolder
-   MyPicturesFolder
-   LocalAppDataFolder

## <a name="result"></a>Resultado

ICE91 publica las siguientes advertencias.



| Advertencia ice91                                                                                                                                                                                                                            | Descripción                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| El archivo ' 1 ' se instalará en el directorio por usuario ' 2 ' que no varía en \[ \] función del valor \[ \] [**ALLUSERS.**](allusers.md) Este archivo no se copiará en el perfil de cada usuario, aunque se desee una instalación por equipo.     | El archivo se instala en un directorio solo por usuario. No se instala en el perfil de cada usuario durante una instalación por equipo.      |
| IniFile ' 1 ' se instalará en el directorio por usuario ' 2 ' que no varía en \[ \] función del valor \[ \] [**ALLUSERS.**](allusers.md) Este archivo no se copiará en el perfil de cada usuario, aunque se desee una instalación por equipo.  | El .ini se instala en un directorio solo por usuario. No se instala en el perfil de cada usuario durante una instalación por equipo. |
| El acceso directo ' 1 ' se instalará en el directorio por usuario ' 2 ' que no \[ varía en función del valor \] \[ \] [**ALLUSERS.**](allusers.md) Este archivo no se copiará en el perfil de cada usuario, aunque se desee una instalación por equipo. | El acceso directo se instala en un directorio solo por usuario. No se instala en el perfil de cada usuario durante una instalación por equipo.  |



 

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
| MyDir         | FavoritosCarpeta    |
| MyIniDir      | LocalAppDataFolder |
| MyShortcutDir | PersonalFolder     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



