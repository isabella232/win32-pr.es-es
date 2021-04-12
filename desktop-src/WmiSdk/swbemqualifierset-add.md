---
description: El método Add del objeto SWbemQualifierSet agrega un objeto SWbemQualifier a la colección SWbemQualifierSet. Si ya existe un calificador con el mismo nombre en la colección, se reemplaza.
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: Método SWbemQualifierSet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Add
- ISWbemQualifierSet.Add
- ISWbemQualifierSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bbbef15ccc45aeba5b7e3c03f6cb9448cfe03ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361439"
---
# <a name="swbemqualifiersetadd-method"></a><span data-ttu-id="8ee67-104">SWbemQualifierSet. Add (método)</span><span class="sxs-lookup"><span data-stu-id="8ee67-104">SWbemQualifierSet.Add method</span></span>

<span data-ttu-id="8ee67-105">El método **Add** del objeto [**SWbemQualifierSet**](swbemqualifierset.md) agrega un objeto [**SWbemQualifier**](swbemqualifier.md) a la colección **SWbemQualifierSet** .</span><span class="sxs-lookup"><span data-stu-id="8ee67-105">The **Add** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object adds an [**SWbemQualifier**](swbemqualifier.md) object to the **SWbemQualifierSet** collection.</span></span> <span data-ttu-id="8ee67-106">Si ya existe un calificador con el mismo nombre en la colección, se reemplaza.</span><span class="sxs-lookup"><span data-stu-id="8ee67-106">If a qualifier with the same name already exists in the collection, it is replaced.</span></span>

<span data-ttu-id="8ee67-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8ee67-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8ee67-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ee67-108">Syntax</span></span>


```VB
objQualifier = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal bPropagatesToSubclasses ], _
  [ ByVal bPropagatesToInstances ], _
  [ ByVal bOverridable ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8ee67-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ee67-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ee67-110">*strName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ee67-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee67-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ee67-111">Required.</span></span> <span data-ttu-id="8ee67-112">Nombre del nuevo calificador.</span><span class="sxs-lookup"><span data-stu-id="8ee67-112">Name of the new qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="8ee67-113">*varVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ee67-113">*varVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee67-114">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ee67-114">Required.</span></span> <span data-ttu-id="8ee67-115">Valor de variante del nuevo calificador.</span><span class="sxs-lookup"><span data-stu-id="8ee67-115">Variant value of the new qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="8ee67-116">*bPropagatesToSubclasses* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8ee67-116">*bPropagatesToSubclasses* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee67-117">Valor booleano que indica si este nuevo calificador se propaga a las subclases.</span><span class="sxs-lookup"><span data-stu-id="8ee67-117">Boolean value that indicates if this new qualifier is propagated to subclasses.</span></span> <span data-ttu-id="8ee67-118">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="8ee67-118">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="8ee67-119">*bPropagatesToInstances* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8ee67-119">*bPropagatesToInstances* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee67-120">Valor booleano que indica si este nuevo calificador se propaga a las instancias de.</span><span class="sxs-lookup"><span data-stu-id="8ee67-120">Boolean value that indicates if this new qualifier is propagated to instances.</span></span> <span data-ttu-id="8ee67-121">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="8ee67-121">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="8ee67-122">*bOverridable* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8ee67-122">*bOverridable* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee67-123">Valor booleano que indica si se puede invalidar este calificador al propagarse.</span><span class="sxs-lookup"><span data-stu-id="8ee67-123">Boolean value that indicates if this qualifier can be overridden when propagated.</span></span> <span data-ttu-id="8ee67-124">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="8ee67-124">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="8ee67-125">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8ee67-125">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee67-126">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8ee67-126">Reserved.</span></span> <span data-ttu-id="8ee67-127">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="8ee67-127">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ee67-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ee67-128">Return value</span></span>

<span data-ttu-id="8ee67-129">Si es correcto, este método devuelve un objeto [**SWbemQualifier**](swbemqualifier.md) que representa el nuevo calificador.</span><span class="sxs-lookup"><span data-stu-id="8ee67-129">If successful, this method returns an [**SWbemQualifier**](swbemqualifier.md) object that represents the new qualifier.</span></span> <span data-ttu-id="8ee67-130">De lo contrario, se devuelve un objeto **null** .</span><span class="sxs-lookup"><span data-stu-id="8ee67-130">Otherwise, a **null** object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8ee67-131">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8ee67-131">Error codes</span></span>

<span data-ttu-id="8ee67-132">Después de completar el método **Add** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="8ee67-132">After completion of the **Add** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="8ee67-133">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="8ee67-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="8ee67-134">El parámetro *iFlags* no era válido.</span><span class="sxs-lookup"><span data-stu-id="8ee67-134">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8ee67-135">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8ee67-135">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8ee67-136">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8ee67-136">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="8ee67-137">**wbemErrCannotBeKey** -2147749919 (0x8004101F)</span><span class="sxs-lookup"><span data-stu-id="8ee67-137">**wbemErrCannotBeKey** - 2147749919 (0x8004101F)</span></span>
</dt> <dd>

<span data-ttu-id="8ee67-138">Se produjo un intento no válido de especificar un calificador de **clave** en una propiedad que no puede ser una clave.</span><span class="sxs-lookup"><span data-stu-id="8ee67-138">There was an illegal attempt to specify a **Key** qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="8ee67-139">Las claves se especifican en la definición de la clase de un objeto, y no se pueden modificar instancia por instancia.</span><span class="sxs-lookup"><span data-stu-id="8ee67-139">The keys are specified in the class definition for an object and cannot be altered on a per-instance basis.</span></span>

</dd> <dt>

<span data-ttu-id="8ee67-140">**wbemErrInvalidQualifierType** -2147749929 (0x80041029)</span><span class="sxs-lookup"><span data-stu-id="8ee67-140">**wbemErrInvalidQualifierType** - 2147749929 (0x80041029)</span></span>
</dt> <dd>

<span data-ttu-id="8ee67-141">El parámetro *varVal* no es de un tipo de calificador válido.</span><span class="sxs-lookup"><span data-stu-id="8ee67-141">The *varVal* parameter is not of a legal qualifier type.</span></span>

</dd> <dt>

<span data-ttu-id="8ee67-142">**wbemErrOverrideNotAllowed** -2147749914 (0x8004101A)</span><span class="sxs-lookup"><span data-stu-id="8ee67-142">**wbemErrOverrideNotAllowed** - 2147749914 (0x8004101A)</span></span>
</dt> <dd>

<span data-ttu-id="8ee67-143">No es posible realizar la operación **SWbemQualifierSet. Add** en este calificador porque el objeto propietario no permite invalidaciones.</span><span class="sxs-lookup"><span data-stu-id="8ee67-143">It is not possible to perform the **SWbemQualifierSet.Add** operation on this qualifier because the owning object does not permit overrides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ee67-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ee67-144">Requirements</span></span>



| <span data-ttu-id="8ee67-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ee67-145">Requirement</span></span> | <span data-ttu-id="8ee67-146">Value</span><span class="sxs-lookup"><span data-stu-id="8ee67-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee67-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ee67-147">Minimum supported client</span></span><br/> | <span data-ttu-id="8ee67-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ee67-148">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8ee67-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ee67-149">Minimum supported server</span></span><br/> | <span data-ttu-id="8ee67-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ee67-150">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8ee67-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ee67-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ee67-152"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ee67-152"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ee67-153">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8ee67-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="8ee67-154"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8ee67-154"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8ee67-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ee67-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ee67-156"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ee67-156"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8ee67-157">CLSID</span><span class="sxs-lookup"><span data-stu-id="8ee67-157">CLSID</span></span><br/>                    | <span data-ttu-id="8ee67-158">CLSID \_ SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="8ee67-158">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="8ee67-159">IID</span><span class="sxs-lookup"><span data-stu-id="8ee67-159">IID</span></span><br/>                      | <span data-ttu-id="8ee67-160">\_ISWBEMQUALIFIERSET IID</span><span class="sxs-lookup"><span data-stu-id="8ee67-160">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="8ee67-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ee67-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee67-162">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="8ee67-162">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="8ee67-163">**SWbemQualifierSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="8ee67-163">**SWbemQualifierSet.Remove**</span></span>](swbemqualifierset-remove.md)
</dt> </dl>

 

 




