---
title: Métodos de propiedad IADsContainer (Iads.h)
description: Los métodos de propiedad de la interfaz IADsContainer obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información y una explicación general sobre los métodos de propiedad, vea Métodos de propiedad de interfaz.
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsContainer ADSI
topic_type:
- apiref
api_name:
- IADsContainer Property Methods
- IADsContainer.Count
- IADsContainer.get_Count
- IADsContainer.Filter
- IADsContainer.get_Filter
- IADsContainer.put_Filter
- IADsContainer.Hints
- IADsContainer.get_Hints
- IADsContainer.put_Hints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13515bcf90c926db839aad60d49599967ee0d24bedbe0deb4b7d1d21c3c016e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428090"
---
# <a name="iadscontainer-property-methods"></a>Métodos de propiedad IADsContainer

Los métodos de propiedad [**de la interfaz IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información y una explicación general sobre los métodos de propiedad, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Recuento**
</dt> <dd> <dl>

Recupera el número de elementos del contenedor. Cuando **se** establece Filtro, **Recuento** devuelve solo el número de elementos filtrados.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> <dt>

**Filter**
</dt> <dd> <dl>

Recupera o establece el filtro utilizado para seleccionar clases de objeto en una enumeración determinada. Se trata de una matriz variante, cuyo elemento es el nombre de una clase de esquema. Si **Filter** no está establecido o establecido en vacío, el enumerador recupera todos los objetos de todas las clases.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> <dt>

**Sugerencias**
</dt> <dd> <dl>

Matriz variante de **cadenas BSTR.** Cada elemento identifica el nombre de una propiedad que se encuentra en la definición de esquema. El *parámetro vHints* permite al cliente indicar qué atributos se cargarán para cada objeto enumerado. Estos datos se pueden usar para optimizar el acceso a la red. Sin embargo, la implementación exacta es específica del proveedor y actualmente no la usa el proveedor WinNT.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Hints(
  [out] VARIANT* pvHints
);
HRESULT put_Hints(
  [in] VARIANT vHints
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Comentarios

Los procesos de enumeración [**en IADsContainer::get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) **e IADsContainer::get \_ Count** se realizan en los objetos contenidos en la memoria caché. Cuando un contenedor contiene un gran número de objetos, el rendimiento puede verse afectado. Para mejorar el rendimiento, desactive la caché, configure un tamaño de página adecuado y use la [**interfaz IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) Por este motivo, la **propiedad \_ get Count** no se admite en el proveedor LDAP de Microsoft.

## <a name="examples"></a>Ejemplos

En el Visual Basic ejemplo de código siguiente se muestra cómo se pueden usar los métodos de propiedad de [**IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer)


```VB
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
 
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
cont.Hints = Array("adminDescription") ' Load this attribute. Optional.
Debug.Print cont.Get("adminDescription")

' Filter users.
cont.Filter = Array("user")

For Each usr In cont
  Debug.Print usr.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing
```



En el siguiente ejemplo de código de C++ se muestra cómo se pueden usar los métodos de propiedad de [**IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer) Por brevedad, se omite la comprobación de errores.


```C++
IADsContainer *pCont;
IADs *pChild;
IADs *pADs;
 
HRESULT hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM",
                          IID_IADsContainer, 
                          (void**)&pCont);

if(FAILED(hr)){goto Cleanup;}

LPWSTR pszArray[] = { L"adminDescription" };
DWORD dwNumber = sizeof(pszArray)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszArray, dwNumber, &var);
if(FAILED(hr)){goto Cleanup;}

hr = pCont->put_Hints( var );
if(FAILED(hr)){goto Cleanup;}

VariantClear(&var);
 
hr = pCont->QueryInterface(IID_IADs, (void**)pADs);
if(FAILED(hr)){goto Cleanup;}
 
hr = pADs->Get(CComBSTR("adminDescription"), var);
 
LPWSTR pszUsers = {L"user"};
dwNumber = sizeof(pszUsers)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr(pszUsers, dwNumber, &var);
hr = pCont->put_Filter( var );
VariantClear(&var);
 
// Enumerate user objects in the container.
IEnumVARIANT *pEnum = NULL;
hr = ADsBuildEnumerator(pCont, &pEnum);
pCont->Release();    // Not required when users are enumerated.
 
ULONG lFetch;
VariantClear(&var);
while (SUCCEEDED(ADsEnumerateNext(pEnum, 1, &var, &lFetch)) && 
                      lFetch==1) {
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pChild)
    if(SUCCEEDED(hr)) {
        BSTR bstrName;
        pChild->get_Name(&bstrName);
        printf("  %S\n", bstrName);
        SysFreeString(bstrName);
        pChild->Release();
    }
    VariantClear(&var);
}
Cleanup:
    if(pADs)
        pADs->Release();

    if(pCont)
        pCont->Release();

    if(pChild)
        pChild->Release();

    VariantClear(&var);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsContainer se define como 001677D0-FD16-11CE-ABC4-02608C9E7553<br/>        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 





