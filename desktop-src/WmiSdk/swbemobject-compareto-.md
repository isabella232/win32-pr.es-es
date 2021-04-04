---
description: El método CompareTo \_ del objeto SWbemObject compara dos objetos SWbemObject. Esta comparación está sujeta a determinadas restricciones en función de los valores especificados en el parámetro iFlags.
ms.assetid: 38813551-2403-4def-ae57-2b17f72cd180
ms.tgt_platform: multiple
title: Método SWbemObject.CompareTo_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.CompareTo_
- ISWbemObject.CompareTo_
- ISWbemObject.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f77bf9db9ee864e136ba695051445e543b466e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812410"
---
# <a name="swbemobjectcompareto_-method"></a><span data-ttu-id="ccc15-104">SWbemObject. CompareTo ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="ccc15-104">SWbemObject.CompareTo\_ method</span></span>

<span data-ttu-id="ccc15-105">El método **CompareTo \_** del objeto [**SWbemObject**](swbemobject.md) compara dos objetos **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="ccc15-105">The **CompareTo\_** method of the [**SWbemObject**](swbemobject.md) object compares two **SWbemObject** objects.</span></span> <span data-ttu-id="ccc15-106">Esta comparación está sujeta a determinadas restricciones en función de los valores especificados en el parámetro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="ccc15-106">This comparison is subject to certain constraints based on the values specified in the *iFlags* parameter.</span></span>

<span data-ttu-id="ccc15-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ccc15-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ccc15-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ccc15-108">Syntax</span></span>


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ccc15-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ccc15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccc15-110">*objwbemObject* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ccc15-110">*objwbemObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc15-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ccc15-111">Required.</span></span> <span data-ttu-id="ccc15-112">Este parámetro es un objeto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="ccc15-112">This parameter is an [**SWbemObject**](swbemobject.md) object.</span></span> <span data-ttu-id="ccc15-113">Este es el objeto con el que se compara el primer objeto.</span><span class="sxs-lookup"><span data-stu-id="ccc15-113">This is the object with which the first object is compared.</span></span> <span data-ttu-id="ccc15-114">El objeto debe ser una instancia de **SWbemObject** válida.</span><span class="sxs-lookup"><span data-stu-id="ccc15-114">The object must be a valid **SWbemObject** instance.</span></span>

</dd> <dt>

<span data-ttu-id="ccc15-115">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ccc15-115">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc15-116">Especifica las características del objeto que se deben tener en cuenta al comparar un objeto con otros objetos.</span><span class="sxs-lookup"><span data-stu-id="ccc15-116">Specifies the object characteristics to consider when comparing an object with other objects.</span></span> <span data-ttu-id="ccc15-117">Puede usar **wbemComparisonFlagIncludeAll** para tener en cuenta todas las características (este es el valor predeterminado) o cualquier combinación de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="ccc15-117">You can use **wbemComparisonFlagIncludeAll** to consider all features (this is the default), or any combination of the following values.</span></span>

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span data-ttu-id="ccc15-118"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="ccc15-118"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>\*\*\*\*wbemComparisonFlagIncludeAll\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="ccc15-119">Compara todas las propiedades, calificadores y tipos.</span><span class="sxs-lookup"><span data-stu-id="ccc15-119">Compares all properties, qualifiers, and flavors.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span data-ttu-id="ccc15-120"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource \* \* \* \* (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="ccc15-120"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>\*\*\*\*wbemComparisonFlagIgnoreObjectSource\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="ccc15-121">Hace que el origen de los objetos, es decir, el servidor y el espacio de nombres del que proceden, se omitan en comparación con otros objetos.</span><span class="sxs-lookup"><span data-stu-id="ccc15-121">Causes the source of the objects, namely the server and the namespace they came from, to be ignored in comparison to other objects.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span data-ttu-id="ccc15-122"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="ccc15-122"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>\*\*\*\*wbemComparisonFlagIgnoreQualifiers\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="ccc15-123">Hace que todos los calificadores (incluidos **key** y **Dynamic**) se omitan en la comparación.</span><span class="sxs-lookup"><span data-stu-id="ccc15-123">Causes all qualifiers (including **Key** and **Dynamic**) to be ignored in comparison.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span data-ttu-id="ccc15-124"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues \* \* \* \* (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="ccc15-124"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>\*\*\*\*wbemComparisonFlagIgnoreDefaultValues\*\*\*\* (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="ccc15-125">Hace que se omitan los valores predeterminados de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="ccc15-125">Causes default values of properties to be ignored.</span></span> <span data-ttu-id="ccc15-126">Esta marca solo es significativa cuando se comparan clases.</span><span class="sxs-lookup"><span data-stu-id="ccc15-126">This flag is only meaningful when comparing classes.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span data-ttu-id="ccc15-127"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="ccc15-127"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>\*\*\*\*wbemComparisonFlagIgnoreFlavor\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="ccc15-128">Hace que se omitan los tipos de calificador.</span><span class="sxs-lookup"><span data-stu-id="ccc15-128">Causes qualifier flavors to be ignored.</span></span> <span data-ttu-id="ccc15-129">Esta marca tiene en cuenta los valores del calificador, pero omite las distinciones de sabor, como las reglas de propagación y las restricciones de invalidación.</span><span class="sxs-lookup"><span data-stu-id="ccc15-129">This flag takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span data-ttu-id="ccc15-130"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="ccc15-130"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>\*\*\*\*wbemComparisonFlagIgnoreCase\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="ccc15-131">Compara los valores de cadena sin distinguir entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ccc15-131">Compares string values in a case-insensitive manner.</span></span> <span data-ttu-id="ccc15-132">Esto se aplica tanto a las cadenas como a los valores de calificador.</span><span class="sxs-lookup"><span data-stu-id="ccc15-132">This applies both to strings and to qualifier values.</span></span> <span data-ttu-id="ccc15-133">Los nombres de propiedades y calificadores siempre se comparan sin distinguir entre mayúsculas y minúsculas, se especifique o no este marcador.</span><span class="sxs-lookup"><span data-stu-id="ccc15-133">Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span data-ttu-id="ccc15-134"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass \* \* \* \* (8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="ccc15-134"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>\*\*\*\*wbemComparisonFlagIgnoreClass\*\*\*\* (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="ccc15-135">Indica al sistema que asuma que los objetos que se comparan son instancias de la misma clase.</span><span class="sxs-lookup"><span data-stu-id="ccc15-135">Instructs the system to assume that the objects being compared are instances of the same class.</span></span> <span data-ttu-id="ccc15-136">Por consiguiente, esta marca solo compara la información relacionada con la instancia.</span><span class="sxs-lookup"><span data-stu-id="ccc15-136">Consequently, this flag compares instance-related information only.</span></span> <span data-ttu-id="ccc15-137">Utilice este marcador para optimizar el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="ccc15-137">Use this flag to optimize performance.</span></span> <span data-ttu-id="ccc15-138">Si los objetos no son de la misma clase, los resultados no se definen.</span><span class="sxs-lookup"><span data-stu-id="ccc15-138">If the objects are not of the same class, the results are undefined.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccc15-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ccc15-139">Return value</span></span>

<span data-ttu-id="ccc15-140">Este método devuelve el valor booleano **true** si los objetos coinciden.</span><span class="sxs-lookup"><span data-stu-id="ccc15-140">This method returns the Boolean value of **TRUE** if the objects match.</span></span> <span data-ttu-id="ccc15-141">Devuelve **false** si los objetos no coinciden.</span><span class="sxs-lookup"><span data-stu-id="ccc15-141">It returns **FALSE** if the objects do not match.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ccc15-142">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ccc15-142">Error codes</span></span>

<span data-ttu-id="ccc15-143">Después de completar el método **CompareTo \_** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="ccc15-143">After the completion of the **CompareTo\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ccc15-144">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ccc15-144">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ccc15-145">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="ccc15-145">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ccc15-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ccc15-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ccc15-147">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="ccc15-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ccc15-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ccc15-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ccc15-149">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="ccc15-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ccc15-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccc15-150">Requirements</span></span>



| <span data-ttu-id="ccc15-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccc15-151">Requirement</span></span> | <span data-ttu-id="ccc15-152">Value</span><span class="sxs-lookup"><span data-stu-id="ccc15-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc15-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccc15-153">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc15-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccc15-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ccc15-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccc15-155">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc15-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccc15-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ccc15-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ccc15-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccc15-158"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccc15-158"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccc15-159">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ccc15-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="ccc15-160"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ccc15-160"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ccc15-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ccc15-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccc15-162"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccc15-162"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ccc15-163">CLSID</span><span class="sxs-lookup"><span data-stu-id="ccc15-163">CLSID</span></span><br/>                    | <span data-ttu-id="ccc15-164">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="ccc15-164">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="ccc15-165">IID</span><span class="sxs-lookup"><span data-stu-id="ccc15-165">IID</span></span><br/>                      | <span data-ttu-id="ccc15-166">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="ccc15-166">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="ccc15-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccc15-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc15-168">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="ccc15-168">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




