---
description: Las siguientes funciones se usan con la lista de espacio en disco.
ms.assetid: 18693b2d-6b0f-4f9c-b3cf-e50c36e2f2e1
title: Disk-Space list functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e20e6f656110cc3b8c2ebd607f28b5d701ce3007b4ce8812f7e3bcad2f7f5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887371"
---
# <a name="disk-space-list-functions"></a>Disk-Space list functions

Las siguientes funciones se usan con la lista de espacio en disco.



| Función                                                                                         | Descripción                                                                                                                          |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupAdjustDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupadjustdiskspacelista)                                     | Ajusta la cantidad de espacio necesario para una unidad especificada.                                                                          |
| [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)                                     | Crea una lista de espacio en disco y le asigna recursos.                                                                             |
| [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)                                   | Destruye una lista de espacio en disco y libera los recursos asignados a ella.                                                                   |
| [**SetupDuplicateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupduplicatediskspacelista)                               | Duplica una lista de espacio en disco como una nueva lista de espacio en disco independiente.                                                                   |
| [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)                       | Rellena un búfer con las especificaciones de unidad para todas las unidades enumeradas en la lista de espacio en disco.                                       |
| [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)                         | Devuelve la cantidad total de espacio en disco necesaria para completar las operaciones de archivo en una unidad determinada enumerada en la lista de espacio en disco. |
| [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)                                       | Agrega una operación de copia o eliminación de archivos a la lista de espacio en disco.                                                                         |
| [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista)                         | Agrega todas las operaciones de archivo de una sección **Copiar archivos** o Eliminar **archivos** de un archivo INF a una lista de espacio en disco.                    |
| [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)           | Agrega todas las operaciones de archivo de **una sección Instalar** de un archivo INF a la lista de espacio en disco.                                        |
| [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista)                             | Quita una operación de copia o eliminación de archivos de una lista de espacio en disco.                                                                      |
| [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista)               | Quita todas las operaciones de archivo de una sección **Copiar archivos** o Eliminar **archivos** de un archivo INF de una lista de espacio en disco.               |
| [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) | Quita todas las operaciones de archivo de la **sección Instalar** de un archivo INF de la lista de espacio en disco.                                  |



 

 

 



