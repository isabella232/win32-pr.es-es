---
description: El administrador de transacciones de kernel (KTM) es un servicio de administración de transacciones. Hace que las transacciones estén disponibles como objetos de kernel y proporciona servicios de administración de transacciones a los componentes del sistema como NTFS transaccional (TxF).
ms.assetid: 85a79698-a1ae-45a4-805e-25175034fa65
title: Acerca de KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1c477c7f9ae54b86fcee03435310416b38ea8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083358"
---
# <a name="about-ktm"></a><span data-ttu-id="e5128-104">Acerca de KTM</span><span class="sxs-lookup"><span data-stu-id="e5128-104">About KTM</span></span>

<span data-ttu-id="e5128-105">El administrador de transacciones de kernel (KTM) es un servicio de administración de transacciones.</span><span class="sxs-lookup"><span data-stu-id="e5128-105">Kernel Transaction Manager (KTM) is a transaction management service.</span></span> <span data-ttu-id="e5128-106">Hace que las transacciones estén disponibles como objetos de kernel y proporciona servicios de administración de transacciones a los componentes del sistema como [NTFS transaccional](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).</span><span class="sxs-lookup"><span data-stu-id="e5128-106">It makes transactions available as kernel objects and provides transaction management services to system components such as [Transactional NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).</span></span>

<span data-ttu-id="e5128-107">En los temas siguientes se describen los usos y las características de KTM:</span><span class="sxs-lookup"><span data-stu-id="e5128-107">The following topics describe the uses and features of KTM:</span></span>

-   [<span data-ttu-id="e5128-108">¿Qué es una transacción?</span><span class="sxs-lookup"><span data-stu-id="e5128-108">What is a Transaction?</span></span>](what-is-a-transaction.md)
-   [<span data-ttu-id="e5128-109">Trabajar con transacciones</span><span class="sxs-lookup"><span data-stu-id="e5128-109">Working With Transactions</span></span>](programming-model.md)
-   [<span data-ttu-id="e5128-110">Escribir un Administrador de recursos</span><span class="sxs-lookup"><span data-stu-id="e5128-110">Writing a Resource Manager</span></span>](writing-a-resource-manager.md)
-   [<span data-ttu-id="e5128-111">Interoperabilidad con otras características de Windows</span><span class="sxs-lookup"><span data-stu-id="e5128-111">Interoperability With Other Windows Features</span></span>](interoperability-with-other-windows-features.md)
-   [<span data-ttu-id="e5128-112">Derechos de acceso y seguridad de KTM</span><span class="sxs-lookup"><span data-stu-id="e5128-112">KTM Security and Access Rights</span></span>](ktm-security-and-access-rights.md)

<span data-ttu-id="e5128-113">KTM se basa en el [sistema de archivos de registro común](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) para su funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="e5128-113">KTM relies on the [Common Log File System](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) for its operation.</span></span> <span data-ttu-id="e5128-114">CLFS es un sistema de registro que es capaz de habilitar transacciones.</span><span class="sxs-lookup"><span data-stu-id="e5128-114">CLFS is a logging system that is capable of enabling transactions.</span></span>

 

 
