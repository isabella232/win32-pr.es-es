---
title: Métodos de la propiedad IADsSecurityDescriptor (iAds. h)
description: Los métodos de propiedad de la interfaz IADsSecurityDescriptor obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: e0c50740-de98-4913-b3df-6fd53263bcc8
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsSecurityDescriptor ADSI
topic_type:
- apiref
api_name:
- IADsSecurityDescriptor Property Methods
- IADsSecurityDescriptor.Revision
- IADsSecurityDescriptor.get_Revision
- IADsSecurityDescriptor.put_Revision
- IADsSecurityDescriptor.Control
- IADsSecurityDescriptor.get_Control
- IADsSecurityDescriptor.put_Control
- IADsSecurityDescriptor.Owner
- IADsSecurityDescriptor.get_Owner
- IADsSecurityDescriptor.put_Owner
- IADsSecurityDescriptor.OwnerDefaulted
- IADsSecurityDescriptor.get_OwnerDefaulted
- IADsSecurityDescriptor.put_OwnerDefaulted
- IADsSecurityDescriptor.Group
- IADsSecurityDescriptor.get_Group
- IADsSecurityDescriptor.put_Group
- IADsSecurityDescriptor.GroupDefaulted
- IADsSecurityDescriptor.get_GroupDefaultedY
- IADsSecurityDescriptor.put_GroupDefaulted
- IADsSecurityDescriptor.DiscretionaryAcl
- IADsSecurityDescriptor.get_DiscretionaryAcl
- IADsSecurityDescriptor.put_DiscretionaryAcl
- IADsSecurityDescriptor.DaclDefaulted
- IADsSecurityDescriptor.get_DaclDefaulted
- IADsSecurityDescriptor.put_DaclDefaulted
- IADsSecurityDescriptor.SystemAcl
- IADsSecurityDescriptor.get_SystemAcl
- IADsSecurityDescriptor.put_SystemAcl
- IADsSecurityDescriptor.SaclDefaulted
- IADsSecurityDescriptor.get_SaclDefaulted
- IADsSecurityDescriptor.put_SaclDefaulted
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5c07213a2d2a3a1b64621dbc40f707b0900703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150202"
---
# <a name="iadssecuritydescriptor-property-methods"></a><span data-ttu-id="ffa7d-105">Métodos de propiedad IADsSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="ffa7d-105">IADsSecurityDescriptor Property Methods</span></span>

<span data-ttu-id="ffa7d-106">Los métodos de propiedad de la interfaz [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) obtienen o establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-106">The property methods of the [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="ffa7d-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ffa7d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ffa7d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ffa7d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="ffa7d-109">**Control**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-109">**Control**</span></span>
<span data-ttu-id="ffa7d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ffa7d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="ffa7d-111">Marcas que califican el significado del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-111">Flags that qualify the meaning of the security descriptor.</span></span> <span data-ttu-id="ffa7d-112">Los valores se toman de la estructura de [**\_ \_ control de descriptores de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) de Win32.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-112">Values are taken from the Win32 [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) structure.</span></span>

<dt>

<span data-ttu-id="ffa7d-113">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ffa7d-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ffa7d-114">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Control(
  [out] LONG* plControl
);
HRESULT put_Control(
  [in] LONG lControl
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa7d-115">**DaclDefaulted**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-115">**DaclDefaulted**</span></span>
<span data-ttu-id="ffa7d-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ffa7d-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="ffa7d-117">Marca del tipo BOOL que indica si la DACL se deriva de un mecanismo predeterminado, en lugar de proporcionarse explícitamente por el proveedor original del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-117">A flag of the BOOL type that indicates if the DACL is derived from a default mechanism, rather than being provided explicitly by the original provider of the security descriptor.</span></span> <span data-ttu-id="ffa7d-118">Por ejemplo, si el creador de un objeto no especifica una DACL, el objeto recibe la DACL predeterminada del token de acceso del creador.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-118">For example, if an object's creator does not specify a DACL, the object receives the default DACL from the creator's access token.</span></span> <span data-ttu-id="ffa7d-119">Esta marca puede afectar a la forma en que el sistema trata la DACL con respecto a la herencia de ACE.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-119">This flag can affect how the system treats the DACL, with respect to ACE inheritance.</span></span> <span data-ttu-id="ffa7d-120">El sistema omite esta marca si \_ \_ no se ha establecido la marca de DACL de este.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-120">The system ignores this flag if the SE\_DACL\_PRESENT flag is not set.</span></span>

<dt>

<span data-ttu-id="ffa7d-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ffa7d-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ffa7d-122">Tipo de datos de scripting: **variante \_ bool**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-122">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DaclDefaulted(
  [out] VARIANT_BOOL* fDaclDefaulted
);
HRESULT put_DaclDefaulted(
  [in] VARIANT_BOOL fDaclDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa7d-123">**DiscretionaryAcl**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-123">**DiscretionaryAcl**</span></span>
<span data-ttu-id="ffa7d-124"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ffa7d-124"></dt> <dd> <dl></span></span>

<span data-ttu-id="ffa7d-125">Lista de control de acceso discrecional (DACL) que especifica los tipos de acceso concedidos al objeto para usuarios y grupos especificados.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-125">Discretionary access-control list (DACL) that specifies the types of access granted to the object for specified users and groups.</span></span> <span data-ttu-id="ffa7d-126">Para obtener más información acerca de las DACL, vea [DACL NULL y DACL vacías](/windows/desktop/AD/null-dacls-and-empty-dacls).</span><span class="sxs-lookup"><span data-stu-id="ffa7d-126">For more information about DACLs, see [Null DACLs and Empty DACLs](/windows/desktop/AD/null-dacls-and-empty-dacls).</span></span>

<dt>

<span data-ttu-id="ffa7d-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ffa7d-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ffa7d-128">Tipo de datos de scripting: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-128">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DiscretionaryAcl(
  [out] IDispatch** ppIDispDACL
);
HRESULT put_DiscretionaryAcl(
  [in] IDispatch* pIDispDACL
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa7d-129">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-129">**Group**</span></span>
<span data-ttu-id="ffa7d-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ffa7d-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="ffa7d-131">Grupo al que pertenece el identificador de seguridad del propietario.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-131">Group to which the owner's security ID belongs.</span></span>

<dt>

<span data-ttu-id="ffa7d-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ffa7d-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ffa7d-133">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Group(
  [out] BSTR* pbstrGroupl
);
HRESULT put_Group(
  [in] BSTR bstrGroup
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa7d-134">**GroupDefaulted**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-134">**GroupDefaulted**</span></span>
<span data-ttu-id="ffa7d-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ffa7d-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="ffa7d-136">Marca del tipo BOOL que indica si los datos del grupo se derivan de un mecanismo predeterminado, en lugar de que el proveedor original del descriptor de seguridad lo proporcione explícitamente.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-136">A flag of the BOOL type that indicates if the group data is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span>

<dt>

<span data-ttu-id="ffa7d-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ffa7d-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ffa7d-138">Tipo de datos de scripting: **variante \_ bool**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-138">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GroupDefaultedY(
  [out] VARIANT_BOOL* fGroupDefaulted
);
HRESULT put_GroupDefaulted(
  [in] VARIANT_BOOL fGroupDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa7d-139">**Propietario**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-139">**Owner**</span></span>
<span data-ttu-id="ffa7d-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ffa7d-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="ffa7d-141">Propietario del objeto.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-141">Object owner.</span></span>

<dt>

<span data-ttu-id="ffa7d-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ffa7d-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ffa7d-143">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwnerl
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa7d-144">**OwnerDefaulted**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-144">**OwnerDefaulted**</span></span>
<span data-ttu-id="ffa7d-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ffa7d-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="ffa7d-146">Marca del tipo BOOL que indica que los datos del propietario se derivan de un mecanismo predeterminado, en lugar de que el proveedor original del descriptor de seguridad lo proporcione explícitamente.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-146">A flag of the BOOL type that indicates that the owner data is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span>

<dt>

<span data-ttu-id="ffa7d-147">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ffa7d-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ffa7d-148">Tipo de datos de scripting: **variante \_ bool**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-148">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OwnerDefaulted(
  [out] VARIANT_BOOL* fOwnerDefaulted
);
HRESULT put_OwnerDefaulted(
  [in] VARIANT_BOOL fOwnerDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa7d-149">**Revisión**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-149">**Revision**</span></span>
<span data-ttu-id="ffa7d-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ffa7d-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="ffa7d-151">Nivel de revisión del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-151">Revision level of the security descriptor.</span></span> <span data-ttu-id="ffa7d-152">Este valor se toma de la estructura [**de \_ \_ información de la revisión ACL**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) de Win32.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-152">This value is taken from the Win32 [**ACL\_REVISION\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) structure.</span></span> <span data-ttu-id="ffa7d-153">Todas las ACE de una ACL deben estar en el mismo nivel de revisión.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-153">All ACEs in an ACL must be at the same revision level.</span></span>

<dt>

<span data-ttu-id="ffa7d-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ffa7d-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ffa7d-155">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-155">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Revision(
  [out] LONG* plRevision
);
HRESULT put_Revision(
  [in] LONG lRevision
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa7d-156">**SaclDefaulted**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-156">**SaclDefaulted**</span></span>
<span data-ttu-id="ffa7d-157"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ffa7d-157"></dt> <dd> <dl></span></span>

<span data-ttu-id="ffa7d-158">Marca del tipo BOOL que indica que la SACL se deriva de un mecanismo predeterminado, en lugar de que el proveedor original del descriptor de seguridad lo proporcione explícitamente.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-158">A flag of the BOOL type that indicates that the SACL is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span> <span data-ttu-id="ffa7d-159">Esta marca puede afectar al modo en que el sistema controla la SACL con respecto a la herencia de ACE.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-159">This flag can affect how the system handles the SACL, with respect to ACE inheritance.</span></span> <span data-ttu-id="ffa7d-160">El sistema omite esta marca si \_ \_ no se ha establecido la marca de SACL de se presente.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-160">The system ignores this flag if the SE\_SACL\_PRESENT flag is not set.</span></span>

<dt>

<span data-ttu-id="ffa7d-161">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ffa7d-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ffa7d-162">Tipo de datos de scripting: **variante \_ bool**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-162">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SaclDefaulted(
  [out] VARIANT_BOOL* fSaclDefaulted
);
HRESULT put_SaclDefaulted(
  [in] VARIANT_BOOL fSaclDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa7d-163">**SystemAcl**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-163">**SystemAcl**</span></span>
<span data-ttu-id="ffa7d-164"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ffa7d-164"></dt> <dd> <dl></span></span>

<span data-ttu-id="ffa7d-165">Lista de control de acceso del sistema utilizada para generar registros de auditoría para el objeto.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-165">System access-control list used to generate audit records for the object.</span></span>

<dt>

<span data-ttu-id="ffa7d-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ffa7d-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ffa7d-167">Tipo de datos de scripting: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-167">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SystemAcl(
  [out] IDispatch** ppIDispSACL
);
HRESULT put_SystemAcl(
  [in] IDispatch* pIDispSACL
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="ffa7d-168">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ffa7d-168">Examples</span></span>

<span data-ttu-id="ffa7d-169">En el ejemplo de código siguiente se muestra cómo enumerar un descriptor de seguridad existente.</span><span class="sxs-lookup"><span data-stu-id="ffa7d-169">The following code example shows how to enumerate an existing security descriptor.</span></span>


```VB
Dim ou As IADs
Dim sd As IADsSecurityDescriptor
Dim dacl As IADsAccessControlList
Dim sacl As IADsAccessControlList

On Error GoTo Cleanup 
 
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = ou.Get("ntSecurityDescriptor")
Debug.Print sd.Owner
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
Set dacl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
' Add code to perform an operation with the Discretionary and System ACLs.

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
    Set sd = Nothing
    Set dacl = Nothing
    Set sacl = Nothing
```



## <a name="requirements"></a><span data-ttu-id="ffa7d-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffa7d-170">Requirements</span></span>



| <span data-ttu-id="ffa7d-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffa7d-171">Requirement</span></span> | <span data-ttu-id="ffa7d-172">Value</span><span class="sxs-lookup"><span data-stu-id="ffa7d-172">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa7d-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffa7d-173">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa7d-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffa7d-174">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="ffa7d-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffa7d-175">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa7d-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffa7d-176">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ffa7d-177">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffa7d-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffa7d-178"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffa7d-178"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="ffa7d-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ffa7d-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffa7d-180"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffa7d-180"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="ffa7d-181">IID</span><span class="sxs-lookup"><span data-stu-id="ffa7d-181">IID</span></span><br/>                      | <span data-ttu-id="ffa7d-182">IID \_ IADsSecurityDescriptor se define como B8C787CA-9BDD-11D0-852C-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="ffa7d-182">IID\_IADsSecurityDescriptor is defined as B8C787CA-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ffa7d-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffa7d-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa7d-184">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-184">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[<span data-ttu-id="ffa7d-185">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-185">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="ffa7d-186">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="ffa7d-186">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> </dl>

 

