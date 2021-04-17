---
description: El Coordinador de transacciones distribuidas (DTC) permite transacciones distribuidas o transacciones que están bajo el control de varios administradores de recursos en uno o varios sistemas. KTM y DTC funcionan conjuntamente para lograrlo.
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: Interoperabilidad con otras características de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa3aeac3d920b408a9a18c32eab83cf747525e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687831"
---
# <a name="interoperability-with-other-windows-features"></a><span data-ttu-id="2ee7a-104">Interoperabilidad con otras características de Windows</span><span class="sxs-lookup"><span data-stu-id="2ee7a-104">Interoperability With Other Windows Features</span></span>

<span data-ttu-id="2ee7a-105">El [Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) permite *transacciones distribuidas* o transacciones que están bajo el control de varios administradores de recursos en uno o varios sistemas.</span><span class="sxs-lookup"><span data-stu-id="2ee7a-105">The [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) enables *distributed transactions*, or transactions that are under the control of multiple resource managers on one or more systems.</span></span> <span data-ttu-id="2ee7a-106">KTM y DTC funcionan conjuntamente para lograrlo.</span><span class="sxs-lookup"><span data-stu-id="2ee7a-106">KTM and DTC work closely together to accomplish this.</span></span>

<span data-ttu-id="2ee7a-107">COM+ expone un modelo declarativo para la programación transaccional.</span><span class="sxs-lookup"><span data-stu-id="2ee7a-107">COM+ exposes a declarative model for transactional programming.</span></span> <span data-ttu-id="2ee7a-108">En otras palabras, el programador declara la medida en la que un objeto puede aprovechar las transacciones y el tiempo de ejecución de COM+ administra las transacciones en nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="2ee7a-108">In other words, the programmer declares the extent to which an object can take advantage of transactions, and the COM+ runtime manages the transactions on the object's behalf.</span></span> <span data-ttu-id="2ee7a-109">Por ejemplo, un objeto se puede declarar para que participe en una transacción solo si ya existe una, para requerir una transacción (se crea una si aún no existe), para requerir una nueva transacción (se crea una con independencia de si ya existe) o no es transaccional.</span><span class="sxs-lookup"><span data-stu-id="2ee7a-109">For example, an object can be declared to participate in a transaction only if one already exists, to require a transaction (one is created if it does not already exist), to require a new transaction (one is created regardless of whether one already exists), or is not transactional.</span></span> <span data-ttu-id="2ee7a-110">Estas transacciones administradas mediante declaración se utilizan automáticamente en las conexiones de base de datos creadas por objetos COM+ que se ejecutan en el contexto de una transacción.</span><span class="sxs-lookup"><span data-stu-id="2ee7a-110">These declaratively-managed transactions are automatically used on database connections created by COM+ objects that are executing in the context of a transaction.</span></span>

 

 
