---
description: Devuelve un objeto SWbemObjectSet.
ms.assetid: cfe08956-7215-4e2e-a279-6e86f14e5c27
ms.tgt_platform: multiple
title: Método SWbemServices. subclasses (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e8c23dee5ee3f0a1cf5babe37d0ccb6aa0a3ac7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715711"
---
# <a name="swbemservicessubclassesof-method"></a><span data-ttu-id="fa553-103">SWbemServices. subclasses (método)</span><span class="sxs-lookup"><span data-stu-id="fa553-103">SWbemServices.SubclassesOf method</span></span>

<span data-ttu-id="fa553-104">El método **subclasses** del objeto [**SWbemServices**](swbemservices.md) devuelve un objeto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="fa553-104">The **SubclassesOf** method of the [**SWbemServices**](swbemservices.md) object returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="fa553-105">Este objeto es una colección de subclases de una clase especificada.</span><span class="sxs-lookup"><span data-stu-id="fa553-105">This object is a collection of subclasses of a specified class.</span></span> <span data-ttu-id="fa553-106">Los elementos de la colección devuelta se pueden obtener mediante métodos de colección estándar.</span><span class="sxs-lookup"><span data-stu-id="fa553-106">Items in the returned collection can be obtained using standard collection methods.</span></span> <span data-ttu-id="fa553-107">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="fa553-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="fa553-108">Este método solo funciona con objetos de clase.</span><span class="sxs-lookup"><span data-stu-id="fa553-108">This method only works for class objects.</span></span>

<span data-ttu-id="fa553-109">Se llama al método en el modo semisincrónico.</span><span class="sxs-lookup"><span data-stu-id="fa553-109">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="fa553-110">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="fa553-110">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="fa553-111">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="fa553-111">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa553-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa553-112">Syntax</span></span>


```VB
objWbemObjectSet = .SubclassesOf( _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="fa553-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa553-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa553-114">*strSuperclass* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="fa553-114">*strSuperclass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fa553-115">Especifica un nombre de clase principal.</span><span class="sxs-lookup"><span data-stu-id="fa553-115">Specifies a parent class name.</span></span> <span data-ttu-id="fa553-116">Solo las subclases de esta clase se devuelven en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="fa553-116">Only subclasses of this class return in the enumerator.</span></span> <span data-ttu-id="fa553-117">Si deja este parámetro en blanco y si *iFlags* es **wbemQueryFlagShallow**, solo se devuelven las clases de nivel superior (es decir, las clases que no tienen clase primaria).</span><span class="sxs-lookup"><span data-stu-id="fa553-117">If you leave this parameter blank, and if *iFlags* is **wbemQueryFlagShallow**, only the top-level classes are returned (that is, classes that have no parent class).</span></span> <span data-ttu-id="fa553-118">Si este parámetro está en blanco y *iFlags* es **wbemQueryFlagDeep** , se devuelven todas las clases del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="fa553-118">If this parameter is blank and *iFlags* is **wbemQueryFlagDeep** all classes within the namespace are returned.</span></span>

</dd> <dt>

<span data-ttu-id="fa553-119">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="fa553-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fa553-120">Determina la información detallada que enumera la llamada.</span><span class="sxs-lookup"><span data-stu-id="fa553-120">Determines how detailed the call enumerates.</span></span> <span data-ttu-id="fa553-121">Los valores predeterminados para este parámetro son **wbemFlagReturnImmediately** y **wbemQueryFlagDeep**.</span><span class="sxs-lookup"><span data-stu-id="fa553-121">The default values for this parameter are **wbemFlagReturnImmediately** and **wbemQueryFlagDeep**.</span></span> <span data-ttu-id="fa553-122">Este parámetro puede aceptar los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fa553-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="fa553-123"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="fa553-123"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="fa553-124">Fuerza a la enumeración a incluir solo las subclases inmediatas de la clase primaria especificada.</span><span class="sxs-lookup"><span data-stu-id="fa553-124">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="fa553-125"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="fa553-125"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="fa553-126">Valor predeterminado para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="fa553-126">Default for this parameter.</span></span> <span data-ttu-id="fa553-127">Este valor fuerza la enumeración recursiva en todas las subclases que se derivan de la clase primaria especificada.</span><span class="sxs-lookup"><span data-stu-id="fa553-127">This value forces recursive enumeration into all subclasses that are derived from the specified parent class.</span></span> <span data-ttu-id="fa553-128">La clase primaria no se devuelve en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="fa553-128">The parent class is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="fa553-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="fa553-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="fa553-130">Hace que la llamada se devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="fa553-130">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="fa553-131"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="fa553-131"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="fa553-132">Hace que esta llamada se bloquee hasta que se complete la llamada.</span><span class="sxs-lookup"><span data-stu-id="fa553-132">Causes this call to block until the call has completed.</span></span> <span data-ttu-id="fa553-133">Esta marca llama al método en el modo sincrónico.</span><span class="sxs-lookup"><span data-stu-id="fa553-133">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="fa553-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="fa553-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="fa553-135">Hace que WMI devuelva datos de modificación de clase con la definición de clase base.</span><span class="sxs-lookup"><span data-stu-id="fa553-135">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="fa553-136">Para obtener más información, consulte [localizar información de clase WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="fa553-136">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fa553-137">*objWbemNamedValueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="fa553-137">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fa553-138">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="fa553-138">Typically, this is undefined.</span></span> <span data-ttu-id="fa553-139">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fa553-139">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider servicing the request.</span></span> <span data-ttu-id="fa553-140">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="fa553-140">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa553-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa553-141">Return value</span></span>

<span data-ttu-id="fa553-142">Si el método se realiza correctamente, se devuelve un objeto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="fa553-142">If the method is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fa553-143">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="fa553-143">Error codes</span></span>

<span data-ttu-id="fa553-144">Después de completar el método **subclasses** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="fa553-144">After the completion of the **SubclassesOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="fa553-145">Una colección devuelta con cero elementos no es un error.</span><span class="sxs-lookup"><span data-stu-id="fa553-145">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="fa553-146">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="fa553-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="fa553-147">El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.</span><span class="sxs-lookup"><span data-stu-id="fa553-147">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="fa553-148">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="fa553-148">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="fa553-149">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="fa553-149">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="fa553-150">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="fa553-150">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="fa553-151">La clase especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="fa553-151">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="fa553-152">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="fa553-152">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="fa553-153">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="fa553-153">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="fa553-154">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="fa553-154">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="fa553-155">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="fa553-155">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="fa553-156">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fa553-156">Examples</span></span>

<span data-ttu-id="fa553-157">En el siguiente ejemplo de PowerShell se muestra cómo recuperar las subclases de una clase en un sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="fa553-157">The following PowerShell sample shows how to retrieve the subclasses of a class on a remote system.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="fa553-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa553-158">Requirements</span></span>



| <span data-ttu-id="fa553-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa553-159">Requirement</span></span> | <span data-ttu-id="fa553-160">Value</span><span class="sxs-lookup"><span data-stu-id="fa553-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa553-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa553-161">Minimum supported client</span></span><br/> | <span data-ttu-id="fa553-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa553-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa553-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa553-163">Minimum supported server</span></span><br/> | <span data-ttu-id="fa553-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa553-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa553-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa553-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa553-166"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa553-166"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa553-167">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fa553-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="fa553-168"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fa553-168"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fa553-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fa553-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa553-170"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa553-170"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fa553-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="fa553-171">CLSID</span></span><br/>                    | <span data-ttu-id="fa553-172">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="fa553-172">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="fa553-173">IID</span><span class="sxs-lookup"><span data-stu-id="fa553-173">IID</span></span><br/>                      | <span data-ttu-id="fa553-174">\_ISWBEMSERVICES IID</span><span class="sxs-lookup"><span data-stu-id="fa553-174">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="fa553-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa553-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa553-176">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="fa553-176">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="fa553-177">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="fa553-177">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




