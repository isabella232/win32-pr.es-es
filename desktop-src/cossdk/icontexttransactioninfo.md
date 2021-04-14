---
description: Proporciona acceso a las propiedades del objeto de contexto relacionadas con las transacciones.
ms.assetid: 3b309153-be7d-444e-be23-777887f1ee95
title: Interfaz IContextTransactionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 499ab2371eda6dda6512b5fddb097d3adc2a6f05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496331"
---
# <a name="icontexttransactioninfo-interface"></a><span data-ttu-id="915da-103">Interfaz IContextTransactionInfo</span><span class="sxs-lookup"><span data-stu-id="915da-103">IContextTransactionInfo interface</span></span>

<span data-ttu-id="915da-104">Proporciona acceso a las propiedades del objeto de contexto relacionadas con las transacciones.</span><span class="sxs-lookup"><span data-stu-id="915da-104">Provides access to context object properties that relate to transactions.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="915da-105">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="915da-105">When to implement</span></span>

<span data-ttu-id="915da-106">No debe implementar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="915da-106">You should not implement this interface.</span></span> <span data-ttu-id="915da-107">La implementación estándar proporciona una funcionalidad completa.</span><span class="sxs-lookup"><span data-stu-id="915da-107">The standard implementation provides complete functionality.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="915da-108">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="915da-108">When to use</span></span>

<span data-ttu-id="915da-109">Utilice esta interfaz para tener acceso a las propiedades del objeto de contexto relacionadas con las transacciones.</span><span class="sxs-lookup"><span data-stu-id="915da-109">Use this interface to access context object properties that relate to transactions.</span></span>

## <a name="members"></a><span data-ttu-id="915da-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="915da-110">Members</span></span>

<span data-ttu-id="915da-111">La interfaz **IContextTransactionInfo** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="915da-111">The **IContextTransactionInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="915da-112">**IContextTransactionInfo** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="915da-112">**IContextTransactionInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="915da-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="915da-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="915da-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="915da-114">Methods</span></span>

<span data-ttu-id="915da-115">La interfaz **IContextTransactionInfo** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="915da-115">The **IContextTransactionInfo** interface has these methods.</span></span>



| <span data-ttu-id="915da-116">Método</span><span class="sxs-lookup"><span data-stu-id="915da-116">Method</span></span>                                                                                         | <span data-ttu-id="915da-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="915da-117">Description</span></span>                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="915da-118">**FetchTransaction**</span><span class="sxs-lookup"><span data-stu-id="915da-118">**FetchTransaction**</span></span>](icontexttransactioninfo-registertransactionproxy.md)                   | <span data-ttu-id="915da-119">Recupera el proxy de transacción o de transacción asociado al contexto actual, si existe.</span><span class="sxs-lookup"><span data-stu-id="915da-119">Retrieves the transaction or transaction proxy that is associated with the current context, if any.</span></span><br/>              |
| [<span data-ttu-id="915da-120">**GetTxIsolationLevelAndTimeout**</span><span class="sxs-lookup"><span data-stu-id="915da-120">**GetTxIsolationLevelAndTimeout**</span></span>](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | <span data-ttu-id="915da-121">Recupera el nivel de aislamiento y el valor de tiempo de espera de una transacción hospedada en el contexto de la transacción raíz.</span><span class="sxs-lookup"><span data-stu-id="915da-121">Retrieves the isolation level and timeout value of a transaction that is hosted in the root transaction context.</span></span><br/> |
| [<span data-ttu-id="915da-122">**RegisterTransactionProxy**</span><span class="sxs-lookup"><span data-stu-id="915da-122">**RegisterTransactionProxy**</span></span>](icontexttransactioninfo-fetchtransaction.md)                   | <span data-ttu-id="915da-123">Asocia una implementación de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) con el contexto actual.</span><span class="sxs-lookup"><span data-stu-id="915da-123">Associates an [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation with the current context.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="915da-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="915da-124">Requirements</span></span>



| <span data-ttu-id="915da-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="915da-125">Requirement</span></span> | <span data-ttu-id="915da-126">Value</span><span class="sxs-lookup"><span data-stu-id="915da-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="915da-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="915da-127">Minimum supported client</span></span><br/> | <span data-ttu-id="915da-128">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="915da-128">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="915da-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="915da-129">Minimum supported server</span></span><br/> | <span data-ttu-id="915da-130">Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]</span><span class="sxs-lookup"><span data-stu-id="915da-130">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



 

