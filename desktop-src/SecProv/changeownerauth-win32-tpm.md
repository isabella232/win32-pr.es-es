---
description: Cambia el valor de autorización del propietario del TPM.
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: Método ChangeOwnerAuth de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ChangeOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 02ca13049df20c57eeb5cc594bde1b247df0eb3829c757b64b8bd31f87e3796b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004688"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a>Método ChangeOwnerAuth de la clase Tpm de \_ Win32

El **método ChangeOwnerAuth** de la [**clase \_ Tpm de Win32**](win32-tpm.md) cambia el valor de autorización del propietario del TPM.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangeOwnerAuth(
  [in, optional] string OldOwnerAuth,
  [in, optional] string NewOwnerAuth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OldOwnerAuth* \[ en, opcional\]
</dt> <dd>

Tipo: **cadena**

Cadena que denomina el valor de autorización del propietario del TPM actual del dispositivo. Use el [**método ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una contraseña a este valor de autorización. No se proporciona el parámetro *OldOwnerAuth* o se proporciona una cadena vacía; este método obtiene el valor del Registro si está presente.

</dd> <dt>

*NewOwnerAuth* \[ en, opcional\]
</dt> <dd>

Tipo: **cadena**

Cadena que denomina el nuevo valor de autorización del propietario de TPM. Use el [**método ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una contraseña a este valor de autorización. El *parámetro NewOwnerAuth* no puede estar vacío ni **null.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                              | Método realizado correctamente.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>                   | El valor actual de autorización del propietario del TPM es incorrecto.<br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**TPM \_ E \_ DEFENDER \_ LOCK \_ RUNNING**</dt> <dt>2150107139 (0x80280803)</dt> </dl>      | El TPM se está defiendo frente a ataques de diccionario y se encuentra en un período de tiempo de espera. Para obtener más información, vea el [**método ResetAuthLockOut.**](resetauthlockout-win32-tpm.md)<br/>                                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ AD SCHEMA NOT \_ \_ \_ INSTALLED**</dt> <dt>2150694922 (0x8031000A)</dt> </dl> | No se puede guardar la información de recuperación en la red. El equipo se ha configurado para almacenar información de recuperación para Active Directory Domain Services. Para obtener instrucciones sobre cómo configurar Active Directory, consulte guía de configuración de Cifrado de unidad BitLocker: Copia de seguridad de [BitLocker](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10))y la información de recuperación de TPM Active Directory .<br/> |
| <dl> <dt>**Error de conexión**</dt> <dt>2147943755 conexión (0x8007054B)</dt> </dl>                  | No se puede guardar la información de recuperación en la red. El equipo se ha configurado para almacenar información de recuperación para Active Directory Domain Services. Se requiere una conexión de red para continuar.<br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a>Comentarios

El **método ChangeOwnerAuth hace** una copia de seguridad de la nueva autorización del propietario de TPM Active Directory Domain Services si se han directiva de grupo configuración adecuada.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                      |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> </dl>

 

 
