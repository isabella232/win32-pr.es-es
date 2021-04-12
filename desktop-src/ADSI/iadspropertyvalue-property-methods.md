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
# <a name="iadspropertyvalue-property-methods"></a>Métodos de propiedad IADsPropertyValue

Los métodos de propiedad de la interfaz [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) proporcionan acceso a las propiedades que se describen en la tabla siguiente. Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**ADsType**
</dt> <dd> <dl>

El tipo de datos del valor de la propiedad, tomado de la enumeración [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) , de la propiedad Value.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
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

**Boolean**
</dt> <dd> <dl>

Valor booleano.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
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

**CaseExactString**
</dt> <dd> <dl>

Cadena que se va a interpretar. Distingue mayúsculas de minúsculas.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
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

**CaseIgnoreString**
</dt> <dd> <dl>

Cadena que se va a interpretar. No hay distinción de mayúsculas y minúsculas.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
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

**DNString**
</dt> <dd> <dl>

Cadena que identifica el nombre distintivo (ruta de acceso) de un objeto de valor de servicio de directorio.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
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

**Entero**
</dt> <dd> <dl>

Valor entero.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
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

**LargeInteger**
</dt> <dd> <dl>

Puntero a la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) del objeto que implementa [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) para este valor.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **IDispatch**
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

**NumericString**
</dt> <dd> <dl>

Texto que se va a interpretar. Tipo numérico.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
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

**OctetString**
</dt> <dd> <dl>

Matriz Variant de caracteres de un byte.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante**
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

**PrintableString**
</dt> <dd> <dl>

Mostrar o imprimir cadena.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
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

**SecurityDescriptor**
</dt> <dd> <dl>

Puntero a la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) del objeto que implementa [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) para este valor.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **IDispatch**
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

**UTCTime**
</dt> <dd> <dl>

Fecha del tipo de **\_ datos VT** expresado en formato de hora universal coordinada (UTC).

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **fecha**
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

 

## <a name="remarks"></a>Observaciones

Las propiedades [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) solo establecerán o recuperarán un valor de propiedad del tipo especificado. Por ejemplo, la propiedad **CaseIgnoreString** de un atributo de tipo **\_ \_ cadena DN ADSTYPE**, como el atributo **distinguishedName** , producirá un error. La propiedad **CaseIgnoreString** solo funcionará en atributos de tipo **ADS \_ Case \_ Ignore \_ String**. En la tabla siguiente se asigna el valor de [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) a la propiedad **IADsPropertyValue** correspondiente que se puede usar para tener acceso a ese tipo de atributo. Si un valor **ADSTYPEENUM** no aparece en esta tabla, no está disponible en la interfaz **IADsPropertyValue** . La interfaz [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) se debe usar para obtener los datos en los otros formatos.



| Valor [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) | Propiedad [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) |
|------------------------------------------|---------------------------------------------------------|
| **ADSTYPE \_ \_ cadena DN**                  | **DNString**                                            |
| **\_ \_ cadena exacta de caso ADSTYPE \_**         | **CaseExactString**                                     |
| **ADSTYPE \_ caso \_ omitir \_ cadena**        | **CaseIgnoreString**                                    |
| **ADSTYPE \_ cadena imprimible \_**           | **PrintableString**                                     |
| **ADSTYPE \_ \_ cadena numérica**             | **NumericString**                                       |
| **ADSTYPE \_ booleano**                     | **Boolean**                                             |
| **\_entero ADSTYPE**                     | **Entero**                                             |
| **ADSTYPE \_ cadena de octeto \_**               | **OctetString**                                         |
| **\_hora UTC de ADSTYPE \_**                   | **UTCTime**                                             |
| **\_entero grande de ADSTYPE \_**              | **LargeInteger**                                        |
| **descriptor de seguridad de ADSTYPE \_ NT \_ \_**    | **SecurityDescriptor**                                  |



 

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo recuperar una propiedad de la lista de propiedades.


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



En el código siguiente se muestra cómo usar **IADsPropertyValue:: get \_ CaseIgnoreString** para recuperar el valor de la propiedad Description de una lista de propiedades.


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsPropertyValue se define como 79FA9AD0-A97C-11D0-8534-00C04FD8D503<br/>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

