---
description: El Windows Installer instala y quita los bloques de recursos a los que se hace referencia como componentes de Windows Installer. Para obtener más información, vea grupo de tablas básicas y componentes y características.
ms.assetid: e51dffed-d1cb-4a12-8615-0c0f612f993b
title: Especificar componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98cb254498236b85ab5c2bc0df3bd32892227b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908121"
---
# <a name="specifying-components"></a>Especificar componentes

El Windows Installer instala y quita los bloques de recursos a los que se hace referencia como [componentes de Windows Installer](windows-installer-components.md). Para obtener más información, vea [grupo de tablas básicas](core-tables-group.md) y [componentes y características](components-and-features.md).

En esta sección, agregará información acerca de los componentes utilizados en el ejemplo del Bloc de notas a la [tabla de componentes](component-table.md) que creó en [importar una base de datos en blanco](importing-a-blank-database.md). Para obtener más información, vea [organizar aplicaciones en componentes](organizing-applications-into-components.md) y [definir componentes del instalador](defining-installer-components.md).

El ejemplo de Bloc de notas usa ocho componentes para controlar los recursos.



| Componente | Recursos                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| Baloncesto  | Baseball.txt, sBaseball                                                                                               |
| Concierto   | Concert.txt, sConcert                                                                                                 |
| Dance     | Dance.txt, sDance                                                                                                     |
| Balón  | Football.txt, sFootball                                                                                               |
| Ayuda      | Help.txt, sHelp                                                                                                       |
| January   | January.txt, sJanuary                                                                                                 |
| NewYears  | NewYears.txt, sNewYears                                                                                               |
| Bloc de notas   | Redpark.exe, Readme.txt, sReadme, sNotepad, **HKEY \_ local \_ Machine** \\ **software** \\  \\ **ejemplo de Bloc de notas** de Microsoft |



 

Cada componente debe identificarse con un [GUID](guid.md)de identificador de componente único. Si está reproduciendo el ejemplo, no vuelva a usar los mismos GUID de ID. de componente en la tabla siguiente. En su lugar, use una utilidad como Guidgen.exe para generar nuevos GUID para los componentes.

Asegúrese de usar una cadena de GUID coherente con el tipo de datos Windows Installer GUID. Para obtener más información, vea [cambiar el código de componente](changing-the-component-code.md) y [lo que sucede si se interrumpen las reglas de componentes](what-happens-if-the-component-rules-are-broken.md) .

Use Orca u otro editor de bases de datos para especificar los siguientes datos en la [tabla de componentes](component-table.md) en blanco de MNP2000.msi. No reutilice los GUID que se muestran a continuación en la columna ComponentId en el ejemplo.



| Componente | ComponentId                            | Directorio\_ | Atributos | Condición | Rutas      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Baloncesto  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Concierto   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Concert.txt  |
| Dance     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Dance.txt    |
| Balón  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Ayuda      | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| January   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Bloc de notas   | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

Los directorios de origen y de destino de cada componente se especifican mediante el valor especificado en la \_ columna directorio. El instalador resuelve la ubicación de este directorio con la información de la tabla de directorio. El instalador usa los archivos de ruta de acceso de claves especificados en la columna de ruta de clave para detectar cada componente. Los atributos de ejecución remota se establecen en el ejemplo para que los componentes puedan ejecutarse desde el origen o ejecutarse localmente.

[Continuar](specifying-files-and-file-attributes.md)

 

 



