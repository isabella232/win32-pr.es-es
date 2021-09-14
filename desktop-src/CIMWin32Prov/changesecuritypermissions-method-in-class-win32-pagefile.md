---
description: Cambia los permisos de seguridad para el archivo de paginación lógico especificado en la ruta de acceso del objeto.
ms.assetid: 3abdfa1d-49d8-4676-b7a5-3be528938ec4
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions de la Win32_PageFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc30d8780f7c0573b9a63ff83f16ad46b9d2a70f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361472"
---
# <a name="changesecuritypermissions-method-of-the-win32_pagefile-class"></a>Método ChangeSecurityPermissions de la clase PageFile de Win32 \_

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** cambia los permisos de seguridad para el archivo de paginación lógico especificado en la ruta de acceso del objeto. Si el archivo lógico es un directorio, **ChangeSecurityPermissions es recursivo** y cambia los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.

En este tema se Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SecurityDescriptor* \[ En\]
</dt> <dd>

Expresión que se resuelve en una instancia de [**\_ SecurityDescriptor de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Este descriptor contiene nuevos permisos de seguridad para la instancia de [**\_ PageFile de Win32.**](win32-pagefile.md)

</dd> <dt>

*Opción* \[ En\]
</dt> <dd>

Privilegio de seguridad que se va a modificar. Por ejemplo, para cambiar la seguridad de la lista de control de acceso discrecional (DACL) y del propietario, use:

`Option = 1 + 4`

O bien

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CAMBIO \_ INFORMACIÓN \_ DE SEGURIDAD DEL \_ PROPIETARIO** (1)


</dt> <dd>

Cambie el propietario del archivo lógico.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CAMBIO \_ INFORMACIÓN \_ DE \_ SEGURIDAD DE** GRUPO (2)


</dt> <dd>

Cambie el grupo del archivo lógico.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CAMBIO \_ INFORMACIÓN DE \_ SEGURIDAD \_ DE DACL** (4)


</dt> <dd>

Cambie la DACL del archivo lógico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CAMBIO \_ INFORMACIÓN DE \_ SEGURIDAD \_ DE SACL** (8)


</dt> <dd>

Cambie la lista de control de acceso del sistema (SACL) del archivo lógico.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se cambian los permisos y un número diferente para indicar un error.

<dl> <dt>

**Success**
</dt> <dd>

0

La solicitud se realiza correctamente.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

2

Acceso denegado.

</dd> <dt>

**Error no especificado**
</dt> <dd>

8

Error no especificado.

</dd> <dt>

**Objeto no válido**
</dt> <dd>

9

El nombre especificado no es válido.

</dd> <dt>

**El objeto ya existe**
</dt> <dd>

10

El objeto especificado ya existe

</dd> <dt>

**Sistema de archivos no NTFS**
</dt> <dd>

11

El sistema de archivos no es un sistema de archivos NTFS.

</dd> <dt>

**Plataforma no NT/Windows 2000**
</dt> <dd>

12

La plataforma no está Windows.

</dd> <dt>

**La unidad no es la misma**
</dt> <dd>

13

La unidad no es la misma.

</dd> <dt>

**El directorio no está vacío**
</dt> <dd>

14

El directorio no está vacío.

</dd> <dt>

**Infracción de uso compartido**
</dt> <dd>

15

Hay una infracción de uso compartido.

</dd> <dt>

**Archivo de inicio no válido**
</dt> <dd>

16

El archivo de inicio especificado no es válido.

</dd> <dt>

**Privilegios no mantenidos**
</dt> <dd>

17

Falta un privilegio necesario para la operación.

</dd> <dt>

**parámetro no válido**
</dt> <dd>

21

Un parámetro especificado no es válido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ PageFile**](win32-pagefile.md)
</dt> </dl>

 

