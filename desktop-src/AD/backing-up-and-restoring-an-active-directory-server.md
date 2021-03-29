---
title: Copia de seguridad y restauración de un servidor Active Directory
description: Active Directory Domain Services proporcionan funciones para realizar copias de seguridad y restaurar datos en la base de datos de directorio.
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, uso, copia de seguridad y restauración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92d57c2ddf572db8806aca71282e6b4fd8799ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789639"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a><span data-ttu-id="c6f51-104">Copia de seguridad y restauración de un servidor Active Directory</span><span class="sxs-lookup"><span data-stu-id="c6f51-104">Backing Up and Restoring an Active Directory Server</span></span>

<span data-ttu-id="c6f51-105">Active Directory Domain Services proporcionan funciones para realizar copias de seguridad y restaurar datos en la base de datos de directorio.</span><span class="sxs-lookup"><span data-stu-id="c6f51-105">Active Directory Domain Services provide functions for backing up and restoring data in the directory database.</span></span> <span data-ttu-id="c6f51-106">En esta sección se describe cómo [realizar una copia de seguridad](backing-up-an-active-directory-server.md) y [restaurar](restoring-an-active-directory-server.md) un servidor de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6f51-106">This section describes how to [back up](backing-up-an-active-directory-server.md) and [restore](restoring-an-active-directory-server.md) an Active Directory server.</span></span> <span data-ttu-id="c6f51-107">Para obtener más información acerca de la copia de seguridad de un servidor de Active Directory con las utilidades proporcionadas en los sistemas operativos Windows 2000 y Windows Server 2003, consulte el kit de recursos aplicable, disponible en el sitio web de Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="c6f51-107">For more information about backing up an Active Directory server using the utilities provided in Windows 2000 and Windows Server 2003 operating systems, see the applicable Resource Kit, available on the Microsoft TechNet website.</span></span>

<span data-ttu-id="c6f51-108">La copia de seguridad de un servidor de Active Directory debe realizarse en línea y debe realizarse cuando se instale el Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c6f51-108">Backup of an Active Directory server must be performed online and must be performed when the Active Directory Domain Services are installed.</span></span> <span data-ttu-id="c6f51-109">Active Directory Domain Services se basan en una base de datos Especial y exportan un conjunto de funciones de copia de seguridad que proporcionan la interfaz de copia de seguridad mediante programación.</span><span class="sxs-lookup"><span data-stu-id="c6f51-109">Active Directory Domain Services are built on a special database and export a set of backup functions that provide the programmatic backup interface.</span></span> <span data-ttu-id="c6f51-110">La copia de seguridad no admite copias de seguridad incrementales.</span><span class="sxs-lookup"><span data-stu-id="c6f51-110">The backup does not support incremental backups.</span></span> <span data-ttu-id="c6f51-111">Una aplicación de copia de seguridad se enlaza a un archivo DLL del lado cliente local con puntos de entrada definidos en Ntdsbcli. h.</span><span class="sxs-lookup"><span data-stu-id="c6f51-111">A backup application binds to a local client-side DLL with entry points defined in Ntdsbcli.h.</span></span>

<span data-ttu-id="c6f51-112">La restauración de un servidor de Active Directory siempre se realiza sin conexión.</span><span class="sxs-lookup"><span data-stu-id="c6f51-112">Restoration of an Active Directory server is always performed offline.</span></span>

<span data-ttu-id="c6f51-113">Aunque en los temas de esta sección solo se describe cómo realizar copias de seguridad y restaurar un servidor de Active Directory, tenga en cuenta que los sistemas operativos Windows 2000 y Windows Server 2003 tienen varios componentes de "estado del sistema" que se deben copiar y restaurar juntos.</span><span class="sxs-lookup"><span data-stu-id="c6f51-113">Although the topics in this section describe only how to back up and restore an Active Directory server, be aware that Windows 2000 and the Windows Server 2003 operating systems have several "system state" components that must be backed up and restored together.</span></span> <span data-ttu-id="c6f51-114">Estos componentes de estado del sistema constan de:</span><span class="sxs-lookup"><span data-stu-id="c6f51-114">These system state components consist of:</span></span>

-   <span data-ttu-id="c6f51-115">Archivos de arranque como NTLDR, Ntdetect, todos los archivos protegidos por SFP y configuración del contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="c6f51-115">Boot files such as ntldr, ntdetect, all files protected by SFP, and performance counter configuration</span></span>
-   <span data-ttu-id="c6f51-116">El controlador de Dominio de Active Directory</span><span class="sxs-lookup"><span data-stu-id="c6f51-116">The Active Directory Domain Controller</span></span>
-   <span data-ttu-id="c6f51-117">SysVol (solo controlador de dominio)</span><span class="sxs-lookup"><span data-stu-id="c6f51-117">SysVol (domain controller only)</span></span>
-   <span data-ttu-id="c6f51-118">Servidor de certificados (solo CA)</span><span class="sxs-lookup"><span data-stu-id="c6f51-118">Certificate Server (CA only)</span></span>
-   <span data-ttu-id="c6f51-119">Base de datos de clúster (solo nodo de clúster)</span><span class="sxs-lookup"><span data-stu-id="c6f51-119">Cluster database (cluster node only)</span></span>
-   <span data-ttu-id="c6f51-120">Registro</span><span class="sxs-lookup"><span data-stu-id="c6f51-120">Registry</span></span>
-   <span data-ttu-id="c6f51-121">Base de datos de registro de clase COM+</span><span class="sxs-lookup"><span data-stu-id="c6f51-121">COM+ class registration database</span></span>

<span data-ttu-id="c6f51-122">Se puede realizar una copia de seguridad del estado del sistema en cualquier orden, pero la restauración del estado del sistema debe realizarse en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="c6f51-122">The system state can be backed up in any order, but restoration of the system state must occur in the following order:</span></span>

1.  <span data-ttu-id="c6f51-123">Restaure los archivos de arranque.</span><span class="sxs-lookup"><span data-stu-id="c6f51-123">Restore the boot files.</span></span>
2.  <span data-ttu-id="c6f51-124">Restaure SysVol, servidor de certificados, base de datos de clúster y base de datos de registro de clase COM+, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="c6f51-124">Restore SysVol, Certificate Server, Cluster database and COM+ class registration database, as applicable.</span></span>
3.  <span data-ttu-id="c6f51-125">Restaure el servidor de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6f51-125">Restore the Active Directory server.</span></span>
4.  <span data-ttu-id="c6f51-126">Restaure el registro.</span><span class="sxs-lookup"><span data-stu-id="c6f51-126">Restore the registry.</span></span>

<span data-ttu-id="c6f51-127">Para obtener más información sobre la copia de seguridad y restauración de servicios de Certificate Server, vea [usar las funciones de copia de seguridad y restauración de servicios de certificados](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).</span><span class="sxs-lookup"><span data-stu-id="c6f51-127">For more information about backing up and restoring Certificate Services, see [Using the Certificate Services Backup and Restore Functions](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).</span></span>

<span data-ttu-id="c6f51-128">Para obtener más información acerca de la copia de seguridad y la restauración de Active Directory Domain Services, consulte:</span><span class="sxs-lookup"><span data-stu-id="c6f51-128">For more information about backing up and restoring Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="c6f51-129">Consideraciones sobre la copia de seguridad de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c6f51-129">Considerations for Active Directory Domain Services Backup</span></span>](considerations-for-active-directory-domain-services-backup.md)
-   [<span data-ttu-id="c6f51-130">Copia de seguridad de un servidor Active Directory</span><span class="sxs-lookup"><span data-stu-id="c6f51-130">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
-   [<span data-ttu-id="c6f51-131">Restauración de un servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="c6f51-131">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
-   [<span data-ttu-id="c6f51-132">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="c6f51-132">Directory Backup Functions</span></span>](directory-backup-functions.md)

 

 