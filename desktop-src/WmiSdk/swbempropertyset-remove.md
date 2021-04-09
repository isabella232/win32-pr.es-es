---
description: El método Remove del objeto SWbemPropertySet elimina una propiedad de la colección SWbemPropertySet.
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.tgt_platform: multiple
title: Método SWbemPropertySet. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Remove
- ISWbemPropertySet.Remove
- ISWbemPropertySet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5b6903ae05c801d5903754ef8df0bb02cad51204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155825"
---
# <a name="swbempropertysetremove-method"></a><span data-ttu-id="9997f-103">SWbemPropertySet. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="9997f-103">SWbemPropertySet.Remove method</span></span>

<span data-ttu-id="9997f-104">El método **Remove** del objeto [**SWbemPropertySet**](swbempropertyset.md) elimina una propiedad de la colección **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="9997f-104">The **Remove** method of the [**SWbemPropertySet**](swbempropertyset.md) object deletes a property from the **SWbemPropertySet** collection.</span></span>

<span data-ttu-id="9997f-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9997f-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9997f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9997f-106">Syntax</span></span>


```VB
SWbemPropertySet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9997f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9997f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9997f-108">*strName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9997f-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9997f-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9997f-109">Required.</span></span> <span data-ttu-id="9997f-110">Nombre del elemento que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="9997f-110">Name of the item to remove.</span></span>

</dd> <dt>

<span data-ttu-id="9997f-111">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9997f-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9997f-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9997f-112">Reserved.</span></span> <span data-ttu-id="9997f-113">Este valor debe ser 0 (cero) si se especifica.</span><span class="sxs-lookup"><span data-stu-id="9997f-113">This value must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9997f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9997f-114">Return value</span></span>

<span data-ttu-id="9997f-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9997f-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9997f-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9997f-116">Error codes</span></span>

<span data-ttu-id="9997f-117">Después de completar el método **Remove** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="9997f-117">After completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="9997f-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="9997f-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="9997f-119">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="9997f-119">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="9997f-120">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="9997f-120">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="9997f-121">El usuario intentó eliminar una propiedad que no se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="9997f-121">User attempted to delete a property that cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="9997f-122">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="9997f-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="9997f-123">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="9997f-123">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="9997f-124">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="9997f-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="9997f-125">La propiedad especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="9997f-125">Specified property does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="9997f-126">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="9997f-126">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="9997f-127">Memoria insuficiente para que se ejecute este método.</span><span class="sxs-lookup"><span data-stu-id="9997f-127">Not enough memory for this method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="9997f-128">**wbemErrPropagatedProperty** -142927303552 (0x2147219380)</span><span class="sxs-lookup"><span data-stu-id="9997f-128">**wbemErrPropagatedProperty** - 142927303552 (0x2147219380)</span></span>
</dt> <dd>

<span data-ttu-id="9997f-129">El usuario intentó eliminar una propiedad que no era propiedad.</span><span class="sxs-lookup"><span data-stu-id="9997f-129">User attempted to delete a property that was not owned.</span></span> <span data-ttu-id="9997f-130">Se trataba de una propiedad heredada de una clase principal.</span><span class="sxs-lookup"><span data-stu-id="9997f-130">The property was inherited from a parent class.</span></span>

</dd> <dt>

<span data-ttu-id="9997f-131">**wbemErrResetToDefault** -2147758082 (0x80043002)</span><span class="sxs-lookup"><span data-stu-id="9997f-131">**wbemErrResetToDefault** - 2147758082 (0x80043002)</span></span>
</dt> <dd>

<span data-ttu-id="9997f-132">El usuario eliminó un valor predeterminado de invalidación para la clase actual.</span><span class="sxs-lookup"><span data-stu-id="9997f-132">User deleted an override default value for the current class.</span></span> <span data-ttu-id="9997f-133">Se ha reactivado el valor predeterminado de esta propiedad en la clase primaria.</span><span class="sxs-lookup"><span data-stu-id="9997f-133">The default value for this property in the parent class has been reactivated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9997f-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9997f-134">Remarks</span></span>

<span data-ttu-id="9997f-135">Las propiedades no se pueden quitar de las instancias de clase ni de las clases derivadas con propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9997f-135">Properties cannot be removed from class instances or derived classes with inherited properties.</span></span> <span data-ttu-id="9997f-136">Estos intentos de eliminación provocan un error y no se quita la propiedad. la propiedad se restablece a su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9997f-136">Such deletion attempts raise an error and the property is not removed; the property is reset to its default value.</span></span>

<span data-ttu-id="9997f-137">No se puede recorrer en iteración una colección mientras se quitan elementos porque cuando se quita un elemento de una colección, el puntero de la colección se mueve al siguiente elemento.</span><span class="sxs-lookup"><span data-stu-id="9997f-137">You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element.</span></span> <span data-ttu-id="9997f-138">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="9997f-138">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9997f-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9997f-139">Examples</span></span>

<span data-ttu-id="9997f-140">Para obtener un ejemplo de código que usa este método, vea el tema [**SWbemPropertySet**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="9997f-140">For a code example that uses this method, see the [**SWbemPropertySet**](swbempropertyset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="9997f-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9997f-141">Requirements</span></span>



| <span data-ttu-id="9997f-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="9997f-142">Requirement</span></span> | <span data-ttu-id="9997f-143">Value</span><span class="sxs-lookup"><span data-stu-id="9997f-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9997f-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9997f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9997f-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9997f-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9997f-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9997f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9997f-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9997f-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9997f-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9997f-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="9997f-149"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9997f-149"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9997f-150">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9997f-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="9997f-151"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9997f-151"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9997f-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9997f-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9997f-153"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9997f-153"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9997f-154">CLSID</span><span class="sxs-lookup"><span data-stu-id="9997f-154">CLSID</span></span><br/>                    | <span data-ttu-id="9997f-155">CLSID \_ SWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="9997f-155">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="9997f-156">IID</span><span class="sxs-lookup"><span data-stu-id="9997f-156">IID</span></span><br/>                      | <span data-ttu-id="9997f-157">\_ISWBEMPROPERTYSET IID</span><span class="sxs-lookup"><span data-stu-id="9997f-157">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="9997f-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="9997f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9997f-159">**SWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="9997f-159">**SWbemPropertySet**</span></span>](swbempropertyset.md)
</dt> <dt>

[<span data-ttu-id="9997f-160">**SWbemPropertySet. Add**</span><span class="sxs-lookup"><span data-stu-id="9997f-160">**SWbemPropertySet.Add**</span></span>](swbempropertyset-add.md)
</dt> </dl>

 

 




