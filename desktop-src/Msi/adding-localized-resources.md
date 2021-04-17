---
description: Dependiendo de la aplicación, la localización puede requerir la modificación o adición de recursos como archivos o claves del registro.
ms.assetid: f5af0ecd-cb57-4858-88b4-4608893004f6
title: Agregar recursos localizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7646499e4bb48e3df9fc1527bff1273e6b6784bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667057"
---
# <a name="adding-localized-resources"></a>Agregar recursos localizados

Dependiendo de la aplicación, la localización puede requerir la modificación o adición de recursos como archivos o claves del registro. La localización de la aplicación de ejemplo MNP2000 requiere agregar un archivo adicional al paquete, Fre.txt y las versiones en francés de dos archivos existentes: Help.txt y Readme.txt.

En este caso, el procedimiento recomendado es localizar el paquete de modo que las versiones en inglés y francés puedan coexistir en el equipo de forma segura. Esto incluye no instalar nunca dos archivos diferentes con nombres de archivo idénticos en el mismo directorio. Como Help.txt y Readme.txt tienen nombres de archivo idénticos en las versiones de dos idiomas, el paquete en francés debe instalar estos archivos en un directorio diferente del inglés.

El paquete en francés instala Help.txt en un nuevo subdirectorio de la carpeta RedPark, francés. Dado que la adición de Fre.txt agrega un recurso al componente de ayuda original, el código de componente del componente de ayuda debe ser diferente en los paquetes en francés e inglés. Vea las reglas de los códigos de componente para [cambiar el código de componente](changing-the-component-code.md).

El paquete en francés instala Readme.txt en el directorio francés para que este nombre de archivo no pueda entrar en conflicto con la versión en inglés. El archivo Readme.txt se instala con el componente del Bloc de notas, pero las reglas de componentes no requieren que se cambie el código del componente. En este ejemplo, el código de componente del Bloc de notas no debe cambiarse porque RedPark.exe, los valores del registro especificados en la [tabla del registro](registry-table.md), son compartidos por ambas versiones de idioma. Vea [Agregar información del registro](adding-registry-information.md).

Quite las versiones en Inglés de Help.txt y Readme.txt de los archivos de origen y agregue las nuevas versiones en francés de Help.txt, Readme.txt y Fre.txt. El paquete localizado debe asignar la instalación de archivos desde el origen al destino como se indica a continuación.



| Archivo        | Descripción                  | Ruta de acceso al origen                   | Ruta de acceso al destino                                         |
|-------------|------------------------------|----------------------------------|--------------------------------------------------------|
| Redpark.exe | Archivo ejecutable del editor de texto. | C: \\Redpark.exe del Bloc de notas de ejemplo \\ \\ | \[Redpark.exe en francés de la \] \\ \_ estacion roja \\ \\ |
| Readme.txt  | Un archivo informativo.       | C: \\Readme.txt del Bloc de notas de ejemplo \\ \\  | \[Readme.txt en francés de la \] \\ \_ estacion roja \\ \\  |
| Help.txt    | Manual de ayuda                  | C: \\Help.txt del Bloc de notas de ejemplo \\ \\    | \[Help.txt en francés de la \] \\ \_ estacion roja \\ \\    |
| Fre.txt     | Lista de teléfonos                   | C: \\Fre.txt del Bloc de notas de ejemplo \\ \\     | \[Fre.txt en francés de la \] \\ \_ estacion roja \\ \\     |



 

Use el editor de bases de datos orca que se proporciona con el SDK u otro editor para abrir la tabla de directorios y agregar un registro para la instalación del nuevo directorio, francés.

[Tabla de directorio](directory-table.md)



| Directorio                                        | Directorio \_ primario                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| ARTSDIR                                          | NOTEPADDIR                                       | Arts: eventos       |
| HOLDIR                                           | MONDIR                                           | .: Festivos        |
| MENUDIR                                          | NOTEPADDIR                                       | Menú              |
| MONDIR                                           | NOTEPADDIR                                       | Canaliza              |
| NOTEPADDIR                                       | [**ProgramFilesFolder**](programfilesfolder.md) | \_Estacionamiento rojo: Bloc de notas |
| SPORTDIR                                         | NOTEPADDIR                                       | Deportes: eventos     |
| FRENCHDIR                                        | NOTEPADDIR                                       | Francés:.          |



 

Utilice el editor de tablas para cambiar el ComponentId del componente de ayuda en MNPFren.msi a un nuevo GUID.

[Tabla de componentes](component-table.md)



| Componente | ComponentId                            | Directorio\_ | Atributos | Condición | Rutas      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Baloncesto  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Concierto   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Concert.txt  |
| Dance     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Dance.txt    |
| Balón  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Ayuda      | {9ED21229-FE3C-4FE9-B01D-57E00224FD0B} | NOTEPADDIR  | 2          |           | Help.txt     |
| January   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Bloc de notas   | {19BED232-30AB-11D3-91D3-00C04FD70856} | FRENCHDIR   | 2          |           | Redpark.exe  |



 

Utilice el editor de tablas para agregar Fre.txt a la [tabla de archivos](file-table.md) de MNPFren.msi. Escriba el LANGID para francés en el campo idioma para los archivos localizados. Si el archivo que se va a instalar tiene un idioma distinto al del archivo en el equipo, el instalador favorece el archivo con el idioma que coincida con el producto que se está instalando. Los archivos independientes del idioma se tratan como un solo otro idioma, por lo que el producto que se está instalando se vuelve a favorecer. Para obtener más información, vea [reglas de control de versiones de archivos](file-versioning-rules.md).

[Tabla de archivos](file-table.md)



| Archivo         | Componente\_ | FileName     | FileSize | Versión | Idioma | Atributos | Secuencia |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Baloncesto    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | Concierto     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | Dance       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | Balón    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Ayuda        | Help.txt     | 1000     |         | 1036     | 0          | 1        |
| January.txt  | January     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Bloc de notas     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Bloc de notas     | Readme.txt   | 1000     |         | 1036     | 0          | 1        |
| Fre.txt      | Ayuda        | Fre.txt      | 1000     |         | 1036     | 0          | 1        |



 

Esto completa la localización de ejemplo.

 

 



