---
description: Funciones usadas en la administración de directorios.
ms.assetid: 5517b0e7-2264-4173-8e10-ff7626458bfa
title: Funciones de administración de directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00bc10d0f8d7caddc1ea821c397e16edf600d92c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278463"
---
# <a name="directory-management-functions"></a><span data-ttu-id="ed894-103">Funciones de administración de directorios</span><span class="sxs-lookup"><span data-stu-id="ed894-103">Directory Management Functions</span></span>

<span data-ttu-id="ed894-104">Las siguientes funciones se usan en la administración de directorios.</span><span class="sxs-lookup"><span data-stu-id="ed894-104">The following functions are used in directory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ed894-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ed894-105">In this section</span></span>



| <span data-ttu-id="ed894-106">Función</span><span class="sxs-lookup"><span data-stu-id="ed894-106">Function</span></span>                                                                      | <span data-ttu-id="ed894-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed894-107">Description</span></span>                                                                                                                                                               |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed894-108">**CreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="ed894-108">**CreateDirectory**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)<br/>                         | <span data-ttu-id="ed894-109">Crea un directorio nuevo.</span><span class="sxs-lookup"><span data-stu-id="ed894-109">Creates a new directory.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="ed894-110">**CreateDirectoryEx**</span><span class="sxs-lookup"><span data-stu-id="ed894-110">**CreateDirectoryEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)<br/>                     | <span data-ttu-id="ed894-111">Crea un nuevo directorio con los atributos de un directorio de plantilla especificado.</span><span class="sxs-lookup"><span data-stu-id="ed894-111">Creates a new directory with the attributes of a specified template directory.</span></span><br/>                                                                                 |
| [<span data-ttu-id="ed894-112">**CreateDirectoryTransacted**</span><span class="sxs-lookup"><span data-stu-id="ed894-112">**CreateDirectoryTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)<br/>     | <span data-ttu-id="ed894-113">Crea un nuevo directorio como una operación de transacción, con los atributos de un directorio de plantilla especificado.</span><span class="sxs-lookup"><span data-stu-id="ed894-113">Creates a new directory as a transacted operation, with the attributes of a specified template directory.</span></span><br/>                                                      |
| [<span data-ttu-id="ed894-114">**FindCloseChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="ed894-114">**FindCloseChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification)<br/> | <span data-ttu-id="ed894-115">Detiene la supervisión del controlador de notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="ed894-115">Stops change notification handle monitoring.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="ed894-116">**FindFirstChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="ed894-116">**FindFirstChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)<br/> | <span data-ttu-id="ed894-117">Crea un identificador de notificación de cambio y establece las condiciones iniciales de filtro de notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="ed894-117">Creates a change notification handle and sets up initial change notification filter conditions.</span></span><br/>                                                                |
| [<span data-ttu-id="ed894-118">**FindNextChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="ed894-118">**FindNextChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification)<br/>   | <span data-ttu-id="ed894-119">Solicita que el sistema operativo señale un identificador de notificación de cambio la próxima vez que detecte un cambio adecuado.</span><span class="sxs-lookup"><span data-stu-id="ed894-119">Requests that the operating system signal a change notification handle the next time it detects an appropriate change.</span></span><br/>                                         |
| [<span data-ttu-id="ed894-120">**GetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="ed894-120">**GetCurrentDirectory**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory)<br/>                 | <span data-ttu-id="ed894-121">Recupera el directorio actual del proceso actual.</span><span class="sxs-lookup"><span data-stu-id="ed894-121">Retrieves the current directory for the current process.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="ed894-122">**ReadDirectoryChangesExW**</span><span class="sxs-lookup"><span data-stu-id="ed894-122">**ReadDirectoryChangesExW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesexw)<br/>         | <span data-ttu-id="ed894-123">Recupera información que describe los cambios en el directorio especificado, que puede incluir información extendida si se especifica ese tipo de información.</span><span class="sxs-lookup"><span data-stu-id="ed894-123">Retrieves information that describes the changes within the specified directory, which can include extended information if that information type is specified.</span></span><br/> |
| [<span data-ttu-id="ed894-124">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="ed894-124">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>             | <span data-ttu-id="ed894-125">Recupera información que describe los cambios en el directorio especificado.</span><span class="sxs-lookup"><span data-stu-id="ed894-125">Retrieves information that describes the changes within the specified directory.</span></span><br/>                                                                               |
| [<span data-ttu-id="ed894-126">**RemoveDirectory**</span><span class="sxs-lookup"><span data-stu-id="ed894-126">**RemoveDirectory**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya)<br/>                         | <span data-ttu-id="ed894-127">Elimina un directorio vacío existente.</span><span class="sxs-lookup"><span data-stu-id="ed894-127">Deletes an existing empty directory.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="ed894-128">**RemoveDirectoryTransacted**</span><span class="sxs-lookup"><span data-stu-id="ed894-128">**RemoveDirectoryTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)<br/>     | <span data-ttu-id="ed894-129">Elimina un directorio vacío existente como una operación de transacción.</span><span class="sxs-lookup"><span data-stu-id="ed894-129">Deletes an existing empty directory as a transacted operation.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="ed894-130">**SetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="ed894-130">**SetCurrentDirectory**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)<br/>                 | <span data-ttu-id="ed894-131">Cambia el directorio actual del proceso actual.</span><span class="sxs-lookup"><span data-stu-id="ed894-131">Changes the current directory for the current process.</span></span><br/>                                                                                                         |



 

 

 




