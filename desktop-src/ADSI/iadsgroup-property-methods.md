---
title: Métodos de propiedad IADsGroup (Iads.h)
description: Métodos de propiedad de la interfaz IADsGroup.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- AdsI de métodos de propiedad IADsGroup
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
ms.openlocfilehash: f15a55765a10afef10087e7b28d04304ab0cc2668915a6e6ffa71fc770eb54a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082409"
---
# <a name="iadsgroup-property-methods"></a>Métodos de propiedad IADsGroup

Los métodos de propiedad de [**la interfaz IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) leen y escriben las propiedades siguientes. Para obtener más información, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Descripción**
</dt> <dd> <dl>

Indica la descripción textual de la pertenencia al grupo.

<dt>

Tipo de acceso: lectura y escritura
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

 

## <a name="remarks"></a>Comentarios

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a>Uso de IADsGroup para recuperar descripciones de grupos integrados

En los ejemplos siguientes se muestra cómo recuperar información sobre Windows objetos de grupo por nombre. En un entorno multilingüe, los grupos integrados a veces se conocen por diferentes nombres localizados, lo que significa que no se pueden recuperar directamente mediante identificadores de cadena como "WinNT://Microsoft/Administrators". En ese caso, el usuario puede enlazar al objeto SID conocido del grupo, recuperar el nombre del grupo localizado y proporcionarlo al método GetObject. Para obtener más información, [vea Sids conocidos.](/windows/desktop/SecAuthZ/well-known-sids)

## <a name="examples"></a>Ejemplos

En el Visual Basic siguiente se muestra cómo enlazar a un objeto de grupo y mostrar la descripción del grupo.


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



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID IADsGroup se define como \_ 27636B00-410F-11CF-B1FF-02608C9E7553<br/>            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Iads**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[Métodos de propiedad de interfaz](interface-property-methods.md)
</dt> </dl>

 

