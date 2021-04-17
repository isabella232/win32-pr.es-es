---
description: El sistema de archivos cifrados (EFS) proporciona protección criptográfica de archivos individuales en volúmenes del sistema de archivos NTFS mediante un sistema de clave pública.
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: Cifrado de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c05d8d746e597fe180feffe25f7f553819e822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688468"
---
# <a name="file-encryption"></a><span data-ttu-id="03961-103">Cifrado de archivos</span><span class="sxs-lookup"><span data-stu-id="03961-103">File Encryption</span></span>

<span data-ttu-id="03961-104">El sistema de archivos cifrado, o EFS, proporciona un nivel de seguridad adicional para los archivos y directorios.</span><span class="sxs-lookup"><span data-stu-id="03961-104">The Encrypted File System, or EFS, provides an additional level of security for files and directories.</span></span> <span data-ttu-id="03961-105">Proporciona protección criptográfica de archivos individuales en volúmenes del sistema de archivos NTFS mediante un sistema de clave pública.</span><span class="sxs-lookup"><span data-stu-id="03961-105">It provides cryptographic protection of individual files on NTFS file system volumes using a public-key system.</span></span>

<span data-ttu-id="03961-106">Normalmente, el control de acceso a los objetos de archivo y directorio proporcionados por el modelo de seguridad de Windows es suficiente para proteger el acceso no autorizado a la información confidencial.</span><span class="sxs-lookup"><span data-stu-id="03961-106">Typically, the access control to file and directory objects provided by the Windows security model is sufficient to protect unauthorized access to sensitive information.</span></span> <span data-ttu-id="03961-107">Sin embargo, si se pierde o se roba un equipo portátil que contiene datos confidenciales, la protección de la seguridad de los datos puede verse comprometida.</span><span class="sxs-lookup"><span data-stu-id="03961-107">However, if a laptop that contains sensitive data is lost or stolen, the security protection of that data may be compromised.</span></span> <span data-ttu-id="03961-108">El cifrado de los archivos aumenta la seguridad.</span><span class="sxs-lookup"><span data-stu-id="03961-108">Encrypting the files increases security.</span></span>

<span data-ttu-id="03961-109">Para determinar si un sistema de archivos admite el cifrado de archivos para archivos y directorios, llame a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examine la marca de bits de **\_ \_ cifrado de archivos FS** .</span><span class="sxs-lookup"><span data-stu-id="03961-109">To determine whether a file system supports file encryption for files and directories, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FS\_FILE\_ENCRYPTION** bit flag.</span></span> <span data-ttu-id="03961-110">Tenga en cuenta que los siguientes elementos no se pueden cifrar:</span><span class="sxs-lookup"><span data-stu-id="03961-110">Note that the following items cannot be encrypted:</span></span>

-   <span data-ttu-id="03961-111">Archivos comprimidos</span><span class="sxs-lookup"><span data-stu-id="03961-111">Compressed files</span></span>
-   <span data-ttu-id="03961-112">Archivos de sistema</span><span class="sxs-lookup"><span data-stu-id="03961-112">System files</span></span>
-   <span data-ttu-id="03961-113">Directorios del sistema</span><span class="sxs-lookup"><span data-stu-id="03961-113">System directories</span></span>
-   <span data-ttu-id="03961-114">Directorios raíz</span><span class="sxs-lookup"><span data-stu-id="03961-114">Root directories</span></span>
-   <span data-ttu-id="03961-115">Transacciones</span><span class="sxs-lookup"><span data-stu-id="03961-115">Transactions</span></span>

<span data-ttu-id="03961-116">Los archivos dispersos se pueden cifrar.</span><span class="sxs-lookup"><span data-stu-id="03961-116">Sparse files can be encrypted.</span></span>

<span data-ttu-id="03961-117">TxF no admite la mayoría de las operaciones en archivos del sistema de archivos cifrados (EFS).</span><span class="sxs-lookup"><span data-stu-id="03961-117">TxF does not support most operations on Encrypted File System (EFS) files.</span></span> <span data-ttu-id="03961-118">Las únicas operaciones TxF admiten operaciones de lectura, como [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).</span><span class="sxs-lookup"><span data-stu-id="03961-118">The only operations TxF supports are read operations, such as [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="03961-119">En esta sección</span><span class="sxs-lookup"><span data-stu-id="03961-119">In this section</span></span>



| <span data-ttu-id="03961-120">Tema</span><span class="sxs-lookup"><span data-stu-id="03961-120">Topic</span></span>                                                                                               | <span data-ttu-id="03961-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="03961-121">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03961-122">Administrar archivos y directorios cifrados</span><span class="sxs-lookup"><span data-stu-id="03961-122">Handling Encrypted Files and Directories</span></span>](handling-encrypted-files-and-directories.md)<br/> | <span data-ttu-id="03961-123">Un archivo marcado como cifrado está cifrado mediante el sistema de archivos NTFS mediante el controlador de cifrado actual.</span><span class="sxs-lookup"><span data-stu-id="03961-123">A file marked encrypted is encrypted by the NTFS file system by using the current encryption driver.</span></span><br/>                                                          |
| [<span data-ttu-id="03961-124">Archivos cifrados y claves de usuario</span><span class="sxs-lookup"><span data-stu-id="03961-124">Encrypted Files and User Keys</span></span>](encrypted-files-and-user-keys.md)<br/>                       | <span data-ttu-id="03961-125">Enumera las funciones que se van a usar para crear una nueva clave, agregar una clave a un archivo cifrado, consultar las claves de un archivo cifrado y quitar las claves de un archivo cifrado.</span><span class="sxs-lookup"><span data-stu-id="03961-125">Lists the functions to use to create a new key, add a key to an encrypted file, query the keys for an encrypted file, and remove keys from an encrypted file.</span></span><br/> |
| [<span data-ttu-id="03961-126">Copia de seguridad y restauración de archivos cifrados</span><span class="sxs-lookup"><span data-stu-id="03961-126">Backup and Restore of Encrypted Files</span></span>](backup-and-restore-of-encrypted-files.md)<br/>       | <span data-ttu-id="03961-127">Las funciones de cifrado sin procesar permiten realizar copias de seguridad de archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="03961-127">The raw encryption functions enable backup of encrypted files.</span></span><br/>                                                                                                |



 

<span data-ttu-id="03961-128">Para obtener más información sobre el cifrado, vea [Agregar usuarios a un archivo cifrado](adding-users-to-an-encrypted-file.md).</span><span class="sxs-lookup"><span data-stu-id="03961-128">For more information about encryption, see [Adding Users to an Encrypted File](adding-users-to-an-encrypted-file.md).</span></span>

<span data-ttu-id="03961-129">Para obtener más información sobre la criptografía, vea [Criptografía](/windows/desktop/SecCrypto/cryptography-portal).</span><span class="sxs-lookup"><span data-stu-id="03961-129">For more information about cryptography, see [Cryptography](/windows/desktop/SecCrypto/cryptography-portal).</span></span>

 

