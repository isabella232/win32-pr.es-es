---
description: Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto (este método es una versión extendida del método ChangeSecurityPermissions).
ms.assetid: 29155533-0898-4f8f-af08-f3ea46c8c1d3
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx de la clase CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af2dc82ef54b6f32eee20f17cd61c0769cc64b1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538787"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_logicalfile-class"></a>Método ChangeSecurityPermissionsEx de la \_ clase LogicalFile de CIM

El método **ChangeSecurityPermissionsEx** cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto (este método es una versión extendida del método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md) ). Si el archivo lógico es un directorio, este método actuará de forma recursiva y cambiará los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SecurityDescriptor* \[ de\]
</dt> <dd>

Especifica la información de seguridad.

</dd> <dt>

*Opción* \[ de de\]
</dt> <dd>

Privilegio de seguridad que se va a modificar. Por ejemplo, para cambiar la seguridad de la DACL y el propietario, use

`Option = 1 + 4`

or

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)


</dt> <dd>

Cambiar el propietario del archivo lógico.

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)


</dt> <dd>

Cambiar el grupo del archivo lógico.

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)


</dt> <dd>

Cambie la ACL del archivo lógico.

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)


</dt> <dd>

Cambie la ACL del sistema del archivo lógico.

</dd> </dl> </dd> <dt>

*StopFileName* \[ enuncia\]
</dt> <dd>

Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método. Este parámetro tiene un valor **null** si el método se ejecuta correctamente.

</dd> <dt>

*StartFileName* \[ en, opcional\]
</dt> <dd>

Cadena que representa el archivo secundario (o directorio) que se va a utilizar como punto de partida para este método. Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo (o directorio) en el que se produjo un error de la llamada al método anterior. Si el valor del parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> <dt>

*Recursivo* \[ en, opcional\]
</dt> <dd>

Si **es true**, los permisos de seguridad se aplican de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) . En el caso de las instancias de archivo, este parámetro se omite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.

<dl> <dt>

**Success**
</dt> <dd>

0

Correcto.

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

Objeto no válido.

</dd> <dt>

**El objeto ya existe**
</dt> <dd>

10

El objeto ya existe.

</dd> <dt>

**Sistema de archivos no NTFS**
</dt> <dd>

11

Sistema de archivos no NTFS.

</dd> <dt>

**Plataforma no NT/Windows 2000**
</dt> <dd>

12

Plataforma no Windows.

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

Infracción de uso compartido.

</dd> <dt>

**Archivo de inicio no válido**
</dt> <dd>

16

Archivo de inicio no válido.

</dd> <dt>

**Privilegio no mantenido**
</dt> <dd>

17

Privilegio no mantenido.

</dd> <dt>

**parámetro no válido**
</dt> <dd>

21

Parámetro no válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este método no está implementado actualmente por WMI. Para usar este método, debe implementarlo en su propio proveedor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_LOGICALFILE CIM**](changesecuritypermissionsex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> </dl>

 

