---
description: No es necesario que un proveedor admita las operaciones de instancia parcial. Sin embargo, un proveedor debe ser compatible con toda la semántica de una operación de instancia parcial, procesar una instancia completa o devolver un \_ \_ parámetro no compatible de WBEM E \_ .
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: Compatibilidad con operaciones de Partial-Instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf656688ffbcc6981c6a3e55dc480570ad0f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706078"
---
# <a name="supporting-partial-instance-operations"></a><span data-ttu-id="f80a8-104">Compatibilidad con operaciones de Partial-Instance</span><span class="sxs-lookup"><span data-stu-id="f80a8-104">Supporting Partial-Instance Operations</span></span>

<span data-ttu-id="f80a8-105">No es necesario que un proveedor admita las operaciones de instancia parcial.</span><span class="sxs-lookup"><span data-stu-id="f80a8-105">A provider is not required to support any partial-instance operations.</span></span> <span data-ttu-id="f80a8-106">Sin embargo, un proveedor debe ser compatible con toda la semántica de una operación de instancia parcial, procesar una instancia completa o devolver **un \_ \_ \_ parámetro no compatible de WBEM E**.</span><span class="sxs-lookup"><span data-stu-id="f80a8-106">However, a provider must either support all the semantics of a partial-instance operation, process a complete instance, or return **WBEM\_E\_UNSUPPORTED\_PARAMETER**.</span></span>

<span data-ttu-id="f80a8-107">Al crear un proveedor que admita operaciones de instancia parcial, debe observar las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="f80a8-107">When creating a provider that supports partial-instance operations, you must observe the following rules:</span></span>

-   <span data-ttu-id="f80a8-108">Reutilice el mismo objeto de contexto que WMI envía al proveedor.</span><span class="sxs-lookup"><span data-stu-id="f80a8-108">Reuse the same context object that WMI sends to the provider.</span></span> <span data-ttu-id="f80a8-109">WMI usa el \_ \_ \_ \_ \_ valor con nombre "obtener solicitud de cliente ext" para evitar interbloqueos y quita este cliente antes de reenviar el objeto de contexto a un proveedor.</span><span class="sxs-lookup"><span data-stu-id="f80a8-109">WMI uses the "\_\_GET\_EXT\_CLIENT\_REQUEST" named value to prevent deadlocks and removes this client before forwarding the context object to a provider.</span></span>
-   <span data-ttu-id="f80a8-110">En el caso de las llamadas reentrantes a WMI que no requieran una operación de instancia parcial, asegúrese de volver a pasar el mismo objeto de contexto sin ninguna modificación.</span><span class="sxs-lookup"><span data-stu-id="f80a8-110">For reentrant calls back into WMI that do not require a partial-instance operation, ensure to pass back the same context object without any modifications.</span></span> <span data-ttu-id="f80a8-111">WMI recibe el objeto de contexto sin el \_ \_ \_ \_ valor con nombre "Get ext Client \_ Request" establecido y elimina todos los valores con nombre asociados a las operaciones de instancia parcial del objeto de contexto antes de pasarlos a otros proveedores.</span><span class="sxs-lookup"><span data-stu-id="f80a8-111">WMI receives the context object without the "\_\_GET\_EXT\_CLIENT\_REQUEST" named value set and deletes all named values associated with partial-instance operations from the context object before passing it to other providers.</span></span> <span data-ttu-id="f80a8-112">No cambiar el objeto de contexto impide que otros proveedores reciban operaciones de recuperación de instancia parcial destinadas a un objeto diferente no relacionado.</span><span class="sxs-lookup"><span data-stu-id="f80a8-112">Not changing the context object blocks other providers from receiving partial-instance retrieval operations intended for a different, unrelated object.</span></span>
-   <span data-ttu-id="f80a8-113">Para realizar una operación de instancia parcial reentrante mientras se lleva a cabo una solicitud, establezca el \_ \_ \_ \_ valor y la propiedad "obtener solicitud de cliente ext \_ " que faltan.</span><span class="sxs-lookup"><span data-stu-id="f80a8-113">To perform a reentrant partial-instance operation while carrying out a request, set the missing "\_\_GET\_EXT\_CLIENT\_REQUEST" named value and property clear.</span></span> <span data-ttu-id="f80a8-114">Opcionalmente, puede modificar las propiedades en el \_ \_ \_ \_ valor con nombre "obtener propiedades ext" antes de volver a enviar el objeto de contexto a WMI con la llamada reentrante.</span><span class="sxs-lookup"><span data-stu-id="f80a8-114">Optionally, you can modify the properties in the "\_\_GET\_EXT\_PROPERTIES" named value before sending the context object back into WMI with the reentrant call.</span></span>
-   <span data-ttu-id="f80a8-115">No tener acceso al objeto de contexto después de devolverlo a WMI durante una llamada reentrante; otros proveedores pueden modificar las listas de propiedades u otros valores durante la reentrada.</span><span class="sxs-lookup"><span data-stu-id="f80a8-115">Do not access the context object after you return it to WMI during a reentrant call; other providers may modify the property lists or other values during reentrancy.</span></span> <span data-ttu-id="f80a8-116">Puede examinar o modificar el objeto de contexto solo mientras dure la llamada a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que implemente.</span><span class="sxs-lookup"><span data-stu-id="f80a8-116">You can examine or modify the context object only for the duration of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) call that you implement.</span></span>

 

 



