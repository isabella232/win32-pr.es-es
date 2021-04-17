---
description: El método Add del objeto SWbemPropertySet agrega un objeto SWbemProperty a la colección SWbemPropertySet. Si ya existe una propiedad con el mismo nombre en la colección, su contenido se reemplaza con la nueva definición.
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: Método SWbemPropertySet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Add
- ISWbemPropertySet.Add
- ISWbemPropertySet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ad5b40d31d162b287bdb1a387cd0602e0be1ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716989"
---
# <a name="swbempropertysetadd-method"></a><span data-ttu-id="b7b2a-104">SWbemPropertySet. Add (método)</span><span class="sxs-lookup"><span data-stu-id="b7b2a-104">SWbemPropertySet.Add method</span></span>

<span data-ttu-id="b7b2a-105">El método **Add** del objeto [**SWbemPropertySet**](swbempropertyset.md) agrega un objeto [**SWbemProperty**](swbemproperty.md) a la colección **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="b7b2a-105">The **Add** method of the [**SWbemPropertySet**](swbempropertyset.md) object adds an [**SWbemProperty**](swbemproperty.md) object to the **SWbemPropertySet** collection.</span></span> <span data-ttu-id="b7b2a-106">Si ya existe una propiedad con el mismo nombre en la colección, su contenido se reemplaza con la nueva definición.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-106">If a property with the same name already exists in the collection, its contents are replaced with the new definition.</span></span>

> [!Note]  
> <span data-ttu-id="b7b2a-107">El valor de la propiedad agregada es **null** (sin asignar) después de esta operación.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-107">The value of the added property is **NULL** (unassigned) after this operation.</span></span> <span data-ttu-id="b7b2a-108">Para establecer o cambiar el valor de una propiedad de WMI, debe establecer la propiedad [**Value**](swbemdatetime-value.md) del objeto [**SWbemProperty**](swbemproperty.md) devuelto.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-108">To set or change the value of a WMI property, you must set the [**Value**](swbemdatetime-value.md) property of the returned [**SWbemProperty**](swbemproperty.md) object.</span></span>

 

<span data-ttu-id="b7b2a-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b7b2a-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7b2a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7b2a-110">Syntax</span></span>


```VB
objProperty = .Add( _
  ByVal strName, _
  ByVal iCIMType, _
  [ ByVal bIsArray ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b7b2a-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7b2a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7b2a-112">*strName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7b2a-112">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7b2a-113">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-113">Required.</span></span> <span data-ttu-id="b7b2a-114">Nombre de la nueva propiedad.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-114">Name of the new property.</span></span>

</dd> <dt>

<span data-ttu-id="b7b2a-115">*iCIMType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7b2a-115">*iCIMType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7b2a-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-116">Required.</span></span> <span data-ttu-id="b7b2a-117">Entero que representa el calificador **CIMType** de la nueva propiedad.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-117">An integer that represents the **CIMType** qualifier of the new property.</span></span> <span data-ttu-id="b7b2a-118">Vea [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) para obtener la lista con los calificadores **CIMType** y sus valores.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-118">See [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) for the list with the **CIMType** qualifiers and their values.</span></span>

</dd> <dt>

<span data-ttu-id="b7b2a-119">*bIsArray* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b7b2a-119">*bIsArray* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7b2a-120">Especifica si la propiedad es un tipo de matriz.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-120">Specifies whether the property is an array type.</span></span> <span data-ttu-id="b7b2a-121">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-121">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b7b2a-122">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b7b2a-122">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7b2a-123">Reserved y debe ser cero si se especifica.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-123">Reserved and must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7b2a-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7b2a-124">Return value</span></span>

<span data-ttu-id="b7b2a-125">Si es correcto, este método devuelve un objeto [**SWbemProperty**](swbemproperty.md) que representa la nueva propiedad.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-125">If successful, this method returns an [**SWbemProperty**](swbemproperty.md) object that represents the new property.</span></span> <span data-ttu-id="b7b2a-126">De lo contrario, se devuelve un objeto **null** .</span><span class="sxs-lookup"><span data-stu-id="b7b2a-126">Otherwise, a **null** object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b7b2a-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b7b2a-127">Error codes</span></span>

<span data-ttu-id="b7b2a-128">Después de completar el método **Add** , el objeto **Err** puede contener uno de los códigos de error siguientes.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-128">After completion of the **Add** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="b7b2a-129">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b7b2a-129">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b7b2a-130">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-130">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="b7b2a-131">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b7b2a-131">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b7b2a-132">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-132">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="b7b2a-133">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b7b2a-133">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b7b2a-134">Memoria insuficiente para que se ejecute este método.</span><span class="sxs-lookup"><span data-stu-id="b7b2a-134">Not enough memory for this method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="b7b2a-135">**wbemErrInvalidPropertyType** -2147749930</span><span class="sxs-lookup"><span data-stu-id="b7b2a-135">**wbemErrInvalidPropertyType** - 2147749930</span></span>
</dt> <dd>

<span data-ttu-id="b7b2a-136">No se reconoce el calificador **CIMType** .</span><span class="sxs-lookup"><span data-stu-id="b7b2a-136">The **CIMType** qualifier is not recognized.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b7b2a-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b7b2a-137">Examples</span></span>

<span data-ttu-id="b7b2a-138">Para obtener un ejemplo de código que usa este método, vea el tema [**SWbemPropertySet**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="b7b2a-138">For a code example that uses this method, see the [**SWbemPropertySet**](swbempropertyset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7b2a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7b2a-139">Requirements</span></span>



| <span data-ttu-id="b7b2a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7b2a-140">Requirement</span></span> | <span data-ttu-id="b7b2a-141">Value</span><span class="sxs-lookup"><span data-stu-id="b7b2a-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b2a-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7b2a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b7b2a-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7b2a-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7b2a-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7b2a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b7b2a-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7b2a-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7b2a-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7b2a-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7b2a-147"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7b2a-147"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7b2a-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b7b2a-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="b7b2a-149"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b7b2a-149"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b7b2a-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7b2a-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7b2a-151"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7b2a-151"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b7b2a-152">CLSID</span><span class="sxs-lookup"><span data-stu-id="b7b2a-152">CLSID</span></span><br/>                    | <span data-ttu-id="b7b2a-153">CLSID \_ SWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="b7b2a-153">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="b7b2a-154">IID</span><span class="sxs-lookup"><span data-stu-id="b7b2a-154">IID</span></span><br/>                      | <span data-ttu-id="b7b2a-155">\_ISWBEMPROPERTYSET IID</span><span class="sxs-lookup"><span data-stu-id="b7b2a-155">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="b7b2a-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7b2a-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7b2a-157">**SWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="b7b2a-157">**SWbemPropertySet**</span></span>](swbempropertyset.md)
</dt> <dt>

[<span data-ttu-id="b7b2a-158">**SWbemPropertySet. Remove**</span><span class="sxs-lookup"><span data-stu-id="b7b2a-158">**SWbemPropertySet.Remove**</span></span>](swbempropertyset-remove.md)
</dt> <dt>

[<span data-ttu-id="b7b2a-159">**SWbemProperty. Value**</span><span class="sxs-lookup"><span data-stu-id="b7b2a-159">**SWbemProperty.Value**</span></span>](swbemproperty-value.md)
</dt> </dl>

 

 




