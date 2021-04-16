---
title: Métodos de la propiedad IADsMembers (iAds. h)
description: Los métodos de la interfaz IADsMembers leen y escriben las propiedades descritas en este tema. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: ed4e98e5-053c-4d3b-bcd0-3add96bbe120
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsMembers ADSI
topic_type:
- apiref
api_name:
- IADsMembers Property Methods
- IADsMembers.Count
- IADsMembers.get_Count
- IADsMembers.Filter
- IADsMembers.get_Filter
- IADsMembers.put_Filter
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af047d6fe52fdd7d808b1d7e5dbfb35303d3ff59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658301"
---
# <a name="iadsmembers-property-methods"></a>Métodos de propiedad IADsMembers

Los métodos de la interfaz [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) leen y escriben las propiedades descritas en este tema. Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Recuento**
</dt> <dd> <dl>

Indica el número de elementos del contenedor. Si se establece el filtro, Count solo devuelve el número de elementos que se ajustan a la descripción del filtro.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **largo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCountr
);
```


</dt> </dl> </dd> <dt>

**Filter**
</dt> <dd> <dl>

Indica el filtro. La sintaxis de las entradas de la matriz de filtros es la misma que la del filtro utilizado en la interfaz [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante**
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


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Observaciones

Los proveedores del sistema ADSI no admiten el método de propiedad **IADsMembers:: get \_ Count** .

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo utilizar los métodos de propiedad de esta interfaz.


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://myComputer/someGroup")
grp.members.filter = Array("user")
For Each usr In grp.Members
    MsgBox usr.Name & "," & usr.Class & "," & usr.AdsPath
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



En el ejemplo de código siguiente se usa el método de **\_ filtro IADsMembers::p UT** para preparar una enumeración de la colección de miembros de un grupo.


```C++
IADsGroup *pGroup;
HRESULT hr = S_OK;

LPWSTR grpPath = L"WinNT://myComputer/someGroup";
hr = ADsGetObject(grpPath,IID_IADsGroup,(void**)&pGroup);
if(FAILED(hr)){goto Cleanup;}

IADsMembers *pMembers;
hr = pGroup->Members(&pMembers);
if(FAILED(hr)){goto Cleanup;}

hr = pGroup->Release();

SAFEARRAY *sa = CreateSafeArray(L"user");
hr = pMembers->put_Filter(sa);
if(FAILED(hr)){goto Cleanup;}

hr = EnumMembers(pMembers);    // For more information, and a 
                               // code example, see 
                               // IADsMembers::get__NewEnum.
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup) pGroup->Release();
    if(pMembers) pMembers->Release();
    return hr;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsMembers se define como 451A0030-72EC-11cf-B03B-00AA006E0975<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[**IADsMembers:: get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum)
</dt> <dt>

[**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)
</dt> <dt>

[Métodos de propiedad de interfaz](interface-property-methods.md)
</dt> </dl>

 

 





