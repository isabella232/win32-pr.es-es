---
description: Transacciones COM+
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: Transacciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef51f4c8ed5e37101f64d36af385c93ac7e69ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423400"
---
# <a name="com-transactions"></a><span data-ttu-id="c75a5-103">Transacciones COM+</span><span class="sxs-lookup"><span data-stu-id="c75a5-103">COM+ Transactions</span></span>

<span data-ttu-id="c75a5-104">Al comprar un libro de una librería en línea, puede usar una tarjeta de crédito para el dinero de un libro.</span><span class="sxs-lookup"><span data-stu-id="c75a5-104">When you purchase a book from an online bookstore, you use a credit card to trade money for a book.</span></span> <span data-ttu-id="c75a5-105">Después de enviar el pedido, una serie de operaciones relacionadas (validación de la tarjeta de crédito, comprobación de la disponibilidad del inventario, etc.) garantiza que obtendrá el libro y que la librería obtenga su dinero.</span><span class="sxs-lookup"><span data-stu-id="c75a5-105">After you submit your order, a series of related operations (validation of your credit card, verification of inventory availability, and so forth) ensures that you get the book and that the bookstore gets your money.</span></span> <span data-ttu-id="c75a5-106">Si se produce un error en una sola operación de la serie durante el intercambio, se produce un error en todo el intercambio.</span><span class="sxs-lookup"><span data-stu-id="c75a5-106">If a single operation in the series fails during the exchange, the entire exchange fails.</span></span> <span data-ttu-id="c75a5-107">No se obtiene el libro y la librería no obtiene el dinero.</span><span class="sxs-lookup"><span data-stu-id="c75a5-107">You do not get the book, and the bookstore does not get your money.</span></span>

<span data-ttu-id="c75a5-108">La tecnología responsable de la realización de este intercambio en línea con equilibrio y predicción se denomina *procesamiento de transacciones*.</span><span class="sxs-lookup"><span data-stu-id="c75a5-108">The technology responsible for making this online exchange balanced and predictable is called *transaction processing*.</span></span> <span data-ttu-id="c75a5-109">Mediante programación, una *transacción* es una unidad de trabajo en la que se producen una serie de operaciones.</span><span class="sxs-lookup"><span data-stu-id="c75a5-109">Programmatically, a *transaction* is a unit of work in which a series of operations occur.</span></span> <span data-ttu-id="c75a5-110">COM+ utiliza transacciones mediante programación para asegurarse de que los recursos no se actualizan de forma permanente a menos que todas las operaciones dentro de la transacción se completen correctamente.</span><span class="sxs-lookup"><span data-stu-id="c75a5-110">COM+ uses programmatic transactions to ensure that resources are not permanently updated unless all operations within the transaction complete successfully.</span></span> <span data-ttu-id="c75a5-111">Al enlazar un conjunto de operaciones relacionadas en una transacción de COM+ que se completa o completa correctamente, puede simplificar enormemente la recuperación de errores.</span><span class="sxs-lookup"><span data-stu-id="c75a5-111">By binding a set of related operations together in a COM+ transaction that either completely succeeds or completely fails, you can vastly simplify error recovery.</span></span>

<span data-ttu-id="c75a5-112">En los siguientes temas se presenta la teoría general del procesamiento de transacciones, se ofrece una visión más detallada de las transacciones en COM+ y se presentan sugerencias prácticas para escribir componentes transaccionales.</span><span class="sxs-lookup"><span data-stu-id="c75a5-112">The following topics introduce general transaction processing theory, provide a closer look at transactions in COM+, and present practical tips for writing transactional components.</span></span>



| <span data-ttu-id="c75a5-113">Tema</span><span class="sxs-lookup"><span data-stu-id="c75a5-113">Topic</span></span>                                                                   | <span data-ttu-id="c75a5-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c75a5-114">Description</span></span>                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="c75a5-115">Conceptos de transacciones de COM+</span><span class="sxs-lookup"><span data-stu-id="c75a5-115">COM+ Transactions Concepts</span></span>](com--transactions-concepts.md)<br/> | <span data-ttu-id="c75a5-116">Presenta términos y conceptos básicos.</span><span class="sxs-lookup"><span data-stu-id="c75a5-116">Presents basic terms and concepts.</span></span><br/>                                  |
| [<span data-ttu-id="c75a5-117">Tareas de transacciones de COM+</span><span class="sxs-lookup"><span data-stu-id="c75a5-117">COM+ Transactions Tasks</span></span>](com--transactions-tasks.md)<br/>       | <span data-ttu-id="c75a5-118">Proporciona información práctica sobre la escritura de componentes transaccionales.</span><span class="sxs-lookup"><span data-stu-id="c75a5-118">Provides practical information on writing transactional components.</span></span><br/> |



 

 

 




