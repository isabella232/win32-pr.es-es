---
description: Los escritores pueden ajustar el rendimiento de varios tipos de copia de seguridad en el nivel de conjunto de archivos indicando a través de un tipo de copia de seguridad de especificación de archivo, indicado por una máscara de bits o bit a bit o de los miembros de la \_ \_ enumeración de tipo de copia de seguridad de especificación de archivo de VSS \_ \_ .
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Compatibilidad con esquemas de nivel de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460d256a3eaa016933e697687d05e26838c14ae2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002949"
---
# <a name="file-level-schema-support"></a><span data-ttu-id="05c35-103">Compatibilidad con esquemas de nivel de archivo</span><span class="sxs-lookup"><span data-stu-id="05c35-103">File Level Schema Support</span></span>

<span data-ttu-id="05c35-104">Los escritores pueden ajustar el rendimiento de varios tipos de copia de seguridad en el nivel de [*conjunto de archivos*](vssgloss-f.md) indicando a través de un tipo de copia de seguridad de especificación de archivo, indicado por una máscara de bits o bit a bit o de los miembros de la enumeración de tipo de [**\_ copia de \_ \_ seguridad \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) de especificación de archivo de VSS.</span><span class="sxs-lookup"><span data-stu-id="05c35-104">Writers can fine-tune the performance of various types of backup at the [*file set*](vssgloss-f.md) level by indicating through a file specification backup type, indicated by a bit mask or bitwise OR of the members of the [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) enumeration.</span></span>

<span data-ttu-id="05c35-105">En el caso de los tipos de copia de seguridad especificados, el escritor indica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="05c35-105">For specified types of backup, the writer indicates the following:</span></span>

-   <span data-ttu-id="05c35-106">Si será necesario crear una instantánea del volumen para realizar correctamente la copia de seguridad de un conjunto de archivos.</span><span class="sxs-lookup"><span data-stu-id="05c35-106">Whether it will be necessary to shadow copy the volume to properly back up a file set.</span></span> <span data-ttu-id="05c35-107">Por ejemplo, si los archivos de un conjunto de archivos no están abiertos exclusivamente por el escritor y pueden asegurarse de que es estable, no se necesita una instantánea.</span><span class="sxs-lookup"><span data-stu-id="05c35-107">For instance, if the files in a file set are not exclusively opened by the writer and it can ensure that it is stable, a shadow copy is not needed.</span></span>
-   <span data-ttu-id="05c35-108">Si el solicitante tiene que realizar la copia de seguridad de forma que, independientemente de la hora de la última modificación u otros problemas, se restaurará la versión actual de los archivos del conjunto de archivos en la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="05c35-108">Whether the requester has to perform the backup in such a way that, regardless of last modification time or other issues, the version of the file set's files current at backup will be restored.</span></span> <span data-ttu-id="05c35-109">Normalmente, esto significa que el conjunto de archivos se copia como parte de la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="05c35-109">Typically, this means that the file set is copied as part of the backup.</span></span>

<span data-ttu-id="05c35-110">Los valores del [**\_ tipo de \_ copia \_ de \_ seguridad de especificación de archivo de VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que indican el requisito de instantánea son:</span><span class="sxs-lookup"><span data-stu-id="05c35-110">The values of [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) that indicate shadow copy requirement are:</span></span>

-   <span data-ttu-id="05c35-111">VSS \_ FSBT \_ todas las \_ instantáneas \_ necesarias</span><span class="sxs-lookup"><span data-stu-id="05c35-111">VSS\_FSBT\_ALL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="05c35-112">se \_ \_ requiere una \_ instantánea \_ completa de FSBT de VSS</span><span class="sxs-lookup"><span data-stu-id="05c35-112">VSS\_FSBT\_FULL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="05c35-113">se \_ \_ requiere la \_ instantánea \_ diferencial FSBT de VSS</span><span class="sxs-lookup"><span data-stu-id="05c35-113">VSS\_FSBT\_DIFFERENTIAL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="05c35-114">se \_ \_ requiere la instantánea incremental FSBT de VSS \_ \_</span><span class="sxs-lookup"><span data-stu-id="05c35-114">VSS\_FSBT\_INCREMENTAL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="05c35-115">se \_ \_ requiere la \_ instantánea de registro FSBT de VSS \_</span><span class="sxs-lookup"><span data-stu-id="05c35-115">VSS\_FSBT\_LOG\_SNAPSHOT\_REQUIRED</span></span>

<span data-ttu-id="05c35-116">Los valores del [**\_ tipo de \_ copia \_ de \_ seguridad de especificación de archivo de VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que indican el requisito de hacer una copia de seguridad de un archivo son:</span><span class="sxs-lookup"><span data-stu-id="05c35-116">The values of [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) that indicate the requirement to back up a file are:</span></span>

-   <span data-ttu-id="05c35-117">VSS \_ FSBT \_ todas las \_ copias de seguridad \_ necesarias</span><span class="sxs-lookup"><span data-stu-id="05c35-117">VSS\_FSBT\_ALL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="05c35-118">se \_ \_ requiere la \_ copia de seguridad completa de FSBT de VSS \_</span><span class="sxs-lookup"><span data-stu-id="05c35-118">VSS\_FSBT\_FULL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="05c35-119">se \_ \_ requiere la \_ copia de seguridad diferencial FSBT \_ de VSS</span><span class="sxs-lookup"><span data-stu-id="05c35-119">VSS\_FSBT\_DIFFERENTIAL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="05c35-120">se \_ \_ requiere la copia de seguridad incremental FSBT de VSS \_ \_</span><span class="sxs-lookup"><span data-stu-id="05c35-120">VSS\_FSBT\_INCREMENTAL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="05c35-121">se \_ \_ requiere la \_ copia de seguridad de registros FSBT \_ de VSS</span><span class="sxs-lookup"><span data-stu-id="05c35-121">VSS\_FSBT\_LOG\_BACKUP\_REQUIRED</span></span>

<span data-ttu-id="05c35-122">De forma predeterminada, los conjuntos de archivos se etiquetan con un tipo de copia de seguridad de especificación de archivo de VSS \_ FSBT \_ All \_ backup \_ required \| VSS \_ FSBT \_ All \_ Snapshot \_ required, lo que significa que siempre se requiere una instantánea en el control de los archivos del conjunto de archivos y que los archivos deben copiarse en todos los tipos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="05c35-122">By default, file sets are tagged with a file specification backup type of VSS\_FSBT\_ALL\_BACKUP\_REQUIRED \| VSS\_FSBT\_ALL\_SNAPSHOT\_REQUIRED, meaning that a shadow copy is always required in handling the file set's files, and that the files should be copied in all types of backup.</span></span>

 

 



