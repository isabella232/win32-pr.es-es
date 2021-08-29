---
description: Cambia los permisos de seguridad para el archivo de dispositivo lógico especificado en la ruta de acceso del objeto.
ms.assetid: 4b3e1a0e-3c9e-45bb-8c7b-cbbc8f9d1265
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions de la CIM_DeviceFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 91b5fa3284b39729d87550f508fbad4fdf339d211f5a6beec429ef18095ff0e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925055"
---
# <a name="changesecuritypermissions-method-of-the-cim_devicefile-class"></a>Método ChangeSecurityPermissions de la clase \_ DeviceFile de CIM

El **método ChangeSecurityPermissions** cambia los permisos de seguridad para el archivo de dispositivo lógico especificado en la ruta de acceso del objeto. Si el archivo lógico es un directorio, este método actuará de forma recursiva, cambiando los permisos de seguridad para todos los archivos y subdirectorios que contiene el directorio. Este método se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

Especifica la información de seguridad.

> [!Caution]  
> Una **lista de** control de acceso (ACL) NULL en la estructura DESCRIPTOR DE [**\_ SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado.

 

</dd> <dt>

*Opción* \[ En\]
</dt> <dd>

Privilegio de seguridad que se modificará. Por ejemplo, para cambiar el propietario y la seguridad de DACL, use:

`Option = 1 + 4`

o

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CAMBIO \_ INFORMACIÓN \_ DE \_ SEGURIDAD DEL** PROPIETARIO (1)


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

Cambie la ACL del archivo lógico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CAMBIO \_ INFORMACIÓN DE \_ SEGURIDAD \_ DE SACL** (8)


</dt> <dd>

Cambie la ACL del sistema del archivo lógico.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error.

<dl> <dt>

**Success**
</dt> <dd>

0

Correcto.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

2

Acceso denegado:

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

**Privilegios no mantenidos**
</dt> <dd>

17

Privilegios no mantenidos.

</dd> <dt>

**parámetro no válido**
</dt> <dd>

21

Parámetro no válido.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ DeviceFile**](changesecuritypermissions-method-in-class-cim-devicefile.md)
</dt> <dt>

[**CIM \_ DeviceFile**](cim-devicefile.md)
</dt> </dl>

 

