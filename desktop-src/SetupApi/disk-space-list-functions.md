---
description: Las siguientes funciones se usan con la lista de espacio en disco.
ms.assetid: 18693b2d-6b0f-4f9c-b3cf-e50c36e2f2e1
title: Funciones de lista de Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f520cc7a3ddcd0b12b27bd11768a95231a8ed4b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360902"
---
# <a name="disk-space-list-functions"></a>Funciones de lista de Disk-Space

Las siguientes funciones se usan con la lista de espacio en disco.



| Función                                                                                         | Descripción                                                                                                                          |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupAdjustDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupadjustdiskspacelista)                                     | Ajusta la cantidad de espacio necesario para una unidad especificada.                                                                          |
| [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)                                     | Crea una lista de espacio en disco y le asigna recursos.                                                                             |
| [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)                                   | Destruye una lista de espacio en disco, liberando los recursos asignados a ella.                                                                   |
| [**SetupDuplicateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupduplicatediskspacelista)                               | Duplica una lista de espacio en disco como una lista nueva de espacio en disco independiente.                                                                   |
| [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)                       | Rellena un búfer con las especificaciones de unidad de todas las unidades enumeradas en la lista espacio en disco.                                       |
| [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)                         | Devuelve la cantidad total de espacio en disco necesaria para completar las operaciones de archivo en una unidad determinada incluida en la lista de espacio en disco. |
| [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)                                       | Agrega una operación de copia o eliminación de archivos a la lista de espacio en disco.                                                                         |
| [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista)                         | Agrega todas las operaciones de archivo de una sección **copiar archivos** o **eliminar archivos** de un archivo INF a una lista de espacio en disco.                    |
| [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)           | Agrega todas las operaciones de archivo en una sección de **instalación** de un archivo INF a la lista de espacio en disco.                                        |
| [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista)                             | Quita una operación de copia o eliminación de un archivo de una lista de espacio en disco.                                                                      |
| [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista)               | Quita todas las operaciones de archivo en una sección **copiar archivos** o **eliminar archivos** de un archivo INF de una lista de espacio en disco.               |
| [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) | Quita todas las operaciones de archivo de la sección de **instalación** de un archivo INF de la lista de espacio en disco.                                  |



 

 

 



