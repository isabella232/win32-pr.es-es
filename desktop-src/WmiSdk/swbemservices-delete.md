---
description: Elimina la clase o instancia que se especifica en la ruta de acceso del objeto. Solo se pueden eliminar objetos en el espacio de nombres actual.
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.tgt_platform: multiple
title: Método SWbemServices. Delete (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Delete
- ISWbemServices.Delete
- ISWbemServices.Delete
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690dc595471baa5514d7f1ab84a8f6def16ee5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497836"
---
# <a name="swbemservicesdelete-method"></a><span data-ttu-id="09917-104">SWbemServices. Delete (método)</span><span class="sxs-lookup"><span data-stu-id="09917-104">SWbemServices.Delete method</span></span>

<span data-ttu-id="09917-105">El método **Delete** del objeto [**SWbemServices**](swbemservices.md) elimina la clase o la instancia que se especifica en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="09917-105">The **Delete** method of the [**SWbemServices**](swbemservices.md) object deletes the class or instance that is specified in the object path.</span></span> <span data-ttu-id="09917-106">Solo se pueden eliminar objetos en el espacio de nombres actual.</span><span class="sxs-lookup"><span data-stu-id="09917-106">You can only delete objects in the current namespace.</span></span>

<span data-ttu-id="09917-107">Si un proveedor dinámico proporciona la clase o la instancia, no se puede eliminar este objeto a menos que el proveedor admita la eliminación de la clase o la instancia.</span><span class="sxs-lookup"><span data-stu-id="09917-107">If a dynamic provider supplies the class or instance, you cannot delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="09917-108">Se llama a este método en el modo sincrónico.</span><span class="sxs-lookup"><span data-stu-id="09917-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="09917-109">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="09917-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="09917-110">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="09917-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="09917-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09917-111">Syntax</span></span>


```VB
SWbemServices.Delete( _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="09917-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09917-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09917-113">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="09917-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="09917-114">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="09917-114">Required.</span></span> <span data-ttu-id="09917-115">Cadena que contiene la ruta de acceso al objeto que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="09917-115">String that contains the object path to the object that you want to delete.</span></span> <span data-ttu-id="09917-116">Para obtener más información, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="09917-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="09917-117">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="09917-117">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="09917-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="09917-118">Reserved.</span></span> <span data-ttu-id="09917-119">Este valor debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="09917-119">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="09917-120">*objWbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="09917-120">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="09917-121">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="09917-121">Typically, this is undefined.</span></span> <span data-ttu-id="09917-122">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que presta servicio a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="09917-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="09917-123">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="09917-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09917-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09917-124">Return value</span></span>

<span data-ttu-id="09917-125">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="09917-125">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="09917-126">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="09917-126">Error codes</span></span>

<span data-ttu-id="09917-127">Después de completar el método **Delete** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="09917-127">After the completion of the **Delete** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="09917-128">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="09917-128">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="09917-129">El contexto actual no tiene los derechos de seguridad adecuados para eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="09917-129">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="09917-130">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="09917-130">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="09917-131">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="09917-131">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="09917-132">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="09917-132">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="09917-133">La clase especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="09917-133">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="09917-134">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="09917-134">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="09917-135">No se puede eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="09917-135">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="09917-136">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="09917-136">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="09917-137">El objeto no existe.</span><span class="sxs-lookup"><span data-stu-id="09917-137">Object does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="09917-138">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="09917-138">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="09917-139">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="09917-139">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09917-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09917-140">Remarks</span></span>

<span data-ttu-id="09917-141">El método **SWbemServices. Delete** se puede usar cuando la propiedad de clave del objeto no tiene un valor, porque este método solo requiere una ruta de acceso de objeto como entrada.</span><span class="sxs-lookup"><span data-stu-id="09917-141">The **SWbemServices.Delete** method can be used when the key property for the object is not given a value, because this method only requires an object path as input.</span></span> <span data-ttu-id="09917-142">Este método se puede usar en situaciones en las que se produce un error en [**SWbemObject. Delete \_**](swbemobject-delete-.md) por falta de un valor de clave.</span><span class="sxs-lookup"><span data-stu-id="09917-142">This method can be used in situations where [**SWbemObject.Delete\_**](swbemobject-delete-.md) fails for lack of a key value.</span></span> <span data-ttu-id="09917-143">Si el objeto se confirma en WMI a través de [**SWbemObject \_ . put**](swbemobject-put-.md), se obtuvo un objeto [**SWbemObjectPath**](swbemobjectpath.md) a través de la llamada.</span><span class="sxs-lookup"><span data-stu-id="09917-143">If the object is committed to WMI through [**SWbemObject.Put\_**](swbemobject-put-.md), then an [**SWbemObjectPath**](swbemobjectpath.md) object was obtained through the call.</span></span>

## <a name="examples"></a><span data-ttu-id="09917-144">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="09917-144">Examples</span></span>

<span data-ttu-id="09917-145">En el ejemplo siguiente se crea una nueva clase, se agrega una propiedad que no es una clave, se escribe la nueva clase en el repositorio y se muestra la ruta de acceso del nuevo objeto de clase.</span><span class="sxs-lookup"><span data-stu-id="09917-145">The following example creates a new class, adds a property that is not a key, writes the new class to the repository, and displays the path of the new class object.</span></span> <span data-ttu-id="09917-146">A continuación, el script genera una instancia de la nueva clase, escribe la instancia y muestra la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="09917-146">The script then spawns an instance of the new class, writes the instance, and displays the path.</span></span> <span data-ttu-id="09917-147">Tenga en cuenta que el script elimina la clase y sus instancias del repositorio mediante la eliminación de la clase.</span><span class="sxs-lookup"><span data-stu-id="09917-147">Note that the script deletes both the class and its instances from the repository by deleting the class.</span></span> <span data-ttu-id="09917-148">Para obtener más información sobre las clases e instancias de WMI, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md) y [modelo de información común](common-information-model.md).</span><span class="sxs-lookup"><span data-stu-id="09917-148">For more information about WMI classes and instances, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Common Information Model](common-information-model.md).</span></span>


```VB
wbemCimtypeSint32 = 3
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' Integer property
objClass.Properties_.Add "iProperty", wbemCimtypeSint32  
objClass.Properties_("iProperty").Qualifiers_.Add "key", TRUE 

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.iProperty = 1000

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objSWbemService.Delete("NewClass")
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a><span data-ttu-id="09917-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09917-149">Requirements</span></span>



| <span data-ttu-id="09917-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="09917-150">Requirement</span></span> | <span data-ttu-id="09917-151">Value</span><span class="sxs-lookup"><span data-stu-id="09917-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09917-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09917-152">Minimum supported client</span></span><br/> | <span data-ttu-id="09917-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09917-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="09917-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09917-154">Minimum supported server</span></span><br/> | <span data-ttu-id="09917-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09917-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="09917-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09917-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="09917-157"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="09917-157"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="09917-158">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="09917-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="09917-159"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="09917-159"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="09917-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="09917-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09917-161"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09917-161"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="09917-162">CLSID</span><span class="sxs-lookup"><span data-stu-id="09917-162">CLSID</span></span><br/>                    | <span data-ttu-id="09917-163">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="09917-163">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="09917-164">IID</span><span class="sxs-lookup"><span data-stu-id="09917-164">IID</span></span><br/>                      | <span data-ttu-id="09917-165">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="09917-165">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="09917-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="09917-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09917-167">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="09917-167">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="09917-168">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="09917-168">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> </dl>

 

 




