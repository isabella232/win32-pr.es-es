---
description: Cambia los permisos de seguridad para el archivo de datos lógico especificado en la ruta de acceso del objeto (este método es una versión extendida del método ChangeSecurityPermissions).
ms.assetid: baf50a6e-f624-464e-946d-975aeba88ac2
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx de la CIM_DataFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e66efe81f8b45c2339dc511d283b2f349360061b580b60308c3e69b3e6c0b0cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010019"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_datafile-class"></a>Método ChangeSecurityPermissionsEx de la clase \_ DataFile de CIM

El **método ChangeSecurityPermissionsEx** cambia los permisos de seguridad para el archivo de datos lógico especificado en la ruta de acceso del objeto (este método es una versión extendida del [**método ChangeSecurityPermissions).**](changesecuritypermissions-method-in-class-cim-datafile.md) Si el archivo lógico es realmente un directorio, este método actuará de forma recursiva, cambiando los permisos de seguridad para todos los archivos y subdirectorios que contiene el directorio.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

*SecurityDescriptor* \[ En\]
</dt> <dd>

Especifica información de seguridad.

> [!Note]  
> Una **ACL NULL** en la estructura DESCRIPTOR DE [**\_ SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado. Para obtener más información sobre las implicaciones del acceso ilimitado, vea [Crear un descriptor de seguridad para un nuevo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

*Opción* \[ En\]
</dt> <dd>

Privilegio de seguridad que se debe modificar. Por ejemplo, para cambiar el propietario y la seguridad de DACL, use:

`Option = 1 + 4` o `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

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

Cambie la ACL del archivo lógico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CAMBIO \_ INFORMACIÓN DE \_ SEGURIDAD \_ DE SACL** (8)


</dt> <dd>

Cambie la ACL del sistema del archivo lógico.

</dd> </dl> </dd> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Cadena que representa el nombre del archivo (o directorio) en el que se ha fallado el método. Este parámetro es **NULL** si el método se realiza correctamente.

</dd> <dt>

*StartFileName* \[ in, opcional\]
</dt> <dd>

Cadena que representa el archivo secundario (o directorio) que se va a usar como punto de partida para este método. Normalmente, el *parámetro StartFileName* es el *parámetro StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior. Si este parámetro es **null,** la operación se realiza en el archivo (o directorio) especificado en la **llamada a ExecMethod.**

Si *se usa StartFileName,* *Recursive* también debe establecerse en true.

</dd> <dt>

*Recursiva* \[ in, opcional\]
</dt> <dd>

Si **es True**, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ DataFile de CIM.**](cim-datafile.md) En el caso de las instancias de archivo, este parámetro se omite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

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

El nombre de objeto especificado no es válido.

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

El archivo de inicio no es válido.

</dd> <dt>

**Privilegios no mantenidos**
</dt> <dd>

17

Privilegio no mantenido.

</dd> <dt>

**parámetro no válido**
</dt> <dd>

21

Un parámetro no es válido.

</dd> </dl>

## <a name="remarks"></a>Comentarios

WMI implementa el método **ChangeSecurityPermissionsEx** [**en CIM \_ DataFile.**](cim-datafile.md)

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Archivo de datos CIM \_**](changesecuritypermissionsex-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[Tareas wmi: archivos y carpetas](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Constantes de derechos de acceso a archivos y directorios**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

