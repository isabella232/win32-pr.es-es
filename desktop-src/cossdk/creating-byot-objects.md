---
description: Crear objetos de transacciones
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Crear objetos de transacciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544c5085061be5d1100706930a3e1617ec24890
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705306"
---
# <a name="creating-byot-objects"></a><span data-ttu-id="acc3a-103">Crear objetos de transacciones</span><span class="sxs-lookup"><span data-stu-id="acc3a-103">Creating BYOT Objects</span></span>

<span data-ttu-id="acc3a-104">Un nuevo objeto de transacciones crea objetos con transacciones manuales.</span><span class="sxs-lookup"><span data-stu-id="acc3a-104">A new BYOT object creates objects with manual transactions.</span></span> <span data-ttu-id="acc3a-105">Las dos interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) y [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), tienen un único método, **CreateInstance**, que toma un puntero de interfaz de **ITransaction** y una dirección URL de sugerencia, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="acc3a-105">The two interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) and [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), have a single method, **CreateInstance**, which take an **ITransaction** interface pointer and TIP URL, respectively.</span></span> <span data-ttu-id="acc3a-106">[**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) devuelve un puntero de interfaz al objeto recién creado, que se da de alta en la transacción especificada.</span><span class="sxs-lookup"><span data-stu-id="acc3a-106">[**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) returns an interface pointer to the newly created object, which is enlisted within the specified transaction.</span></span>

<span data-ttu-id="acc3a-107">Cuando se libera un objeto con una transacción manual, COM+ no intenta confirmar la transacción.</span><span class="sxs-lookup"><span data-stu-id="acc3a-107">When an object with a manual transaction is released, COM+ does not attempt to commit the transaction.</span></span> <span data-ttu-id="acc3a-108">La transacción se controla explícitamente por el administrador de transacciones externo que disponía la transacción en la que se creó este objeto.</span><span class="sxs-lookup"><span data-stu-id="acc3a-108">The transaction is controlled explicitly by the external transaction manager that dispensed the transaction under which this object had been created.</span></span>

> [!Note]  
> <span data-ttu-id="acc3a-109">El objeto de transacciones. ByotServerEx se debe importar en una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="acc3a-109">The Byot.ByotServerEx object needs to be imported into a COM+ application.</span></span>

 

 

 



