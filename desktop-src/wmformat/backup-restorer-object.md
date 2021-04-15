---
title: Objeto de restaurador de copia de seguridad
description: Objeto de restaurador de copia de seguridad
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- SDK de Windows Media Format, objetos de restauración de copia de seguridad
- Advanced Systems Format (ASF), objetos de restauración de copia de seguridad
- ASF (formato de sistemas avanzados), objetos de restauración de copia de seguridad
- objetos, objetos de restauración de copia de seguridad
- restaurador de copias de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08e8bec9bb7bbc2a45fbf632e69d230a2536633
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105676343"
---
# <a name="backup-restorer-object"></a><span data-ttu-id="4d749-108">Objeto de restaurador de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="4d749-108">Backup Restorer Object</span></span>

<span data-ttu-id="4d749-109">El restaurador de copias de seguridad proporciona interfaces para administrar las licencias de copia de seguridad, normalmente en medios extraíbles, y, a continuación, restaurar esas licencias en un nuevo equipo.</span><span class="sxs-lookup"><span data-stu-id="4d749-109">The backup restorer provides interfaces to handle backing up licenses, typically onto removable media, and then restoring those licenses onto a new computer.</span></span>

<span data-ttu-id="4d749-110">La función [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) crea el objeto de almacén de copias de seguridad, que establece un puntero a una interfaz [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) .</span><span class="sxs-lookup"><span data-stu-id="4d749-110">The backup restorer object is created by the [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) function, which sets a pointer to an [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) interface.</span></span> <span data-ttu-id="4d749-111">Las demás interfaces del objeto de almacén de copia de seguridad se pueden obtener llamando al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="4d749-111">The other interfaces of the backup restorer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="4d749-112">El objeto de almacén de copia de seguridad admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="4d749-112">The following interfaces are supported by the backup restorer object.</span></span>



| <span data-ttu-id="4d749-113">Interfaz</span><span class="sxs-lookup"><span data-stu-id="4d749-113">Interface</span></span>                                              | <span data-ttu-id="4d749-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d749-114">Description</span></span>                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d749-115">**IWMBackupRestoreProps**</span><span class="sxs-lookup"><span data-stu-id="4d749-115">**IWMBackupRestoreProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | <span data-ttu-id="4d749-116">Establece y recupera las propiedades requeridas por las interfaces [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) y [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) .</span><span class="sxs-lookup"><span data-stu-id="4d749-116">Sets and retrieves properties required by the [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) and [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) interfaces.</span></span> |
| [<span data-ttu-id="4d749-117">**IWMLicenseBackup**</span><span class="sxs-lookup"><span data-stu-id="4d749-117">**IWMLicenseBackup**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | <span data-ttu-id="4d749-118">Realiza una copia de seguridad de las licencias, normalmente para que se puedan restaurar en otro equipo.</span><span class="sxs-lookup"><span data-stu-id="4d749-118">Backs up licenses, typically so that they can be restored onto another computer.</span></span>                                                                          |
| [<span data-ttu-id="4d749-119">**IWMLicenseRestore**</span><span class="sxs-lookup"><span data-stu-id="4d749-119">**IWMLicenseRestore**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | <span data-ttu-id="4d749-120">Restaura las licencias.</span><span class="sxs-lookup"><span data-stu-id="4d749-120">Restores licenses.</span></span>                                                                                                                                        |



 

<span data-ttu-id="4d749-121">La aplicación debe implementar la siguiente interfaz de devolución de llamada para poder usar el objeto de almacén de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4d749-121">The following callback interface must be implemented by the application in order to use the backup restorer object.</span></span>



| <span data-ttu-id="4d749-122">Interfaz</span><span class="sxs-lookup"><span data-stu-id="4d749-122">Interface</span></span>                                      | <span data-ttu-id="4d749-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d749-123">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="4d749-124">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="4d749-124">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="4d749-125">Recibe mensajes de estado de los procesos que se ejecutan en un subproceso independiente.</span><span class="sxs-lookup"><span data-stu-id="4d749-125">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4d749-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d749-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d749-127">**Copia de seguridad y restauración de licencias**</span><span class="sxs-lookup"><span data-stu-id="4d749-127">**Backing Up and Restoring Licenses**</span></span>](backing-up-and-restoring-licenses.md)
</dt> <dt>

[<span data-ttu-id="4d749-128">**Objects**</span><span class="sxs-lookup"><span data-stu-id="4d749-128">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




