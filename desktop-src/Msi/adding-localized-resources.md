---
description: En función de la aplicación, la localización puede requerir modificar o agregar recursos como archivos o claves del Registro.
ms.assetid: f5af0ecd-cb57-4858-88b4-4608893004f6
title: Agregar recursos localizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de37bfd3c216018f6c4a6f6866206020576153e55383a9d6b36e67533bbb3b6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829245"
---
# <a name="adding-localized-resources"></a>Agregar recursos localizados

En función de la aplicación, la localización puede requerir modificar o agregar recursos como archivos o claves del Registro. La localización de la aplicación de ejemplo MNP2000 requiere agregar un archivo adicional al paquete, Fre.txt, y las versiones en francés de dos archivos existentes: Help.txt y Readme.txt.

En este caso, el procedimiento recomendado es localización del paquete para que las versiones en inglés y francés puedan coexistir de forma segura en el equipo. Esto incluye no instalar nunca dos archivos diferentes con nombres de archivo idénticos en el mismo directorio. Dado Help.txt y Readme.txt tienen nombres de archivo idénticos en las dos versiones de idioma, el paquete francés debe instalar estos archivos en un directorio diferente al inglés.

El paquete francés Help.txt en un nuevo subdirectorio de la carpeta RedPark, francés. Dado que la adición de Fre.txt agrega un recurso al componente de Ayuda original, el código del componente de Ayuda debe ser diferente en los paquetes en francés e inglés. Vea las reglas de los códigos de componente en [Cambio del código de componente](changing-the-component-code.md).

El paquete en francés Readme.txt en el directorio francés para que este nombre de archivo no entre en conflicto con la versión en inglés. El archivo Readme.txt se instala con el componente Bloc de notas, pero las reglas de componente no requieren cambiar el código del componente. En este ejemplo, el código de componente de Bloc de notas no debe cambiarse porque RedPark.exe, los valores del Registro especificados en la tabla [del](registry-table.md)Registro , se comparten entre ambas versiones del lenguaje. Vea [Agregar información del Registro.](adding-registry-information.md)

Quite las versiones en inglés de Help.txt y Readme.txt de los archivos de origen y agregue las nuevas versiones en francés de Help.txt, Readme.txt y Fre.txt. El paquete localizado debe asignar la instalación de archivos de origen a destino como se muestra a continuación.



| Archivo        | Descripción                  | Ruta de acceso al origen                   | Ruta de acceso al destino                                         |
|-------------|------------------------------|----------------------------------|--------------------------------------------------------|
| Redpark.exe | Archivo ejecutable del editor de texto. | C: \\ Ejemplo \\ Bloc de notas \\Redpark.exe | \[ProgramFilesFolder \] \\ Red Park French \_ \\ \\Redpark.exe |
| Readme.txt  | Un archivo informativo.       | C: \\ Ejemplo \\ Bloc de notas \\Readme.txt  | \[ProgramFilesFolder \] \\ Red Park French \_ \\ \\Readme.txt  |
| Help.txt    | Manual de ayuda                  | C: \\ Ejemplo \\ Bloc de notas \\Help.txt    | \[ProgramFilesFolder \] \\ Red Park French \_ \\ \\Help.txt    |
| Fre.txt     | Teléfono lista de aplicaciones                   | C: \\ Ejemplo \\ Bloc de notas \\Fre.txt     | \[ProgramFilesFolder \] \\ Red Park French \_ \\ \\Fre.txt     |



 

Use el editor de base de datos Orca que se proporciona con el SDK, u otro editor, para abrir la tabla Directorio y agregar un registro para la instalación del nuevo directorio, francés.

[Tabla de directorios](directory-table.md)



| Directorio                                        | Elemento primario \_ del directorio                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| ASÍNSTEDIR                                          | NOTEPADDIR                                       | Events:Events       |
| HOLDIR                                           | MONDIR                                           | .:Holidays        |
| MENUDIR                                          | NOTEPADDIR                                       | Menú              |
| MONDIR                                           | NOTEPADDIR                                       | Puerta              |
| NOTEPADDIR                                       | [**ProgramFilesFolder**](programfilesfolder.md) | Red \_ Park:Bloc de notas |
| SPORTDIR                                         | NOTEPADDIR                                       | Sports:Events     |
| FRENCHDIR                                        | NOTEPADDIR                                       | Francés:.          |



 

Use el editor de tablas para cambiar el ComponentId del componente de Ayuda MNPFren.msi a un nuevo GUID.

[Tabla de componentes](component-table.md)



| Componente | Componentid                            | Directorio\_ | Atributos | Condición | Ruta de acceso de clave      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Béisbol  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Concierto   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | ASÍNSTEDIR     | 2          |           | Concert.txt  |
| Baile     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | ASÍNSTEDIR     | 2          |           | Dance.txt    |
| Fútbol  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Ayuda      | {9ED21229-FE3C-4FE9-B01D-57E00224FD0B} | NOTEPADDIR  | 2          |           | Help.txt     |
| January   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Bloc de notas   | {19BED232-30AB-11D3-91D3-00C04FD70856} | FRENCHDIR   | 2          |           | Redpark.exe  |



 

Use el editor de tablas para agregar Fre.txt a [la tabla Archivo](file-table.md) de MNPFren.msi. Escriba el LANGID en francés en el campo Idioma de los archivos localizados. Todas las demás cosas son iguales, si el archivo que se instala tiene un idioma diferente al del archivo en la máquina, el instalador favorece el archivo con el idioma que coincide con el producto que se está instalando. Los archivos neutrales de idioma se tratan como un idioma más, por lo que el producto que se instala se favorece de nuevo. Para obtener más información, vea [Reglas de control de versiones de archivos](file-versioning-rules.md).

[Tabla de archivos](file-table.md)



| Archivo         | Componente\_ | FileName     | FileSize | Versión | Lenguaje | Atributos | Secuencia |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Béisbol    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | Concierto     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | Baile       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | Fútbol    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Ayuda        | Help.txt     | 1000     |         | 1036     | 0          | 1        |
| January.txt  | January     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Bloc de notas     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Bloc de notas     | Readme.txt   | 1000     |         | 1036     | 0          | 1        |
| Fre.txt      | Ayuda        | Fre.txt      | 1000     |         | 1036     | 0          | 1        |



 

Esto completa la localización de ejemplo.

 

 



