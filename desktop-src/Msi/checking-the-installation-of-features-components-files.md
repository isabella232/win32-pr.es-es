---
description: Si después de ejecutar una instalación, debe comprobar que se ha instalado una característica determinada, un componente o un archivo, active la opción de registro detallado durante la instalación. Consulte Windows Installer opciones de registro y de la línea de comandos.
ms.assetid: c4547e5d-ea71-494f-9d92-c7fef23bcc0f
title: Comprobar la instalación de características, componentes y archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7cab15b4f0590ee5613865d4b7c21439eec6dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652591"
---
# <a name="checking-the-installation-of-features-components-files"></a>Comprobar la instalación de características, componentes y archivos

Si después de ejecutar una instalación, debe comprobar que se ha instalado una característica determinada, un componente o un archivo, active la opción de registro detallado durante la instalación. Consulte [Windows Installer](windows-installer-logging.md) opciones de registro y de la [línea de comandos](command-line-options.md).

El registro detallado incluye una entrada para cada característica y componente que puede instalar el paquete de instalación. El registro indica cuál era el estado de esa característica o componente antes de la instalación, qué estado solicitó la instalación y en qué estado dejó el instalador la característica o componente. Las entradas de características y componentes en el registro aparecen como los ejemplos siguientes.

``` syntax
MSI (s) (40:A4): Feature: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
MSI (s) (40:A4): Component: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
```

Este registro detallado indica que:

-   el estado de la instalación de la característica de QuickTest y el componente no estaba presente antes de ejecutar el paquete
-   el paquete solicitó una instalación local de estos
-   la característica y el componente se dejaron en el estado instalado localmente después de ejecutar el paquete.

La etiqueta "installed" en el registro hace referencia al estado de instalación actual de la característica o componente "Request" hace referencia al estado de instalación solicitado de la característica o componente. "Acción" hace referencia al estado de acción real de la característica o componente.

En la tabla siguiente se enumeran los posibles estados de componente o característica que pueden aparecer en el registro.



| Entrada de registro              | Descripción                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Solicitud: null          | Ninguna solicitud.                                                                                                     |
| Acción: null           | No se realiza ninguna acción.                                                                                                |
| Instalado: ausente      | El componente o característica no está instalado actualmente.                                                                |
| Solicitud: ausente        | Se desinstalará el componente de solicitudes de instalación o la característica.                                                      |
| Acción: ausente         | El instalador desinstala realmente componentes o características.                                                             |
| Instalado: local       | El componente o característica está instalado actualmente para ejecutarse de forma local.                                                       |
| Solicitud: local         | El componente o característica de solicitudes de instalación se instala para ejecutarse localmente.                                           |
| Acción: local          | En realidad, el instalador instala componentes o características para ejecutarse localmente.                                                  |
| Instalado: origen      | El componente o característica está instalado actualmente para ejecutarse desde el origen.                                                 |
| Solicitado: origen      | La instalación solicita que se instale el componente o característica para ejecutarse desde el origen.                                |
| Acción: origen         | El instalador instala realmente el componente o característica para ejecutar desde el origen.                                        |
| Instalado: anuncio   | La característica está anunciada actualmente. Los componentes nunca se anuncian.                                               |
| Solicitud: anuncio     | La característica de solicitudes de instalación se instala como una característica anunciada.                                            |
| Acción: anunciar      | El instalador instala realmente la característica como una característica anunciada.                                               |
| Solicitud: reinstalar     | La característica de solicitudes de instalación se vuelve a instalar. Los componentes no usan el estado de reinstalación.                            |
| Acción: reinstalar      | En realidad, el instalador vuelve a instalar la característica.                                                                          |
| Instalado: actual     | La característica está instalada actualmente en el estado de instalación creada de forma predeterminada.                                           |
| Solicitud: actual       | La característica de solicitudes de instalación se instala en el estado de instalación creada de forma predeterminada.                               |
| Acción: actual        | El instalador instala realmente la característica en el estado de instalación creado de forma predeterminada.                                  |
| Acción: FileAbsent     | El instalador desinstala realmente los archivos del componente y deja todos los demás recursos del componente instalado.      |
| Acción: HKCRAbsent     | El instalador quita realmente la información HKCR del componente. La información de archivos y no HKCR permanecerá.                  |
| Acción: HKCRFileAbsent | El instalador quita realmente la información y los archivos HKCR del componente. Todos los demás recursos del componente permanecen. |



 

El registro detallado tiene una entrada para cada archivo que puede instalar el paquete. El registro indica lo que se ha realizado en el archivo y proporciona una explicación. Las entradas de archivo del registro aparecen como en el ejemplo siguiente.

``` syntax
MSI (s) (40:A4): File: C:\Test\TESTDB.EXE;  Won't Overwrite;  Existing
 file is of an equal version
```

Este registro indica que el instalador no sobrescribirá el archivo de Testdb.exe existente porque el archivo existente es el mismo que la versión que se está instalando.

> [!Note]  
> Si necesita crear un paquete de instalación que busque un archivo o directorio existente en el equipo del usuario durante una instalación, use el método descrito en [Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

 

 

 



