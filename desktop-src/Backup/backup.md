---
title: Copia de seguridad
description: Permita que las aplicaciones de copia de seguridad se comuniquen con otras aplicaciones y servicios sobre las operaciones de copia de seguridad y restauración. Realice una copia de seguridad en cinta, inicialice la cinta y recupere la información de la unidad de cinta. Mantener archivos duplicados con el almacén de instancia única (SIS).
ms.assetid: 97c3e2c4-8214-4093-bd13-3c38c91e08bd
keywords:
- Copia de seguridad de backup
- copia de seguridad, Inicio
- restauración de copias de seguridad de operaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689a5a4613bdf029b270947b523727ea00a6e05d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149451"
---
# <a name="backup"></a><span data-ttu-id="84def-108">Copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="84def-108">Backup</span></span>

<span data-ttu-id="84def-109">Las claves del registro para copias de seguridad y restauración permiten a las aplicaciones de copia de seguridad comunicarse con otras aplicaciones y servicios sobre las operaciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="84def-109">Registry keys for backup and restore allow backup applications to communicate with other applications and services about backup and restore operations.</span></span> <span data-ttu-id="84def-110">Para obtener más información, vea [claves y valores del registro para copias de seguridad y restauración](registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="84def-110">For more information, see [Registry Keys and Values for Backup and Restore](registry-keys-for-backup-and-restore.md).</span></span>

<span data-ttu-id="84def-111">La API de copia de seguridad en cinta permite a las aplicaciones de copia de seguridad leer y escribir en una cinta, inicializar una cinta y recuperar la información de la unidad de cinta o cinta.</span><span class="sxs-lookup"><span data-stu-id="84def-111">The tape backup API enables backup applications to read from and write to a tape, initialize a tape, and retrieve tape or tape drive information.</span></span> <span data-ttu-id="84def-112">Para obtener más información, consulte [copia de seguridad en cinta](tape-backup.md).</span><span class="sxs-lookup"><span data-stu-id="84def-112">For more information, see [Tape Backup](tape-backup.md).</span></span>

<span data-ttu-id="84def-113">El almacén de instancia única (SIS) es una arquitectura diseñada para mantener archivos duplicados con una sobrecarga mínima.</span><span class="sxs-lookup"><span data-stu-id="84def-113">Single-instance store (SIS) is an architecture designed to maintain duplicate files with a minimum of overhead.</span></span> <span data-ttu-id="84def-114">La aplicación de copia de seguridad usa la API de copia de seguridad de SIS para tener acceso a la arquitectura de SIS.</span><span class="sxs-lookup"><span data-stu-id="84def-114">Backup application use the SIS backup API to access the SIS architecture.</span></span> <span data-ttu-id="84def-115">Para obtener más información, vea [almacenamiento de instancia única y copia de seguridad de SIS](single-instance-store-and-sis-backup.md).</span><span class="sxs-lookup"><span data-stu-id="84def-115">For more information, see [Single-Instance Store and SIS Backup](single-instance-store-and-sis-backup.md).</span></span>

<span data-ttu-id="84def-116">La copia de seguridad y restauración de archivos cifrados está habilitada por la API de cifrado sin formato, que lee y escribe archivos cifrados y mantiene los datos en formato cifrado.</span><span class="sxs-lookup"><span data-stu-id="84def-116">Backup and restore of encrypted files is enabled by the raw encryption API, which reads and writes encrypted files while keeping the data in encrypted format.</span></span> <span data-ttu-id="84def-117">La API permite que se realicen copias de seguridad y restauraciones de los datos cifrados de estos archivos, a la vez que se cumplen los objetivos de mantenimiento de la seguridad de los datos de los que se ha realizado una copia de seguridad y que se pueden usar en una aplicación que no tiene permiso para utilizar las claves de cifrado en el archivo.</span><span class="sxs-lookup"><span data-stu-id="84def-117">The API allows the encrypted data in these files to be backed up and restored, while meeting the goals of maintaining the security of the backed up data, and being usable by an application that lacks permission to use the encryption keys on the file.</span></span> <span data-ttu-id="84def-118">Para obtener más información, vea [copia de seguridad y restauración de archivos cifrados](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).</span><span class="sxs-lookup"><span data-stu-id="84def-118">For more information, see [Backup and Restore of Encrypted Files](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).</span></span>

<span data-ttu-id="84def-119">La herramienta Srdelayed puede permitir que las aplicaciones de recuperación del estado del sistema muevan, eliminen y establezcan el nombre corto de los archivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="84def-119">The Srdelayed tool can enable system state recovery applications to move, delete, and set the short name of system files.</span></span> <span data-ttu-id="84def-120">Para obtener más información, vea [Srdelayed.exe](srdelayed-exe.md).</span><span class="sxs-lookup"><span data-stu-id="84def-120">For more information, see [Srdelayed.exe](srdelayed-exe.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84def-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84def-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84def-122">Referencia de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="84def-122">Backup Reference</span></span>](backup-reference.md)
</dt> </dl>

 

 