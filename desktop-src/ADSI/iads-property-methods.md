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
# <a name="iads-property-methods"></a><span data-ttu-id="f6f9f-105">Métodos de propiedades de IADs</span><span class="sxs-lookup"><span data-stu-id="f6f9f-105">IADs Property Methods</span></span>

<span data-ttu-id="f6f9f-106">Los métodos de propiedad de la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) obtienen o establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-106">The property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="f6f9f-107">Para obtener más información sobre los métodos de propiedad, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f6f9f-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f6f9f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6f9f-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="f6f9f-109">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-109">**ADsPath**</span></span>
<span data-ttu-id="f6f9f-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f6f9f-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="f6f9f-111">Cadena ADsPath de este objeto.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-111">The ADsPath string of this object.</span></span> <span data-ttu-id="f6f9f-112">La cadena identifica de forma única este objeto en un entorno de red.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-112">The string uniquely identifies this object in a network environment.</span></span> <span data-ttu-id="f6f9f-113">El objeto siempre se puede recuperar utilizando esta ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-113">The object can always be retrieved using this path.</span></span>

<dt>

<span data-ttu-id="f6f9f-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6f9f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6f9f-115">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-115">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsPath(
  [out] BSTR* pbstrADsPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f6f9f-116">**Clase**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-116">**Class**</span></span>
<span data-ttu-id="f6f9f-117"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f6f9f-117"></dt> <dd> <dl></span></span>

<span data-ttu-id="f6f9f-118">Nombre de la clase de esquema de objetos.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-118">The name of the object Schema class.</span></span>

<dt>

<span data-ttu-id="f6f9f-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6f9f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6f9f-120">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-120">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Class(
  [out] BSTR* pbstrClass
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f6f9f-121">**GUID**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-121">**GUID**</span></span>
<span data-ttu-id="f6f9f-122"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f6f9f-122"></dt> <dd> <dl></span></span>

<span data-ttu-id="f6f9f-123">Identificador único global del objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-123">The globally unique identifier of the directory object.</span></span> <span data-ttu-id="f6f9f-124">La interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) convierte el **GUID** de una cadena de octetos, almacenada en un servidor de directorio, en un formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-124">The [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface converts the **GUID** from an octet string, as stored on a directory server, into a string format.</span></span>

<dt>

<span data-ttu-id="f6f9f-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6f9f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6f9f-126">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-126">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GUID(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f6f9f-127">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-127">**Name**</span></span>
<span data-ttu-id="f6f9f-128"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f6f9f-128"></dt> <dd> <dl></span></span>

<span data-ttu-id="f6f9f-129">Nombre relativo del objeto como se denomina en el servicio de directorio subyacente.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-129">The relative name of the object as named within the underlying directory service.</span></span> <span data-ttu-id="f6f9f-130">Este nombre distingue este objeto de sus elementos del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-130">This name distinguishes this object from its siblings.</span></span>

<dt>

<span data-ttu-id="f6f9f-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6f9f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6f9f-132">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f6f9f-133">**Parent**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-133">**Parent**</span></span>
<span data-ttu-id="f6f9f-134"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f6f9f-134"></dt> <dd> <dl></span></span>

<span data-ttu-id="f6f9f-135">Cadena ADsPath del contenedor principal.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-135">The ADsPath string of the parent container.</span></span> <span data-ttu-id="f6f9f-136">Active Directory no permite la formación del ADsPath de un objeto determinado mediante la concatenación de las propiedades **Parent** y **Name** .</span><span class="sxs-lookup"><span data-stu-id="f6f9f-136">Active Directory does not permit the formation of the ADsPath of a given object by concatenating the **Parent** and **Name** properties.</span></span> <span data-ttu-id="f6f9f-137">Aunque esta operación podría funcionar en algunos proveedores, no se garantiza que funcione para todas las implementaciones.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-137">While this operation might work in some providers, it is not guaranteed to work for all implementations.</span></span> <span data-ttu-id="f6f9f-138">Se garantiza que el atributo ADsPath es válido y siempre debe usarse para recuperar el puntero de interfaz de un objeto.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-138">The ADsPath is guaranteed to be valid and should always be used to retrieve an object's interface pointer.</span></span>

<dt>

<span data-ttu-id="f6f9f-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6f9f-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6f9f-140">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-140">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parent(
  [out] BSTR* pbstrParent
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f6f9f-141">**Esquema**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-141">**Schema**</span></span>
<span data-ttu-id="f6f9f-142"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f6f9f-142"></dt> <dd> <dl></span></span>

<span data-ttu-id="f6f9f-143">Cadena ADsPath del objeto de clase de esquema de este objeto.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-143">The ADsPath string of the Schema class object of this object.</span></span>

<dt>

<span data-ttu-id="f6f9f-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6f9f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6f9f-145">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-145">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="f6f9f-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6f9f-146">Remarks</span></span>

<span data-ttu-id="f6f9f-147">En Active Directory, el **GUID** devuelto desde el GUID es una cadena de cadenas hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-147">In Active Directory, the **GUID** returned from GUID is a string of hexadecimals.</span></span> <span data-ttu-id="f6f9f-148">Utilice el **GUID** resultante para enlazar directamente con el objeto.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-148">Use the resultant **GUID** to bind to the object directly.</span></span>


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



<span data-ttu-id="f6f9f-149">donde xxx es el valor devuelto por la propiedad GUID.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-149">where xxx is the value returned from the GUID property.</span></span> <span data-ttu-id="f6f9f-150">Para obtener más información, vea [usar objectGUID para enlazar a un objeto](/windows/desktop/AD/using-objectguid-to-bind-to-an-object).</span><span class="sxs-lookup"><span data-stu-id="f6f9f-150">For more information, see [Using objectGUID to Bind to an Object](/windows/desktop/AD/using-objectguid-to-bind-to-an-object).</span></span> <span data-ttu-id="f6f9f-151">Tenga en cuenta que si usa un GUID para enlazar a un objeto, el método de la propiedad **ADsPath** devuelve valores distintos de los valores normales que se devolverían si usara un nombre distintivo (DN) para enlazar al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-151">Be aware that if you use a GUID to bind to an object, the **ADsPath** property method returns values that are different from the normal values that would be returned if you used a distinguished name (DN) to bind to the same object.</span></span> <span data-ttu-id="f6f9f-152">Por ejemplo, en la tabla siguiente se enumeran los valores devueltos al usar los dos métodos de enlace diferentes para enlazar al mismo objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-152">For example, the following table lists the values returned when using the two different binding methods to bind to the same user object.</span></span>



|             | <span data-ttu-id="f6f9f-153">Enlazar mediante DN</span><span class="sxs-lookup"><span data-stu-id="f6f9f-153">Bind using DN</span></span>                                           | <span data-ttu-id="f6f9f-154">Enlazar mediante GUID</span><span class="sxs-lookup"><span data-stu-id="f6f9f-154">Bind using GUID</span></span>                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f6f9f-155">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-155">**Name**</span></span>    | <span data-ttu-id="f6f9f-156">CN = Jeff Smith</span><span class="sxs-lookup"><span data-stu-id="f6f9f-156">CN=Jeff Smith</span></span>                                           | <span data-ttu-id="f6f9f-157">CN = Jeff Smith</span><span class="sxs-lookup"><span data-stu-id="f6f9f-157">CN=Jeff Smith</span></span>                                               |
| <span data-ttu-id="f6f9f-158">**Parent**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-158">**Parent**</span></span>  | <span data-ttu-id="f6f9f-159">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span><span class="sxs-lookup"><span data-stu-id="f6f9f-159">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span></span>               | <span data-ttu-id="f6f9f-160">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span><span class="sxs-lookup"><span data-stu-id="f6f9f-160">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span></span>                   |
| <span data-ttu-id="f6f9f-161">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-161">**ADsPath**</span></span> | <span data-ttu-id="f6f9f-162">LDAP://server/CN=Jeff Smith, CN = users, DC = Fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="f6f9f-162">LDAP://server/CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=com</span></span> | <span data-ttu-id="f6f9f-163">LDAP://server/<GUID = c0f59dfcf507d311a99e0000f879f7c7></span><span class="sxs-lookup"><span data-stu-id="f6f9f-163">LDAP://server/<GUID=c0f59dfcf507d311a99e0000f879f7c7></span></span> |



 

> [!Note]  
> <span data-ttu-id="f6f9f-164">El proveedor de WinNT no admite el enlace con el **GUID** del objeto y devuelve la propiedad **GUID** en un formato de cadena ligeramente diferente.</span><span class="sxs-lookup"><span data-stu-id="f6f9f-164">The WinNT provider does not support binding using the object **GUID**, and returns the **GUID** property in a slightly different string format.</span></span>

 

## <a name="examples"></a><span data-ttu-id="f6f9f-165">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f6f9f-165">Examples</span></span>

<span data-ttu-id="f6f9f-166">En el ejemplo de código siguiente se muestra cómo recuperar datos de objeto mediante métodos de propiedad de la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="f6f9f-166">The following code example shows how to retrieve object data using property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


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



<span data-ttu-id="f6f9f-167">En el ejemplo de código siguiente se muestra cómo recuperar datos de objeto mediante métodos de propiedad de la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="f6f9f-167">The following code example shows how to retrieve object data using property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


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



<span data-ttu-id="f6f9f-168">En el ejemplo de código siguiente se muestra cómo trabajar con los métodos de propiedad de la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="f6f9f-168">The following code example shows how to work with the property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f6f9f-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6f9f-169">Requirements</span></span>



| <span data-ttu-id="f6f9f-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6f9f-170">Requirement</span></span> | <span data-ttu-id="f6f9f-171">Value</span><span class="sxs-lookup"><span data-stu-id="f6f9f-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f9f-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6f9f-172">Minimum supported client</span></span><br/> | <span data-ttu-id="f6f9f-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6f9f-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f6f9f-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6f9f-174">Minimum supported server</span></span><br/> | <span data-ttu-id="f6f9f-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6f9f-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f6f9f-176">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6f9f-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6f9f-177"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6f9f-177"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="f6f9f-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6f9f-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6f9f-179"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6f9f-179"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="f6f9f-180">IID</span><span class="sxs-lookup"><span data-stu-id="f6f9f-180">IID</span></span><br/>                      | <span data-ttu-id="f6f9f-181">El IID \_ de IID se define como FD8256D0-FD15-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="f6f9f-181">IID\_IADs is defined as FD8256D0-FD15-11CE-ABC4-02608C9E7553</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f6f9f-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6f9f-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6f9f-183">**IADs**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-183">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="f6f9f-184">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="f6f9f-184">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 

