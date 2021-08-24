---
title: Win32_VirtualDesktopSession clase
description: Administra una sesión de escritorio virtual.
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Win32_VirtualDesktopSession clase Servicios de Escritorio remoto
- Win32_VirtualDesktopSession clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession.VMHostName
- Win32_VirtualDesktopSession.SessionId
- Win32_VirtualDesktopSession.VMName
- Win32_VirtualDesktopSession.ConnectState
- Win32_VirtualDesktopSession.UserName
- Win32_VirtualDesktopSession.DomainName
- Win32_VirtualDesktopSession.CollectionId
- Win32_VirtualDesktopSession.ClientMachineName
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e039df658ded4534e3e2582f08ba4e5f5a04530d810349fff5633730a84332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137428"
---
# <a name="win32_virtualdesktopsession-class"></a>Clase VirtualDesktopSession de Win32 \_

Administra una sesión de escritorio virtual.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_VirtualDesktopSession
{
  string VMHostName;
  uint32 SessionId;
  string VMName;
  uint32 ConnectState;
  string UserName;
  string DomainName;
  string CollectionId;
  string ClientMachineName;
};
```

## <a name="members"></a>Miembros

La **clase \_ VirtualDesktopSession de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ VirtualDesktopSession de Win32** tiene estos métodos.



| Método                                                         | Descripción                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**Desconectar**](disconnect-win32-virtualdesktopsession.md)   | Desconecta la sesión de escritorio virtual.<br/>                        |
| [**Cerrar sesión**](logoff-win32-virtualdesktopsession.md)           | Cierra la sesión del usuario de escritorio virtual.<br/>             |
| [**SendMessage**](sendmessage-win32-virtualdesktopsession.md) | Envíe un mensaje al usuario a través de la sesión de escritorio virtual.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ VirtualDesktopSession de Win32** tiene estas propiedades.

<dl> <dt>

**ClientMachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el nombre del equipo cliente que está conectado a la sesión.

</dd> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el nombre de la colección de escritorios virtuales que hospeda la máquina virtual.

</dd> <dt>

**ConnectState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el estado de la conexión a la sesión.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el nombre de dominio del usuario.

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene el identificador de la sesión de escritorio virtual.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el nombre de la cuenta de usuario asignada a la sesión.

</dd> <dt>

**VMHostName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene el nombre del servidor host Escritorio remoto virtualización que hospeda la máquina virtual.

</dd> <dt>

**VMName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el nombre de la máquina virtual que está asignada a la sesión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ cimv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Escritorio remoto Management Services Provider](rdms-api-reference.md)
</dt> </dl>

 

