---
description: En los ejemplos siguientes se usan las funciones de administración de archivos.
ms.assetid: 0879898b-b661-48b3-af94-9ba24811503f
title: Uso de la administración de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88838ee99dde16c5c2288c00e2e2f3b35747dae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083234"
---
# <a name="using-file-management"></a><span data-ttu-id="c13e8-103">Uso de la administración de archivos</span><span class="sxs-lookup"><span data-stu-id="c13e8-103">Using File Management</span></span>

<span data-ttu-id="c13e8-104">En los ejemplos siguientes se usan las funciones de administración de archivos.</span><span class="sxs-lookup"><span data-stu-id="c13e8-104">The following samples use the file management functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c13e8-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c13e8-105">In this section</span></span>



| <span data-ttu-id="c13e8-106">Tema</span><span class="sxs-lookup"><span data-stu-id="c13e8-106">Topic</span></span>                                                                                                   | <span data-ttu-id="c13e8-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c13e8-107">Description</span></span>                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c13e8-108">Agregar usuarios a un archivo cifrado</span><span class="sxs-lookup"><span data-stu-id="c13e8-108">Adding Users to an Encrypted File</span></span>](adding-users-to-an-encrypted-file.md)<br/>                   | <span data-ttu-id="c13e8-109">Código de ejemplo que muestra cómo agregar un nuevo usuario a un archivo cifrado existente mediante la función [**AddUsersToEncryptedFile**](/windows/desktop/api/Winefs/nf-winefs-adduserstoencryptedfile) .</span><span class="sxs-lookup"><span data-stu-id="c13e8-109">Example code that shows how to add a new user to an existing encrypted file by using the [**AddUsersToEncryptedFile**](/windows/desktop/api/Winefs/nf-winefs-adduserstoencryptedfile) function.</span></span><br/>                         |
| [<span data-ttu-id="c13e8-110">Anexar un archivo a otro archivo</span><span class="sxs-lookup"><span data-stu-id="c13e8-110">Appending One File to Another File</span></span>](appending-one-file-to-another-file.md)<br/>                 | <span data-ttu-id="c13e8-111">Código de ejemplo que muestra cómo una aplicación puede anexar un archivo al final de otro archivo, incluido cómo abrir y cerrar archivos, leer y escribir en archivos, y bloquear y desbloquear archivos.</span><span class="sxs-lookup"><span data-stu-id="c13e8-111">Example code that shows how an application can append one file to the end of another file, including how to open and close files, read and write to files, and lock and unlock files.</span></span><br/> |
| [<span data-ttu-id="c13e8-112">Crear y usar un archivo temporal</span><span class="sxs-lookup"><span data-stu-id="c13e8-112">Creating and Using a Temporary File</span></span>](creating-and-using-a-temporary-file.md)<br/>               | <span data-ttu-id="c13e8-113">Código de ejemplo que muestra cómo crear un archivo temporal para la manipulación de datos mediante las funciones GetTempFileName y GetTempPath.</span><span class="sxs-lookup"><span data-stu-id="c13e8-113">Example code that shows how to create a temporary file for data manipulation purposes by using the GetTempFileName and GetTempPath functions.</span></span><br/>                                         |
| [<span data-ttu-id="c13e8-114">Bloquear y desbloquear intervalos de bytes en archivos</span><span class="sxs-lookup"><span data-stu-id="c13e8-114">Locking and Unlocking Byte Ranges in Files</span></span>](locking-and-unlocking-byte-ranges-in-files.md)<br/> | <span data-ttu-id="c13e8-115">Código de ejemplo que muestra el bloqueo del intervalo de bytes y el desbloqueo mediante las funciones LockFileEx y UnlockFileEx.</span><span class="sxs-lookup"><span data-stu-id="c13e8-115">Example code that shows byte range locking and unlocking by using the LockFileEx and UnlockFileEx functions.</span></span><br/>                                                                          |
| [<span data-ttu-id="c13e8-116">Apertura de un archivo para lectura o escritura</span><span class="sxs-lookup"><span data-stu-id="c13e8-116">Opening a File for Reading or Writing</span></span>](opening-a-file-for-reading-or-writing.md)<br/>           | <span data-ttu-id="c13e8-117">Código de ejemplo que muestra cómo utilizar la función CreateFile para crear un nuevo archivo o abrir un archivo existente.</span><span class="sxs-lookup"><span data-stu-id="c13e8-117">Example code that shows how to use the CreateFile function to create a new file or open an existing file.</span></span><br/>                                                                             |
| [<span data-ttu-id="c13e8-118">Recuperar y cambiar atributos de archivo</span><span class="sxs-lookup"><span data-stu-id="c13e8-118">Retrieving and Changing File Attributes</span></span>](retrieving-and-changing-file-attributes.md)<br/>       | <span data-ttu-id="c13e8-119">Código de ejemplo que muestra cómo usar la función GetFileAttributesEx para recuperar atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="c13e8-119">Example code that shows how to use the GetFileAttributesEx function to retrieve file attributes.</span></span><br/>                                                                                      |
| [<span data-ttu-id="c13e8-120">Probar el final de un archivo</span><span class="sxs-lookup"><span data-stu-id="c13e8-120">Testing for the End of a File</span></span>](testing-for-the-end-of-a-file.md)<br/>                           | <span data-ttu-id="c13e8-121">Código de ejemplo que muestra cómo probar el final del archivo durante una operación de lectura sincrónica y durante una operación de lectura asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c13e8-121">Example code that shows how to test for the end of file during a synchronous read operation and during an asynchronous read operation.</span></span><br/>                                                |
| [<span data-ttu-id="c13e8-122">Usar secuencias</span><span class="sxs-lookup"><span data-stu-id="c13e8-122">Using Streams</span></span>](using-streams.md)<br/>                                                           | <span data-ttu-id="c13e8-123">Código de ejemplo que muestra cómo usar secuencias básicas del sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="c13e8-123">Example code that shows how to use basic NTFS file system streams.</span></span><br/>                                                                                                                    |



 

 

 




