---
description: El \_ método Delete del objeto SWbemObject elimina la clase actual o la instancia actual.
ms.assetid: bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb
ms.tgt_platform: multiple
title: Método SWbemObject.Delete_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Delete_
- ISWbemObject.Delete_
- ISWbemObject.Delete_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d994c8a9b9e0af9d4bd884c89cd67280513c9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082975"
---
# <a name="swbemobjectdelete_-method"></a><span data-ttu-id="91398-103">SWbemObject. Delete ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="91398-103">SWbemObject.Delete\_ method</span></span>

<span data-ttu-id="91398-104">El **método \_ Delete** del objeto [**SWbemObject**](swbemobject.md) elimina la clase actual o la instancia actual.</span><span class="sxs-lookup"><span data-stu-id="91398-104">The **Delete\_** method of the [**SWbemObject**](swbemobject.md) object deletes either the current class or the current instance.</span></span> <span data-ttu-id="91398-105">Si un proveedor dinámico proporciona la clase o la instancia, a veces no es posible eliminar este objeto a menos que el proveedor admita la eliminación de la clase o la instancia.</span><span class="sxs-lookup"><span data-stu-id="91398-105">If a dynamic provider supplies the class or instance, it is sometimes not possible to delete this object unless the provider supports class or instance deletion.</span></span> <span data-ttu-id="91398-106">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="91398-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="91398-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91398-107">Syntax</span></span>


```VB
SWbemObject.Delete_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="91398-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91398-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91398-109">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="91398-109">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="91398-110">Reserved y debe ser 0 (cero) si se especifica.</span><span class="sxs-lookup"><span data-stu-id="91398-110">Reserved and must be 0 (zero) if specified.</span></span>

</dd> <dt>

<span data-ttu-id="91398-111">*objwbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="91398-111">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="91398-112">Normalmente, este parámetro no está definido.</span><span class="sxs-lookup"><span data-stu-id="91398-112">This parameter is typically undefined.</span></span> <span data-ttu-id="91398-113">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="91398-113">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="91398-114">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="91398-114">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91398-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91398-115">Return value</span></span>

<span data-ttu-id="91398-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="91398-116">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="91398-117">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="91398-117">Error codes</span></span>

<span data-ttu-id="91398-118">Después de completar el **método \_ Delete** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="91398-118">After completion of the **Delete\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="91398-119">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="91398-119">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="91398-120">El contexto actual no tiene los derechos de seguridad adecuados para eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="91398-120">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="91398-121">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="91398-121">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="91398-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="91398-122">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="91398-123">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="91398-123">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="91398-124">La clase especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="91398-124">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="91398-125">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="91398-125">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="91398-126">No se puede eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="91398-126">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="91398-127">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="91398-127">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="91398-128">El objeto no existía.</span><span class="sxs-lookup"><span data-stu-id="91398-128">Object did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="91398-129">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="91398-129">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="91398-130">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="91398-130">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91398-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91398-131">Remarks</span></span>

<span data-ttu-id="91398-132">Se produce un error en el método **Delete \_** si se crea una nueva instancia de [**SWbemObject**](swbemobject.md) , pero no se proporciona ningún valor para la propiedad Key.</span><span class="sxs-lookup"><span data-stu-id="91398-132">The **Delete\_** method fails if a new instance of [**SWbemObject**](swbemobject.md) is created, but no value is supplied for the key property.</span></span> <span data-ttu-id="91398-133">Instrumental de administración de Windows (WMI) genera automáticamente un valor de identificador único global (GUID), pero **SWbemObject. Delete \_** no acepta un valor GUID.</span><span class="sxs-lookup"><span data-stu-id="91398-133">Windows Management Instrumentation (WMI) generates a globally unique identifier (GUID) value automatically, but a GUID value is not accepted by **SWbemObject.Delete\_**.</span></span> <span data-ttu-id="91398-134">En este caso, [**SWbemServices. Delete**](swbemservices-delete.md), que usa la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="91398-134">In this case, [**SWbemServices.Delete**](swbemservices-delete.md), which uses the object path works.</span></span> <span data-ttu-id="91398-135">Tenga en cuenta que el método [**SWbemObject. put \_**](swbemobject-put-.md) devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) después de confirmar un objeto en WMI.</span><span class="sxs-lookup"><span data-stu-id="91398-135">Note that an [**SWbemObjectPath**](swbemobjectpath.md) object is returned by the [**SWbemObject.Put\_**](swbemobject-put-.md) method after an object is committed to WMI.</span></span>

## <a name="examples"></a><span data-ttu-id="91398-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="91398-136">Examples</span></span>

<span data-ttu-id="91398-137">En el ejemplo siguiente se crea una nueva clase; agrega una propiedad de clave; escribe la nueva clase en el repositorio; y muestra la ruta de acceso del nuevo objeto de clase.</span><span class="sxs-lookup"><span data-stu-id="91398-137">The following example creates a new class; adds a key property; writes the new class to the repository; and displays the path of the new class object.</span></span> <span data-ttu-id="91398-138">Después, el script genera una instancia de la nueva clase; lo escribe; y muestra la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="91398-138">The script then spawns an instance of the new class; writes it; and displays the path.</span></span> <span data-ttu-id="91398-139">Tenga en cuenta que el script elimina la clase y sus instancias del repositorio mediante la eliminación de la clase.</span><span class="sxs-lookup"><span data-stu-id="91398-139">Note that the script deletes both the class and its instances from the repository by simply deleting the class.</span></span>


```VB
On Error Resume Next
wbemCimtypeString = 8             ' String datatype
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString 
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.Add "key", TRUE

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objClass.Delete_()
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a><span data-ttu-id="91398-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91398-140">Requirements</span></span>



| <span data-ttu-id="91398-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="91398-141">Requirement</span></span> | <span data-ttu-id="91398-142">Value</span><span class="sxs-lookup"><span data-stu-id="91398-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91398-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91398-143">Minimum supported client</span></span><br/> | <span data-ttu-id="91398-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91398-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91398-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91398-145">Minimum supported server</span></span><br/> | <span data-ttu-id="91398-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91398-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91398-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91398-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="91398-148"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="91398-148"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="91398-149">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="91398-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="91398-150"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="91398-150"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="91398-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="91398-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91398-152"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91398-152"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="91398-153">CLSID</span><span class="sxs-lookup"><span data-stu-id="91398-153">CLSID</span></span><br/>                    | <span data-ttu-id="91398-154">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="91398-154">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="91398-155">IID</span><span class="sxs-lookup"><span data-stu-id="91398-155">IID</span></span><br/>                      | <span data-ttu-id="91398-156">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="91398-156">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




