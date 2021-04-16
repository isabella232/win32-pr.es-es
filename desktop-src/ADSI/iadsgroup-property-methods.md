---
title: Métodos de la propiedad IADsGroup (iAds. h)
description: Métodos de propiedad de la interfaz IADsGroup.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsGroup ADSI
topic_type:
- apiref
api_name:
- IADsGroup Property Methods
- IADsGroup.Description
- IADsGroup.get_Description
- IADsGroup.put_Description
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 665cb91a55298012e4e906c2972da5371e3960be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658303"
---
# <a name="iadsgroup-property-methods"></a>Métodos de propiedad IADsGroup

Los métodos de propiedad de la interfaz [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) leen y escriben las siguientes propiedades. Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Descripción**
</dt> <dd> <dl>

Indica la descripción textual de la pertenencia al grupo.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Observaciones

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a>Usar IADsGroup para recuperar descripciones de grupos integrados

En los siguientes ejemplos se muestra cómo recuperar información acerca de los objetos de grupo de Windows por nombre. En un entorno multilingüe, a veces se conocen los nombres localizados de los grupos integrados, lo que significa que no se pueden recuperar directamente mediante el uso de identificadores de cadena como "WinNT://Microsoft/Administrators". En ese caso, el usuario puede enlazar con el objeto de SID conocido del grupo, recuperar el nombre de grupo localizado y proporcionarlo al método GetObject. Para obtener más información, vea [SID conocidos](/windows/desktop/SecAuthZ/well-known-sids).

## <a name="examples"></a>Ejemplos

En el siguiente Visual Basic ejemplo se muestra cómo enlazar a un objeto de grupo y mostrar la descripción del grupo.


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
Debug.Print grp.Description

Cleanup
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



En el siguiente ejemplo de C++ se muestra cómo enlazar a un objeto de grupo y mostrar la descripción del grupo.


```C++
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://localHost/Administrators";
BSTR bstr;

hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);

if(FAILED(hr)) {goto Cleanup;}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Description: %S\n",bstr);

Cleanup:
    SysFreeString(bstr);
    if(pGroup) 
        pGroup->Release();

    return hr;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsGroup se define como 27636B00-410F-11cf-B1FF-02608C9E7553<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[Métodos de propiedad de interfaz](interface-property-methods.md)
</dt> </dl>

 

