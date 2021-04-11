---
description: El \_ método PutAsync de SWbemObject crea o actualiza de forma asincrónica una instancia o un objeto de clase a instrumental de administración de Windows (WMI).
ms.assetid: ff738412-fcca-4e4a-a178-0d1d391ec99b
ms.tgt_platform: multiple
title: Método SWbemObject.PutAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.PutAsync_
- ISWbemObject.PutAsync_
- ISWbemObject.PutAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3530c3883763773f53bec81aeee8b0d199170133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279110"
---
# <a name="swbemobjectputasync_-method"></a><span data-ttu-id="b3393-103">SWbemObject. PutAsync, \_ método</span><span class="sxs-lookup"><span data-stu-id="b3393-103">SWbemObject.PutAsync\_ method</span></span>

<span data-ttu-id="b3393-104">El **método \_ PutAsync** de [**SWbemObject**](swbemobject.md) crea o actualiza de forma asincrónica una instancia o un objeto de clase a instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b3393-104">The **PutAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously creates or updates an instance or class object to Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="b3393-105">Puede usar este método después de modificar cualquier propiedad o método de **SWbemObject** y de que los cambios se escriban en WMI.</span><span class="sxs-lookup"><span data-stu-id="b3393-105">You can use this method after you modify any properties or methods in **SWbemObject**, and your changes are written to WMI.</span></span>

<span data-ttu-id="b3393-106">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b3393-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b3393-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3393-107">Syntax</span></span>


```VB
SWbemObject.PutAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b3393-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3393-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3393-109">*objWbemSink* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b3393-109">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3393-110">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b3393-110">Required.</span></span> <span data-ttu-id="b3393-111">Receptor de objeto que recibe de forma asincrónica el resultado de la operación **Put** .</span><span class="sxs-lookup"><span data-stu-id="b3393-111">Object sink that asynchronously receives the result of the **put** operation.</span></span>

</dd> <dt>

<span data-ttu-id="b3393-112">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b3393-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b3393-113">Determina si la llamada crea o actualiza la clase o instancia y si la llamada se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b3393-113">Determines if the call creates or updates the class or instance and if the call returns immediately.</span></span> <span data-ttu-id="b3393-114">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b3393-114">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="b3393-115"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="b3393-115"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>\*\*\*\*wbemChangeFlagUpdateCompatible\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b3393-116">Permite actualizar una clase si no hay clases derivadas y no hay ninguna instancia para esa clase.</span><span class="sxs-lookup"><span data-stu-id="b3393-116">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="b3393-117">También permite las actualizaciones en todos los casos si el cambio es solo para calificadores no importantes (por ejemplo, el calificador de **Descripción** ).</span><span class="sxs-lookup"><span data-stu-id="b3393-117">It also allows updates in all cases if the change is just to unimportant qualifiers (for example the **Description** qualifier).</span></span> <span data-ttu-id="b3393-118">Éste es el comportamiento predeterminado de esta llamada y se utiliza para la compatibilidad con versiones anteriores de WMI.</span><span class="sxs-lookup"><span data-stu-id="b3393-118">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="b3393-119">Si la clase tiene instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="b3393-119">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="b3393-120"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="b3393-120"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>\*\*\*\*wbemChangeFlagUpdateSafeMode\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="b3393-121">Permite actualizaciones de clases, incluso si hay clases secundarias, si el cambio no provoca conflictos con las clases secundarias.</span><span class="sxs-lookup"><span data-stu-id="b3393-121">Allows updates of classes, even if there are child classes, if the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="b3393-122">Puede usar esta marca al agregar una nueva propiedad a una clase base que no se mencionó anteriormente en ninguna de las clases secundarias.</span><span class="sxs-lookup"><span data-stu-id="b3393-122">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="b3393-123">Si la clase tiene instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="b3393-123">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="b3393-124"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode \* \* \* \* (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="b3393-124"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>\*\*\*\*WbemChangeFlagUpdateForceMode\*\*\*\* (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="b3393-125">Fuerza la actualización de las clases cuando existen clases secundarias en conflicto.</span><span class="sxs-lookup"><span data-stu-id="b3393-125">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="b3393-126">Por ejemplo, esta marca fuerza una actualización si se definió un calificador de clase en una clase secundaria y la clase base intenta agregar el mismo calificador en conflicto con el existente.</span><span class="sxs-lookup"><span data-stu-id="b3393-126">For example, this flag forces an update if a class qualifier was defined in a child class, and the base class attempts to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="b3393-127">En el modo de fuerza, este conflicto se resuelve eliminando el calificador en conflicto de la clase secundaria.</span><span class="sxs-lookup"><span data-stu-id="b3393-127">In force mode this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="b3393-128">Si la clase tiene instancias, se produce un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="b3393-128">If the class has instances the update fails.</span></span>

<span data-ttu-id="b3393-129">El uso del modo Force para actualizar una clase estática produce la eliminación de todas las instancias de esa clase.</span><span class="sxs-lookup"><span data-stu-id="b3393-129">Using force mode to update a static class results in the deletion of all instances of that class.</span></span> <span data-ttu-id="b3393-130">Una actualización forzada en una clase de proveedor no elimina las instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="b3393-130">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="b3393-131"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="b3393-131"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>\*\*\*\*wbemChangeFlagCreateOrUpdate\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b3393-132">Hace que se cree la clase o instancia si no existe o se sobrescribe si ya existe.</span><span class="sxs-lookup"><span data-stu-id="b3393-132">Causes the class or instance to be created if it does not exist or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="b3393-133"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly \* \* \* \* (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="b3393-133"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>\*\*\*\*wbemChangeFlagCreateOnly\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="b3393-134">Se usa solo para creación.</span><span class="sxs-lookup"><span data-stu-id="b3393-134">Used for creation only.</span></span> <span data-ttu-id="b3393-135">Se produce un error en la llamada si la clase o la instancia ya existe.</span><span class="sxs-lookup"><span data-stu-id="b3393-135">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="b3393-136"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="b3393-136"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>\*\*\*\*wbemChangeFlagUpdateOnly\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="b3393-137">Hace que esta llamada se actualice.</span><span class="sxs-lookup"><span data-stu-id="b3393-137">Causes this call to update.</span></span> <span data-ttu-id="b3393-138">La clase o instancia debe existir para que la llamada sea correcta.</span><span class="sxs-lookup"><span data-stu-id="b3393-138">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="b3393-139"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="b3393-139"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="b3393-140">Hace que la llamada se devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b3393-140">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="b3393-141"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="b3393-141"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b3393-142">Hace que esta llamada se bloquee hasta que se complete la consulta.</span><span class="sxs-lookup"><span data-stu-id="b3393-142">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="b3393-143"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="b3393-143"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="b3393-144">Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="b3393-144">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="b3393-145"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="b3393-145"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b3393-146">Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="b3393-146">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="b3393-147"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="b3393-147"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b3393-148">Hace que WMI escriba datos de modificación de clase junto con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="b3393-148">Causes WMI to write class amendment data along with the base class definition.</span></span> <span data-ttu-id="b3393-149">Para obtener más información acerca de los calificadores modificados, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="b3393-149">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b3393-150">*objWbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b3393-150">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b3393-151">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="b3393-151">Typically, this is undefined.</span></span> <span data-ttu-id="b3393-152">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b3393-152">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="b3393-153">Un proveedor que admite o requiere esta información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="b3393-153">A provider that supports or requires this information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="b3393-154">*objWbemAsyncContext* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b3393-154">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b3393-155">Se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que devuelve al receptor del objeto para identificar el origen de la llamada asincrónica original.</span><span class="sxs-lookup"><span data-stu-id="b3393-155">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="b3393-156">Utilice este parámetro si va a realizar varias llamadas asincrónicas mediante el mismo receptor de objetos.</span><span class="sxs-lookup"><span data-stu-id="b3393-156">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="b3393-157">Para usar este parámetro, cree un objeto **SWbemNamedValueSet** y use el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando.</span><span class="sxs-lookup"><span data-stu-id="b3393-157">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="b3393-158">Este objeto **SWbemNamedValueSet** se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="b3393-158">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="b3393-159">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b3393-159">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3393-160">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3393-160">Return value</span></span>

<span data-ttu-id="b3393-161">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b3393-161">This method does not return a value.</span></span> <span data-ttu-id="b3393-162">Si la llamada se realiza correctamente, el evento [**OnObjectPut**](swbemsink-onobjectput.md) del receptor del objeto proporcionado recibe un objeto [**SWbemObjectPath**](swbemobjectpath.md) , que contiene la ruta de acceso del objeto de la instancia o la clase que se confirma correctamente en WMI.</span><span class="sxs-lookup"><span data-stu-id="b3393-162">If the call is successful, the [**OnObjectPut**](swbemsink-onobjectput.md) event of the supplied object sink receives an [**SWbemObjectPath**](swbemobjectpath.md) object, containing the object path of the instance or class that is successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b3393-163">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b3393-163">Error codes</span></span>

<span data-ttu-id="b3393-164">Después de completar el método **PutAsync \_** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="b3393-164">After the completion of the **PutAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b3393-165">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b3393-165">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b3393-166">El usuario actual no tiene permiso para actualizar una instancia de la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="b3393-166">Current user does not have permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="b3393-167">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="b3393-167">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="b3393-168">Se especificó la marca **wbemChangeFlagCreateOnly** , pero la instancia ya existe.</span><span class="sxs-lookup"><span data-stu-id="b3393-168">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b3393-169">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b3393-169">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b3393-170">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="b3393-170">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b3393-171">**wbemErrIllegalNull** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="b3393-171">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="b3393-172">Se especificó un valor de **Nothing** para una propiedad que no puede ser **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="b3393-172">A value of **Nothing** was specified for a property that may not be **Nothing**.</span></span> <span data-ttu-id="b3393-173">Un ejemplo de este tipo de propiedad es uno marcado por un calificador de **clave**, **indexado** o **no \_ null** .</span><span class="sxs-lookup"><span data-stu-id="b3393-173">An example of such a property is one that is marked by a **Key**, **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b3393-174">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="b3393-174">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="b3393-175">La instancia especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="b3393-175">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b3393-176">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b3393-176">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b3393-177">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b3393-177">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b3393-178">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="b3393-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="b3393-179">Se especificó la marca **wbemChangeFlagUpdateOnly** , pero la instancia o la clase no existen.</span><span class="sxs-lookup"><span data-stu-id="b3393-179">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="b3393-180">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="b3393-180">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="b3393-181">No se han establecido todas las propiedades requeridas para las clases.</span><span class="sxs-lookup"><span data-stu-id="b3393-181">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="b3393-182">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b3393-182">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b3393-183">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="b3393-183">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3393-184">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3393-184">Remarks</span></span>

<span data-ttu-id="b3393-185">Esta llamada se devuelve inmediatamente y el resultado de la operación **Put** se devuelve al llamador a través de las devoluciones de llamada entregadas al receptor que se especifica en *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="b3393-185">This call returns immediately, and the result of the **put** operation is returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="b3393-186">Implemente el *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="b3393-186">Implement the *objWbemSink*.</span></span> <span data-ttu-id="b3393-187">Método [**OnObjectPut**](swbemsink-onobjectput.md) para obtener la ruta de acceso del objeto de la instancia o la clase que se escribe en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="b3393-187">[**OnObjectPut**](swbemsink-onobjectput.md) method to obtain the object path of the instance or class that is written to the WMI repository.</span></span> <span data-ttu-id="b3393-188">Para obtener más información acerca de los métodos de receptor, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b3393-188">For more information about sink methods, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="b3393-189">Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor.</span><span class="sxs-lookup"><span data-stu-id="b3393-189">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b3393-190">Esto supone riesgos de seguridad para los scripts y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b3393-190">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b3393-191">Para eliminar los riesgos, utilice la comunicación sincrónica o semisincrónica.</span><span class="sxs-lookup"><span data-stu-id="b3393-191">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="b3393-192">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b3393-192">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3393-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3393-193">Requirements</span></span>



| <span data-ttu-id="b3393-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3393-194">Requirement</span></span> | <span data-ttu-id="b3393-195">Value</span><span class="sxs-lookup"><span data-stu-id="b3393-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3393-196">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3393-196">Minimum supported client</span></span><br/> | <span data-ttu-id="b3393-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3393-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b3393-198">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3393-198">Minimum supported server</span></span><br/> | <span data-ttu-id="b3393-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3393-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b3393-200">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3393-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3393-201"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3393-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3393-202">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b3393-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="b3393-203"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b3393-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b3393-204">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b3393-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3393-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3393-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b3393-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="b3393-206">CLSID</span></span><br/>                    | <span data-ttu-id="b3393-207">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="b3393-207">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="b3393-208">IID</span><span class="sxs-lookup"><span data-stu-id="b3393-208">IID</span></span><br/>                      | <span data-ttu-id="b3393-209">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="b3393-209">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="b3393-210">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3393-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3393-211">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="b3393-211">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="b3393-212">**SWbemObjectPath. Class**</span><span class="sxs-lookup"><span data-stu-id="b3393-212">**SWbemObjectPath.Class**</span></span>](swbemobjectpath-class.md)
</dt> <dt>

[<span data-ttu-id="b3393-213">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="b3393-213">**SWbemProperty**</span></span>](swbemproperty.md)
</dt> <dt>

[<span data-ttu-id="b3393-214">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="b3393-214">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

