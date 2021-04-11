---
title: Métodos de la propiedad IADsClass (iAds. h)
description: Los métodos de propiedad de la interfaz IADsClass obtienen o establecen las siguientes propiedades. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsClass ADSI
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358bc33347f035af92303a4ce9879105cd247a3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150777"
---
# <a name="iadsclass-property-methods"></a>Métodos de propiedad IADsClass

Los métodos de propiedad de la interfaz [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) obtienen o establecen las siguientes propiedades. Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Descripción**
</dt> <dd> <dl>

Valor booleano que indica si esta clase es abstracta o no abstracta. Si es **true**, esta clase es una clase abstracta y no se puede crear directamente una instancia de ella en el servicio de directorio. Las clases abstractas solo se pueden usar como superclases.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **booleano**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

**AuxDerivedFrom**
</dt> <dd> <dl>

Matriz de cadenas ADsPath que indican las clases de Super auxiliar de las que se deriva esta clase.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**Auxiliar**
</dt> <dd> <dl>

Valor booleano que indica si esta clase es auxiliar o no. Si es **true**, esta clase es una clase auxiliar y no se pueden crear instancias directamente en el servicio de directorio. Las clases auxiliares solo se pueden usar como súper clases de otras clases auxiliares o como origen de propiedades adicionales en clases estructurales.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **booleano**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

**CLSID**
</dt> <dd> <dl>

CLSID opcional específico del proveedor que identifica el objeto COM que implementa esta clase.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

**Contenedor**
</dt> <dd> <dl>

Valor booleano que indica si esta clase puede ser un contenedor de otras clases de objeto. Si este valor es **true**, puede llamar al método **Get \_ Container** para obtener una matriz de las clases de objeto que esta clase puede contener.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **booleano**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

**Containment**
</dt> <dd> <dl>

Matriz **BSTR** en la que cada elemento es el nombre de una clase de objeto que esta clase puede contener.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

**DerivedFrom**
</dt> <dd> <dl>

Matriz de cadenas ADsPath que indican las clases de las que se deriva esta clase.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**HelpFileContext**
</dt> <dd> <dl>

IDENTIFICADOR de contexto dentro de **HelpFileName** donde se puede encontrar información específica de esta clase.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

**HelpFileName**
</dt> <dd> <dl>

Nombre de un archivo de ayuda que contiene más información sobre los objetos de esta clase.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

**MandatoryProperties**
</dt> <dd> <dl>

**SAFEARRAY** de **Variant** s que enumera las propiedades que se deben establecer para que esta clase se escriba en el almacenamiento. Si la clase solo contiene una propiedad, **Get \_ MandatoryProperties** devolverá un **BSTR**.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

**NamingProperties**
</dt> <dd> <dl>

**SAFEARRAY** de **BSTR** s que enumera las propiedades utilizadas para asignar nombres a los atributos de esta clase de esquema.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

**OID**
</dt> <dd> <dl>

Identificador de objeto específico del proveedor que define esta clase. Esto se proporciona para permitir la extensión de esquema, mediante Active Directory, en servicios de directorio que requieran OID específicos del proveedor para las clases.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

**OptionalProperties**
</dt> <dd> <dl>

**SAFEARRAY** de **Variant** s que enumera las propiedades opcionales para esta clase de esquema. Si la clase solo contiene una propiedad, **Get \_ OptionalProperties** devolverá un **BSTR**.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

**PossibleSuperiors**
</dt> <dd> <dl>

Matriz de cadenas ADsPath que indican las clases de esquema que pueden contener instancias de esta clase.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

**PrimaryInterface**
</dt> <dd> <dl>

GUID opcional del identificador específico del proveedor que asocia una interfaz a los objetos de esta clase de esquema. Por ejemplo, la clase "User" que admite [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) y **PrimaryInterface** se identifica mediante **IID \_ IADsUser**. Debe estar en el formato de cadena estándar de un GUID, tal y como se define en COM. Este GUID es el valor que aparece en la propiedad [**IADs:: get \_ GUID**](/windows/desktop/api/Iads/nn-iads-iads) en las instancias de esta clase para los proveedores que implementan esta propiedad. La identificación de una clase de esquema por parte de IID de la interfaz principal del código de clase permite el uso de **QueryInterface** en tiempo de ejecución para determinar si un objeto es de la clase deseada.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo utilizar la interfaz [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) para determinar si un objeto puede ser un contenedor y, si es así, enumera los nombres de los objetos contenidos.


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



En el ejemplo de código siguiente se muestra cómo utilizar la interfaz [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) para determinar si un objeto puede ser un contenedor y, si es así, enumera los nombres de los objetos contenidos.


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsClass se define como C8F93DD0-4AE0-11cf-9E73-00AA004A5691<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**IADsClass:: Qualifiers**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 





