---
title: Métodos de propiedad IADsSyntax (Iads.h)
description: Los métodos de propiedad de la interfaz IADsSyntax obtienen o establecen las propiedades enumeradas en la tabla siguiente. Para obtener más información sobre los métodos de propiedad, vea Métodos de propiedad de interfaz.
ms.assetid: a216a55d-63eb-4fdf-a67f-8d4b5eb74262
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propiedad IADsSyntax
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
ms.openlocfilehash: c193bba78bfe215d37bdfdedf5d45bd73f1a85606b3dab6e5a3c233cece8db18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961904"
---
# <a name="iadssyntax-property-methods"></a>Métodos de propiedad IADsSyntax

Los métodos de propiedad [**de la interfaz IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) obtienen o establecen las propiedades enumeradas en la tabla siguiente. Para obtener más información sobre los métodos de propiedad, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**OleAutoDataType**
</dt> <dd> <dl>

Recupera y establece un **valor LONG** que contiene el valor de la constante **VT \_ xxx** para el tipo de datos automation que representa esta sintaxis.

Active Directory admite las siguientes **constantes XXX \_ de VT** para el tipo de datos automation que representa esta sintaxis:

-   **VT \_ BOOL** BOOL
-   **VT \_ BSTR** BSTR
-   **VT \_ BSTRT** BSTRT
-   **VT \_ CY** CURRENCY
-   **VT \_ DATE** Date
-   **VT \_ EMPTY** **NULL**
-   **VT \_ ERROR** No válido
-   **VT \_ I2** short
-   **VT \_ I4** long
-   **VT \_ R4** real
-   **VT \_ R8** double
-   **VT \_ UI1** BYTE

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
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

 

## <a name="remarks"></a>Comentarios

Una matriz de bytes sin signo, **VT \_ UI1** VT ARRAY podría significar que el proveedor ha asignado una sintaxis que no se puede asignar a un tipo virtual de \| **\_** Automation.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se examina la sintaxis del atributo **OperatingSystemVersion** de un equipo en una red a través del proveedor WinNT. La sintaxis del resultado es una cadena.


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



En el ejemplo de código siguiente se examina la sintaxis del atributo **OperatingSystemVersion** de un equipo en una red a través del proveedor WinNT. La sintaxis del resultado es una cadena. Por brevedad, se omite la comprobación de errores.


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



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsSyntax se define como C8F93DD2-4AE0-11CF-9E73-00AA004A5691<br/>           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





