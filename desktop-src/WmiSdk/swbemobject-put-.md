---
description: El \_ método put de SWbemObject crea o actualiza una instancia o un objeto de clase para instrumental de administración de Windows (WMI). Puede usar este método después de modificar cualquier propiedad o método de un SWbemObject y de que los cambios se escriban en WMI.
ms.assetid: c636ff95-9f3e-4ba9-adf3-30b981be02a4
ms.tgt_platform: multiple
title: Método SWbemObject.Put_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Put_
- ISWbemObject.Put_
- ISWbemObject.Put_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9f5ca9b79c9def8f209da37e0ef1cfddefa0dbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715737"
---
# <a name="swbemobjectput_-method"></a><span data-ttu-id="b2cd9-104">SWbemObject. put ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="b2cd9-104">SWbemObject.Put\_ method</span></span>

<span data-ttu-id="b2cd9-105">El **método \_ Put** de [**SWbemObject**](swbemobject.md) crea o actualiza una instancia o un objeto de clase para instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b2cd9-105">The **Put\_** method of [**SWbemObject**](swbemobject.md) creates or updates an instance or a class object to Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="b2cd9-106">Puede usar este método después de modificar cualquier propiedad o método de un **SWbemObject** y de que los cambios se escriban en WMI.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-106">You can use this method after you modify any properties or methods in an **SWbemObject**, and your changes are written to WMI.</span></span>

<span data-ttu-id="b2cd9-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b2cd9-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2cd9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2cd9-108">Syntax</span></span>


```VB
objObjectPath = .Put_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b2cd9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2cd9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2cd9-110">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b2cd9-110">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2cd9-111">Este parámetro determina si la llamada crea o actualiza la clase o instancia y si la llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-111">This parameter determines if the call creates or updates the class or instance and if the call returns immediately.</span></span> <span data-ttu-id="b2cd9-112">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-112">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="b2cd9-113"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="b2cd9-113"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>\*\*\*\*wbemChangeFlagUpdateCompatible\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b2cd9-114">Permite actualizar una clase si no hay clases derivadas y no hay ninguna instancia para esa clase.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-114">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="b2cd9-115">También permite las actualizaciones en todos los casos si el cambio es solo para calificadores no importantes (por ejemplo, el calificador de **Descripción** ).</span><span class="sxs-lookup"><span data-stu-id="b2cd9-115">It also allows updates in all cases if the change is just to unimportant qualifiers (for example, the **Description** qualifier).</span></span> <span data-ttu-id="b2cd9-116">Éste es el comportamiento predeterminado de esta llamada y se utiliza para la compatibilidad con versiones anteriores de WMI.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-116">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="b2cd9-117">Si la clase tiene instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-117">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="b2cd9-118"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="b2cd9-118"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>\*\*\*\*wbemChangeFlagUpdateSafeMode\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="b2cd9-119">Permite actualizaciones de clases aunque haya clases secundarias si el cambio no provoca conflictos con las clases secundarias.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-119">Allows updates of classes even if there are child classes if the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="b2cd9-120">Puede usar esta marca al agregar una nueva propiedad a una clase base que no se mencionó anteriormente en ninguna de las clases secundarias.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-120">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="b2cd9-121">Si la clase tiene instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-121">If the class has instances the update fails.</span></span> <span data-ttu-id="b2cd9-122">Si la clase tiene instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-122">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="b2cd9-123"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode \* \* \* \* (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="b2cd9-123"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>\*\*\*\*WbemChangeFlagUpdateForceMode\*\*\*\* (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="b2cd9-124">Esta marca fuerza las actualizaciones de clases cuando existen clases secundarias en conflicto.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-124">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="b2cd9-125">Por ejemplo, esta marca forzará una actualización si se definió un calificador de clase en una clase secundaria y la clase base intenta agregar el mismo calificador y en conflicto con el existente.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-125">For example, this flag will force an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier and in conflict with the existing one.</span></span> <span data-ttu-id="b2cd9-126">En el modo Force, este conflicto se resolvería eliminando el calificador en conflicto de la clase secundaria.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-126">In force mode this conflict would be resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="b2cd9-127">Si la clase tiene instancias, se producirá un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-127">If the class has instances the update will fail.</span></span>

<span data-ttu-id="b2cd9-128">El uso del modo Force para actualizar una clase estática produce la eliminación de todas las instancias de esa clase.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-128">Using force mode to update a static class results in the deletion of all instances of that class.</span></span> <span data-ttu-id="b2cd9-129">Una actualización forzada en una clase de proveedor no elimina las instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-129">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="b2cd9-130"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="b2cd9-130"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>\*\*\*\*wbemChangeFlagCreateOrUpdate\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b2cd9-131">Hace que se cree la clase o instancia si no existe o se sobrescribe si ya existe.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-131">Causes the class or instance to be created if it does not exist or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="b2cd9-132"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly \* \* \* \* (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="b2cd9-132"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>\*\*\*\*wbemChangeFlagCreateOnly\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="b2cd9-133">Se usa solo para creación.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-133">Used for creation only.</span></span> <span data-ttu-id="b2cd9-134">Se produce un error en la llamada si la clase o la instancia ya existe.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-134">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="b2cd9-135"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="b2cd9-135"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>\*\*\*\*wbemChangeFlagUpdateOnly\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="b2cd9-136">Hace que esta llamada se actualice.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-136">Causes this call to update.</span></span> <span data-ttu-id="b2cd9-137">La clase o instancia debe existir para que la llamada sea correcta.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-137">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="b2cd9-138"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="b2cd9-138"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="b2cd9-139">Hace que la llamada se devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-139">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="b2cd9-140"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="b2cd9-140"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b2cd9-141">Hace que esta llamada se bloquee hasta que se complete la consulta.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-141">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="b2cd9-142"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="b2cd9-142"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b2cd9-143">Hace que WMI escriba datos de modificación de clases, así como la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-143">Causes WMI to write class amendment data as well as the base class definition.</span></span> <span data-ttu-id="b2cd9-144">Para obtener más información acerca de los calificadores modificados, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="b2cd9-144">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b2cd9-145">*objwbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b2cd9-145">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2cd9-146">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-146">Typically, this is undefined.</span></span> <span data-ttu-id="b2cd9-147">De lo contrario, se trata de un objeto [**SWbemObjectPath**](swbemobjectpath.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-147">Otherwise, this is an [**SWbemObjectPath**](swbemobjectpath.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="b2cd9-148">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-148">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2cd9-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2cd9-149">Return value</span></span>

<span data-ttu-id="b2cd9-150">Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="b2cd9-150">If the call is successful, an [**SWbemObjectPath**](swbemobjectpath.md) object is returned.</span></span> <span data-ttu-id="b2cd9-151">Este objeto contiene la ruta de acceso del objeto de la instancia o la clase que se ha confirmado correctamente en WMI.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-151">This object contains the object path of the instance or class that has been successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b2cd9-152">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b2cd9-152">Error codes</span></span>

<span data-ttu-id="b2cd9-153">Después de completar el método **Put \_** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-153">After the completion of the **Put\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b2cd9-154">**wbemErrAccessDenied** -2147749891</span><span class="sxs-lookup"><span data-stu-id="b2cd9-154">**wbemErrAccessDenied** - 2147749891</span></span>
</dt> <dd>

<span data-ttu-id="b2cd9-155">El usuario actual no tiene permiso para actualizar una instancia de la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-155">Current user does not have permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="b2cd9-156">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="b2cd9-156">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="b2cd9-157">Se especificó la marca **wbemChangeFlagCreateOnly** , pero la instancia ya existe.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-157">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b2cd9-158">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b2cd9-158">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b2cd9-159">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-159">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b2cd9-160">**wbemErrIllegalNull** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="b2cd9-160">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="b2cd9-161">Se especificó un valor de **Nothing** para una propiedad que no puede ser **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-161">A value of **Nothing** was specified for a property that may not be **Nothing**.</span></span> <span data-ttu-id="b2cd9-162">Un ejemplo de este tipo de propiedad está marcado por un calificador de **clave,** **indexado** o **no \_ null** .</span><span class="sxs-lookup"><span data-stu-id="b2cd9-162">An example of such a property is one marked by a **Key,** **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b2cd9-163">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="b2cd9-163">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="b2cd9-164">La instancia especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-164">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b2cd9-165">**wbemErrInvalidParameter** -0x80041008</span><span class="sxs-lookup"><span data-stu-id="b2cd9-165">**wbemErrInvalidParameter** - 0x80041008</span></span>
</dt> <dd>

<span data-ttu-id="b2cd9-166">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-166">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b2cd9-167">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="b2cd9-167">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="b2cd9-168">Se especificó la marca **wbemChangeFlagUpdateOnly** , pero la instancia o la clase no existen.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-168">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="b2cd9-169">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="b2cd9-169">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="b2cd9-170">No se han establecido todas las propiedades requeridas para las clases.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-170">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="b2cd9-171">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b2cd9-171">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b2cd9-172">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="b2cd9-172">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2cd9-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2cd9-173">Requirements</span></span>



| <span data-ttu-id="b2cd9-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2cd9-174">Requirement</span></span> | <span data-ttu-id="b2cd9-175">Value</span><span class="sxs-lookup"><span data-stu-id="b2cd9-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2cd9-176">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2cd9-176">Minimum supported client</span></span><br/> | <span data-ttu-id="b2cd9-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2cd9-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b2cd9-178">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2cd9-178">Minimum supported server</span></span><br/> | <span data-ttu-id="b2cd9-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2cd9-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b2cd9-180">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2cd9-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2cd9-181"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2cd9-181"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2cd9-182">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b2cd9-182">Type library</span></span><br/>             | <dl> <span data-ttu-id="b2cd9-183"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b2cd9-183"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b2cd9-184">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2cd9-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2cd9-185"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2cd9-185"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2cd9-186">CLSID</span><span class="sxs-lookup"><span data-stu-id="b2cd9-186">CLSID</span></span><br/>                    | <span data-ttu-id="b2cd9-187">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="b2cd9-187">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="b2cd9-188">IID</span><span class="sxs-lookup"><span data-stu-id="b2cd9-188">IID</span></span><br/>                      | <span data-ttu-id="b2cd9-189">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="b2cd9-189">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="b2cd9-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2cd9-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2cd9-191">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="b2cd9-191">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="b2cd9-192">**SWbemObjectPath. Class**</span><span class="sxs-lookup"><span data-stu-id="b2cd9-192">**SWbemObjectPath.Class**</span></span>](swbemobjectpath-class.md)
</dt> <dt>

[<span data-ttu-id="b2cd9-193">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="b2cd9-193">**SWbemProperty**</span></span>](swbemproperty.md)
</dt> <dt>

[<span data-ttu-id="b2cd9-194">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="b2cd9-194">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

