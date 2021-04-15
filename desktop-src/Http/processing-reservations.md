---
title: Procesar reservas
description: El administrador del sistema realiza las reservas de partes del espacio de nombres de la dirección URL y se colocan en el almacén de reserva persistente.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0a78fd6d374ede14e0eba7c1b22ad33ba50648
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104421587"
---
# <a name="processing-reservations"></a><span data-ttu-id="3035c-103">Procesar reservas</span><span class="sxs-lookup"><span data-stu-id="3035c-103">Processing Reservations</span></span>

<span data-ttu-id="3035c-104">El administrador del sistema realiza las reservas de partes del espacio de nombres de la dirección URL y se colocan en el almacén de reserva persistente.</span><span class="sxs-lookup"><span data-stu-id="3035c-104">Reservations for portions of the URL namespace are made by the system administrator and placed in the persistent reservation store.</span></span> <span data-ttu-id="3035c-105">La raíz del espacio de nombres de la dirección URL para HTTP es propiedad del administrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="3035c-105">The root of the URL namespace for HTTP is owned by the system administrator.</span></span> <span data-ttu-id="3035c-106">En todos los valores de host y puerto, siempre se asumen las dos reservas siguientes en la raíz del espacio de nombres **relativeUri** .</span><span class="sxs-lookup"><span data-stu-id="3035c-106">For all host and port values, the following two reservations are always assumed at the root of the **relativeUri** namespace.</span></span>



| <span data-ttu-id="3035c-107">Espacio de nombres reservado</span><span class="sxs-lookup"><span data-stu-id="3035c-107">Namespace reserved</span></span>                 | <span data-ttu-id="3035c-108">Reservado para</span><span class="sxs-lookup"><span data-stu-id="3035c-108">Reserved for</span></span>              |
|------------------------------------|---------------------------|
| <span data-ttu-id="3035c-109"> https:// <host> :<port>/</span><span class="sxs-lookup"><span data-stu-id="3035c-109">https://<host>:<port>/</span></span>  | <span data-ttu-id="3035c-110">Administrador de LocalSystem</span><span class="sxs-lookup"><span data-stu-id="3035c-110">LocalSystem Administrator</span></span> |
| <span data-ttu-id="3035c-111"> https:// <host> :<port>/</span><span class="sxs-lookup"><span data-stu-id="3035c-111">https://<host>:<port>/</span></span> | <span data-ttu-id="3035c-112">Administrador de LocalSystem</span><span class="sxs-lookup"><span data-stu-id="3035c-112">LocalSystem Administrator</span></span> |



 

<span data-ttu-id="3035c-113">Estas reservas implícitas no se pueden quitar.</span><span class="sxs-lookup"><span data-stu-id="3035c-113">These implicit reservations cannot be removed.</span></span> <span data-ttu-id="3035c-114">Sin embargo, es posible delegar reservas de raíz explícitas a otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="3035c-114">However, it is possible to delegate explicit root reservations to other users.</span></span> <span data-ttu-id="3035c-115">Las reservas como las siguientes crearían estas delegaciones:</span><span class="sxs-lookup"><span data-stu-id="3035c-115">Reservations such as the following would create such delegations:</span></span>



| <span data-ttu-id="3035c-116">Espacio de nombres reservado</span><span class="sxs-lookup"><span data-stu-id="3035c-116">Namespace reserved</span></span>        | <span data-ttu-id="3035c-117">Reservado para</span><span class="sxs-lookup"><span data-stu-id="3035c-117">Reserved for</span></span> |
|---------------------------|--------------|
| `https://+:80/`           | <span data-ttu-id="3035c-118">UsuarioA, Usuarioc</span><span class="sxs-lookup"><span data-stu-id="3035c-118">UserA, UserC</span></span> |
| `https://adatum.com:443/` | <span data-ttu-id="3035c-119">UserB</span><span class="sxs-lookup"><span data-stu-id="3035c-119">UserB</span></span>        |



 

<span data-ttu-id="3035c-120">Si el administrador del sistema quita estas reservas delegadas, la propiedad del espacio de nombres se revierte a la reserva implícita para los valores de puerto y host correspondientes.</span><span class="sxs-lookup"><span data-stu-id="3035c-120">If these delegated reservations are removed by the system administrator, ownership of the namespace reverts to the implicit reservation for the corresponding host and port values.</span></span>

 

 




