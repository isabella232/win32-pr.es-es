---
description: El Windows instala y quita bloques de recursos denominados Windows Installer. Para obtener más información, vea Grupo de tablas principales y Componentes y características.
ms.assetid: e51dffed-d1cb-4a12-8615-0c0f612f993b
title: Especificar componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2264784d3edaad5b46017e3d337f8abfec66e1b60d18ba54388b03beddb13b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628005"
---
# <a name="specifying-components"></a>Especificar componentes

El Windows instala y quita bloques de recursos denominados Windows [Installer Components](windows-installer-components.md). Para obtener más información, [vea Grupo de tablas principales](core-tables-group.md) y Componentes y [características.](components-and-features.md)

En esta sección agregará información sobre los componentes utilizados [](component-table.md) por el ejemplo Bloc de notas a la tabla de componentes que creó en [Importar una base de datos en blanco](importing-a-blank-database.md). Para obtener más información, vea [Organizar aplicaciones en componentes y](organizing-applications-into-components.md) Definir componentes del [instalador](defining-installer-components.md).

En Bloc de notas ejemplo se usan ocho componentes para controlar los recursos.



| Componente | Recursos                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| Béisbol  | Baseball.txt, sBaseball                                                                                               |
| Concierto   | Concert.txt, sConcert                                                                                                 |
| Baile     | Dance.txt, sDance                                                                                                     |
| Fútbol  | Football.txt, sFootball                                                                                               |
| Ayuda      | Help.txt, sHelp                                                                                                       |
| January   | January.txt, sJanuary                                                                                                 |
| NewYears  | NewYears.txt, sNewYears                                                                                               |
| Bloc de notas   | Redpark.exe, Readme.txt, sReadme, sNotepad, **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Bloc de notas Sample** |



 

Cada componente debe identificarse con un GUID de identificador de [componente único.](guid.md) Si va a reproducir el ejemplo, no reutilice los mismos GUID de identificador de componente en la tabla siguiente. En su lugar, use una utilidad como Guidgen.exe para generar nuevos GUID para los componentes.

Asegúrese de usar una cadena GUID coherente con el tipo de Windows GUID del instalador. Para obtener más información, vea [Cambiar el código de componente](changing-the-component-code.md) y ¿Qué ocurre si se han roto las reglas de [componente?](what-happens-if-the-component-rules-are-broken.md)

Use Orca u otro editor de bases de datos para escribir los datos siguientes en la tabla [de componentes en](component-table.md) blanco MNP2000.msi. No reutilice los GUID que se muestran a continuación en la columna ComponentId del ejemplo.



| Componente | Componentid                            | Directorio\_ | Atributos | Condición | Ruta de acceso de clave      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Béisbol  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Concierto   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | NOCIONESDIR     | 2          |           | Concert.txt  |
| Baile     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | NOCIONESDIR     | 2          |           | Dance.txt    |
| Fútbol  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Ayuda      | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| January   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Bloc de notas   | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

El valor especificado en la columna Directory especifica los directorios de origen y destino de cada \_ componente. El instalador resuelve la ubicación de este directorio mediante la información de la tabla Directory. El instalador usa los archivos de ruta de acceso de clave especificados en la columna KeyPath para detectar cada componente. Los atributos de ejecución remota se establecen en el ejemplo para que los componentes puedan ejecutarse desde el origen o ejecutarse localmente.

[Continuar](specifying-files-and-file-attributes.md)

 

 



