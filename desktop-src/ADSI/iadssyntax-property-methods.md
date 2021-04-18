---
title: Métodos de la propiedad IADsSyntax (iAds. h)
description: Los métodos de propiedad de la interfaz IADsSyntax obtienen o establecen las propiedades enumeradas en la tabla siguiente. Para obtener más información sobre los métodos de propiedad, vea métodos de propiedad de interfaz.
ms.assetid: a216a55d-63eb-4fdf-a67f-8d4b5eb74262
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsSyntax ADSI
topic_type:
- apiref
api_name:
- IADsSyntax Property Methods
- IADsSyntax.OleAutoDataType
- IADsSyntax.get_OleAutoDataType
- IADsSyntax.put_OleAutoDataType
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a41c84efb4f48171913156823e18a301236290
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534042"
---
# <a name="iadssyntax-property-methods"></a>Métodos de propiedad IADsSyntax

Los métodos de propiedad de la interfaz [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) obtienen o establecen las propiedades enumeradas en la tabla siguiente. Para obtener más información sobre los métodos de propiedad, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**OleAutoDataType**
</dt> <dd> <dl>

Recupera y establece un valor de **tipo Long** que contiene el valor de la constante **VT \_ XXX** para el tipo de datos de Automation que representa esta sintaxis.

Active Directory admite las siguientes constantes **VT \_ XXX** para el tipo de datos de Automation que representa esta sintaxis:

-   **VT \_ BOOL** bool
-   **VT \_ BSTR BSTR**
-   **VT \_ BSTRT** BSTRT
-   **VT \_ moneda CY**
-   **VT \_ Fecha de fecha**
-   **VT \_** **null** vacío
-   **VT \_ ERROR** no válido
-   **VT \_ De i2** corto
-   **VT \_ I4** Long
-   **VT \_ R4** real
-   **VT \_ R8** doble
-   **VT \_ UI1** byte

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OleAutoDataType(
  [out] LONG* plAutoDataType
);
HRESULT put_OleAutoDataType(
  [in] LONG lAutoDataType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Observaciones

Una matriz de bytes sin signo, la **matriz VT \_ UI1** \| **VT \_** podría significar que el proveedor ha asignado una sintaxis que no se puede asignar a un tipo virtual de automatización.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se examina la sintaxis del atributo **OperatingSystemVersion** de un equipo en una red a través del proveedor de Winnt. La sintaxis del resultado es una cadena.


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sy As IADsSyntax
Dim sc As IADsContainer
On Error GoTo Cleanup

Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystemVersion")
Set sy = GetObject(sc.ADsPath & "/" & pr.Syntax)
 
MsgBox "Automation data types: " & sy.OleAutoDataType

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sy = Nothing
    Set sc = Nothing
```



En el ejemplo de código siguiente se examina la sintaxis del atributo **OperatingSystemVersion** de un equipo en una red a través del proveedor de Winnt. La sintaxis del resultado es una cadena. Por motivos de brevedad, se omite la comprobación de errores.


```C++
#include <stdio.h>
#include <activeds.h>
#include <atlbase.h>
 
IADs *pObj = NULL;
IADsClass *pCls = NULL;
IADsProperty *pProp = NULL;
IADsSyntax *pSyn = NULL;
IADsContainer *pCont = NULL;
 
HRESULT hr = ADsGetObject(L"WinNT://myMachine,computer",
                          IID_IADs,
                          (void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
VARIANT var;
VariantInit(&var);
CComBSTR sbstr;
 
pObj->get_Schema(&sbstr);
printf("Object schema: %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsClass,(void**)&pCls);
if(FAILED(hr)){goto Cleanup;}

pCls->get_Parent(&sbstr);
printf("Object class's container:  %S\n", sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr)){goto Cleanup;}
pCont->QueryInterface(IID_IADs,(void**)&pObj);
pObj->get_ADsPath(&sbstr);
printf("Container's AdsPath:  %S\n",sbstr);
 
IDispatch *pDisp;
hr = pCont->GetObject(CComBSTR("Property"),
                      CComBSTR("OperatingSystemVersion"),
                      (IDispatch**)&pDisp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pDisp->QueryInterface(IID_IADsProperty, (void**)&pProp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pProp->get_Syntax(&sbstr);
if(FAILED(hr)){goto Cleanup;}
printf("Property Syntax:  %S\n",sbstr);
 
printf("ADsPath of the syntax object %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsSyntax, (void**)&pSyn);
if(FAILED(hr)){goto Cleanup;}

long lType;
pSyn->get_OleAutoDataType(&lType);
printf("Property syntax's OleAutoDataType: %d\n", lType);

Cleanup:
    if(pObj)
        pObj->Release();

    if(pProp)
        pProp->Release();

    if(pCls)
        pCls->Release();

    if(pSyn)
        pSyn->Release();

    if(pCont)
        pCont->Release();
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsSyntax se define como C8F93DD2-4AE0-11cf-9E73-00AA004A5691<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





