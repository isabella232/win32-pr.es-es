---
description: Los cuadros de diálogo se especifican en la columna Diálogo de la tabla Diálogo. Para obtener más información sobre cómo agregar un cuadro de diálogo o un cuadro de diálogo a una interfaz de usuario, vea Uso del Interfaz de usuario.
ms.assetid: 7cecb1c6-3dc3-48a1-94b9-1976c72b7764
title: Cuadros de diálogo (Windows Instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5695a8d936d0933983407ba52a531ea839137c09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158582"
---
# <a name="dialog-boxes-windows-installer"></a>Cuadros de diálogo (Windows Instalador)

Los cuadros de diálogo se especifican en la columna Diálogo de la [tabla Dialog](dialog-table.md). Para obtener más información sobre cómo agregar un cuadro de diálogo o un cuadro de diálogo a una interfaz de usuario, vea [Using the Interfaz de usuario](using-the-user-interface.md).

## <a name="reserved-dialog-box-names"></a>Nombres de cuadro de diálogo reservados

Los siguientes nombres de cuadro de diálogo están reservados por Windows Installer y no deben usarse para ningún cuadro de diálogo personalizado creado por el usuario. El instalador requiere que estos cuadros de diálogo aparezcan en la [tabla Dialog con](dialog-table.md) los siguientes nombres reservados. Cada cuadro de diálogo y nombre solo se pueden enumerar una vez. Los desarrolladores deben crear estos cuadros de diálogo en la interfaz de usuario. Para obtener información sobre cómo obtener una vista previa de los cuadros de diálogo, vea [Importing the Interfaz de usuario](importing-the-user-interface.md).



| Nombre del cuadro de diálogo                                      | Breve descripción del cuadro de diálogo                                                                                                                                         |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cuadro de diálogo FilesInUse](filesinuse-dialog.md)           | Alerta al usuario de los procesos de sobrescritura o eliminación de archivos.                                                                                                                 |
| [Cuadro de diálogo FirstRun](firstrun-dialog.md)               | Recopila el nombre de usuario, el nombre de la empresa y el identificador del producto.                                                                                                                       |
| [Cuadro de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) | Alerta al usuario para que procese la sobrescritura o eliminación de archivos y ofrece al usuario la opción de usar [el](/windows/desktop/RstMgr/restart-manager-portal) Administrador de reinicio para cerrar y reiniciar aplicaciones. |



 

## <a name="required-dialog-boxes"></a>Cuadros de diálogo obligatorios

Durante la instalación, algunos eventos hacen que [](using-a-sequence-table.md) Windows Installer compruebe las tablas de secuencia de la interfaz de usuario en el paquete y muestre el cuadro de diálogo especificado. Por ejemplo, en el caso de un error irresal, Windows Installer muestra el cuadro de diálogo que aparece con un número de secuencia de -3 en la tabla de secuencias de la interfaz de usuario, independientemente de cómo se llame a ese cuadro de diálogo en la tabla [Dialog](dialog-table.md). En la tabla siguiente se enumeran los eventos específicos y su número de secuencia correspondiente en la tabla de secuencias de la interfaz de usuario:



| Tipo de evento                        | Número de secuencia de tabla de secuencias de la interfaz de usuario | Descripción del cuadro de diálogo                              |
|--------------------------------------|-----------------------------------------------|--------------------------------------------------------|
| [Error irreales](fatalerror-dialog.md) | -3                                            | La instalación se finalizó por un error irreales.      |
| [Salida del usuario](userexit-dialog.md)     | -2                                            | La instalación se finalizó a petición del usuario. |
| [Salir](exit-dialog.md)              | -1                                            | La instalación se completó correctamente.               |



 

Además, el autor del paquete debe crear un cuadro de diálogo genérico para mostrar Windows error del [instalador.](error-dialog.md) Este cuadro de diálogo puede tener cualquier nombre, pero este nombre debe especificarse en la **propiedad ErrorDialog.**

## <a name="typical-dialog-boxes"></a>Cuadros de diálogo típicos

Los cuadros de diálogo siguientes son opcionales y se incluyen normalmente en la interfaz de usuario de creación de un paquete de instalación. Estos diálogos son típicos de la mayoría de los [asistentes de interfaz de usuario](user-interface-wizard-behavior.md) para instalar archivos. Estos cuadros de diálogo pueden tener cualquier nombre en la tabla Diálogo. Los nombres que se muestran solo se recomiendan para mayor claridad y se pueden modificar según sea necesario. Por ejemplo, se pueden usar dos cuadros de diálogo **LicenseAgreement** personalizados diferentes en el paquete y distinguirlos en la tabla Dialog por los nombres ProfessionalLicenseAgreement y LimitedLicenseAgreement.



| Tipo de cuadro de diálogo                                             | Breve descripción del cuadro de diálogo                         |
|-------------------------------------------------------------|---------------------------------------------------------|
| [DiskCost (cuadro de diálogo)](diskcost-dialog.md)                  | Indica que no hay suficiente espacio en disco para la instalación. |
| [Examinar (Cuadro de diálogo)](browse-dialog.md)                      | Permite al usuario seleccionar un directorio.                     |
| [Cuadro de diálogo Cancelar](cancel-dialog.md)                      | Confirma una solicitud para finalizar la instalación.       |
| [Cuadro de diálogo Contrato de licencia](licenseagreement-dialog.md) | Cuadro modal que muestra el contrato de licencia.             |
| [Cuadro de diálogo Selección](selection-dialog.md)                | Cuadro modal que permite al usuario seleccionar elementos.            |



 

 

 
