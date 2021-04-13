---
description: La propiedad privileges es un objeto SWbemPrivilegeSet. Esta propiedad se usa para habilitar o deshabilitar privilegios específicos de Windows. Es posible que tenga que establecer uno de estos privilegios para realizar tareas específicas mediante la API de Instrumental de administración de Windows (WMI).
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: Propiedad SWbemSecurity. Privileges (Wbemdisp. h)
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
ms.openlocfilehash: 6fd8e1c0f9b6667b49d0956bcea5ac9e187443d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276115"
---
# <a name="swbemsecurityprivileges-property"></a>Propiedad SWbemSecurity. privileges

La propiedad **privileges** es un objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) . Esta propiedad se usa para habilitar o deshabilitar privilegios específicos de Windows. Es posible que tenga que establecer uno de estos privilegios para realizar tareas específicas mediante la API de Instrumental de administración de Windows (WMI).

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Esta configuración permite conceder o revocar privilegios como parte de una cadena de moniker WMI. Para obtener una lista completa de los valores aplicables, consulte [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) y las [**constantes de privilegios**](privilege-constants.md).

Puede cambiar los privilegios definidos para los objetos [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)y [**SwbemLocator**](swbemlocator.md) agregando objetos [**SWbemPrivilege**](swbemprivilege.md) a la propiedad **privileges** .

Hay diferencias fundamentales en el modo en que las distintas versiones de Windows controlan los cambios en los privilegios. Si está desarrollando una aplicación que solo se usa en plataformas Windows, puede establecer o revocar los privilegios en cualquier momento.

En el ejemplo siguiente se establece **SeDebugPrivilege** en la conexión de moniker inicial para obtener un objeto [**SWbemServices**](swbemservices.md) .


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



Para obtener más información sobre cómo dar formato a la cadena de seguridad para una conexión de moniker, vea [**constantes de privilegios**](privilege-constants.md).

En el ejemplo siguiente se realiza la misma tarea, pero se establece el privilegio después del inicio de sesión inicial en WMI.


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



Tenga en cuenta que para las llamadas a [**SwbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md), debe usar el nombre completo del privilegio de seguridad, por ejemplo, "SeDebugPrivilege" en lugar de "debug".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSecurity<br/>                                                         |
| IID<br/>                      | \_ISWBEMSECURITY IID<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Ejecutar operaciones con privilegios](executing-privileged-operations.md)
</dt> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> </dl>

 

 




