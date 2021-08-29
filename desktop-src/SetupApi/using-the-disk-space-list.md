---
description: Para poder agregar o quitar operaciones de archivo de la lista de espacio en disco, debe crearla mediante la función SetupCreateDiskSpaceList.
ms.assetid: 287fd84a-dc8c-4a5c-b998-db5f2fbee5f1
title: Uso de la Disk-Space lista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f715f9e62cc1cbd6019752ab1e7c7ebb365947736b15fd153767c01586ddb008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664595"
---
# <a name="using-the-disk-space-list"></a>Uso de la Disk-Space lista

Para poder agregar o quitar operaciones de archivo de la lista de espacio en disco, debe crearla mediante la función [**SetupCreateDiskSpaceList.**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)

Después de crear una lista de espacio en disco, puede agregar operaciones individuales de copia o eliminación de archivos a la lista mediante [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista). Para agregar todas las operaciones de copia o eliminación de archivos en una sección INF completa, use las funciones [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) o [**SetupAddInstallSectionToDiskSpaceList.**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)

Después de agregar todas las operaciones de instalación a la lista de espacio en disco, puede consultarla para averiguar cuánto espacio en disco se necesita para la instalación especificada mediante la función [**SetupQuerySpaceRequiredOnDrive.**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)

La [**función SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) devuelve las especificaciones de unidad para cada unidad de destino a la que se hace referencia en las operaciones de archivo en la lista de espacio en disco. Puede usar esta información para comparar mediante programación el espacio disponible en estas unidades con el espacio requerido por la instalación.

Para quitar una operación de archivo de la lista de espacio en disco, use la [**función SetupRemoveFromDiskSpaceList.**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) Para quitar todas las operaciones de copia o eliminación de archivos de una sección INF completa, use las funciones [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) o [**SetupRemoveInstallSectionFromDiskSpaceList.**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista)

Una vez que la lista de espacio en disco ya no es necesaria, puede liberar los recursos asignados mediante una llamada a la función [**SetupDestroyDiskSpaceList.**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)

 

 



