---
description: Marcas de coherencia y de realización
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: Marcas de coherencia y de realización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a61d1f715d06e6bfb6632b9bbb59276074c4d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539430"
---
# <a name="consistent-and-done-flags"></a><span data-ttu-id="1b2fa-103">Marcas de coherencia y de realización</span><span class="sxs-lookup"><span data-stu-id="1b2fa-103">Consistent and Done Flags</span></span>

<span data-ttu-id="1b2fa-104">COM+ siempre crea un objeto de contexto antes de activar un objeto transaccional.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-104">COM+ always creates a context object before activating a transactional object.</span></span> <span data-ttu-id="1b2fa-105">El objeto de contexto contiene información relacionada con el objeto, como su creador y su identificador de transacción.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-105">The context object holds object-related information, such as its creator and its transaction identifier.</span></span> <span data-ttu-id="1b2fa-106">Cada objeto de contexto también contiene una marca *coherente* y una *marca Done*.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-106">Each context object also contains a *consistent flag* and a *done flag*.</span></span> <span data-ttu-id="1b2fa-107">Juntas, estas marcas determinan el estado del objeto transaccional.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-107">Together these flags determine the status of the transactional object.</span></span>

<span data-ttu-id="1b2fa-108">La marca coherente indica que el objeto transaccional es coherente o incoherente.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-108">The consistent flag indicates that the transactional object is either consistent or inconsistent.</span></span> <span data-ttu-id="1b2fa-109">Los detalles específicos de lo que hace que el estado de un objeto sea coherente es el programador.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-109">The specific details of what makes an object's state consistent is up to the programmer.</span></span> <span data-ttu-id="1b2fa-110">Cuando una llamada al método establece esta marca en true, el objeto es coherente.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-110">When a method call sets this flag to True, the object is consistent.</span></span> <span data-ttu-id="1b2fa-111">False indica que el objeto es incoherente.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-111">False indicates that the object is inconsistent.</span></span> <span data-ttu-id="1b2fa-112">COM+ establece la marca en true cuando crea una instancia de objeto.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-112">COM+ sets the flag to True when it creates an object instance.</span></span> <span data-ttu-id="1b2fa-113">Un objeto coherente está listo para continuar con la transacción.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-113">A consistent object is ready to proceed with the transaction.</span></span> <span data-ttu-id="1b2fa-114">Mientras un objeto permanece activo, las llamadas posteriores al método pueden cambiar repetidamente la marca coherente de true a false y viceversa.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-114">While an object remains active, subsequent method calls can repeatedly switch the consistent flag from True to False and vice versa.</span></span>

<span data-ttu-id="1b2fa-115">La marca Done determina la duración de una transacción.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-115">The done flag determines the duration of a transaction.</span></span> <span data-ttu-id="1b2fa-116">Cuando una llamada de método devuelve, COM+ inspecciona la marca done.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-116">When a method call returns, COM+ inspects the done flag.</span></span> <span data-ttu-id="1b2fa-117">Si el método establece esta marca en true, COM+ desactiva el objeto y anota la marca coherente.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-117">If the method sets this flag to True, COM+ deactivates the object and notes the consistent flag.</span></span> <span data-ttu-id="1b2fa-118">Cuando la marca Done es false, COM+ no desactiva el objeto ni anota la marca coherente.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-118">When the done flag is False, COM+ neither deactivates the object nor notes the consistent flag.</span></span> <span data-ttu-id="1b2fa-119">COM+ establece la marca done en false cuando crea una instancia de objeto.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-119">COM+ sets the done flag to False when it creates an object instance.</span></span>

<span data-ttu-id="1b2fa-120">La marca coherente convierte un voto para confirmar o anular la transacción en la que se ejecuta, y la marca Done finaliza el voto.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-120">The consistent flag casts a vote to commit or abort the transaction in which it executes, and the done flag finalizes the vote.</span></span> <span data-ttu-id="1b2fa-121">COM+ inspecciona la marca coherente cuando la marca Done está establecida en true en una llamada al método que devuelve o cuando el objeto se desactiva.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-121">COM+ inspects the consistent flag when the done flag is set to True on a method call return or when the object deactivates.</span></span> <span data-ttu-id="1b2fa-122">Aunque la marca coherente de un objeto puede cambiar repetidamente dentro de cada llamada al método, solo el último cambio cuenta.</span><span class="sxs-lookup"><span data-stu-id="1b2fa-122">Although an object's consistent flag can change repeatedly within each method call, only the last change counts.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b2fa-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b2fa-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b2fa-124">Administrar transacciones automáticas en COM+</span><span class="sxs-lookup"><span data-stu-id="1b2fa-124">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[<span data-ttu-id="1b2fa-125">Establecimiento de las marcas coherente y realizada</span><span class="sxs-lookup"><span data-stu-id="1b2fa-125">Setting the Consistent and Done Flags</span></span>](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



