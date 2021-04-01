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
# <a name="iadssecuritydescriptor-property-methods"></a>Métodos de propiedad IADsSecurityDescriptor

Los métodos de propiedad de la interfaz [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Control**
</dt> <dd> <dl>

Marcas que califican el significado del descriptor de seguridad. Los valores se toman de la estructura de [**\_ \_ control de descriptores de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) de Win32.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
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

**DaclDefaulted**
</dt> <dd> <dl>

Marca del tipo BOOL que indica si la DACL se deriva de un mecanismo predeterminado, en lugar de proporcionarse explícitamente por el proveedor original del descriptor de seguridad. Por ejemplo, si el creador de un objeto no especifica una DACL, el objeto recibe la DACL predeterminada del token de acceso del creador. Esta marca puede afectar a la forma en que el sistema trata la DACL con respecto a la herencia de ACE. El sistema omite esta marca si \_ \_ no se ha establecido la marca de DACL de este.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante \_ bool**
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

**DiscretionaryAcl**
</dt> <dd> <dl>

Lista de control de acceso discrecional (DACL) que especifica los tipos de acceso concedidos al objeto para usuarios y grupos especificados. Para obtener más información acerca de las DACL, vea [DACL NULL y DACL vacías](/windows/desktop/AD/null-dacls-and-empty-dacls).

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **IDispatch**
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

**Grupo**
</dt> <dd> <dl>

Grupo al que pertenece el identificador de seguridad del propietario.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
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

**GroupDefaulted**
</dt> <dd> <dl>

Marca del tipo BOOL que indica si los datos del grupo se derivan de un mecanismo predeterminado, en lugar de que el proveedor original del descriptor de seguridad lo proporcione explícitamente.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante \_ bool**
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

**Propietario**
</dt> <dd> <dl>

Propietario del objeto.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
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

**OwnerDefaulted**
</dt> <dd> <dl>

Marca del tipo BOOL que indica que los datos del propietario se derivan de un mecanismo predeterminado, en lugar de que el proveedor original del descriptor de seguridad lo proporcione explícitamente.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante \_ bool**
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

**Revisión**
</dt> <dd> <dl>

Nivel de revisión del descriptor de seguridad. Este valor se toma de la estructura [**de \_ \_ información de la revisión ACL**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) de Win32. Todas las ACE de una ACL deben estar en el mismo nivel de revisión.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
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

**SaclDefaulted**
</dt> <dd> <dl>

Marca del tipo BOOL que indica que la SACL se deriva de un mecanismo predeterminado, en lugar de que el proveedor original del descriptor de seguridad lo proporcione explícitamente. Esta marca puede afectar al modo en que el sistema controla la SACL con respecto a la herencia de ACE. El sistema omite esta marca si \_ \_ no se ha establecido la marca de SACL de se presente.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante \_ bool**
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

**SystemAcl**
</dt> <dd> <dl>

Lista de control de acceso del sistema utilizada para generar registros de auditoría para el objeto.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **IDispatch**
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

 

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo enumerar un descriptor de seguridad existente.


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IADsSecurityDescriptor se define como B8C787CA-9BDD-11D0-852C-00C04FD8D503<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> </dl>

 

