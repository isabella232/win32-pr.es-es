---
description: Cambia los permisos de seguridad para el archivo de dispositivo especificado en la ruta de acceso del objeto (este método es una versión extendida del método ChangeSecurityPermissions).
ms.assetid: 5ad54470-6961-4c0d-9d2a-d3eaf81d75f4
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx de la clase CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f2c7261844542f6414052517432c2e8ff3f1194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153232"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_devicefile-class"></a>Método ChangeSecurityPermissionsEx de la \_ clase DeviceFile de CIM

El método **ChangeSecurityPermissionsEx** cambia los permisos de seguridad para el archivo de dispositivo especificado en la ruta de acceso del objeto (este método es una versión extendida del método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md) ). Si el archivo lógico es un directorio, este método actúa de forma recursiva y cambia los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio. Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

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

> [!Caution]  
> Una ACL **nula** en la estructura del [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado.

 

</dd> <dt>

*Opción* \[ de de\]
</dt> <dd>

Privilegio de seguridad que se va a modificar. Por ejemplo, para cambiar la seguridad de la DACL y el propietario, use

`Option = 1 + 4`

or

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)


</dt> <dd>

Cambiar el propietario del archivo lógico.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)


</dt> <dd>

Cambiar el grupo del archivo lógico.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)


</dt> <dd>

Cambie la ACL del archivo lógico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)


</dt> <dd>

Cambie la ACL del sistema del archivo lógico.

</dd> </dl> </dd> <dt>

*StopFileName* \[ enuncia\]
</dt> <dd>

Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método. Este parámetro es **null** si el método se ejecuta correctamente.

</dd> <dt>

*StartFileName* \[ en, opcional\]
</dt> <dd>

Archivo secundario (o directorio) que se va a usar como punto de partida para este método. Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior. Si este parámetro es **null**, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> <dt>

*Recursivo* \[ en, opcional\]
</dt> <dd>

Si es **true**, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ DeviceFile de CIM**](cim-devicefile.md) . En el caso de las instancias de archivo, este parámetro se omite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.

<dl> <dt>


</dt> <dd>

0

Correcto.

</dd> <dt>


</dt> <dd>

2

Acceso denegado.

</dd> <dt>


</dt> <dd>

8

Error no especificado.

</dd> <dt>


</dt> <dd>

9

Objeto no válido.

</dd> <dt>


</dt> <dd>

10

El objeto ya existe.

</dd> <dt>


</dt> <dd>

11

Sistema de archivos no NTFS.

</dd> <dt>


</dt> <dd>

12

Plataforma no Windows.

</dd> <dt>


</dt> <dd>

13

La unidad no es la misma.

</dd> <dt>


</dt> <dd>

14

El directorio no está vacío.

</dd> <dt>


</dt> <dd>

15

Infracción de uso compartido.

</dd> <dt>


</dt> <dd>

16

Archivo de inicio no válido.

</dd> <dt>


</dt> <dd>

17

Privilegio no mantenido.

</dd> <dt>


</dt> <dd>

21

Parámetro no válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este método no está implementado actualmente por WMI. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

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

[\_DEVICEFILE CIM](changesecuritypermissionsex-method-in-class-cim-devicefile.md)
</dt> <dt>

[**\_DEVICEFILE CIM**](cim-devicefile.md)
</dt> </dl>

 

