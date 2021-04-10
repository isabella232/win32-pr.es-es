---
description: Tareas de transacciones de COM+
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: Tareas de transacciones de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70aaebd3e788e1ff12e86b7831979f055367fea7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153264"
---
# <a name="com-transactions-tasks"></a><span data-ttu-id="addf7-103">Tareas de transacciones de COM+</span><span class="sxs-lookup"><span data-stu-id="addf7-103">COM+ Transactions Tasks</span></span>

<span data-ttu-id="addf7-104">Aunque el procesamiento automático de transacciones en COM+ le permite dedicar tiempo de desarrollo más productivo a la creación y configuración de objetos que desea que participen en transacciones automáticas, hay algunas tareas de programación que puede realizar para adaptar el comportamiento de las transacciones a los requisitos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="addf7-104">While automatic transaction processing in COM+ allows you to spend more productive development time in creating and configuring objects that you want to participate in automatic transactions, there are some programming tasks you can perform to tailor transaction behavior to your application requirements.</span></span>

<span data-ttu-id="addf7-105">En los temas siguientes se describen las opciones de programación específicas relacionadas con el procesamiento de transacciones.</span><span class="sxs-lookup"><span data-stu-id="addf7-105">The following topics discuss specific programming options related to transaction processing.</span></span>



| <span data-ttu-id="addf7-106">Tema</span><span class="sxs-lookup"><span data-stu-id="addf7-106">Topic</span></span>                                                                                             | <span data-ttu-id="addf7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="addf7-107">Description</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="addf7-108">Establecer el atributo de transacción</span><span class="sxs-lookup"><span data-stu-id="addf7-108">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)<br/>             | <span data-ttu-id="addf7-109">Describe cómo establecer los valores de atributo de transacción para los objetos de transacción.</span><span class="sxs-lookup"><span data-stu-id="addf7-109">Describes how to set transaction attribute values for your transaction objects.</span></span><br/>         |
| [<span data-ttu-id="addf7-110">Establecer el nivel de aislamiento de la transacción</span><span class="sxs-lookup"><span data-stu-id="addf7-110">Setting the Transaction Isolation Level</span></span>](setting-the-transaction-isolation-level.md)<br/> | <span data-ttu-id="addf7-111">Describe cómo establecer los niveles de aislamiento de transacción para los objetos de transacción.</span><span class="sxs-lookup"><span data-stu-id="addf7-111">Describes how to set the transaction isolation levels for your transaction objects.</span></span><br/>     |
| [<span data-ttu-id="addf7-112">Establecer el tiempo de espera de la transacción</span><span class="sxs-lookup"><span data-stu-id="addf7-112">Setting the Transaction Time-Out</span></span>](setting-the-transaction-time-out.md)<br/>               | <span data-ttu-id="addf7-113">Describe cómo establecer intervalos de tiempo de espera para las transacciones.</span><span class="sxs-lookup"><span data-stu-id="addf7-113">Describes how to set time-out intervals for your transactions.</span></span><br/>                          |
| [<span data-ttu-id="addf7-114">Establecimiento de las marcas coherente y realizada</span><span class="sxs-lookup"><span data-stu-id="addf7-114">Setting the Consistent and Done Flags</span></span>](setting-the-consistent-and-done-flags.md)<br/>     | <span data-ttu-id="addf7-115">Muestra cómo utilizar las marcas coherente y completada para controlar el resultado de una transacción.</span><span class="sxs-lookup"><span data-stu-id="addf7-115">Shows how to use the consistent and done flags to control the outcome of a transaction.</span></span><br/> |
| [<span data-ttu-id="addf7-116">Crear objetos de transacciones</span><span class="sxs-lookup"><span data-stu-id="addf7-116">Creating BYOT Objects</span></span>](creating-byot-objects.md)<br/>                                     | <span data-ttu-id="addf7-117">Describe cómo crear objetos para que pueda llevar su propia transacción (transacciones).</span><span class="sxs-lookup"><span data-stu-id="addf7-117">Describes how to create objects so you can Bring Your Own Transaction (BYOT).</span></span><br/>           |



 

> [!Note]  
> <span data-ttu-id="addf7-118">Como norma general, cualquier componente que actualice el estado persistente debe admitir transacciones.</span><span class="sxs-lookup"><span data-stu-id="addf7-118">As a general rule, any component that updates persistent state should support transactions.</span></span> <span data-ttu-id="addf7-119">Los componentes que combinan las operaciones de dos o más objetos en una sola tarea deben usar transacciones para simplificar la recuperación de errores.</span><span class="sxs-lookup"><span data-stu-id="addf7-119">Components that combine the operations of two or more objects into a single task should use transactions to simplify error recovery.</span></span> <span data-ttu-id="addf7-120">Además, para liberar recursos, como las conexiones de base de datos, las transacciones en COM+ deben ser tan cortas como se puedan hacer.</span><span class="sxs-lookup"><span data-stu-id="addf7-120">Also, to release resources, such as database connections, transactions in COM+ should be as short as you can make them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="addf7-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="addf7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="addf7-122">Conceptos de transacciones de COM+</span><span class="sxs-lookup"><span data-stu-id="addf7-122">COM+ Transactions Concepts</span></span>](com--transactions-concepts.md)
</dt> </dl>

 

 




