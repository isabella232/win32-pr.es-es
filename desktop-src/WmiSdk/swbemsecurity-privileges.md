---
description: La propiedad Privileges es un objeto SWbemPrivilegeSet. Esta propiedad se usa para habilitar o deshabilitar privilegios de Windows específicos. Es posible que tenga que establecer uno de estos privilegios para realizar tareas específicas mediante la API Windows Management Instrumentation (WMI).
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: Propiedad SWbemSecurity.Privileges (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.Privileges
- ISWbemSecurity.Privileges
- ISWbemSecurity.get_Privileges
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a4b2ca68f0377616d693c677281b90f2e4650fcacc941e205e1732ae5a91e4b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897505"
---
# <a name="swbemsecurityprivileges-property"></a>Propiedad SWbemSecurity.Privileges

La **propiedad Privileges** es [**un objeto SWbemPrivilegeSet.**](swbemprivilegeset.md) Esta propiedad se usa para habilitar o deshabilitar privilegios de Windows específicos. Es posible que tenga que establecer uno de estos privilegios para realizar tareas específicas mediante la API Windows Management Instrumentation (WMI).

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Esta configuración permite conceder o revocar privilegios como parte de una cadena de moniker WMI. Para obtener la lista completa de valores aplicables, [**vea WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) and [**Privilege Constants**](privilege-constants.md).

Puede cambiar los privilegios definidos para los objetos [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet,**](swbemobjectset.md) [**SWbemObjectPath**](swbemobjectpath.md)y [**SwbemLocator**](swbemlocator.md) agregando objetos [**SWbemPrivilege**](swbemprivilege.md) a la **propiedad Privileges.**

Hay diferencias fundamentales en la forma en que las distintas versiones Windows los cambios en los privilegios. Si está desarrollando una aplicación que solo se usa en Windows plataformas, puede establecer o revocar privilegios en cualquier momento.

En el ejemplo siguiente se establece **SeDebugPrivilege en** la conexión de moniker inicial para obtener [**un objeto SWbemServices.**](swbemservices.md)


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



Para obtener más información sobre cómo dar formato a la cadena de seguridad para una conexión de moniker, vea [**Constantes de privilegios**](privilege-constants.md).

En el ejemplo siguiente se realiza la misma tarea, pero se establece el privilegio después del inicio de sesión inicial en WMI.


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



Tenga en cuenta que para las llamadas a [**SwbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md), debe usar el nombre completo del privilegio de seguridad, por ejemplo, "SeDebugPrivilege" en lugar de "Debug".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSecurity<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemSecurity<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Ejecución de operaciones con privilegios](executing-privileged-operations.md)
</dt> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> </dl>

 

 




