---
title: Agregar una reserva
description: La base de datos de enrutamiento contiene la lista de reserva.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358181cbe57a046f5af54f7adf17bdadb24c3ddc
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104533586"
---
# <a name="adding-a-reservation"></a><span data-ttu-id="b5c87-103">Agregar una reserva</span><span class="sxs-lookup"><span data-stu-id="b5c87-103">Adding a Reservation</span></span>

<span data-ttu-id="b5c87-104">La base de datos de enrutamiento contiene la lista de reserva.</span><span class="sxs-lookup"><span data-stu-id="b5c87-104">The routing database contains the reservation list.</span></span> <span data-ttu-id="b5c87-105">La lista de reserva consta de los usuarios a los que se permite el acceso al espacio de nombres, así como el nivel de acceso de cada usuario que se muestra en la reserva.</span><span class="sxs-lookup"><span data-stu-id="b5c87-105">The reservation list consists of the users that are allowed access to the namespace, as well as the level of access for each user listed under the reservation.</span></span> <span data-ttu-id="b5c87-106">Cuando se agregan o eliminan reservas, se busca en la base de datos de enrutamiento para determinar los privilegios de acceso.</span><span class="sxs-lookup"><span data-stu-id="b5c87-106">When reservations are added or deleted, the routing database is searched to determine access privileges.</span></span>

<span data-ttu-id="b5c87-107">Además de comprobar el ID. de usuario, la API del servidor HTTP también comprueba los conflictos en las reservas existentes antes de instalar una nueva reserva.</span><span class="sxs-lookup"><span data-stu-id="b5c87-107">In addition to checking the users ID, the HTTP Server API also checks for conflicts in existing reservations before installing a new reservation.</span></span>

<span data-ttu-id="b5c87-108">**Para agregar una nueva reserva**</span><span class="sxs-lookup"><span data-stu-id="b5c87-108">**To add a new reservation**</span></span>

1.  <span data-ttu-id="b5c87-109">Si el número de puerto de UrlPrefix tiene reservas o registros para un esquema diferente del esquema en el UrlPrefix, se produce un error en el registro.</span><span class="sxs-lookup"><span data-stu-id="b5c87-109">If the port number in the UrlPrefix has reservations or registrations for a scheme different from the scheme in the UrlPrefix, the registration fails.</span></span> <span data-ttu-id="b5c87-110">HTTP y HTTPS no se admiten en el mismo puerto.</span><span class="sxs-lookup"><span data-stu-id="b5c87-110">HTTP and HTTPS cannot be supported on the same port.</span></span>
2.  <span data-ttu-id="b5c87-111">Busque el depósito adecuado para el registro (consulte la sección [enrutamiento de solicitudes entrantes](routing-incoming-requests.md) ), en función del tipo de host.</span><span class="sxs-lookup"><span data-stu-id="b5c87-111">Locate the appropriate bucket for the registration (see the [Routing Incoming Requests](routing-incoming-requests.md) section), based on the host type.</span></span> <span data-ttu-id="b5c87-112">Los pasos restantes son relativos a este cubo.</span><span class="sxs-lookup"><span data-stu-id="b5c87-112">The remaining steps are relative to this bucket.</span></span>
3.  <span data-ttu-id="b5c87-113">Seleccione las entradas de reserva con los componentes de esquema, host y puerto que coincidan con el UrlPrefix que se va a reservar.</span><span class="sxs-lookup"><span data-stu-id="b5c87-113">Select reservation entries with scheme, host and port components that match the UrlPrefix being reserved.</span></span> <span data-ttu-id="b5c87-114">A partir de estos, busque la entrada con el valor de *relativeUri* que coincida más largo y que no sea igual a relativeUri en la reserva (es decir, el *nodo primario*).</span><span class="sxs-lookup"><span data-stu-id="b5c87-114">From these, locate the entry with the longest matching *relativeUri* that is not equal to the relativeUri in the reservation (that is, the *parent node*).</span></span> <span data-ttu-id="b5c87-115">Si la entrada existe, evalúe los derechos de acceso en función de la ACL asignada a esa entrada.</span><span class="sxs-lookup"><span data-stu-id="b5c87-115">If the entry exists, then evaluate access rights based on the ACL assigned to that entry.</span></span>
4.  <span data-ttu-id="b5c87-116">Si no se encuentra un nodo primario, se trata de una reserva con un objeto relativeUri vacío o una *reserva raíz*.</span><span class="sxs-lookup"><span data-stu-id="b5c87-116">If a parent node was not found, this is a reservation with an empty relativeUri, or *root reservation*.</span></span> <span data-ttu-id="b5c87-117">Conceda derechos de acceso solo si el autor de la llamada se registra en las cuentas LocalSystem o administrador.</span><span class="sxs-lookup"><span data-stu-id="b5c87-117">Grant access rights only if the caller is registered under the LocalSystem or Administrator accounts.</span></span>
5.  <span data-ttu-id="b5c87-118">Si se conceden derechos de acceso, compruebe si hay reservas duplicadas.</span><span class="sxs-lookup"><span data-stu-id="b5c87-118">If access rights are granted, check for duplicate reservations.</span></span> <span data-ttu-id="b5c87-119">Si existe una entrada de reserva con el mismo esquema, puerto, host y relativeUri, \_ \_ se devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="b5c87-119">If a reservation entry exists with the same scheme, port, host and relativeUri, an ERROR\_ALREADY\_EXISTS code is returned.</span></span>
    > [!Note]  
    > <span data-ttu-id="b5c87-120">La actualización de una entrada existente debe realizarse en dos pasos: Elimine la entrada y agregue una nueva.</span><span class="sxs-lookup"><span data-stu-id="b5c87-120">Updating an existing entry should be performed in two steps: delete the entry and add a new one.</span></span>

     

<span data-ttu-id="b5c87-121">Si los pasos anteriores se realizan correctamente, se introduce una nueva entrada de reserva en la base de datos de reserva.</span><span class="sxs-lookup"><span data-stu-id="b5c87-121">If the above steps succeed, a new reservation entry is entered into the reservation database.</span></span>

> [!Note]  
> <span data-ttu-id="b5c87-122">La nueva entrada se crea con la ACL especificada y no hereda las ACL de la entrada *primaria* .</span><span class="sxs-lookup"><span data-stu-id="b5c87-122">The new entry is created with the specified ACL and does not inherit ACLs from the *parent* entry.</span></span>

 

<span data-ttu-id="b5c87-123">En los siguientes ejemplos se muestra el proceso de reserva.</span><span class="sxs-lookup"><span data-stu-id="b5c87-123">The following examples illustrate the reservation process.</span></span>

-   <span data-ttu-id="b5c87-124">Reserva 1: `https://+:80/vroot/subdir/` por administrador para el usuario a y el usuario C se realiza correctamente y se especifica en el cubo "+".</span><span class="sxs-lookup"><span data-stu-id="b5c87-124">Reservation 1: `https://+:80/vroot/subdir/` by Admin for User A and User C succeeds and is entered into the "+" bucket.</span></span>
-   <span data-ttu-id="b5c87-125">Reserva 2: `https://adatum.com:80/vroot/` por el administrador del usuario B se realiza correctamente y se especifica en el cubo "host explícito".</span><span class="sxs-lookup"><span data-stu-id="b5c87-125">Reservation 2: `https://adatum.com:80/vroot/` by Admin for User B succeeds and is entered into the "Explicit host" bucket.</span></span>
-   <span data-ttu-id="b5c87-126">Reserva 3: el `https://adatum.com:80/vroot/subdir/otherdir/` usuario B para el usuario C se realiza correctamente debido a la reserva 2.</span><span class="sxs-lookup"><span data-stu-id="b5c87-126">Reservation 3: `https://adatum.com:80/vroot/subdir/otherdir/` by User B for User C succeeds due to reservation 2.</span></span>
-   <span data-ttu-id="b5c87-127">Reserva 4: `https://+:80/vroot/subdir/otherdir/` por el usuario a para el usuario E se realiza correctamente debido A la reserva 1.</span><span class="sxs-lookup"><span data-stu-id="b5c87-127">Reservation 4: `https://+:80/vroot/subdir/otherdir/` by User A for User E succeeds due to reservation 1.</span></span>
-   <span data-ttu-id="b5c87-128">Reserva 5: `https://adatum.com:80/vroot/subdir/otherdir/` por el usuario a para el usuario E produce un error.</span><span class="sxs-lookup"><span data-stu-id="b5c87-128">Reservation 5: `https://adatum.com:80/vroot/subdir/otherdir/` by User A for User E fails.</span></span> <span data-ttu-id="b5c87-129">Acceso denegado debido a la reserva 2.</span><span class="sxs-lookup"><span data-stu-id="b5c87-129">Access denied due to reservation 2.</span></span>
-   <span data-ttu-id="b5c87-130">Reserva 6: `https://+:80/vroot/subdir/` el administrador del usuario a produce un error.</span><span class="sxs-lookup"><span data-stu-id="b5c87-130">Reservation 6: `https://+:80/vroot/subdir/` by Admin for User A fails.</span></span> <span data-ttu-id="b5c87-131">La reserva entra en conflicto con la reserva 1.</span><span class="sxs-lookup"><span data-stu-id="b5c87-131">The reservation conflicts with reservation 1.</span></span>
-   <span data-ttu-id="b5c87-132">Reserva 7: `https://adatum.com:80/newroot/` por el usuario a para el usuario a, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="b5c87-132">Reservation 7: `https://adatum.com:80/newroot/` by User A for User A fails.</span></span> <span data-ttu-id="b5c87-133">Acceso denegado debido a la reserva de raíz implícita de `https://adatum.com:80/` para LocalSystem o administrador.</span><span class="sxs-lookup"><span data-stu-id="b5c87-133">Access denied due to implicit root reservation of `https://adatum.com:80/` for LocalSystem or Administrator.</span></span>

<span data-ttu-id="b5c87-134">Las reservas pueden afectar al conjunto de direcciones URL en las solicitudes entregadas a un proceso que ha registrado previamente un UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="b5c87-134">Reservations can affect the set of URLs in requests delivered to a process that has previously registered a UrlPrefix.</span></span> <span data-ttu-id="b5c87-135">Por ejemplo, tenga en cuenta el siguiente caso.</span><span class="sxs-lookup"><span data-stu-id="b5c87-135">For example, consider the following scenario.</span></span>

-   <span data-ttu-id="b5c87-136">Registro: `https://adatum.com:80/vroot/` por aplicación 1 para el usuario A.</span><span class="sxs-lookup"><span data-stu-id="b5c87-136">Registration: `https://adatum.com:80/vroot/` by application 1 for User A.</span></span>
-   <span data-ttu-id="b5c87-137">Una solicitud de `https://adatum.com:80/vroot/subdir/file.htm` se entrega a la aplicación 1.</span><span class="sxs-lookup"><span data-stu-id="b5c87-137">A request for `https://adatum.com:80/vroot/subdir/file.htm` is delivered to application 1.</span></span>
-   <span data-ttu-id="b5c87-138">Reserva: `https://+:80/vroot/subdir/` para el usuario B.</span><span class="sxs-lookup"><span data-stu-id="b5c87-138">Reservation: `https://+:80/vroot/subdir/` for User B.</span></span>
-   <span data-ttu-id="b5c87-139">Ahora se ha rechazado una solicitud de `https://adatum.com:80/vroot/subdir/file.htm` .</span><span class="sxs-lookup"><span data-stu-id="b5c87-139">A request for `https://adatum.com:80/vroot/subdir/file.htm` is now rejected.</span></span>
-   <span data-ttu-id="b5c87-140">Registro: `https://adatum.com:80/vroot/subdir/` por aplicación 2 para el usuario B.</span><span class="sxs-lookup"><span data-stu-id="b5c87-140">Registration: `https://adatum.com:80/vroot/subdir/` by application 2 for User B.</span></span>
-   <span data-ttu-id="b5c87-141">Una solicitud de `https://adatum.com:80/vroot/subdir/file.htm` se entrega a la aplicación 2.</span><span class="sxs-lookup"><span data-stu-id="b5c87-141">A request for `https://adatum.com:80/vroot/subdir/file.htm` is delivered to application 2.</span></span>

 

 




