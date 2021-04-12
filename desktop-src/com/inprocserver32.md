---
title: InprocServer32
description: Registra un servidor en proceso de 32 bits y especifica el modelo de subprocesos del apartamento en el que se puede ejecutar el servidor.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- Clave del registro InprocServer32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daae9d495ad588e0dc710b63fe7d7ae9f48c11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532344"
---
# <a name="inprocserver32"></a><span data-ttu-id="99c7d-104">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="99c7d-104">InprocServer32</span></span>

<span data-ttu-id="99c7d-105">Registra un servidor en proceso de 32 bits y especifica el modelo de subprocesos del apartamento en el que se puede ejecutar el servidor.</span><span class="sxs-lookup"><span data-stu-id="99c7d-105">Registers a 32-bit in-process server and specifies the threading model of the apartment the server can run in.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="99c7d-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="99c7d-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a><span data-ttu-id="99c7d-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99c7d-107">Remarks</span></span>

<span data-ttu-id="99c7d-108">**ThreadingModel** es un valor de **reg \_ SZ** que especifica el modelo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="99c7d-108">**ThreadingModel** is a **REG\_SZ** value the specifies the threading model.</span></span> <span data-ttu-id="99c7d-109">Los valores posibles se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="99c7d-109">The possible values are shown in the following table.</span></span>



| <span data-ttu-id="99c7d-110">Value</span><span class="sxs-lookup"><span data-stu-id="99c7d-110">Value</span></span>     | <span data-ttu-id="99c7d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="99c7d-111">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="99c7d-112">Procesamiento</span><span class="sxs-lookup"><span data-stu-id="99c7d-112">Apartment</span></span> | <span data-ttu-id="99c7d-113">Apartamento de un solo subproceso</span><span class="sxs-lookup"><span data-stu-id="99c7d-113">Single-threaded apartment</span></span>                  |
| <span data-ttu-id="99c7d-114">Ambos</span><span class="sxs-lookup"><span data-stu-id="99c7d-114">Both</span></span>      | <span data-ttu-id="99c7d-115">Apartamento de un solo subproceso o multiproceso</span><span class="sxs-lookup"><span data-stu-id="99c7d-115">Single-threaded or multithreaded apartment</span></span> |
| <span data-ttu-id="99c7d-116">Gratuito</span><span class="sxs-lookup"><span data-stu-id="99c7d-116">Free</span></span>      | <span data-ttu-id="99c7d-117">Apartamento multiproceso</span><span class="sxs-lookup"><span data-stu-id="99c7d-117">Multithreaded apartment</span></span>                    |
| <span data-ttu-id="99c7d-118">Neutra</span><span class="sxs-lookup"><span data-stu-id="99c7d-118">Neutral</span></span>   | <span data-ttu-id="99c7d-119">Apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="99c7d-119">Neutral apartment</span></span>                          |



 

<span data-ttu-id="99c7d-120">Debe utilizar el mismo valor para todos los objetos proporcionados por el servidor en proceso.</span><span class="sxs-lookup"><span data-stu-id="99c7d-120">You must use the same value for every object provided by the in-process server.</span></span>

<span data-ttu-id="99c7d-121">Si **ThreadingModel** no está presente o no está establecido en un valor, el servidor se carga en el primer apartamento que se inicializó en el proceso.</span><span class="sxs-lookup"><span data-stu-id="99c7d-121">If **ThreadingModel** is not present or is not set to a value, the server is loaded into the first apartment that was initialized in the process.</span></span> <span data-ttu-id="99c7d-122">A veces, este apartamento se conoce como el contenedor uniproceso (STA) principal.</span><span class="sxs-lookup"><span data-stu-id="99c7d-122">This apartment is sometimes referred to as the main single-threaded apartment (STA).</span></span> <span data-ttu-id="99c7d-123">Si COM inicializa el primer STA de un proceso, en lugar de una llamada explícita a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), se denomina el STA del host.</span><span class="sxs-lookup"><span data-stu-id="99c7d-123">If the first STA in a process is initialized by COM, rather than by an explicit call to [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), it is called the host STA.</span></span> <span data-ttu-id="99c7d-124">Por ejemplo, COM crea un STA de host si un servidor en proceso que se va a cargar requiere un STA, pero actualmente no hay ningún STA en el proceso.</span><span class="sxs-lookup"><span data-stu-id="99c7d-124">For example, COM creates a host STA if an in-process server to be loaded requires an STA but there is currently no STA in the process.</span></span>

<span data-ttu-id="99c7d-125">Siempre que sea posible, el servidor en proceso se carga en el mismo contenedor que el cliente que lo carga.</span><span class="sxs-lookup"><span data-stu-id="99c7d-125">Whenever possible, the in-process server is loaded in the same apartment as the client that loads it.</span></span> <span data-ttu-id="99c7d-126">Si el modelo de subprocesos del apartamento de cliente no es compatible con el modelo especificado, el servidor se carga como se indica en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="99c7d-126">If the threading model of the client apartment is not compatible with the model specified, the server is loaded as indicated in the following table.</span></span>



| <span data-ttu-id="99c7d-127">Modelo de subprocesos del servidor</span><span class="sxs-lookup"><span data-stu-id="99c7d-127">Threading model of server</span></span> | <span data-ttu-id="99c7d-128">El servidor de apartamento se ejecuta en</span><span class="sxs-lookup"><span data-stu-id="99c7d-128">Apartment server is run in</span></span> |
|---------------------------|----------------------------|
| <not specified>     | <span data-ttu-id="99c7d-129">STA principal</span><span class="sxs-lookup"><span data-stu-id="99c7d-129">Main STA</span></span>                   |
| <span data-ttu-id="99c7d-130">Ambos</span><span class="sxs-lookup"><span data-stu-id="99c7d-130">Both</span></span>                      | <span data-ttu-id="99c7d-131">Mismo apartamento que el cliente</span><span class="sxs-lookup"><span data-stu-id="99c7d-131">Same apartment as client</span></span>   |
| <span data-ttu-id="99c7d-132">Gratuito</span><span class="sxs-lookup"><span data-stu-id="99c7d-132">Free</span></span>                      | <span data-ttu-id="99c7d-133">Apartamento multiproceso</span><span class="sxs-lookup"><span data-stu-id="99c7d-133">Multithreaded apartment</span></span>    |
| <span data-ttu-id="99c7d-134">Neutra</span><span class="sxs-lookup"><span data-stu-id="99c7d-134">Neutral</span></span>                   | <span data-ttu-id="99c7d-135">Apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="99c7d-135">Neutral apartment</span></span>          |



 

<span data-ttu-id="99c7d-136">Si el modelo de subprocesos del servidor es apartamento, el apartamento en el que se carga el servidor depende del apartamento en el que se ejecuta el cliente, como se indica en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="99c7d-136">If the threading model of the server is Apartment, the apartment the server is loaded in depends on the apartment the client is running in, as indicated in the following table.</span></span>



| <span data-ttu-id="99c7d-137">El cliente de contenedor se ejecuta en</span><span class="sxs-lookup"><span data-stu-id="99c7d-137">Apartment client is run in</span></span> | <span data-ttu-id="99c7d-138">El servidor de apartamento se ejecuta en</span><span class="sxs-lookup"><span data-stu-id="99c7d-138">Apartment server is run in</span></span> |
|----------------------------|----------------------------|
| <span data-ttu-id="99c7d-139">Multiproceso</span><span class="sxs-lookup"><span data-stu-id="99c7d-139">Multithreaded</span></span>              | <span data-ttu-id="99c7d-140">STA de host</span><span class="sxs-lookup"><span data-stu-id="99c7d-140">Host STA</span></span>                   |
| <span data-ttu-id="99c7d-141">Neutro (en el subproceso STA)</span><span class="sxs-lookup"><span data-stu-id="99c7d-141">Neutral (on STA thread)</span></span>    | <span data-ttu-id="99c7d-142">Mismo apartamento que el cliente</span><span class="sxs-lookup"><span data-stu-id="99c7d-142">Same apartment as client</span></span>   |
| <span data-ttu-id="99c7d-143">Neutro (en subproceso MTA)</span><span class="sxs-lookup"><span data-stu-id="99c7d-143">Neutral (on MTA thread)</span></span>    | <span data-ttu-id="99c7d-144">STA de host</span><span class="sxs-lookup"><span data-stu-id="99c7d-144">Host STA</span></span>                   |



 

<span data-ttu-id="99c7d-145">COM también puede crear un contenedor multiproceso (MTA) de host.</span><span class="sxs-lookup"><span data-stu-id="99c7d-145">COM can also create a host multithreaded apartment (MTA).</span></span> <span data-ttu-id="99c7d-146">Si un cliente de un contenedor uniproceso solicita un servidor en proceso cuyo modelo de subprocesos es gratuito cuando no hay ningún MTA en el proceso, COM crea un MTA de host y carga el servidor en él.</span><span class="sxs-lookup"><span data-stu-id="99c7d-146">If a client in a single-threaded apartment requests an in-process server whose threading model is Free when there is no MTA in the process, COM creates a host MTA and loads the server into it.</span></span>

<span data-ttu-id="99c7d-147">En el caso de un servidor de 32 bits en proceso, se deben registrar las claves [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InProcServer32** y que se pueden [**Insertar**](insertable.md) .</span><span class="sxs-lookup"><span data-stu-id="99c7d-147">For a 32-bit in-process server, the [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32**, and [**Insertable**](insertable.md) keys must be registered.</span></span> <span data-ttu-id="99c7d-148">La entrada **InprocServer** solo es necesaria para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="99c7d-148">The **InprocServer** entry is needed only for backward compatibility.</span></span> <span data-ttu-id="99c7d-149">Si falta, la clase sigue funcionando, pero no se puede cargar en aplicaciones de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="99c7d-149">If it is missing, the class still works but it cannot be loaded in 16-bit applications.</span></span>

<span data-ttu-id="99c7d-150">Si un contenedor está buscando en el registro un servidor en proceso, la versión de 16 bits tiene prioridad con un contenedor de 16 bits y la versión de 32 bits tiene prioridad con un contenedor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="99c7d-150">If a container is searching the registry for an in-process server, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99c7d-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="99c7d-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99c7d-152">**InprocServer**</span><span class="sxs-lookup"><span data-stu-id="99c7d-152">**InprocServer**</span></span>](inprocserver.md)
</dt> </dl>

 

 




