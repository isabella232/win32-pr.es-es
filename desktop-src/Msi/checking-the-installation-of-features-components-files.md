---
description: Si después de ejecutar una instalación, debe comprobar que se ha instalado una característica, un componente o un archivo determinados, active la opción de registro detallado durante la instalación. Vea Windows registro del instalador y opciones de línea de comandos.
ms.assetid: c4547e5d-ea71-494f-9d92-c7fef23bcc0f
title: Comprobar la instalación de características, componentes, archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866b4f7b042c97660e43a92fc55eeb99e2f1e9f3574a9b03c4d3d6e6096504c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145617"
---
# <a name="checking-the-installation-of-features-components-files"></a>Comprobar la instalación de características, componentes, archivos

Si después de ejecutar una instalación, debe comprobar que se ha instalado una característica, un componente o un archivo determinados, active la opción de registro detallado durante la instalación. Vea [Windows registro del instalador y](windows-installer-logging.md) opciones de la línea de [comandos](command-line-options.md).

El registro detallado incluye una entrada para cada característica y componente que el paquete de instalación puede instalar. El registro indica cuál era el estado de esa característica o componente antes de la instalación, qué estado solicitó la instalación y en qué estado dejó el instalador la característica o componente. Las entradas de características y componentes del registro aparecen como los ejemplos siguientes.

``` syntax
MSI (s) (40:A4): Feature: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
MSI (s) (40:A4): Component: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
```

Este registro detallado indica que:

-   el estado de instalación de la característica y componente QuickTest no estaba presente antes de ejecutar el paquete
-   el paquete solicitó una instalación local de estos
-   La característica y el componente se dejaron en el estado instalado localmente después de ejecutar el paquete.

La etiqueta "Instalado" en el registro hace referencia al estado de instalación actual de la característica o componente; "Solicitud" hace referencia al estado de instalación solicitado de la característica o componente. "Acción" hace referencia al estado de acción real de la característica o componente.

En la tabla siguiente se enumeran los posibles estados de componente o característica que pueden aparecer en el registro.



| Entrada de registro              | Descripción                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Solicitud: Null          | Sin solicitud.                                                                                                     |
| Acción: Null           | No se ha realizado ninguna acción.                                                                                                |
| Instalado: Ausente      | El componente o característica no está instalado actualmente.                                                                |
| Solicitud: Absent        | Componente o característica de solicitudes de instalación que se desinstalarán.                                                      |
| Acción: Ausente         | El instalador desinstala realmente el componente o la característica.                                                             |
| Instalado: Local       | El componente o característica está instalado actualmente para ejecutarse localmente.                                                       |
| Solicitud: Local         | El componente o la característica de solicitudes de instalación se instalan para ejecutarse localmente.                                           |
| Acción: Local          | El instalador instala realmente el componente o la característica para ejecutar localmente.                                                  |
| Instalado: Origen      | El componente o característica está instalado actualmente para ejecutarse desde el origen.                                                 |
| Solicitado: Origen      | La instalación solicita que ese componente o característica se instale para ejecutarse desde el origen.                                |
| Acción: Origen         | El instalador instala realmente el componente o la característica que se ejecutará desde el origen.                                        |
| Instalado: Anunciar   | La característica se anuncia actualmente. Los componentes nunca se anuncian.                                               |
| Solicitud: Anunciar     | La característica de solicitudes de instalación se instalará como una característica anunciada.                                            |
| Acción: Anunciar      | El instalador instala realmente la característica como una característica anunciada.                                               |
| Solicitud: Reinstalar     | Característica de solicitudes de instalación que se va a volver a instalar. Los componentes no usan el estado de reinstalación.                            |
| Acción: Reinstalar      | El instalador vuelve a instalar la característica.                                                                          |
| Instalado: Actual     | La característica está instalada actualmente en el estado de instalación de creación predeterminado.                                           |
| Solicitud: Actual       | La característica de solicitudes de instalación se instalará en el estado de instalación de creación predeterminado.                               |
| Acción: Actual        | El instalador instala realmente la característica en el estado de instalación de creación predeterminado.                                  |
| Acción: FileAbsent     | El instalador desinstala realmente los archivos del componente y deja instalados todos los demás recursos del componente.      |
| Acción: HKCRAbsent     | El instalador quita realmente la información de HKCR del componente. La información de archivos y no HKCR permanece.                  |
| Acción: HKCRFileAbsent | El instalador quita realmente la información y los archivos HKCR del componente. Todos los demás recursos del componente permanecen. |



 

El registro detallado tiene una entrada para cada archivo que puede instalar el paquete. El registro indica lo que se hizo al archivo y proporciona alguna explicación. Las entradas de archivo del registro aparecen como en el ejemplo siguiente.

``` syntax
MSI (s) (40:A4): File: C:\Test\TESTDB.EXE;  Won't Overwrite;  Existing
 file is of an equal version
```

Este registro indica que el instalador no sobrescribirá el archivo Testdb.exe existente porque el archivo existente es el mismo que la versión que se está instalando.

> [!Note]  
> Si necesita crear un paquete de instalación que busque un archivo o directorio existente en el equipo del usuario durante una instalación, use el método descrito en Búsqueda de [aplicaciones, archivos,](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)entradas del Registro o entradas de .ini existentes.

 

 

 



