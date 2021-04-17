---
description: El método CompareTo \_ del objeto SWbemLastError compara dos objetos SWbemObject. Esta comparación está sujeta a determinadas restricciones en función de los valores especificados en el parámetro iFlags.
ms.assetid: 541510e4-ef8d-4436-966f-19c5df422281
ms.tgt_platform: multiple
title: Método SWbemLastError.CompareTo_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c24eb6e57e81c6c44922b2d6643be65198951ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715741"
---
# <a name="swbemlasterrorcompareto_-method"></a><span data-ttu-id="a09b6-104">SWbemLastError. CompareTo ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="a09b6-104">SWbemLastError.CompareTo\_ method</span></span>

<span data-ttu-id="a09b6-105">El método **CompareTo \_** del objeto [**SWbemLastError**](swbemlasterror.md) compara dos objetos [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="a09b6-105">The **CompareTo\_** method of the [**SWbemLastError**](swbemlasterror.md) object compares two [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="a09b6-106">Esta comparación está sujeta a determinadas restricciones en función de los valores especificados en el parámetro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="a09b6-106">This comparison is subject to certain constraints based on the values specified in the *iFlags* parameter.</span></span>

<span data-ttu-id="a09b6-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a09b6-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a09b6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a09b6-108">Syntax</span></span>


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a09b6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a09b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a09b6-110">*objwbemObject* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a09b6-110">*objwbemObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a09b6-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a09b6-111">Required.</span></span> <span data-ttu-id="a09b6-112">Objeto de la clase [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="a09b6-112">An [**SWbemObject**](swbemobject.md) class object.</span></span> <span data-ttu-id="a09b6-113">Este parámetro es el objeto con el que se compara el primer objeto.</span><span class="sxs-lookup"><span data-stu-id="a09b6-113">This parameter is the object with which the first object is compared.</span></span> <span data-ttu-id="a09b6-114">El objeto debe ser una instancia de **SWbemObject** válida.</span><span class="sxs-lookup"><span data-stu-id="a09b6-114">The object must be a valid **SWbemObject** instance.</span></span>

</dd> <dt>

<span data-ttu-id="a09b6-115">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a09b6-115">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a09b6-116">Entero que especifica las marcas adicionales para la operación.</span><span class="sxs-lookup"><span data-stu-id="a09b6-116">An integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="a09b6-117">Este parámetro especifica las características del objeto que se deben tener en cuenta al realizar comparaciones de objetos.</span><span class="sxs-lookup"><span data-stu-id="a09b6-117">This parameter specifies the object characteristics to consider when object comparisons are made.</span></span> <span data-ttu-id="a09b6-118">Puede usar **wbemComparisonFlagIncludeAll** para tener en cuenta todas las características (valor predeterminado) o cualquier combinación de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="a09b6-118">You can use **wbemComparisonFlagIncludeAll** to consider all features (default) or any combination of the following values.</span></span>

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span data-ttu-id="a09b6-119"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll \* \* \* \* (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="a09b6-119"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>\*\*\*\*wbemComparisonFlagIncludeAll\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="a09b6-120">Hace que se comparen todas las propiedades, calificadores y sabores.</span><span class="sxs-lookup"><span data-stu-id="a09b6-120">Causes all properties, qualifiers, and flavors to be compared.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span data-ttu-id="a09b6-121"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="a09b6-121"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>\*\*\*\*wbemComparisonFlagIgnoreQualifiers\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="a09b6-122">Hace que todos los calificadores (incluidos **key** y **Dynamic**) se omitan en la comparación.</span><span class="sxs-lookup"><span data-stu-id="a09b6-122">Causes all qualifiers (including **Key** and **Dynamic**) to be ignored in comparison.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span data-ttu-id="a09b6-123"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource \* \* \* \* (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="a09b6-123"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>\*\*\*\*wbemComparisonFlagIgnoreObjectSource\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="a09b6-124">Hace que el origen de los objetos, es decir, el servidor y el espacio de nombres del que proceden, se omitan en comparación con otros objetos.</span><span class="sxs-lookup"><span data-stu-id="a09b6-124">Causes the source of the objects, namely the server and the namespace they came from, to be ignored in comparison to other objects.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span data-ttu-id="a09b6-125"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues \* \* \* \* (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="a09b6-125"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>\*\*\*\*wbemComparisonFlagIgnoreDefaultValues\*\*\*\* (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="a09b6-126">Hace que se omitan los valores predeterminados de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="a09b6-126">Causes the default values of properties to be ignored.</span></span> <span data-ttu-id="a09b6-127">Esta marca solo es significativa cuando se comparan clases.</span><span class="sxs-lookup"><span data-stu-id="a09b6-127">This flag is only meaningful when comparing classes.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span data-ttu-id="a09b6-128"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass \* \* \* \* (8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="a09b6-128"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>\*\*\*\*wbemComparisonFlagIgnoreClass\*\*\*\* (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="a09b6-129">Indica al sistema que asuma que los objetos que se comparan son instancias de la misma clase.</span><span class="sxs-lookup"><span data-stu-id="a09b6-129">Instructs the system to assume that the objects being compared are instances of the same class.</span></span> <span data-ttu-id="a09b6-130">Por consiguiente, esta marca solo compara la información relacionada con la instancia.</span><span class="sxs-lookup"><span data-stu-id="a09b6-130">Consequently, this flag compares instance-related information only.</span></span> <span data-ttu-id="a09b6-131">Utilice este marcador para optimizar el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="a09b6-131">Use this flag to optimize performance.</span></span> <span data-ttu-id="a09b6-132">Si los objetos no son de la misma clase, los resultados no se definen.</span><span class="sxs-lookup"><span data-stu-id="a09b6-132">If the objects are not of the same class, the results are undefined.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span data-ttu-id="a09b6-133"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="a09b6-133"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>\*\*\*\*wbemComparisonFlagIgnoreCase\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="a09b6-134">Hace que los valores de cadena se comparen de manera que no distinga mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a09b6-134">Causes string values to be compared in a case-insensitive manner.</span></span> <span data-ttu-id="a09b6-135">Esto se aplica tanto a las cadenas como a los valores de calificador.</span><span class="sxs-lookup"><span data-stu-id="a09b6-135">This applies both to strings and to qualifier values.</span></span> <span data-ttu-id="a09b6-136">Los nombres de propiedades y calificadores siempre se comparan sin distinguir entre mayúsculas y minúsculas, se especifique o no este marcador.</span><span class="sxs-lookup"><span data-stu-id="a09b6-136">Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span data-ttu-id="a09b6-137"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="a09b6-137"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>\*\*\*\*wbemComparisonFlagIgnoreFlavor\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="a09b6-138">Hace que se omitan los tipos de calificador.</span><span class="sxs-lookup"><span data-stu-id="a09b6-138">Causes qualifier flavors to be ignored.</span></span> <span data-ttu-id="a09b6-139">Este marcador sigue tomando valores del calificador en una cuenta, pero omite las distinciones de modos tales como las reglas de propagación y las restricciones de reemplazamiento.</span><span class="sxs-lookup"><span data-stu-id="a09b6-139">This flag still takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a09b6-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a09b6-140">Return value</span></span>

<span data-ttu-id="a09b6-141">El método **CompareTo \_** devuelve el valor booleano **true** si los objetos coinciden; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="a09b6-141">The **CompareTo\_** method returns the Boolean value **TRUE** if the objects match; otherwise, it returns **FALSE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a09b6-142">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a09b6-142">Error codes</span></span>

<span data-ttu-id="a09b6-143">Tras completar el método **CompareTo \_** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="a09b6-143">Upon the completion of the **CompareTo\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a09b6-144">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a09b6-144">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a09b6-145">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="a09b6-145">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a09b6-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="a09b6-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a09b6-147">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="a09b6-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a09b6-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="a09b6-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a09b6-149">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="a09b6-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a09b6-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a09b6-150">Requirements</span></span>



| <span data-ttu-id="a09b6-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="a09b6-151">Requirement</span></span> | <span data-ttu-id="a09b6-152">Value</span><span class="sxs-lookup"><span data-stu-id="a09b6-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a09b6-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a09b6-153">Minimum supported client</span></span><br/> | <span data-ttu-id="a09b6-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a09b6-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a09b6-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a09b6-155">Minimum supported server</span></span><br/> | <span data-ttu-id="a09b6-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a09b6-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a09b6-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a09b6-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="a09b6-158"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a09b6-158"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a09b6-159">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a09b6-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="a09b6-160"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a09b6-160"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a09b6-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a09b6-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a09b6-162"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a09b6-162"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a09b6-163">CLSID</span><span class="sxs-lookup"><span data-stu-id="a09b6-163">CLSID</span></span><br/>                    | <span data-ttu-id="a09b6-164">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="a09b6-164">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="a09b6-165">IID</span><span class="sxs-lookup"><span data-stu-id="a09b6-165">IID</span></span><br/>                      | <span data-ttu-id="a09b6-166">\_ISWBEMLASTERROR IID</span><span class="sxs-lookup"><span data-stu-id="a09b6-166">IID\_ISWbemLastError</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="a09b6-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="a09b6-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a09b6-168">**SWbemLastError**</span><span class="sxs-lookup"><span data-stu-id="a09b6-168">**SWbemLastError**</span></span>](swbemlasterror.md)
</dt> <dt>

[<span data-ttu-id="a09b6-169">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="a09b6-169">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




