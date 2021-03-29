---
description: Administrar directorios con tabla de entradas de directorio, identificadores de directorio, puntos de reanálisis.
title: Sistemas de archivos locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f624ef1999b81adb63ba1d5b7e349259cabd53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812518"
---
# <a name="local-file-systems"></a><span data-ttu-id="4e922-103">Sistemas de archivos locales</span><span class="sxs-lookup"><span data-stu-id="4e922-103">Local File Systems</span></span>

<span data-ttu-id="4e922-104">Un *sistema de archivos* permite a las aplicaciones almacenar y recuperar archivos en dispositivos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="4e922-104">A *file system* enables applications to store and retrieve files on storage devices.</span></span> <span data-ttu-id="4e922-105">Los archivos se colocan en una estructura jerárquica.</span><span class="sxs-lookup"><span data-stu-id="4e922-105">Files are placed in a hierarchical structure.</span></span> <span data-ttu-id="4e922-106">El sistema de archivos especifica las convenciones de nomenclatura de los archivos y el formato para especificar la ruta de acceso a un archivo en la estructura de árbol.</span><span class="sxs-lookup"><span data-stu-id="4e922-106">The file system specifies naming conventions for files and the format for specifying the path to a file in the tree structure.</span></span>

<span data-ttu-id="4e922-107">Cada sistema de archivos consta de uno o varios controladores y bibliotecas de vínculos dinámicos que definen los formatos de datos y las características del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="4e922-107">Each file system consists of one or more drivers and dynamic-link libraries that define the data formats and features of the file system.</span></span> <span data-ttu-id="4e922-108">Los sistemas de archivos pueden existir en muchos tipos diferentes de dispositivos de almacenamiento, incluidos discos duros, gramolas, discos ópticos extraíbles, unidades de copia de seguridad en cinta y tarjetas de memoria.</span><span class="sxs-lookup"><span data-stu-id="4e922-108">File systems can exist on many different types of storage devices, including hard disks, jukeboxes, removable optical disks, tape back-up units, and memory cards.</span></span>

<span data-ttu-id="4e922-109">Todos los sistemas de archivos compatibles con Windows tienen los siguientes componentes de almacenamiento:</span><span class="sxs-lookup"><span data-stu-id="4e922-109">All file systems supported by Windows have the following storage components:</span></span>

-   <span data-ttu-id="4e922-110">Volumen.</span><span class="sxs-lookup"><span data-stu-id="4e922-110">Volumes.</span></span> <span data-ttu-id="4e922-111">Un *volumen* es una colección de directorios y archivos.</span><span class="sxs-lookup"><span data-stu-id="4e922-111">A *volume* is a collection of directories and files.</span></span>
-   <span data-ttu-id="4e922-112">Directorio.</span><span class="sxs-lookup"><span data-stu-id="4e922-112">Directories.</span></span> <span data-ttu-id="4e922-113">Un *directorio* es una colección jerárquica de directorios y archivos.</span><span class="sxs-lookup"><span data-stu-id="4e922-113">A *directory* is a hierarchical collection of directories and files.</span></span>
-   <span data-ttu-id="4e922-114">Archivos.</span><span class="sxs-lookup"><span data-stu-id="4e922-114">Files.</span></span> <span data-ttu-id="4e922-115">Un *archivo* es una agrupación lógica de datos relacionados.</span><span class="sxs-lookup"><span data-stu-id="4e922-115">A *file* is a logical grouping of related data.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4e922-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4e922-116">In this section</span></span>



| <span data-ttu-id="4e922-117">Tema</span><span class="sxs-lookup"><span data-stu-id="4e922-117">Topic</span></span>                                                                | <span data-ttu-id="4e922-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e922-118">Description</span></span>                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e922-119">Administración de directorios</span><span class="sxs-lookup"><span data-stu-id="4e922-119">Directory Management</span></span>](directory-management.md)<br/>          | <span data-ttu-id="4e922-120">Un *directorio* es una colección jerárquica de directorios y archivos.</span><span class="sxs-lookup"><span data-stu-id="4e922-120">A *directory* is a hierarchical collection of directories and files.</span></span> <span data-ttu-id="4e922-121">La única restricción del número de archivos que pueden estar contenidos en un único directorio es el tamaño físico del disco en el que se encuentra el directorio.</span><span class="sxs-lookup"><span data-stu-id="4e922-121">The only constraint on the number of files that can be contained in a single directory is the physical size of the disk on which the directory is located.</span></span><br/> |
| [<span data-ttu-id="4e922-122">Administración de discos</span><span class="sxs-lookup"><span data-stu-id="4e922-122">Disk Management</span></span>](disk-management.md)<br/>                    | <span data-ttu-id="4e922-123">Un *disco duro* es un disco rígido dentro de un equipo que almacena y proporciona acceso relativamente rápido a grandes cantidades de datos.</span><span class="sxs-lookup"><span data-stu-id="4e922-123">A *hard disk* is a rigid disk inside a computer that stores and provides relatively quick access to large amounts of data.</span></span> <span data-ttu-id="4e922-124">Es el tipo de almacenamiento que se usa con más frecuencia con Windows.</span><span class="sxs-lookup"><span data-stu-id="4e922-124">It is the type of storage most often used with Windows.</span></span> <span data-ttu-id="4e922-125">El sistema también admite medios extraíbles.</span><span class="sxs-lookup"><span data-stu-id="4e922-125">The system also supports removable media.</span></span><br/>    |
| [<span data-ttu-id="4e922-126">Administración de archivos</span><span class="sxs-lookup"><span data-stu-id="4e922-126">File Management</span></span>](file-management.md)<br/>                    | <span data-ttu-id="4e922-127">Un *objeto de archivo* proporciona una representación de un recurso (un dispositivo físico o un recurso ubicado en un dispositivo físico) que se puede administrar mediante el sistema de e/s.</span><span class="sxs-lookup"><span data-stu-id="4e922-127">A *file object* provides a representation of a resource (either a physical device or a resource located on a physical device) that can be managed by the I/O system.</span></span><br/>                                                            |
| [<span data-ttu-id="4e922-128">NTFS transaccional (TxF)</span><span class="sxs-lookup"><span data-stu-id="4e922-128">Transactional NTFS (TxF)</span></span>](transactional-ntfs-portal.md)<br/> | <span data-ttu-id="4e922-129">NTFS transaccional (TxF) permite realizar operaciones de archivo en un volumen del sistema de archivos NTFS en una transacción.</span><span class="sxs-lookup"><span data-stu-id="4e922-129">Transactional NTFS (TxF) allows file operations on an NTFS file system volume to be performed in a transaction.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="4e922-130">Administración del volumen</span><span class="sxs-lookup"><span data-stu-id="4e922-130">Volume Management</span></span>](volume-management.md)<br/>                | <span data-ttu-id="4e922-131">El nivel más alto de organización en el sistema de archivos es el *volumen*.</span><span class="sxs-lookup"><span data-stu-id="4e922-131">The highest level of organization in the file system is the *volume*.</span></span> <span data-ttu-id="4e922-132">Un sistema de archivos reside en un volumen.</span><span class="sxs-lookup"><span data-stu-id="4e922-132">A file system resides on a volume.</span></span><br/>                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="4e922-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e922-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4e922-134">[Referencia técnica de FAT](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="4e922-134">[FAT Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="4e922-135">[Tecnologías de sistemas de archivos](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="4e922-135">[File Systems Technologies](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="4e922-136">[Referencia técnica de NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="4e922-136">[NTFS Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span></span>
</dt> </dl>

 

