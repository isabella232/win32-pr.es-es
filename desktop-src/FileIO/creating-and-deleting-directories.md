---
description: Una aplicación puede crear y eliminar directorios mediante programación.
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: Crear y eliminar directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140547594271e13bc78bfa78336f167f228879a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155300"
---
# <a name="creating-and-deleting-directories"></a><span data-ttu-id="1d187-103">Crear y eliminar directorios</span><span class="sxs-lookup"><span data-stu-id="1d187-103">Creating and Deleting Directories</span></span>

<span data-ttu-id="1d187-104">Una aplicación puede crear y eliminar directorios mediante programación.</span><span class="sxs-lookup"><span data-stu-id="1d187-104">An application can programmatically create and delete directories.</span></span>

<span data-ttu-id="1d187-105">Para crear un nuevo directorio, use la función [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)o [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="1d187-105">To create a new directory, use the [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa), or [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) function.</span></span> <span data-ttu-id="1d187-106">A un directorio se le asigna el nombre especificado cuando se crea.</span><span class="sxs-lookup"><span data-stu-id="1d187-106">A directory is given the name specified when it is created.</span></span> <span data-ttu-id="1d187-107">Las convenciones para asignar nombres a un directorio siguen las convenciones de nomenclatura de un archivo.</span><span class="sxs-lookup"><span data-stu-id="1d187-107">The conventions for naming a directory follow the conventions for naming a file.</span></span> <span data-ttu-id="1d187-108">Para obtener una descripción de estas convenciones, vea [asignar un nombre a un archivo](naming-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="1d187-108">For a description of these conventions, see [Naming a File](naming-a-file.md).</span></span>

<span data-ttu-id="1d187-109">Para eliminar un directorio existente, use la función [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) o [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="1d187-109">To delete an existing directory, use the [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) or [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) function.</span></span> <span data-ttu-id="1d187-110">Antes de quitar un directorio, debe asegurarse de que el directorio está vacío y de que tiene el privilegio de eliminación de acceso para el directorio.</span><span class="sxs-lookup"><span data-stu-id="1d187-110">Before removing a directory, you must ensure that the directory is empty and that you have the delete access privilege for the directory.</span></span> <span data-ttu-id="1d187-111">Para hacer esto último, llame a la función [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="1d187-111">To do the latter, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) function.</span></span>

 

 
