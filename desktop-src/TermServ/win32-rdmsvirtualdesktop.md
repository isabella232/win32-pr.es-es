---
title: Win32_RDMSVirtualDesktop (clase)
description: Representa un escritorio virtual.
ms.assetid: e2952ec0-38d0-4a1c-b423-3ae1fbc701b3
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktop clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDMSVirtualDesktop de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop.Name
- Win32_RDMSVirtualDesktop.HostName
- Win32_RDMSVirtualDesktop.Status
- Win32_RDMSVirtualDesktop.CollectionAlias
- Win32_RDMSVirtualDesktop.SessionState
- Win32_RDMSVirtualDesktop.SessionUserName
- Win32_RDMSVirtualDesktop.UserName
- Win32_RDMSVirtualDesktop.UserDomain
- Win32_RDMSVirtualDesktop.VMState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247c49c7ad069b4feff3469ac21ec803ebc9f741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676708"
---
# <a name="win32_rdmsvirtualdesktop-class"></a>\_Clase Win32 RDMSVirtualDesktop

Representa un escritorio virtual.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktop
{
  string Name;
  string HostName;
  uint32 Status;
  string CollectionAlias;
  string SessionState;
  string SessionUserName;
  string UserName;
  string UserDomain;
  uint32 VMState;
};
```

## <a name="members"></a>Miembros

La **clase \_ RDMSVirtualDesktop de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ RDMSVirtualDesktop** tiene estos métodos.



| Método                                                                                              | Descripción                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**GetUserAssignment**](getuserassignment-win32-rdmsvirtualdesktop.md)                             | Recupera el nombre de usuario y el nombre de dominio del usuario que está asignado al escritorio virtual.<br/> |
| [**GetVirtualDesktopAssignedToUser**](getvirtualdesktopassignedtouser-win32-rdmsvirtualdesktop.md) | Recupera el escritorio virtual asignado al usuario especificado.<br/>                       |
| [**GetVirtualDesktopDetails**](getvirtualdesktopdetails-win32-rdmsvirtualdesktop.md)               | Recupera la información adicional sobre el escritorio virtual.<br/>                             |
| [**GetVirtualDesktopState**](getvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | Recupera el estado del escritorio virtual.<br/>                                                 |
| [**RemoveUserAssignment**](removeuserassignment-win32-rdmsvirtualdesktop.md)                       | Quita la asignación de usuario del escritorio virtual.<br/>                                       |
| [**SetUserAssignment**](setuserassignment-win32-rdmsvirtualdesktop.md)                             | Asigna un escritorio virtual a un usuario.<br/>                                                        |
| [**SetVirtualDesktopState**](setvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | Actualiza el estado del escritorio virtual.<br/>                                                   |



 

### <a name="properties"></a>Propiedades

La **clase \_ RDMSVirtualDesktop de Win32** tiene estas propiedades.

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtiene el alias de la colección de escritorios virtuales que administra la máquina virtual.

</dd> <dt>

**HostName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el nombre del equipo que hospeda la máquina virtual.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene el nombre de la máquina virtual.

</dd> <dt>

**SqlConnectionString**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtiene el estado de la sesión de escritorio virtual.

</dd> <dt>

**SessionUserName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtiene el nombre de usuario del usuario que ha iniciado sesión en la sesión de escritorio virtual.

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el estado de la máquina virtual.

</dd> <dt>

**UserDomain**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtiene el nombre de dominio del usuario que se asigna al escritorio virtual.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtiene el nombre de usuario asignado al escritorio virtual.

</dd> <dt>

**VMState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el estado del escritorio virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | RDMs raíz de \\ cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Proveedor de servicios de administración de Escritorio remoto](rdms-api-reference.md)
</dt> </dl>

 

