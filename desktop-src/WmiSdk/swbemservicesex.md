---
description: Extiende la funcionalidad de SWbemServices.
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: Objeto SWbemServicesEx (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx
- ISWbemServicesEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8ed41cbab38e24958705c24aefc9ea5e9e67357e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155817"
---
# <a name="swbemservicesex-object"></a><span data-ttu-id="492a0-103">Objeto SWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="492a0-103">SWbemServicesEx object</span></span>

<span data-ttu-id="492a0-104">El objeto **SWbemServicesEx** amplía la funcionalidad de [**SWbemServices**](swbemservices.md).</span><span class="sxs-lookup"><span data-stu-id="492a0-104">The **SWbemServicesEx** object extends the functionality of [**SWbemServices**](swbemservices.md).</span></span> <span data-ttu-id="492a0-105">Los métodos [**Put**](swbemservicesex-put.md) y [**PutAsync**](swbemservicesex-putasync.md) permiten guardar una clase o una instancia en varios espacios de nombres o en un espacio de nombres diferente del que se creó en una instancia.</span><span class="sxs-lookup"><span data-stu-id="492a0-105">The [**Put**](swbemservicesex-put.md) and [**PutAsync**](swbemservicesex-putasync.md) methods allow a class or an instance to be saved to multiple namespaces or to a different namespace than the one where an instance was created.</span></span> <span data-ttu-id="492a0-106">Este objeto no se puede crear mediante la llamada [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript.</span><span class="sxs-lookup"><span data-stu-id="492a0-106">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="492a0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="492a0-107">Members</span></span>

<span data-ttu-id="492a0-108">El objeto **SWbemServicesEx** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="492a0-108">The **SWbemServicesEx** object has these types of members:</span></span>

-   [<span data-ttu-id="492a0-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="492a0-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="492a0-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="492a0-110">Methods</span></span>

<span data-ttu-id="492a0-111">El objeto **SWbemServicesEx** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="492a0-111">The **SWbemServicesEx** object has these methods.</span></span>



| <span data-ttu-id="492a0-112">Método</span><span class="sxs-lookup"><span data-stu-id="492a0-112">Method</span></span>                                       | <span data-ttu-id="492a0-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="492a0-113">Description</span></span>                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="492a0-114">**Pondrán**</span><span class="sxs-lookup"><span data-stu-id="492a0-114">**Put**</span></span>](swbemservicesex-put.md)           | <span data-ttu-id="492a0-115">Guarda el objeto en el espacio de nombres enlazado al objeto **SWbemServicesEx** y devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) que contiene la ruta de acceso del objeto en el que se escribieron los datos.</span><span class="sxs-lookup"><span data-stu-id="492a0-115">Saves the object to the namespace bound to the **SWbemServicesEx** object and returns an [**SWbemObjectPath**](swbemobjectpath.md) object that contains the path of the object to which the data was written.</span></span><br/> |
| [<span data-ttu-id="492a0-116">**PutAsync**</span><span class="sxs-lookup"><span data-stu-id="492a0-116">**PutAsync**</span></span>](swbemservicesex-putasync.md) | <span data-ttu-id="492a0-117">Guarda un objeto de forma asincrónica en un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="492a0-117">Saves an object asynchronously to a namespace.</span></span><br/>                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="492a0-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="492a0-118">Remarks</span></span>

<span data-ttu-id="492a0-119">Se puede llamar a los métodos de esta clase en el modo semisincrónico o en el modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="492a0-119">The methods in this class can be called in either the semisynchronous mode or the asynchronous mode.</span></span> <span data-ttu-id="492a0-120">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="492a0-120">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="492a0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="492a0-121">Requirements</span></span>



| <span data-ttu-id="492a0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="492a0-122">Requirement</span></span> | <span data-ttu-id="492a0-123">Value</span><span class="sxs-lookup"><span data-stu-id="492a0-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="492a0-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="492a0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="492a0-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="492a0-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="492a0-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="492a0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="492a0-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="492a0-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="492a0-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="492a0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="492a0-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="492a0-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="492a0-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="492a0-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="492a0-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="492a0-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="492a0-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="492a0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="492a0-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="492a0-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="492a0-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="492a0-134">CLSID</span></span><br/>                    | <span data-ttu-id="492a0-135">CLSID \_ ISWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="492a0-135">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="492a0-136">IID</span><span class="sxs-lookup"><span data-stu-id="492a0-136">IID</span></span><br/>                      | <span data-ttu-id="492a0-137">\_ISWBEMSERVICESEX IID</span><span class="sxs-lookup"><span data-stu-id="492a0-137">IID\_ISWbemServicesEx</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="492a0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="492a0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="492a0-139">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="492a0-139">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="492a0-140">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="492a0-140">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

