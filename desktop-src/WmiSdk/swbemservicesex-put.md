---
description: Devuelve un objeto SWbemObjectPath que contiene la ruta de acceso del objeto en el que se escribieron los datos.
ms.assetid: 1a9a718d-875d-4102-9d9d-3d10be162f58
ms.tgt_platform: multiple
title: Método SWbemServicesEx. put (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.Put
- ISWbemServicesEx.Put
- ISWbemServicesEx.Put
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e495a38262e6b6f7dd8b67424b74db74c025be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715712"
---
# <a name="swbemservicesexput-method"></a><span data-ttu-id="848e1-103">SWbemServicesEx. put (método)</span><span class="sxs-lookup"><span data-stu-id="848e1-103">SWbemServicesEx.Put method</span></span>

<span data-ttu-id="848e1-104">El método **Put** del objeto [**SWbemServicesEx**](swbemservicesex.md) guarda el objeto en el espacio de nombres enlazado al objeto y devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) que contiene la ruta de acceso del objeto en el que se escribieron los datos.</span><span class="sxs-lookup"><span data-stu-id="848e1-104">The **Put** method of the [**SWbemServicesEx**](swbemservicesex.md) object saves the object to the namespace bound to the object and returns an [**SWbemObjectPath**](swbemobjectpath.md) object that contains the path of the object to which the data was written.</span></span>

<span data-ttu-id="848e1-105">Se llama a este método en el modo semisincrónico.</span><span class="sxs-lookup"><span data-stu-id="848e1-105">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="848e1-106">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="848e1-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="848e1-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="848e1-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="848e1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="848e1-108">Syntax</span></span>


```VB
objObjectPath = .Put( _
  ByVal objWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="848e1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="848e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="848e1-110">*objWbemObject*</span><span class="sxs-lookup"><span data-stu-id="848e1-110">*objWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="848e1-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="848e1-111">Required.</span></span> <span data-ttu-id="848e1-112">Nuevo objeto que se va a colocar en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="848e1-112">The new object to be put in the namespace.</span></span> <span data-ttu-id="848e1-113">Puede ser un objeto recién creado o un objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="848e1-113">This can be either a newly created object or a modified object.</span></span>

</dd> <dt>

<span data-ttu-id="848e1-114">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="848e1-114">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="848e1-115">Este parámetro determina si la llamada crea o actualiza el objeto y si la llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="848e1-115">This parameter determines if the call creates or updates the object and if the call returns immediately.</span></span> <span data-ttu-id="848e1-116">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="848e1-116">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="848e1-117"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="848e1-117"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="848e1-118">Permite actualizar una clase si no hay clases derivadas y no hay ninguna instancia para esa clase.</span><span class="sxs-lookup"><span data-stu-id="848e1-118">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="848e1-119">También permite las actualizaciones en todos los casos si el cambio solo se debe a calificadores no importantes (por ejemplo, el calificador de **Descripción** ).</span><span class="sxs-lookup"><span data-stu-id="848e1-119">It also allows updates in all cases if the change is only to unimportant qualifiers (for example, the **Description** qualifier).</span></span> <span data-ttu-id="848e1-120">Éste es el comportamiento predeterminado de esta llamada y se utiliza para la compatibilidad con versiones anteriores de WMI.</span><span class="sxs-lookup"><span data-stu-id="848e1-120">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="848e1-121">Si la clase tiene instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="848e1-121">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="848e1-122"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="848e1-122"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="848e1-123">Permite actualizaciones de clases aunque haya clases secundarias, cuando el cambio no cause conflictos con las clases secundarias.</span><span class="sxs-lookup"><span data-stu-id="848e1-123">Allows updates of classes even if there are child classes, when the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="848e1-124">Puede usar esta marca al agregar una nueva propiedad a una clase base que no se mencionó anteriormente en ninguna de las clases secundarias.</span><span class="sxs-lookup"><span data-stu-id="848e1-124">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="848e1-125">Si la clase tiene instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="848e1-125">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="848e1-126"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="848e1-126"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="848e1-127">Esta marca fuerza las actualizaciones de clases cuando existen clases secundarias en conflicto.</span><span class="sxs-lookup"><span data-stu-id="848e1-127">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="848e1-128">Por ejemplo, esta marca fuerza una actualización si se definió un calificador de clase en una clase secundaria y la clase base intenta agregar el mismo calificador en conflicto con el existente.</span><span class="sxs-lookup"><span data-stu-id="848e1-128">For example, this flag forces an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="848e1-129">En el modo Force, este conflicto se resuelve eliminando el calificador en conflicto de la clase secundaria.</span><span class="sxs-lookup"><span data-stu-id="848e1-129">In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="848e1-130">Si la clase tiene instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="848e1-130">If the class has instances, the update fails.</span></span>

<span data-ttu-id="848e1-131">El uso del modo Force para actualizar una clase estática provoca la eliminación de todas las instancias de esa clase.</span><span class="sxs-lookup"><span data-stu-id="848e1-131">The use of the force mode to update a static class causes the deletion of all instances of that class.</span></span> <span data-ttu-id="848e1-132">Una actualización forzada en una clase de proveedor no elimina las instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="848e1-132">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="848e1-133"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="848e1-133"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="848e1-134">Hace que se cree la clase o instancia si no existe o se sobrescribe si ya existe.</span><span class="sxs-lookup"><span data-stu-id="848e1-134">Causes the class or instance to be created if it does not exist, or overwritten if it already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="848e1-135"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="848e1-135"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="848e1-136">Se usa solo para creación.</span><span class="sxs-lookup"><span data-stu-id="848e1-136">Used for creation only.</span></span> <span data-ttu-id="848e1-137">Se produce un error en la llamada si la clase o la instancia ya existe.</span><span class="sxs-lookup"><span data-stu-id="848e1-137">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="848e1-138"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="848e1-138"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="848e1-139">Hace que esta llamada solo realice una actualización.</span><span class="sxs-lookup"><span data-stu-id="848e1-139">Causes this call to only do an update.</span></span> <span data-ttu-id="848e1-140">La clase o instancia debe existir para que la llamada sea correcta.</span><span class="sxs-lookup"><span data-stu-id="848e1-140">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="848e1-141"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="848e1-141"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="848e1-142">Hace que la llamada se devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="848e1-142">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="848e1-143"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="848e1-143"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="848e1-144">Hace que esta llamada se bloquee hasta que se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="848e1-144">Causes this call to block until the operation has completed.</span></span> <span data-ttu-id="848e1-145">Esta marca llama al método en el modo sincrónico.</span><span class="sxs-lookup"><span data-stu-id="848e1-145">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="848e1-146"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="848e1-146"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="848e1-147">Hace que WMI escriba datos de modificación de clases, así como la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="848e1-147">Causes WMI to write class amendment data as well as the base class definition.</span></span> <span data-ttu-id="848e1-148">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="848e1-148">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="848e1-149">*objWbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="848e1-149">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="848e1-150">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="848e1-150">Typically, this is undefined.</span></span> <span data-ttu-id="848e1-151">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que presta servicio a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="848e1-151">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="848e1-152">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="848e1-152">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="848e1-153">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="848e1-153">Return value</span></span>

<span data-ttu-id="848e1-154">Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="848e1-154">If the call is successful, an [**SWbemObjectPath**](swbemobjectpath.md) object is returned.</span></span> <span data-ttu-id="848e1-155">Este objeto contiene la ruta de acceso del objeto de la instancia o la clase que se ha confirmado correctamente en WMI.</span><span class="sxs-lookup"><span data-stu-id="848e1-155">This object contains the object path of the instance or class that has been successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="848e1-156">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="848e1-156">Error codes</span></span>

<span data-ttu-id="848e1-157">Después de completar el método **Put** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="848e1-157">After the completion of the **Put** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="848e1-158">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="848e1-158">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="848e1-159">El usuario actual no tiene permiso para la operación.</span><span class="sxs-lookup"><span data-stu-id="848e1-159">Current user does not have the permission for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="848e1-160">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="848e1-160">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="848e1-161">Se especificó la marca **wbemChangeFlagCreateOnly** , pero la instancia ya existe.</span><span class="sxs-lookup"><span data-stu-id="848e1-161">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="848e1-162">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="848e1-162">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="848e1-163">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="848e1-163">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="848e1-164">**wbemErrIllegalNull** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="848e1-164">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="848e1-165">Se especificó un valor **null** para una propiedad que no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="848e1-165">A value of **NULL** was specified for a property that cannot be **NULL**.</span></span> <span data-ttu-id="848e1-166">Un ejemplo de este tipo de propiedad está marcado por un calificador de [**clave**](standard-qualifiers.md), **indexado** o **no \_ null** .</span><span class="sxs-lookup"><span data-stu-id="848e1-166">An example of such a property is one marked by a [**Key**](standard-qualifiers.md), **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="848e1-167">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="848e1-167">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="848e1-168">El objeto especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="848e1-168">The specified object is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="848e1-169">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="848e1-169">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="848e1-170">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="848e1-170">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="848e1-171">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="848e1-171">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="848e1-172">Se especificó la marca **wbemChangeFlagUpdateOnly** , pero la instancia o la clase no existen.</span><span class="sxs-lookup"><span data-stu-id="848e1-172">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="848e1-173">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="848e1-173">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="848e1-174">No se han establecido todas las propiedades requeridas para las clases.</span><span class="sxs-lookup"><span data-stu-id="848e1-174">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="848e1-175">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="848e1-175">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="848e1-176">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="848e1-176">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="848e1-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="848e1-177">Requirements</span></span>



| <span data-ttu-id="848e1-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="848e1-178">Requirement</span></span> | <span data-ttu-id="848e1-179">Value</span><span class="sxs-lookup"><span data-stu-id="848e1-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="848e1-180">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="848e1-180">Minimum supported client</span></span><br/> | <span data-ttu-id="848e1-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="848e1-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="848e1-182">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="848e1-182">Minimum supported server</span></span><br/> | <span data-ttu-id="848e1-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="848e1-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="848e1-184">Encabezado</span><span class="sxs-lookup"><span data-stu-id="848e1-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="848e1-185"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="848e1-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="848e1-186">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="848e1-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="848e1-187"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="848e1-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="848e1-188">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="848e1-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="848e1-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="848e1-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="848e1-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="848e1-190">CLSID</span></span><br/>                    | <span data-ttu-id="848e1-191">CLSID \_ ISWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="848e1-191">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="848e1-192">IID</span><span class="sxs-lookup"><span data-stu-id="848e1-192">IID</span></span><br/>                      | <span data-ttu-id="848e1-193">\_ISWBEMSERVICESEX IID</span><span class="sxs-lookup"><span data-stu-id="848e1-193">IID\_ISWbemServicesEx</span></span><br/>                                                        |



 

 




