---
description: Los cuadros de diálogo se especifican en la columna diálogo de la tabla del cuadro de diálogo. Para obtener más información sobre cómo agregar un cuadro de diálogo o una cartelera a una interfaz de usuario, consulte uso de la interfaz de usuario.
ms.assetid: 7cecb1c6-3dc3-48a1-94b9-1976c72b7764
title: Cuadros de diálogo (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5695a8d936d0933983407ba52a531ea839137c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277557"
---
# <a name="dialog-boxes-windows-installer"></a>Cuadros de diálogo (Windows Installer)

Los cuadros de diálogo se especifican en la columna diálogo de la [tabla del cuadro de diálogo](dialog-table.md). Para obtener más información sobre cómo agregar un cuadro de diálogo o una cartelera a una interfaz de usuario, consulte [uso de la interfaz de usuario](using-the-user-interface.md).

## <a name="reserved-dialog-box-names"></a>Nombres de cuadros de diálogo reservados

Los nombres de los siguientes cuadros de diálogo están reservados por Windows Installer y no se deben usar para los cuadros de diálogo personalizados creados por el usuario. El instalador requiere que estos cuadros de diálogo se muestren en la [tabla del cuadro de diálogo](dialog-table.md) con los siguientes nombres reservados. Cada cuadro de diálogo y nombre solo puede aparecer una vez. Los desarrolladores deben crear estos cuadros de diálogo en la interfaz de usuario. Para obtener información sobre cómo obtener una vista previa de los cuadros de diálogo, vea [importar la interfaz de usuario](importing-the-user-interface.md).



| Nombre del cuadro de diálogo                                      | Breve descripción del cuadro de diálogo                                                                                                                                         |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cuadro de diálogo FilesInUse](filesinuse-dialog.md)           | Alerta al usuario para procesar la sobrescritura o eliminación de archivos.                                                                                                                 |
| [Cuadro de diálogo FirstRun](firstrun-dialog.md)               | Recopila el nombre de usuario, el nombre de la compañía y el ID. del producto.                                                                                                                       |
| [Cuadro de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) | Alerta al usuario de que se va a procesar la sobrescritura o eliminación de archivos y proporciona al usuario la opción de usar el [Administrador de reinicio](/windows/desktop/RstMgr/restart-manager-portal) para cerrar y reiniciar las aplicaciones. |



 

## <a name="required-dialog-boxes"></a>Cuadros de diálogo obligatorios

Durante la instalación, ciertos eventos hacen que Windows Installer comprueben las tablas de secuencia de la [interfaz de usuario](using-a-sequence-table.md) del paquete y muestren el cuadro de diálogo especificado. Por ejemplo, en el caso de un error irrecuperable, Windows Installer muestra el cuadro de diálogo que aparece con un número de secuencia de-3 en la tabla de secuencia de la interfaz de usuario, independientemente de lo que se denomine en la tabla del cuadro de [diálogo](dialog-table.md). En la tabla siguiente se enumeran los eventos específicos y su número de secuencia correspondiente en la tabla de secuencia de la interfaz de usuario:



| Tipo de evento                        | Número de secuencia de la tabla de secuencias de la interfaz de usuario | Descripción del cuadro de diálogo                              |
|--------------------------------------|-----------------------------------------------|--------------------------------------------------------|
| [Error irrecuperable](fatalerror-dialog.md) | -3                                            | La instalación finalizó debido a un error irrecuperable.      |
| [Salida del usuario](userexit-dialog.md)     | -2                                            | La instalación se terminó en la solicitud del usuario. |
| [Salir](exit-dialog.md)              | -1                                            | La instalación se completó correctamente.               |



 

Además, el autor del paquete debe crear un cuadro de diálogo genérico para mostrar Windows Installer mensajes de [error](error-dialog.md) . Este cuadro de diálogo puede tener cualquier nombre, pero este nombre debe especificarse en la propiedad **ErrorDialog** .

## <a name="typical-dialog-boxes"></a>Cuadros de diálogo típicos

Los siguientes cuadros de diálogo son opcionales y se incluyen normalmente en la interfaz de usuario creada de un paquete de instalación. Estos cuadros de diálogo son típicos de la mayoría de los asistentes para la [interfaz de usuario](user-interface-wizard-behavior.md) para instalar archivos. Estos cuadros de diálogo pueden tener cualquier nombre en la tabla del cuadro de diálogo. Los nombres que se muestran solo se recomiendan para mayor claridad y se pueden modificar según sea necesario. Por ejemplo, se pueden usar dos cuadros de diálogo **LicenseAgreement** personalizados diferentes en el paquete y distinguirlos en la tabla de diálogo con los nombres ProfessionalLicenseAgreement y LimitedLicenseAgreement.



| Tipo de cuadro de diálogo                                             | Breve descripción del cuadro de diálogo                         |
|-------------------------------------------------------------|---------------------------------------------------------|
| [Cuadro de diálogo DiskCost](diskcost-dialog.md)                  | Indica que no hay suficiente espacio en disco para la instalación. |
| [Examinar (Cuadro de diálogo)](browse-dialog.md)                      | Permite al usuario seleccionar un directorio.                     |
| [Cancelar (cuadro de diálogo)](cancel-dialog.md)                      | Confirma una solicitud para finalizar la instalación.       |
| [Cuadro de diálogo contrato de licencia](licenseagreement-dialog.md) | Cuadro modal que muestra el contrato de licencia.             |
| [Cuadro de diálogo Selección](selection-dialog.md)                | Cuadro modal que permite al usuario seleccionar elementos.            |



 

 

 
