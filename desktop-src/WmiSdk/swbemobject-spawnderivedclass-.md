---
description: Use el \_ método SpawnDerivedClass del objeto SWbemObject para crear un objeto de clase derivada a partir del objeto actual. El objeto debe ser una definición de clase que se convierte en la clase primaria del objeto generado.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: Método SWbemObject.SpawnDerivedClass_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b26e1d894e5ccc0d0fcec9d7ac9ad0101d18c7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276126"
---
# <a name="swbemobjectspawnderivedclass_-method"></a><span data-ttu-id="867be-104">SWbemObject. SpawnDerivedClass, \_ método</span><span class="sxs-lookup"><span data-stu-id="867be-104">SWbemObject.SpawnDerivedClass\_ method</span></span>

<span data-ttu-id="867be-105">Use el **método \_ SpawnDerivedClass** del objeto [**SWbemObject**](swbemobject.md) para crear un objeto de clase derivada a partir del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="867be-105">Use the **SpawnDerivedClass\_** method of the [**SWbemObject**](swbemobject.md) object to create a derived class object from the current object.</span></span> <span data-ttu-id="867be-106">El objeto debe ser una definición de clase que se convierte en la clase primaria del objeto generado.</span><span class="sxs-lookup"><span data-stu-id="867be-106">The object must be a class definition that becomes the parent class of the spawned object.</span></span>

<span data-ttu-id="867be-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="867be-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="867be-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="867be-108">Syntax</span></span>


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="867be-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="867be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="867be-110">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="867be-110">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="867be-111">Reserved y debe ser 0 (cero) si se especifica.</span><span class="sxs-lookup"><span data-stu-id="867be-111">Reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="867be-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="867be-112">Return value</span></span>

<span data-ttu-id="867be-113">Si la llamada se realiza correctamente, el objeto [**SWbemObject**](swbemobject.md) contiene el nuevo objeto de definición de clase.</span><span class="sxs-lookup"><span data-stu-id="867be-113">If the call is successful, the [**SWbemObject**](swbemobject.md) object contains the new class definition object.</span></span> <span data-ttu-id="867be-114">No se devuelve ningún objeto cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="867be-114">No object returns when there is an error.</span></span>

## <a name="error-codes"></a><span data-ttu-id="867be-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="867be-115">Error codes</span></span>

<span data-ttu-id="867be-116">Después de completar el método **SpawnDerivedClass \_** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="867be-116">After the completion of the **SpawnDerivedClass\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="867be-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="867be-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="867be-118">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="867be-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="867be-119">**wbemErrIllegalOperation** -2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="867be-119">**wbemErrIllegalOperation** - 2147749918 (0x8004101E)</span></span>
</dt> <dd>

<span data-ttu-id="867be-120">El usuario solicitó una operación no válida, como generar una clase a partir de una instancia.</span><span class="sxs-lookup"><span data-stu-id="867be-120">User requested an illegal operation, such as spawning a class from an instance.</span></span>

</dd> <dt>

<span data-ttu-id="867be-121">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="867be-121">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="867be-122">La clase de origen no se definió por completo ni se registró en WMI, por lo que no se permite una nueva clase derivada.</span><span class="sxs-lookup"><span data-stu-id="867be-122">Source class was not completely defined or registered with WMI, so a new derived class is not permitted.</span></span>

</dd> <dt>

<span data-ttu-id="867be-123">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="867be-123">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="867be-124">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="867be-124">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="867be-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="867be-125">Remarks</span></span>

<span data-ttu-id="867be-126">El objeto que se devuelve automáticamente se convierte en una subclase del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="867be-126">The object that is returned automatically becomes a subclass of the current object.</span></span> <span data-ttu-id="867be-127">Este comportamiento no se puede invalidar.</span><span class="sxs-lookup"><span data-stu-id="867be-127">This behavior cannot be overridden.</span></span> <span data-ttu-id="867be-128">No hay ningún otro método por el que pueda crear clases derivadas.</span><span class="sxs-lookup"><span data-stu-id="867be-128">There is no other method by which you can create derived classes.</span></span>

<span data-ttu-id="867be-129">No se puede crear una clase derivada a partir de una clase que sea local para su propio proceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="867be-129">You cannot create a derived class from a class that is local to your own client process.</span></span> <span data-ttu-id="867be-130">Antes de utilizar este método para crear una clase derivada, debe crear la clase base.</span><span class="sxs-lookup"><span data-stu-id="867be-130">Before use this method to create a derived class, you must create the base class.</span></span> <span data-ttu-id="867be-131">Para crear la clase base, llame a [**SWbemObject. \_ Put**](swbemobject-put-.md)y recupere la clase base mediante [**SWbemServices. Get**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="867be-131">To create the base class, call [**SWbemObject.Put\_**](swbemobject-put-.md), and retrieve the base class using [**SWbemServices.Get**](swbemservices-get.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="867be-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="867be-132">Requirements</span></span>



| <span data-ttu-id="867be-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="867be-133">Requirement</span></span> | <span data-ttu-id="867be-134">Value</span><span class="sxs-lookup"><span data-stu-id="867be-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="867be-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="867be-135">Minimum supported client</span></span><br/> | <span data-ttu-id="867be-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="867be-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="867be-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="867be-137">Minimum supported server</span></span><br/> | <span data-ttu-id="867be-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="867be-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="867be-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="867be-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="867be-140"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="867be-140"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="867be-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="867be-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="867be-142"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="867be-142"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="867be-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="867be-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="867be-144"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="867be-144"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="867be-145">CLSID</span><span class="sxs-lookup"><span data-stu-id="867be-145">CLSID</span></span><br/>                    | <span data-ttu-id="867be-146">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="867be-146">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="867be-147">IID</span><span class="sxs-lookup"><span data-stu-id="867be-147">IID</span></span><br/>                      | <span data-ttu-id="867be-148">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="867be-148">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




