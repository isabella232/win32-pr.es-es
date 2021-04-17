---
description: Implementar NTFS transaccional (TxF) y el registro transaccional (TxR). TxF permite operaciones del sistema de archivos transaccionales en NTFS. TxR permite operaciones del registro transaccionales. Coordine el sistema de archivos y las operaciones del registro con una transacción.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Administrador de transacciones de kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281050461163d5fd0cde64af79e70569d613888e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652999"
---
# <a name="kernel-transaction-manager"></a><span data-ttu-id="b4347-106">Administrador de transacciones de kernel</span><span class="sxs-lookup"><span data-stu-id="b4347-106">Kernel Transaction Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="b4347-107">Propósito</span><span class="sxs-lookup"><span data-stu-id="b4347-107">Purpose</span></span>

<span data-ttu-id="b4347-108">El administrador de transacciones de kernel (KTM) permite el desarrollo de aplicaciones que utilizan transacciones.</span><span class="sxs-lookup"><span data-stu-id="b4347-108">The Kernel Transaction Manager (KTM) enables the development of applications that use transactions.</span></span> <span data-ttu-id="b4347-109">El propio motor de transacciones se encuentra dentro del kernel, pero las transacciones se pueden desarrollar para transacciones de modo de usuario o de kernel, y dentro de un solo host o entre hosts distribuidos.</span><span class="sxs-lookup"><span data-stu-id="b4347-109">The transaction engine itself is within the kernel, but transactions can be developed for kernel- or user-mode transactions, and within a single host or among distributed hosts.</span></span>

<span data-ttu-id="b4347-110">El KTM se usa para implementar NTFS transaccional (TxF) y el registro transaccional (TxR).</span><span class="sxs-lookup"><span data-stu-id="b4347-110">The KTM is used to implement Transactional NTFS (TxF) and Transactional Registry (TxR).</span></span> <span data-ttu-id="b4347-111">TxF permite operaciones del sistema de archivos transaccionales dentro del sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="b4347-111">TxF allows transacted file system operations within the NTFS file system.</span></span> <span data-ttu-id="b4347-112">TxR permite operaciones del registro transaccionales.</span><span class="sxs-lookup"><span data-stu-id="b4347-112">TxR allows transacted registry operations.</span></span> <span data-ttu-id="b4347-113">KTM permite a las aplicaciones cliente coordinar las operaciones del registro y del sistema de archivos con una transacción.</span><span class="sxs-lookup"><span data-stu-id="b4347-113">KTM enables client applications to coordinate file system and registry operations with a transaction.</span></span>

<span data-ttu-id="b4347-114">Para desarrollar una aplicación que coordine las transacciones con recursos distintos de TxF o TxR, primero debe desarrollar un servicio compatible con transacciones de Win32, también denominado administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4347-114">To develop an application that coordinates transactions with resources other than TxF or TxR, you must first develop a Win32 transaction-aware service, also called a resource manager.</span></span>

<span data-ttu-id="b4347-115">Las aplicaciones administradas y COM+ deben usar sus administradores de transacciones nativos.</span><span class="sxs-lookup"><span data-stu-id="b4347-115">Managed and COM+ applications should use their native transaction managers.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="b4347-116">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="b4347-116">Where applicable</span></span>

<span data-ttu-id="b4347-117">KTM se puede usar con aplicaciones y administradores de recursos hospedados en Windows Vista o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b4347-117">KTM can be used with applications and resource managers hosted on Windows Vista or Windows Server 2008.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b4347-118">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="b4347-118">Developer audience</span></span>

<span data-ttu-id="b4347-119">La API de KTM está diseñada para que la usen los programadores de C y C++.</span><span class="sxs-lookup"><span data-stu-id="b4347-119">The KTM API is designed for use by C and C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b4347-120">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="b4347-120">Run-time requirements</span></span>

<span data-ttu-id="b4347-121">KTM se admite a partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b4347-121">KTM is supported starting with Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b4347-122">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b4347-122">In this section</span></span>



| <span data-ttu-id="b4347-123">Tema</span><span class="sxs-lookup"><span data-stu-id="b4347-123">Topic</span></span>                                     | <span data-ttu-id="b4347-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4347-124">Description</span></span>                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4347-125">Acerca de</span><span class="sxs-lookup"><span data-stu-id="b4347-125">About</span></span>](about-ktm.md)<br/>         | <span data-ttu-id="b4347-126">Información general sobre las transacciones y las funciones proporcionadas por KTM.</span><span class="sxs-lookup"><span data-stu-id="b4347-126">General information about transactions and the capabilities provided by KTM.</span></span><br/>                           |
| [<span data-ttu-id="b4347-127">Referencia</span><span class="sxs-lookup"><span data-stu-id="b4347-127">Reference</span></span>](ktm-reference.md)<br/> | <span data-ttu-id="b4347-128">Documentación para las funciones, estructuras de datos, enumeraciones y otros elementos de programación de KTM.</span><span class="sxs-lookup"><span data-stu-id="b4347-128">Documentation for the functions, data structures, enumerations, and other programming elements of KTM.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b4347-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4347-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4347-130">Sistema de archivos de registro común</span><span class="sxs-lookup"><span data-stu-id="b4347-130">Common Log File System</span></span>](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[<span data-ttu-id="b4347-131">NTFS transaccional (TxF)</span><span class="sxs-lookup"><span data-stu-id="b4347-131">Transactional NTFS (TxF)</span></span>](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

<span data-ttu-id="b4347-132">[Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/ms684146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b4347-132">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span></span>
</dt> </dl>

 

