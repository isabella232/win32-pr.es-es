---
description: Guarda un objeto de forma asincrónica en un espacio de nombres. Cuando se realiza correctamente, este método envía un evento alcompleto al objeto SWbemSink que se especifica como parámetro de entrada.
ms.assetid: 27da0c60-6dae-482d-a9bf-1aab016d3ae8
ms.tgt_platform: multiple
title: Método SWbemServicesEx. PutAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 06f470ed6f8cbd497ba3d3a3a77c5a8b4e5748c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082974"
---
# <a name="swbemservicesexputasync-method"></a><span data-ttu-id="58f6f-104">SWbemServicesEx. PutAsync, método</span><span class="sxs-lookup"><span data-stu-id="58f6f-104">SWbemServicesEx.PutAsync method</span></span>

<span data-ttu-id="58f6f-105">El método **PutAsync** del objeto [**SWbemServicesEx**](swbemservicesex.md) guarda un objeto de forma asincrónica en un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="58f6f-105">The **PutAsync** method of the [**SWbemServicesEx**](swbemservicesex.md) object saves an object asynchronously to a namespace.</span></span> <span data-ttu-id="58f6f-106">Cuando se realiza correctamente, este método envía un evento [**alcompleto**](swbemsink-oncompleted.md) al objeto [**SWbemSink**](swbemsink.md) que se especifica como parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="58f6f-106">When successful, this method sends an [**OnCompleted**](swbemsink-oncompleted.md) event to the [**SWbemSink**](swbemsink.md) object that is specified as an input parameter.</span></span>

<span data-ttu-id="58f6f-107">Se llama a este método en el modo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="58f6f-107">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="58f6f-108">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="58f6f-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="58f6f-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="58f6f-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="58f6f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58f6f-110">Syntax</span></span>


```VB
SWbemServicesEx.PutAsync( _
  ByVal objWbemSink, _
  ByVal ojbWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="58f6f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58f6f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58f6f-112">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="58f6f-112">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="58f6f-113">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="58f6f-113">Required.</span></span> <span data-ttu-id="58f6f-114">Receptor de objeto que recibe los objetos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="58f6f-114">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="58f6f-115">Cree un objeto [**SWbemSink**](swbemsink.md) para recibir los objetos.</span><span class="sxs-lookup"><span data-stu-id="58f6f-115">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="58f6f-116">*ojbWbemObject*</span><span class="sxs-lookup"><span data-stu-id="58f6f-116">*ojbWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="58f6f-117">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="58f6f-117">Required.</span></span> <span data-ttu-id="58f6f-118">Nuevo objeto que se va a colocar en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="58f6f-118">The new object to be put in the namespace.</span></span> <span data-ttu-id="58f6f-119">Puede tratarse de un objeto recién creado o de un objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="58f6f-119">This may be a newly created object or a modified object.</span></span>

</dd> <dt>

<span data-ttu-id="58f6f-120">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="58f6f-120">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58f6f-121">Este parámetro determina si la llamada crea o actualiza el objeto y si la llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="58f6f-121">This parameter determines whether the call creates or updates the object and whether the call returns immediately.</span></span> <span data-ttu-id="58f6f-122">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="58f6f-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="58f6f-123"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="58f6f-123"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="58f6f-124">Permite actualizar una clase cuando no hay clases derivadas ni instancias para la clase.</span><span class="sxs-lookup"><span data-stu-id="58f6f-124">Allows a class to be updated when there are no derived classes and no instances for the class.</span></span> <span data-ttu-id="58f6f-125">También permite las actualizaciones en todos los casos en los que el cambio solo es a calificadores no importantes, por ejemplo, el calificador de **Descripción** .</span><span class="sxs-lookup"><span data-stu-id="58f6f-125">It also allows updates in all cases when the change is only to unimportant qualifiers, for example, the **Description** qualifier.</span></span> <span data-ttu-id="58f6f-126">Éste es el comportamiento predeterminado de esta llamada y se utiliza para la compatibilidad con versiones anteriores de WMI.</span><span class="sxs-lookup"><span data-stu-id="58f6f-126">This is the default behavior for this call, and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="58f6f-127">Si la clase tiene instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="58f6f-127">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="58f6f-128"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="58f6f-128"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="58f6f-129">Permite actualizaciones de clases incluso cuando hay clases secundarias y el cambio no provoca conflictos con las clases secundarias.</span><span class="sxs-lookup"><span data-stu-id="58f6f-129">Allows updates of classes even when there are child classes and the change does not cause conflicts with the child classes.</span></span> <span data-ttu-id="58f6f-130">Utilice esta marca al agregar una nueva propiedad a una clase base que no se menciona previamente en ninguna de las clases secundarias.</span><span class="sxs-lookup"><span data-stu-id="58f6f-130">Use this flag when adding a new property to a base class that is not mentioned previously in any of the child classes.</span></span> <span data-ttu-id="58f6f-131">Si la clase tiene instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="58f6f-131">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="58f6f-132"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="58f6f-132"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="58f6f-133">Esta marca fuerza las actualizaciones de clases cuando existen clases secundarias en conflicto.</span><span class="sxs-lookup"><span data-stu-id="58f6f-133">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="58f6f-134">Por ejemplo, esta marca fuerza una actualización cuando se define un calificador de clase en una clase secundaria y la clase base intenta agregar el mismo calificador en conflicto con el existente.</span><span class="sxs-lookup"><span data-stu-id="58f6f-134">For example, this flag forces an update when a class qualifier is defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="58f6f-135">En el modo Force, este conflicto se resuelve eliminando el calificador en conflicto de la clase secundaria.</span><span class="sxs-lookup"><span data-stu-id="58f6f-135">In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="58f6f-136">Si la clase tiene instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="58f6f-136">If the class has instances, the update fails.</span></span>

<span data-ttu-id="58f6f-137">El uso del modo Force para actualizar una clase estática provoca la eliminación de todas las instancias de esa clase.</span><span class="sxs-lookup"><span data-stu-id="58f6f-137">The use of the force mode to update a static class causes the deletion of all instances of that class.</span></span> <span data-ttu-id="58f6f-138">Una actualización forzada en una clase de proveedor no elimina las instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="58f6f-138">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="58f6f-139"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="58f6f-139"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="58f6f-140">Hace que se cree la clase o instancia si no existe o se sobrescribe si ya existe.</span><span class="sxs-lookup"><span data-stu-id="58f6f-140">Causes the class or instance to be created if it does not exist, or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="58f6f-141"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="58f6f-141"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="58f6f-142">Se usa solo para creación.</span><span class="sxs-lookup"><span data-stu-id="58f6f-142">Used for creation only.</span></span> <span data-ttu-id="58f6f-143">Se produce un error en la llamada si la clase o la instancia ya existe.</span><span class="sxs-lookup"><span data-stu-id="58f6f-143">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="58f6f-144"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="58f6f-144"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="58f6f-145">Hace que esta llamada se actualice.</span><span class="sxs-lookup"><span data-stu-id="58f6f-145">Causes this call to update.</span></span> <span data-ttu-id="58f6f-146">La clase o instancia debe existir para que la llamada sea correcta.</span><span class="sxs-lookup"><span data-stu-id="58f6f-146">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="58f6f-147"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="58f6f-147"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="58f6f-148">Hace que la llamada se devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="58f6f-148">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="58f6f-149"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="58f6f-149"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="58f6f-150">Hace que esta llamada se bloquee hasta que se complete la consulta.</span><span class="sxs-lookup"><span data-stu-id="58f6f-150">Causes this call to block until the query is complete.</span></span> <span data-ttu-id="58f6f-151">Esta marca llama al método en el modo sincrónico.</span><span class="sxs-lookup"><span data-stu-id="58f6f-151">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="58f6f-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="58f6f-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="58f6f-153">Hace que WMI escriba los datos de modificación de clase y la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="58f6f-153">Causes WMI to write class amendment data and the base class definition.</span></span> <span data-ttu-id="58f6f-154">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="58f6f-154">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="58f6f-155">*objWbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="58f6f-155">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58f6f-156">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="58f6f-156">Typically, this is undefined.</span></span> <span data-ttu-id="58f6f-157">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que presta servicio a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="58f6f-157">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="58f6f-158">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="58f6f-158">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="58f6f-159">*objWbemAsyncContext* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="58f6f-159">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58f6f-160">Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="58f6f-160">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="58f6f-161">Use este parámetro para realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="58f6f-161">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="58f6f-162">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="58f6f-162">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="58f6f-163">Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="58f6f-163">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="58f6f-164">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="58f6f-164">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58f6f-165">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58f6f-165">Return value</span></span>

<span data-ttu-id="58f6f-166">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="58f6f-166">This method does not return a value.</span></span> <span data-ttu-id="58f6f-167">Si la llamada se realiza correctamente, el evento [**OnObjectPut**](swbemsink-onobjectput.md) del receptor del objeto proporcionado recibe un objeto [**SWbemObjectPath**](swbemobjectpath.md) , que contiene la ruta de acceso del objeto de la instancia o la clase que se confirma correctamente en WMI.</span><span class="sxs-lookup"><span data-stu-id="58f6f-167">If the call is successful, the [**OnObjectPut**](swbemsink-onobjectput.md) event of the supplied object sink receives an [**SWbemObjectPath**](swbemobjectpath.md) object, which contains the object path of the instance or class that is successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="58f6f-168">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="58f6f-168">Error codes</span></span>

<span data-ttu-id="58f6f-169">Después de completar el método **PutAsync** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="58f6f-169">After the completion of the **PutAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="58f6f-170">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="58f6f-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="58f6f-171">El usuario actual no tiene permiso para actualizar una instancia de la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="58f6f-171">Current user does not have the permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="58f6f-172">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="58f6f-172">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="58f6f-173">Se especificó la marca **wbemChangeFlagCreateOnly** , pero la instancia ya existe.</span><span class="sxs-lookup"><span data-stu-id="58f6f-173">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="58f6f-174">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="58f6f-174">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="58f6f-175">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="58f6f-175">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="58f6f-176">**wbemErrIllegalNull** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="58f6f-176">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="58f6f-177">Se especificó un valor null para una propiedad que no puede ser null.</span><span class="sxs-lookup"><span data-stu-id="58f6f-177">A value of Null was specified for a property that cannot be Null.</span></span> <span data-ttu-id="58f6f-178">Un ejemplo de este tipo de propiedad está marcado por un calificador de **clave**, **indexado** o **no \_ null** .</span><span class="sxs-lookup"><span data-stu-id="58f6f-178">An example of such a property is one marked by a **Key**, **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="58f6f-179">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="58f6f-179">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="58f6f-180">La instancia especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="58f6f-180">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="58f6f-181">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="58f6f-181">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="58f6f-182">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="58f6f-182">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="58f6f-183">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="58f6f-183">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="58f6f-184">Se especificó la marca **wbemChangeFlagUpdateOnly** , pero la instancia o la clase no existen.</span><span class="sxs-lookup"><span data-stu-id="58f6f-184">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="58f6f-185">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="58f6f-185">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="58f6f-186">No se han establecido todas las propiedades requeridas para las clases.</span><span class="sxs-lookup"><span data-stu-id="58f6f-186">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="58f6f-187">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="58f6f-187">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="58f6f-188">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="58f6f-188">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58f6f-189">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58f6f-189">Remarks</span></span>

<span data-ttu-id="58f6f-190">Esta llamada se devuelve inmediatamente, y los resultados y el estado se devuelven al autor de la llamada a través de los eventos entregados al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="58f6f-190">This call returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="58f6f-191">Para controlar cada objeto cuando llega, cree un *objWbemSink*. Subrutina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="58f6f-191">To handle each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="58f6f-192">Cualquier procesamiento realizado después de que lleguen todos los objetos se realiza en una subrutina de *objWbemSink*. Evento [**Alcompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="58f6f-192">Any processing done after all the objects arrive is done in a subroutine for the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="58f6f-193">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="58f6f-193">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="58f6f-194">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="58f6f-194">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="58f6f-195">Para eliminar los riesgos, consulte [configuración de la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="58f6f-195">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58f6f-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58f6f-196">Requirements</span></span>



| <span data-ttu-id="58f6f-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="58f6f-197">Requirement</span></span> | <span data-ttu-id="58f6f-198">Value</span><span class="sxs-lookup"><span data-stu-id="58f6f-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58f6f-199">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58f6f-199">Minimum supported client</span></span><br/> | <span data-ttu-id="58f6f-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58f6f-200">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58f6f-201">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58f6f-201">Minimum supported server</span></span><br/> | <span data-ttu-id="58f6f-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58f6f-202">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58f6f-203">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58f6f-203">Header</span></span><br/>                   | <dl> <span data-ttu-id="58f6f-204"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="58f6f-204"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="58f6f-205">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="58f6f-205">Type library</span></span><br/>             | <dl> <span data-ttu-id="58f6f-206"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="58f6f-206"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="58f6f-207">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="58f6f-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58f6f-208"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58f6f-208"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="58f6f-209">CLSID</span><span class="sxs-lookup"><span data-stu-id="58f6f-209">CLSID</span></span><br/>                    | <span data-ttu-id="58f6f-210">CLSID \_ ISWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="58f6f-210">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="58f6f-211">IID</span><span class="sxs-lookup"><span data-stu-id="58f6f-211">IID</span></span><br/>                      | <span data-ttu-id="58f6f-212">\_ISWBEMSERVICESEX IID</span><span class="sxs-lookup"><span data-stu-id="58f6f-212">IID\_ISWbemServicesEx</span></span><br/>                                                        |



 

