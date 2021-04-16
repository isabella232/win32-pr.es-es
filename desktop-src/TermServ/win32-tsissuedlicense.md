---
title: Win32_TSIssuedLicense (clase)
description: Describe las instancias de Servicios de Escritorio remoto licencias de acceso de cliente por dispositivo (RDS \ 160; Cal por dispositivo) que se emiten desde un servidor de licencias de Escritorio remoto.
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Win32_TSIssuedLicense clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSIssuedLicense de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense
- Win32_TSIssuedLicense.LicenseId
- Win32_TSIssuedLicense.KeyPackId
- Win32_TSIssuedLicense.sIssuedToUser
- Win32_TSIssuedLicense.sIssuedToComputer
- Win32_TSIssuedLicense.LicenseStatus
- Win32_TSIssuedLicense.IssueDate
- Win32_TSIssuedLicense.ExpirationDate
- Win32_TSIssuedLicense.sHardwareId
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d08a68ddcc15a912de4c674403928211a297e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685996"
---
# <a name="win32_tsissuedlicense-class"></a>\_Clase Win32 TSIssuedLicense

Describe las instancias de Servicios de Escritorio remoto licencias de acceso de cliente por dispositivo (cal por dispositivo de RDS) que se emiten desde un servidor de licencias de Escritorio remoto.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSIssuedLicense
{
  uint32   LicenseId;
  uint32   KeyPackId;
  string   sIssuedToUser;
  string   sIssuedToComputer;
  uint32   LicenseStatus;
  DATETIME IssueDate;
  DATETIME ExpirationDate;
  string   sHardwareId;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSIssuedLicense de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ TSIssuedLicense** tiene estos métodos.



| Método                                         | Descripción                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Revocar**](revoke-win32-tsissuedlicense.md) | Revoca las cal por dispositivo de RDS representadas por el **objeto \_ TSIssuedLicense de Win32** .<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSIssuedLicense de Win32** tiene estas propiedades.

<dl> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica la fecha en la que expirará la licencia.

</dd> <dt>

**IssueDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica la fecha en la que se emitió la licencia.

</dd> <dt>

**KeyPackId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica el paquete de claves de licencia de Servicios de Escritorio remoto.

</dd> <dt>

**LicenseId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificador único para esta licencia.

</dd> <dt>

**Estado de la licencia**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado de la licencia.

<dt>

0
</dt> <dd>

Se desconoce el estado de la licencia.

</dd> <dt>

1
</dt> <dd>

La licencia es una licencia temporal.

</dd> <dt>

2
</dt> <dd>

La licencia está activa.

</dd> <dt>

3
</dt> <dd>

La licencia es una licencia de actualización.

</dd> <dt>

4
</dt> <dd>

La licencia se ha revocado.

</dd> <dt>

5
</dt> <dd>

El estado de la licencia es pendiente.

</dd> <dt>

6
</dt> <dd>

La licencia es una licencia simultánea.

</dd> </dl>

</dd> <dt>

**sHardwareId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de hardware para el que se emitió la licencia.

</dd> <dt>

**sIssuedToComputer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo para el que se emitió la licencia.

</dd> <dt>

**sIssuedToUser**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de usuario para el que se emitió la licencia.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar esta clase, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

