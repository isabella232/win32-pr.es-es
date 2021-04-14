---
title: Métodos de propiedad IADs (iAds. h)
description: Los métodos de propiedad de la interfaz IADs obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información sobre los métodos de propiedad, vea métodos de propiedad de interfaz.
ms.assetid: d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12
ms.tgt_platform: multiple
keywords:
- Métodos de propiedades de IADs ADSI
topic_type:
- apiref
api_name:
- IADs Property Methods
- IADs.ADsPath
- IADs.get_ADsPath
- IADs.Class
- IADs.get_Class
- IADs.GUID
- IADs.get_GUID
- IADs.Name
- IADs.get_Name
- IADs.Parent
- IADs.get_Parent
- IADs.Schema
- IADs.get_Schema
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1134260c780958bcdba8d1f14eac535ddbf4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533819"
---
# <a name="iads-property-methods"></a>Métodos de propiedades de IADs

Los métodos de propiedad de la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información sobre los métodos de propiedad, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**ADsPath**
</dt> <dd> <dl>

Cadena ADsPath de este objeto. La cadena identifica de forma única este objeto en un entorno de red. El objeto siempre se puede recuperar utilizando esta ruta de acceso.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsPath(
  [out] BSTR* pbstrADsPath
);
```


</dt> </dl> </dd> <dt>

**Clase**
</dt> <dd> <dl>

Nombre de la clase de esquema de objetos.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Class(
  [out] BSTR* pbstrClass
);
```


</dt> </dl> </dd> <dt>

**GUID**
</dt> <dd> <dl>

Identificador único global del objeto de directorio. La interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) convierte el **GUID** de una cadena de octetos, almacenada en un servidor de directorio, en un formato de cadena.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GUID(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> <dt>

**Nombre**
</dt> <dd> <dl>

Nombre relativo del objeto como se denomina en el servicio de directorio subyacente. Este nombre distingue este objeto de sus elementos del mismo nivel.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
```


</dt> </dl> </dd> <dt>

**Parent**
</dt> <dd> <dl>

Cadena ADsPath del contenedor principal. Active Directory no permite la formación del ADsPath de un objeto determinado mediante la concatenación de las propiedades **Parent** y **Name** . Aunque esta operación podría funcionar en algunos proveedores, no se garantiza que funcione para todas las implementaciones. Se garantiza que el atributo ADsPath es válido y siempre debe usarse para recuperar el puntero de interfaz de un objeto.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parent(
  [out] BSTR* pbstrParent
);
```


</dt> </dl> </dd> <dt>

**Esquema**
</dt> <dd> <dl>

Cadena ADsPath del objeto de clase de esquema de este objeto.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Observaciones

En Active Directory, el **GUID** devuelto desde el GUID es una cadena de cadenas hexadecimales. Utilice el **GUID** resultante para enlazar directamente con el objeto.


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



donde xxx es el valor devuelto por la propiedad GUID. Para obtener más información, vea [usar objectGUID para enlazar a un objeto](/windows/desktop/AD/using-objectguid-to-bind-to-an-object). Tenga en cuenta que si usa un GUID para enlazar a un objeto, el método de la propiedad **ADsPath** devuelve valores distintos de los valores normales que se devolverían si usara un nombre distintivo (DN) para enlazar al mismo objeto. Por ejemplo, en la tabla siguiente se enumeran los valores devueltos al usar los dos métodos de enlace diferentes para enlazar al mismo objeto de usuario.



|             | Enlazar mediante DN                                           | Enlazar mediante GUID                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| **Nombre**    | CN = Jeff Smith                                           | CN = Jeff Smith                                               |
| **Parent**  | LDAP://server/CN=Users,DC=Fabrikam,DC=com               | LDAP://server/CN=Users,DC=Fabrikam,DC=com                   |
| **ADsPath** | LDAP://server/CN=Jeff Smith, CN = users, DC = Fabrikam, DC = com | LDAP://server/<GUID = c0f59dfcf507d311a99e0000f879f7c7> |



 

> [!Note]  
> El proveedor de WinNT no admite el enlace con el **GUID** del objeto y devuelve la propiedad **GUID** en un formato de cadena ligeramente diferente.

 

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo recuperar datos de objeto mediante métodos de propiedad de la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .


```VB
Dim x As IADs
Dim parent As IADsContainer
Dim cls As IADsClass
Dim op As Variant

On Error GoTo Cleanup

Set x = GetObject("WinNT://Fabrikam/Administrator")
Debug.Print "Object Name: " & x.Name
Debug.Print "Object Path: " & x.ADsPath
Debug.Print "Object Class: " & x.Class
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Debug.Print "Class Name is: " & cls.Name
For Each op In cls.OptionalProperties
    Debug.Print "Optional Property: " & op
Next op

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
    Set parent = Nothing
    Set cls = Nothing
```



En el ejemplo de código siguiente se muestra cómo recuperar datos de objeto mediante métodos de propiedad de la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .


```VB
<HTML>
<head><title></title></head>

<body>
<%
Dim x 
On Error Resume Next
 
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " & x.Name & "<br>"
Response.Write "Object Path: " & x.ADsPath & "<br>"
Response.Write "Object Class: " & x.Class & "<br>"
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Response.Write "Class Name is: " & cls.Name & "<br>"
For Each op In cls.OptionalProperties
    Response.Write "Optional Property: " & op & "<br>"
Next op
%>

</body>
</html>
```



En el ejemplo de código siguiente se muestra cómo trabajar con los métodos de propiedad de la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .


```C++
#include <stdio.h>
#include <activeds.h>
 
int main(int argc, char* argv[])
{
    IADs *pADs = NULL;
    IADsUser *pADsUser = NULL;
    IADsClass *pCls = NULL;
    CComBSTR sbstr;
 
    HRESULT hr = CoInitialize(NULL);
    if (hr != S_OK) { return 0; }
 
    hr=ADsGetObject(L"WinNT://Fabrikam/Administrator",
                IID_IADsUser,
                (void**) &pADsUser);
    if (hr != S_OK) { goto Cleanup; }
 
    hr = pADsUser->QueryInterface(IID_IADs, (void**) &pADs);
    if( hr !=S_OK) { goto Cleanup;}
 
    pADsUser->Release();
 
    if( S_OK == pADs->get_Name(&sbstr) ) {
        printf("Object Name: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_ADsPath(&sbstr) ) {
        printf("Object path: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_Class(&sbstr) ) {
        printf("Object class: %S\n",sbstr);
    }
 
    hr = pADs->get_Schema(&sbstr);
    if ( hr != S_OK) {goto Cleanup;}
 
    hr = ADsGetObject(sbstr,IID_IADsClass, (void**)&pCls);
    if ( hr != S_OK) {goto Cleanup;}
    if( S_OK == pCls->get_Name(&sbstr) ) {
        printf("Class name is %S\n", sbstr);
    }
 
 Cleanup:
    if(pADs)
        pADs->Release();

    if(pIADsUser)
        pADsUser->Release();

    if(IADsClass)
        pADsClass->Release();

    CoUninitialize();

    if(hr==S_OK)
    {
        return 1;
    }
    else
    {
        return 0;
    }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | El IID \_ de IID se define como FD8256D0-FD15-11CE-ABC4-02608C9E7553<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 

