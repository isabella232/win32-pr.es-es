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
# <a name="using-the-disk-space-list"></a><span data-ttu-id="3018a-103">Uso de la lista de Disk-Space</span><span class="sxs-lookup"><span data-stu-id="3018a-103">Using the Disk-Space List</span></span>

<span data-ttu-id="3018a-104">Antes de poder agregar o quitar operaciones de archivo de la lista de espacio en disco, debe crearla con la función [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="3018a-104">Before you can add or remove file operations from the disk-space list, you must create it by using the [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) function.</span></span>

<span data-ttu-id="3018a-105">Después de crear una lista de espacio en disco, puede Agregar operaciones individuales de copia o eliminación de archivos a la lista mediante [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista).</span><span class="sxs-lookup"><span data-stu-id="3018a-105">After you create a disk-space list you can add individual file copy or delete operations to the list by using [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista).</span></span> <span data-ttu-id="3018a-106">Para agregar todas las operaciones de copia o eliminación de archivos en una sección de un archivo INF completo, utilice la función [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) o [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="3018a-106">To add all the file copy or delete operations in an entire INF section, use either the [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) or [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) function.</span></span>

<span data-ttu-id="3018a-107">Después de agregar todas las operaciones de instalación a la lista de espacio en disco, puede consultarlo para averiguar cuánto espacio en disco se necesita para la instalación especificada mediante la función [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) .</span><span class="sxs-lookup"><span data-stu-id="3018a-107">After you add all the installation operations to the disk-space list, you can query it to find out how much disk space is required for the specified installation by using the [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) function.</span></span>

<span data-ttu-id="3018a-108">La función [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) devuelve las especificaciones de unidad para cada unidad de destino a la que se hace referencia en las operaciones de archivo en la lista de espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="3018a-108">The [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) function returns the drive specifications for each target drive referenced in the file operations on the disk-space list.</span></span> <span data-ttu-id="3018a-109">Puede usar esta información para comparar mediante programación el espacio disponible en estas unidades con el espacio necesario para la instalación.</span><span class="sxs-lookup"><span data-stu-id="3018a-109">You can use this information to programmatically compare the available space on these drives with the space required by the installation.</span></span>

<span data-ttu-id="3018a-110">Para quitar una operación de archivo de la lista de espacio en disco, utilice la función [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="3018a-110">To remove a file operation from the disk-space list, use the [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) function.</span></span> <span data-ttu-id="3018a-111">Para quitar todas las operaciones de copia o eliminación de archivos de una sección de un archivo INF completo, utilice la función [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) o [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="3018a-111">To remove all file copy or delete operations from an entire INF section, use the [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) or [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) function.</span></span>

<span data-ttu-id="3018a-112">Una vez que ya no se necesita la lista de espacio en disco, se pueden liberar los recursos asignados a ella mediante una llamada a la función [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) .</span><span class="sxs-lookup"><span data-stu-id="3018a-112">After the disk-space list is no longer required, you can release the resources allocated to it by calling the [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) function.</span></span>

 

 



