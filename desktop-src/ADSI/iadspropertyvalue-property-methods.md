---
title: Métodos de la propiedad IADsPropertyValue (iAds. h)
description: Los métodos de propiedad de la interfaz IADsPropertyValue proporcionan acceso a las propiedades que se describen en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 1039d4a9-bef8-457d-9a32-3743c14adef1
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsPropertyValue ADSI
topic_type:
- apiref
api_name:
- IADsPropertyValue Property Methods
- IADsPropertyValue.ADsType
- IADsPropertyValue.get_ADsType
- IADsPropertyValue.put_ADsType
- IADsPropertyValue.DNString
- IADsPropertyValue.get_DNString
- IADsPropertyValue.put_DNString
- IADsPropertyValue.CaseExactString
- IADsPropertyValue.get_CaseExactString
- IADsPropertyValue.put_CaseExactString
- IADsPropertyValue.CaseIgnoreString
- IADsPropertyValue.get_CaseIgnoreString
- IADsPropertyValue.put_CaseIgnoreString
- IADsPropertyValue.PrintableString
- IADsPropertyValue.get_PrintableString
- IADsPropertyValue.put_PrintableString
- IADsPropertyValue.NumericString
- IADsPropertyValue.get_NumericString
- IADsPropertyValue.put_NumericString
- IADsPropertyValue.Boolean
- IADsPropertyValue.get_Boolean
- IADsPropertyValue.put_Boolean
- IADsPropertyValue.Integer
- IADsPropertyValue.get_Integer
- IADsPropertyValue.put_Integer
- IADsPropertyValue.OctetString
- IADsPropertyValue.get_OctetString
- IADsPropertyValue.put_OctetString
- IADsPropertyValue.SecurityDescriptor
- IADsPropertyValue.get_SecurityDescriptor
- IADsPropertyValue.put_SecurityDescriptor
- IADsPropertyValue.LargeInteger
- IADsPropertyValue.get_LargeInteger
- IADsPropertyValue.put_LargeInteger
- IADsPropertyValue.UTCTime
- IADsPropertyValue.get_UTCTime
- IADsPropertyValue.put_UTCTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196e8097e5beaa5350738971be29de89b43c17a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490246"
---
# <a name="iadspropertyvalue-property-methods"></a><span data-ttu-id="0872d-105">Métodos de propiedad IADsPropertyValue</span><span class="sxs-lookup"><span data-stu-id="0872d-105">IADsPropertyValue Property Methods</span></span>

<span data-ttu-id="0872d-106">Los métodos de propiedad de la interfaz [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) proporcionan acceso a las propiedades que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="0872d-106">The property methods of the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interface provide access to the properties described in the following table.</span></span> <span data-ttu-id="0872d-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="0872d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="0872d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0872d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="0872d-109">**ADsType**</span><span class="sxs-lookup"><span data-stu-id="0872d-109">**ADsType**</span></span>
<span data-ttu-id="0872d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0872d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="0872d-111">El tipo de datos del valor de la propiedad, tomado de la enumeración [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) , de la propiedad Value.</span><span class="sxs-lookup"><span data-stu-id="0872d-111">The data type of the value of the property, taken from the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration, of the value property.</span></span>

<dt>

<span data-ttu-id="0872d-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0872d-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0872d-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="0872d-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* ADsType
);
HRESULT put_ADsType(
  [in] LONG ADsType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0872d-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0872d-114">**Boolean**</span></span>
<span data-ttu-id="0872d-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0872d-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="0872d-116">Valor booleano.</span><span class="sxs-lookup"><span data-stu-id="0872d-116">Boolean value.</span></span>

<dt>

<span data-ttu-id="0872d-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0872d-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0872d-118">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="0872d-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Boolean(
  [out] LONG* lnBoolean
);
HRESULT put_Boolean(
  [in] LONG lnBoolean
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0872d-119">**CaseExactString**</span><span class="sxs-lookup"><span data-stu-id="0872d-119">**CaseExactString**</span></span>
<span data-ttu-id="0872d-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0872d-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="0872d-121">Cadena que se va a interpretar.</span><span class="sxs-lookup"><span data-stu-id="0872d-121">String to be interpreted.</span></span> <span data-ttu-id="0872d-122">Distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0872d-122">Case-sensitive.</span></span>

<dt>

<span data-ttu-id="0872d-123">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0872d-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0872d-124">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0872d-124">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseExactString(
  [out] BSTR* bstrCaseExactString
);
HRESULT put_CaseExactString(
  [in] BSTR bstrCaseExactString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0872d-125">**CaseIgnoreString**</span><span class="sxs-lookup"><span data-stu-id="0872d-125">**CaseIgnoreString**</span></span>
<span data-ttu-id="0872d-126"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0872d-126"></dt> <dd> <dl></span></span>

<span data-ttu-id="0872d-127">Cadena que se va a interpretar.</span><span class="sxs-lookup"><span data-stu-id="0872d-127">String to be interpreted.</span></span> <span data-ttu-id="0872d-128">No hay distinción de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0872d-128">Case insensitive.</span></span>

<dt>

<span data-ttu-id="0872d-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0872d-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0872d-130">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0872d-130">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreString(
  [out] BSTR* bstrCaseIgnoreString
);
HRESULT put_CaseIgnoreString(
  [in] BSTR bstrCaseIgnoreString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0872d-131">**DNString**</span><span class="sxs-lookup"><span data-stu-id="0872d-131">**DNString**</span></span>
<span data-ttu-id="0872d-132"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0872d-132"></dt> <dd> <dl></span></span>

<span data-ttu-id="0872d-133">Cadena que identifica el nombre distintivo (ruta de acceso) de un objeto de valor de servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="0872d-133">String that identifies the distinguished name (path) of a directory service value object.</span></span>

<dt>

<span data-ttu-id="0872d-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0872d-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0872d-135">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0872d-135">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* bstrDNString
);
HRESULT put_DNString(
  [in] BSTR bstrDNString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0872d-136">**Entero**</span><span class="sxs-lookup"><span data-stu-id="0872d-136">**Integer**</span></span>
<span data-ttu-id="0872d-137"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0872d-137"></dt> <dd> <dl></span></span>

<span data-ttu-id="0872d-138">Valor entero.</span><span class="sxs-lookup"><span data-stu-id="0872d-138">Integer value.</span></span>

<dt>

<span data-ttu-id="0872d-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0872d-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0872d-140">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="0872d-140">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Integer(
  [out] LONG* lnInteger
);
HRESULT put_Integer(
  [in] LONG lnInteger
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0872d-141">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="0872d-141">**LargeInteger**</span></span>
<span data-ttu-id="0872d-142"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0872d-142"></dt> <dd> <dl></span></span>

<span data-ttu-id="0872d-143">Puntero a la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) del objeto que implementa [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) para este valor.</span><span class="sxs-lookup"><span data-stu-id="0872d-143">Pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface of the object implementing [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) for this value.</span></span>

<dt>

<span data-ttu-id="0872d-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0872d-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0872d-145">Tipo de datos de scripting: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="0872d-145">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LargeInteger(
  [out] IDispatch** ppLargeInteger
);
HRESULT put_LargeInteger(
  [in] IDispatch* pLargeInteger
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0872d-146">**NumericString**</span><span class="sxs-lookup"><span data-stu-id="0872d-146">**NumericString**</span></span>
<span data-ttu-id="0872d-147"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0872d-147"></dt> <dd> <dl></span></span>

<span data-ttu-id="0872d-148">Texto que se va a interpretar.</span><span class="sxs-lookup"><span data-stu-id="0872d-148">Text to be interpreted.</span></span> <span data-ttu-id="0872d-149">Tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="0872d-149">Numeric type.</span></span>

<dt>

<span data-ttu-id="0872d-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0872d-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0872d-151">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0872d-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NumericString(
  [out] BSTR* bstrNumericString
);
HRESULT put_NumericString(
  [in] BSTR bstrNumericString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0872d-152">**OctetString**</span><span class="sxs-lookup"><span data-stu-id="0872d-152">**OctetString**</span></span>
<span data-ttu-id="0872d-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0872d-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="0872d-154">Matriz Variant de caracteres de un byte.</span><span class="sxs-lookup"><span data-stu-id="0872d-154">Variant array of one-byte characters.</span></span>

<dt>

<span data-ttu-id="0872d-155">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0872d-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0872d-156">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="0872d-156">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetString(
  [in] VARIANT* vOctetString
);
HRESULT put_OctetString(
  [in] VARIANT* vOctetString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0872d-157">**PrintableString**</span><span class="sxs-lookup"><span data-stu-id="0872d-157">**PrintableString**</span></span>
<span data-ttu-id="0872d-158"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0872d-158"></dt> <dd> <dl></span></span>

<span data-ttu-id="0872d-159">Mostrar o imprimir cadena.</span><span class="sxs-lookup"><span data-stu-id="0872d-159">Display or print string.</span></span>

<dt>

<span data-ttu-id="0872d-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0872d-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0872d-161">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0872d-161">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintableString(
  [out] BSTR* bstrPrintableString
);
HRESULT put_PrintableString(
  [in] BSTR bstrPrintableString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0872d-162">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0872d-162">**SecurityDescriptor**</span></span>
<span data-ttu-id="0872d-163"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0872d-163"></dt> <dd> <dl></span></span>

<span data-ttu-id="0872d-164">Puntero a la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) del objeto que implementa [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) para este valor.</span><span class="sxs-lookup"><span data-stu-id="0872d-164">Pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface of the object implementing [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) for this value.</span></span>

<dt>

<span data-ttu-id="0872d-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0872d-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0872d-166">Tipo de datos de scripting: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="0872d-166">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SecurityDescriptor(
  [out] IDispatch** ppSecurityDescriptor
);
HRESULT put_SecurityDescriptor(
  [in] IDispatch* pSecurityDescriptor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0872d-167">**UTCTime**</span><span class="sxs-lookup"><span data-stu-id="0872d-167">**UTCTime**</span></span>
<span data-ttu-id="0872d-168"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0872d-168"></dt> <dd> <dl></span></span>

<span data-ttu-id="0872d-169">Fecha del tipo de **\_ datos VT** expresado en formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="0872d-169">A date of the **VT\_DATE** type expressed in Coordinated Universal Time (UTC) format.</span></span>

<dt>

<span data-ttu-id="0872d-170">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0872d-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0872d-171">Tipo de datos de scripting: **fecha**</span><span class="sxs-lookup"><span data-stu-id="0872d-171">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UTCTime(
  [out] DATE* daUTCTime
);
HRESULT put_UTCTime(
  [in] DATE daUTCTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="0872d-172">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0872d-172">Remarks</span></span>

<span data-ttu-id="0872d-173">Las propiedades [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) solo establecerán o recuperarán un valor de propiedad del tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="0872d-173">The [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) properties will only set or retrieve a property value of the specified type.</span></span> <span data-ttu-id="0872d-174">Por ejemplo, la propiedad **CaseIgnoreString** de un atributo de tipo **\_ \_ cadena DN ADSTYPE**, como el atributo **distinguishedName** , producirá un error.</span><span class="sxs-lookup"><span data-stu-id="0872d-174">For example, the **CaseIgnoreString** property on an attribute of type **ADSTYPE\_DN\_STRING**, like the **distinguishedName** attribute, will result in an error.</span></span> <span data-ttu-id="0872d-175">La propiedad **CaseIgnoreString** solo funcionará en atributos de tipo **ADS \_ Case \_ Ignore \_ String**.</span><span class="sxs-lookup"><span data-stu-id="0872d-175">The **CaseIgnoreString** property will only work on attributes of type **ADS\_CASE\_IGNORE\_STRING**.</span></span> <span data-ttu-id="0872d-176">En la tabla siguiente se asigna el valor de [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) a la propiedad **IADsPropertyValue** correspondiente que se puede usar para tener acceso a ese tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="0872d-176">The following table maps the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value to the corresponding **IADsPropertyValue** property that can be used to access that attribute type.</span></span> <span data-ttu-id="0872d-177">Si un valor **ADSTYPEENUM** no aparece en esta tabla, no está disponible en la interfaz **IADsPropertyValue** .</span><span class="sxs-lookup"><span data-stu-id="0872d-177">If an **ADSTYPEENUM** value is not listed in this table, it is not available from the **IADsPropertyValue** interface.</span></span> <span data-ttu-id="0872d-178">La interfaz [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) se debe usar para obtener los datos en los otros formatos.</span><span class="sxs-lookup"><span data-stu-id="0872d-178">The [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) interface should be used to obtain data in the other formats.</span></span>



| <span data-ttu-id="0872d-179">Valor [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)</span><span class="sxs-lookup"><span data-stu-id="0872d-179">[**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value</span></span> | <span data-ttu-id="0872d-180">Propiedad [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="0872d-180">[**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) property</span></span> |
|------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0872d-181">**ADSTYPE \_ \_ cadena DN**</span><span class="sxs-lookup"><span data-stu-id="0872d-181">**ADSTYPE\_DN\_STRING**</span></span>                  | <span data-ttu-id="0872d-182">**DNString**</span><span class="sxs-lookup"><span data-stu-id="0872d-182">**DNString**</span></span>                                            |
| <span data-ttu-id="0872d-183">**\_ \_ cadena exacta de caso ADSTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="0872d-183">**ADSTYPE\_CASE\_EXACT\_STRING**</span></span>         | <span data-ttu-id="0872d-184">**CaseExactString**</span><span class="sxs-lookup"><span data-stu-id="0872d-184">**CaseExactString**</span></span>                                     |
| <span data-ttu-id="0872d-185">**ADSTYPE \_ caso \_ omitir \_ cadena**</span><span class="sxs-lookup"><span data-stu-id="0872d-185">**ADSTYPE\_CASE\_IGNORE\_STRING**</span></span>        | <span data-ttu-id="0872d-186">**CaseIgnoreString**</span><span class="sxs-lookup"><span data-stu-id="0872d-186">**CaseIgnoreString**</span></span>                                    |
| <span data-ttu-id="0872d-187">**ADSTYPE \_ cadena imprimible \_**</span><span class="sxs-lookup"><span data-stu-id="0872d-187">**ADSTYPE\_PRINTABLE\_STRING**</span></span>           | <span data-ttu-id="0872d-188">**PrintableString**</span><span class="sxs-lookup"><span data-stu-id="0872d-188">**PrintableString**</span></span>                                     |
| <span data-ttu-id="0872d-189">**ADSTYPE \_ \_ cadena numérica**</span><span class="sxs-lookup"><span data-stu-id="0872d-189">**ADSTYPE\_NUMERIC\_STRING**</span></span>             | <span data-ttu-id="0872d-190">**NumericString**</span><span class="sxs-lookup"><span data-stu-id="0872d-190">**NumericString**</span></span>                                       |
| <span data-ttu-id="0872d-191">**ADSTYPE \_ booleano**</span><span class="sxs-lookup"><span data-stu-id="0872d-191">**ADSTYPE\_BOOLEAN**</span></span>                     | <span data-ttu-id="0872d-192">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0872d-192">**Boolean**</span></span>                                             |
| <span data-ttu-id="0872d-193">**\_entero ADSTYPE**</span><span class="sxs-lookup"><span data-stu-id="0872d-193">**ADSTYPE\_INTEGER**</span></span>                     | <span data-ttu-id="0872d-194">**Entero**</span><span class="sxs-lookup"><span data-stu-id="0872d-194">**Integer**</span></span>                                             |
| <span data-ttu-id="0872d-195">**ADSTYPE \_ cadena de octeto \_**</span><span class="sxs-lookup"><span data-stu-id="0872d-195">**ADSTYPE\_OCTET\_STRING**</span></span>               | <span data-ttu-id="0872d-196">**OctetString**</span><span class="sxs-lookup"><span data-stu-id="0872d-196">**OctetString**</span></span>                                         |
| <span data-ttu-id="0872d-197">**\_hora UTC de ADSTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="0872d-197">**ADSTYPE\_UTC\_TIME**</span></span>                   | <span data-ttu-id="0872d-198">**UTCTime**</span><span class="sxs-lookup"><span data-stu-id="0872d-198">**UTCTime**</span></span>                                             |
| <span data-ttu-id="0872d-199">**\_entero grande de ADSTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="0872d-199">**ADSTYPE\_LARGE\_INTEGER**</span></span>              | <span data-ttu-id="0872d-200">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="0872d-200">**LargeInteger**</span></span>                                        |
| <span data-ttu-id="0872d-201">**descriptor de seguridad de ADSTYPE \_ NT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0872d-201">**ADSTYPE\_NT\_SECURITY\_DESCRIPTOR**</span></span>    | <span data-ttu-id="0872d-202">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0872d-202">**SecurityDescriptor**</span></span>                                  |



 

## <a name="examples"></a><span data-ttu-id="0872d-203">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0872d-203">Examples</span></span>

<span data-ttu-id="0872d-204">En el ejemplo de código siguiente se muestra cómo recuperar una propiedad de la lista de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0872d-204">The following code example shows how to retrieve a property from the property list.</span></span>


```VB
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup
 
' Retrieve the property list.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Retrieve a property entry. If you are certain of the property type,
' replace ADSTYPE_UNKNOWN with the actual property type.
Set propEntry = propList.GetPropertyItem("description", ADSTYPE_UNKNOWN)
 
' Print the property entry values.
For Each v In propEntry.Values
    Set propVal = v
    Select Case propVal.ADsType
        Case ADSTYPE_CASE_EXACT_STRING
            Debug.Print propVal.CaseExactString
        Case ADSTYPE_CASE_IGNORE_STRING
            Debug.Print propVal.CaseIgnoreString
        Case Else
            Debug.Print "Unable to handle a property of type: " & propVal.ADsType
    End Select
    
Next

Cleanup:
    If (Err.Number<>0) Then
       Debug.Print "An error has occurred. " & Err.Number
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



<span data-ttu-id="0872d-205">En el código siguiente se muestra cómo usar **IADsPropertyValue:: get \_ CaseIgnoreString** para recuperar el valor de la propiedad Description de una lista de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0872d-205">The following code shows how to use **IADsPropertyValue::get\_CaseIgnoreString** to retrieve the value of the description property from a property list.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADsPropertyValue *pVal = NULL;
IADs *pObj = NULL;
VARIANT var, varItem;
BSTR valStr;
IEnumVARIANT *pEnum = NULL;
LONG lstart = 0;
LONG lend = 0;
LONG lADsType = ADSTYPE_UNKNOWN;
 
VariantInit(&var);
VariantInit(&varItem);
 
// Bind to the directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);

if(FAILED(hr)){goto Cleanup;}

// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}

pObj->GetInfo();
pObj->Release();
 
// Retrieve the property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), ADSTYPE_CASE_IGNORE_STRING, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}

hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Retrieve the value array of the property entry.
hr = pEntry->get_Values(&var);
if(FAILED(hr)){goto Cleanup;}

SAFEARRAY *sa = V_ARRAY( &var );
 
// Retrieve the lower and upper bound. Iterate and print the values.
hr = SafeArrayGetLBound( sa, 1, &lstart );
hr = SafeArrayGetUBound( sa, 1, &lend );
printf(" Property value(s) = ");
for ( long idx=lstart; idx < lend+1; idx++ )    {
    hr = SafeArrayGetElement( sa, &idx, &varItem );
    hr = V_DISPATCH(&varItem)->QueryInterface(IID_IADsPropertyValue,
                                              (void**)&pVal);
    if(FAILED(hr)){goto Cleanup;}

    pVal->get_ADsType(&lADsType);

    switch(lADsType)
    {
        case ADSTYPE_CASE_IGNORE_STRING:
        {
            hr = pVal->get_CaseIgnoreString(&valStr);
            break;
        }
        case ADSTYPE_CASE_EXACT_STRING:
        {
            hr = pVal->get_CaseExactString(&valStr);
            break;
        }
        default:
        {
            valStr = SysAllocString(L"Unable to handle a property of this type");
            break;
        }
    }

    if(FAILED(hr)){goto Cleanup;}
    printf(" %S ", valStr);
    SysFreeString(valStr);
    VariantClear(&varItem);
}
printf("\n");

Cleanup:
    if(pList)
        pList = NULL;

    if(pEntry)
        pEntry = NULL;

    if(pVal)
        pVal = NULL;

    if(pObj)
        pObj = NULL;

    if(pEnum)
        pEnum = NULL;

    SysFreeString(valStr);
    VariantClear(&varItem);
    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="0872d-206">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0872d-206">Requirements</span></span>



| <span data-ttu-id="0872d-207">Requisito</span><span class="sxs-lookup"><span data-stu-id="0872d-207">Requirement</span></span> | <span data-ttu-id="0872d-208">Value</span><span class="sxs-lookup"><span data-stu-id="0872d-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0872d-209">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0872d-209">Minimum supported client</span></span><br/> | <span data-ttu-id="0872d-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0872d-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0872d-211">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0872d-211">Minimum supported server</span></span><br/> | <span data-ttu-id="0872d-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0872d-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0872d-213">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0872d-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="0872d-214"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="0872d-214"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="0872d-215">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0872d-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0872d-216"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0872d-216"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="0872d-217">IID</span><span class="sxs-lookup"><span data-stu-id="0872d-217">IID</span></span><br/>                      | <span data-ttu-id="0872d-218">IID \_ IADsPropertyValue se define como 79FA9AD0-A97C-11D0-8534-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="0872d-218">IID\_IADsPropertyValue is defined as 79FA9AD0-A97C-11D0-8534-00C04FD8D503</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="0872d-219">Vea también</span><span class="sxs-lookup"><span data-stu-id="0872d-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0872d-220">**IADsPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="0872d-220">**IADsPropertyValue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[<span data-ttu-id="0872d-221">**ADSTYPEENUM**</span><span class="sxs-lookup"><span data-stu-id="0872d-221">**ADSTYPEENUM**</span></span>](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[<span data-ttu-id="0872d-222">**IADsPropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="0872d-222">**IADsPropertyEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[<span data-ttu-id="0872d-223">**IADsPropertyList**</span><span class="sxs-lookup"><span data-stu-id="0872d-223">**IADsPropertyList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[<span data-ttu-id="0872d-224">**IADsPropertyValue2**</span><span class="sxs-lookup"><span data-stu-id="0872d-224">**IADsPropertyValue2**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[<span data-ttu-id="0872d-225">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0872d-225">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[<span data-ttu-id="0872d-226">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="0872d-226">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

