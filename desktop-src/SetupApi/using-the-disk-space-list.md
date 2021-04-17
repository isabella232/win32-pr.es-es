---
description: Antes de poder agregar o quitar operaciones de archivo de la lista de espacio en disco, debe crearla con la función SetupCreateDiskSpaceList.
ms.assetid: 287fd84a-dc8c-4a5c-b998-db5f2fbee5f1
title: Uso de la lista de Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a19f100fd5190472f5f6bfebaf74affe1a789cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666941"
---
# <a name="using-the-disk-space-list"></a>Uso de la lista de Disk-Space

Antes de poder agregar o quitar operaciones de archivo de la lista de espacio en disco, debe crearla con la función [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) .

Después de crear una lista de espacio en disco, puede Agregar operaciones individuales de copia o eliminación de archivos a la lista mediante [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista). Para agregar todas las operaciones de copia o eliminación de archivos en una sección de un archivo INF completo, utilice la función [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) o [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) .

Después de agregar todas las operaciones de instalación a la lista de espacio en disco, puede consultarlo para averiguar cuánto espacio en disco se necesita para la instalación especificada mediante la función [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) .

La función [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) devuelve las especificaciones de unidad para cada unidad de destino a la que se hace referencia en las operaciones de archivo en la lista de espacio en disco. Puede usar esta información para comparar mediante programación el espacio disponible en estas unidades con el espacio necesario para la instalación.

Para quitar una operación de archivo de la lista de espacio en disco, utilice la función [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) . Para quitar todas las operaciones de copia o eliminación de archivos de una sección de un archivo INF completo, utilice la función [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) o [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) .

Una vez que ya no se necesita la lista de espacio en disco, se pueden liberar los recursos asignados a ella mediante una llamada a la función [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) .

 

 



