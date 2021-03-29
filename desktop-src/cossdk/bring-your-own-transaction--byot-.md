---
description: Traiga su propia transacción (transacciones)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Traiga su propia transacción (transacciones)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ca6f7f12babbf3ad183c4695a68591d9e181a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666192"
---
# <a name="bring-your-own-transaction-byot"></a><span data-ttu-id="e2360-103">Traiga su propia transacción (transacciones)</span><span class="sxs-lookup"><span data-stu-id="e2360-103">Bring Your Own Transaction (BYOT)</span></span>

<span data-ttu-id="e2360-104">La operación de transacciones permite crear un componente con o para heredar una transacción externa.</span><span class="sxs-lookup"><span data-stu-id="e2360-104">BYOT allows a component to be created with or to inherit an external transaction.</span></span> <span data-ttu-id="e2360-105">Es decir, un componente que todavía no tiene una transacción asociada puede adquirir una transacción.</span><span class="sxs-lookup"><span data-stu-id="e2360-105">That is, a component that does not already have an associated transaction can acquire a transaction.</span></span> <span data-ttu-id="e2360-106">Actualmente, las transacciones MTS son automáticas; Si una instancia de componente vive en una transacción se determina en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="e2360-106">Currently, MTS transactions are automatic; whether a component instance lives in a transaction is determined at creation time.</span></span> <span data-ttu-id="e2360-107">Los atributos transaccionales de un componente y su creador determinan qué transacción está asociada a una instancia determinada.</span><span class="sxs-lookup"><span data-stu-id="e2360-107">The transactional attributes of a component and its creator determine what transaction is associated with a given instance.</span></span> <span data-ttu-id="e2360-108">En todos los casos, MTS controla la duración de las transacciones.</span><span class="sxs-lookup"><span data-stu-id="e2360-108">In all cases, MTS controls transaction lifetimes.</span></span> <span data-ttu-id="e2360-109">COM+ lo amplía para permitir la configuración de un DTC o una transacción TIP ya existentes como la propiedad de transacción del contexto de un componente nuevo.</span><span class="sxs-lookup"><span data-stu-id="e2360-109">COM+ extends this to allow setting an arbitrary pre-existing DTC or TIP transaction as the transaction property of a new component's context.</span></span> <span data-ttu-id="e2360-110">Esto permite asociar los componentes configurados con las transacciones cuya duración está controlada por un monitor de TP, un OTS o un DBMS.</span><span class="sxs-lookup"><span data-stu-id="e2360-110">This allows configured components to be associated with transactions whose lifetimes are controlled by a TP monitor, OTS, or DBMS.</span></span>

> [!Note]  
> <span data-ttu-id="e2360-111">Las transacciones manuales deben usarse con precaución.</span><span class="sxs-lookup"><span data-stu-id="e2360-111">BYOT transactions must be used with caution.</span></span> <span data-ttu-id="e2360-112">En determinadas situaciones, pueden dar lugar a una transacción que abarque varios dominios de sincronización, es decir, que permiten el paralelismo con una transacción, lo que provoca una condición de interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="e2360-112">In certain situations, they can result in a transaction spanning multiple synchronization domains—that is, they allow parallelism with a transaction, causing a deadlock condition.</span></span> <span data-ttu-id="e2360-113">Las transacciones automáticas, en lugar de las transacciones manuales, son el modelo de programación preferido para escritores de componentes empresariales.</span><span class="sxs-lookup"><span data-stu-id="e2360-113">Automatic transactions, rather than BYOT transactions, are the preferred programming model for writers of business components.</span></span>

 

<span data-ttu-id="e2360-114">Las interfaces para las transacciones de transacciones manuales incluyen la interfaz [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) y la interfaz [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) .</span><span class="sxs-lookup"><span data-stu-id="e2360-114">The interfaces for BYOT transactions include the [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) interface and the [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) interface.</span></span> <span data-ttu-id="e2360-115">La interfaz **ICreateWithTransactionEx** crea un objeto que se da de alta en una transacción manual.</span><span class="sxs-lookup"><span data-stu-id="e2360-115">The **ICreateWithTransactionEx** interface creates an object that is enlisted within a manual transaction.</span></span> <span data-ttu-id="e2360-116">La interfaz **ICreateWithTipTransactionEx** crea un objeto que se da de alta en una transacción manual mediante el protocolo de Internet de transacciones (TIP).</span><span class="sxs-lookup"><span data-stu-id="e2360-116">The **ICreateWithTipTransactionEx** interface creates an object that is enlisted within a manual transaction using the Transaction Internet Protocol (TIP).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2360-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e2360-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2360-118">Heredar transacciones manuales</span><span class="sxs-lookup"><span data-stu-id="e2360-118">Inheriting Manual Transactions</span></span>](inheriting-manual-transactions.md)
</dt> </dl>

 

 



