---
description: Si está escribiendo un servicio o componente y necesita usar servicios transaccionales o si necesita supervisar el estado de una transacción de kernel, debe crear un administrador de recursos (RM).
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Escribir un Administrador de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c47f9a0704f6edaea02d752fe39f01fce61c0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677690"
---
# <a name="writing-a-resource-manager"></a><span data-ttu-id="2d536-103">Escribir un Administrador de recursos</span><span class="sxs-lookup"><span data-stu-id="2d536-103">Writing a Resource Manager</span></span>

<span data-ttu-id="2d536-104">Si está escribiendo un servicio o componente y necesita usar servicios transaccionales o si necesita supervisar el estado de una transacción de kernel, debe crear un administrador de recursos (RM).</span><span class="sxs-lookup"><span data-stu-id="2d536-104">If you are writing a service or component and need to use transactional services or if you need to monitor the state of a kernel transaction, you need to create a resource manager (RM).</span></span>

<span data-ttu-id="2d536-105">Para escribir un administrador de recursos, debe crear varios objetos de kernel.</span><span class="sxs-lookup"><span data-stu-id="2d536-105">To write a resource manager, you must create multiple kernel objects.</span></span> <span data-ttu-id="2d536-106">Los objetos que usa un RM son:</span><span class="sxs-lookup"><span data-stu-id="2d536-106">The objects that an RM uses are:</span></span>

-   <span data-ttu-id="2d536-107">Objetos del administrador de transacciones (TM)</span><span class="sxs-lookup"><span data-stu-id="2d536-107">Transaction Manager (TM) objects</span></span>
-   <span data-ttu-id="2d536-108">Objetos Administrador de recursos</span><span class="sxs-lookup"><span data-stu-id="2d536-108">Resource Manager objects</span></span>
-   <span data-ttu-id="2d536-109">Objetos de inscripción</span><span class="sxs-lookup"><span data-stu-id="2d536-109">Enlistment objects</span></span>

<span data-ttu-id="2d536-110">En primer lugar, cree un objeto TM.</span><span class="sxs-lookup"><span data-stu-id="2d536-110">First, create a TM object.</span></span> <span data-ttu-id="2d536-111">Hay dos tipos de TM:</span><span class="sxs-lookup"><span data-stu-id="2d536-111">There are two types of TMs:</span></span>

-   <span data-ttu-id="2d536-112">Volatile: estas TM no tienen un registro y no pueden recuperar su estado</span><span class="sxs-lookup"><span data-stu-id="2d536-112">Volatile – these TMs do not have a log and cannot recover their state</span></span>
-   <span data-ttu-id="2d536-113">Durable: estas TM tienen un registro</span><span class="sxs-lookup"><span data-stu-id="2d536-113">Durable – these TMs have a log</span></span>

<span data-ttu-id="2d536-114">Para crear un TM duradero, debe crear un registro de CLFS y llamar a [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) o hacer que KTM lo cree.</span><span class="sxs-lookup"><span data-stu-id="2d536-114">To create a durable TM, you must either create a CLFS log and call [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) or have KTM create it for you.</span></span> <span data-ttu-id="2d536-115">Después de crear un TM duradero, primero debe recuperar el TM llamando a [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager).</span><span class="sxs-lookup"><span data-stu-id="2d536-115">After a durable TM is created, you must first recover the TM by calling [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager).</span></span> <span data-ttu-id="2d536-116">Una vez recuperado el TM, está disponible para su uso.</span><span class="sxs-lookup"><span data-stu-id="2d536-116">After the TM is recovered, it is available for use.</span></span>

<span data-ttu-id="2d536-117">Si ha recuperado un TM existente, todos los RMs asociados a este TM comenzarán a recibir los mensajes de recuperación.</span><span class="sxs-lookup"><span data-stu-id="2d536-117">If you recovered an existing TM, all RMs associated with this TM will start receiving recovery messages.</span></span> <span data-ttu-id="2d536-118">Para obtener más información, vea [procesamiento de recuperación](recovery-processing.md).</span><span class="sxs-lookup"><span data-stu-id="2d536-118">For more information, see [Recovery Processing](recovery-processing.md).</span></span>

<span data-ttu-id="2d536-119">A continuación, cree un administrador de recursos mediante una llamada a [**CreateResourceManager (**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) con el identificador de TM.</span><span class="sxs-lookup"><span data-stu-id="2d536-119">Next, you create a resource manager by calling [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) with the TM handle.</span></span> <span data-ttu-id="2d536-120">RM puede ser volátil o durable.</span><span class="sxs-lookup"><span data-stu-id="2d536-120">The RM can be volatile or durable.</span></span> <span data-ttu-id="2d536-121">Solo se puede usar TM durable con RMs duradero.</span><span class="sxs-lookup"><span data-stu-id="2d536-121">Only durable TMs can be used with durable RMs.</span></span>

<span data-ttu-id="2d536-122">Al trabajar de forma transaccional, se da de alta en la transacción llamando a [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)y especificando qué notificaciones se van a recibir.</span><span class="sxs-lookup"><span data-stu-id="2d536-122">When working transactionally, you enlist in the transaction by calling [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)and specifying which notifications to receive.</span></span>

<span data-ttu-id="2d536-123">**Nota:**  Puede empezar a recibir notificaciones antes de que se complete la llamada a [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) .</span><span class="sxs-lookup"><span data-stu-id="2d536-123">**Note**  You can start receiving notifications before the call to [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) is completed.</span></span>

<span data-ttu-id="2d536-124">Cuando reciba una notificación, llame a la función "Complete \* " adecuada cuando se complete cualquier trabajo asociado al procesamiento de la notificación.</span><span class="sxs-lookup"><span data-stu-id="2d536-124">When you receive a notification, call the appropriate "Complete\*" function when any work associated with processing the notification is completed.</span></span> <span data-ttu-id="2d536-125">Las funciones completas son:</span><span class="sxs-lookup"><span data-stu-id="2d536-125">The complete functions are:</span></span>

-   [<span data-ttu-id="2d536-126">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="2d536-126">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [<span data-ttu-id="2d536-127">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="2d536-127">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [<span data-ttu-id="2d536-128">**PreprepareComplete**</span><span class="sxs-lookup"><span data-stu-id="2d536-128">**PreprepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

<span data-ttu-id="2d536-129">Si, en algún momento, un administrador de recursos no puede completar el trabajo de la transacción, o si continúa, la aplicación no puede deshacer el trabajo realizado dentro de la transacción, debe revertir la transacción llamando a [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).</span><span class="sxs-lookup"><span data-stu-id="2d536-129">If at any time a resource manager is unable to complete the work of the transaction, or if continuing would render your application unable to undo the work done within the transaction, you must roll back the transaction by calling [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).</span></span>

 

 



