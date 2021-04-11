---
description: Use el \_ método SpawnInstance del objeto SWbemObject para crear una nueva instancia de una clase.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: Método SWbemObject.SpawnInstance_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 804c7d2828723ee8da5dae28321faab62a32a0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279106"
---
# <a name="swbemobjectspawninstance_-method"></a><span data-ttu-id="d64af-103">SWbemObject. SpawnInstance, \_ método</span><span class="sxs-lookup"><span data-stu-id="d64af-103">SWbemObject.SpawnInstance\_ method</span></span>

<span data-ttu-id="d64af-104">Use el **método \_ SpawnInstance** del objeto [**SWbemObject**](swbemobject.md) para crear una nueva instancia de una clase.</span><span class="sxs-lookup"><span data-stu-id="d64af-104">Use the **SpawnInstance\_** method of the [**SWbemObject**](swbemobject.md) object to create a new instance of a class.</span></span> <span data-ttu-id="d64af-105">El objeto actual debe ser una definición de clase obtenida de WMI a través de un método como [**SWbemServices. Get**](swbemservices-get.md) o [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="d64af-105">The current object must be a class definition obtained from WMI via a method such as [**SWbemServices.Get**](swbemservices-get.md) or [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span> <span data-ttu-id="d64af-106">A continuación, use esta definición de clase para crear nuevas instancias.</span><span class="sxs-lookup"><span data-stu-id="d64af-106">Then, use this class definition to create new instances.</span></span> <span data-ttu-id="d64af-107">Cree cada nueva instancia localmente en el proceso y, a continuación, llame a [**SWbemObject. put \_**](swbemobject-put-.md) para crear realmente la instancia en WMI.</span><span class="sxs-lookup"><span data-stu-id="d64af-107">Create each new instance locally within the process, and then call [**SWbemObject.Put\_**](swbemobject-put-.md) to actually create the instance within WMI.</span></span>

> [!Note]  
> <span data-ttu-id="d64af-108">Se admite la generación de una instancia a partir de una instancia de, pero la instancia devuelta está vacía.</span><span class="sxs-lookup"><span data-stu-id="d64af-108">Spawning an instance from an instance is supported, but the returned instance is empty.</span></span>

 

<span data-ttu-id="d64af-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d64af-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d64af-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d64af-110">Syntax</span></span>


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d64af-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d64af-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d64af-112">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d64af-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d64af-113">Reserved y debe ser cero si se especifica.</span><span class="sxs-lookup"><span data-stu-id="d64af-113">Reserved and must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d64af-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d64af-114">Return value</span></span>

<span data-ttu-id="d64af-115">Si se realiza correctamente, esta llamada devuelve un objeto [**SWbemObject**](swbemobject.md) que contiene una nueva instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="d64af-115">If successful, this call returns an [**SWbemObject**](swbemobject.md) object that contains a new instance of the class.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d64af-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d64af-116">Error codes</span></span>

<span data-ttu-id="d64af-117">Después de completar el método **SpawnInstance \_** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="d64af-117">After the completion of the **SpawnInstance\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d64af-118">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="d64af-118">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="d64af-119">El objeto actual no es una definición de clase válida y no puede generar nuevas instancias.</span><span class="sxs-lookup"><span data-stu-id="d64af-119">Current object is not a valid class definition, and it cannot spawn new instances.</span></span> <span data-ttu-id="d64af-120">O bien está incompleto o no se ha registrado con WMI mediante [**SWbemObject. put \_**](swbemobject-put-.md).</span><span class="sxs-lookup"><span data-stu-id="d64af-120">Either it is incomplete, or it has not been registered with WMI using [**SWbemObject.Put\_**](swbemobject-put-.md).</span></span>

</dd> <dt>

<span data-ttu-id="d64af-121">**wbemErrIllegalOperation** -2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="d64af-121">**wbemErrIllegalOperation** - 2147749918 (0x8004101E)</span></span>
</dt> <dd>

<span data-ttu-id="d64af-122">Se devuelve si este método se usa en una instancia de en lugar de en una clase.</span><span class="sxs-lookup"><span data-stu-id="d64af-122">Returned if this method is used on an instance instead of a class.</span></span>

</dd> <dt>

<span data-ttu-id="d64af-123">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d64af-123">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d64af-124">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="d64af-124">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="d64af-125">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d64af-125">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d64af-126">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="d64af-126">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d64af-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d64af-127">Requirements</span></span>



| <span data-ttu-id="d64af-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d64af-128">Requirement</span></span> | <span data-ttu-id="d64af-129">Value</span><span class="sxs-lookup"><span data-stu-id="d64af-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d64af-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d64af-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d64af-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d64af-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d64af-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d64af-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d64af-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d64af-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d64af-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d64af-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d64af-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d64af-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d64af-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d64af-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="d64af-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d64af-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d64af-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d64af-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d64af-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d64af-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d64af-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="d64af-140">CLSID</span></span><br/>                    | <span data-ttu-id="d64af-141">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="d64af-141">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="d64af-142">IID</span><span class="sxs-lookup"><span data-stu-id="d64af-142">IID</span></span><br/>                      | <span data-ttu-id="d64af-143">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="d64af-143">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="d64af-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="d64af-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d64af-145">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="d64af-145">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="d64af-146">**SWbemObject. put\_**</span><span class="sxs-lookup"><span data-stu-id="d64af-146">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)
</dt> <dt>

[<span data-ttu-id="d64af-147">**SWbemServices. get**</span><span class="sxs-lookup"><span data-stu-id="d64af-147">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

 




