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
ms.openlocfilehash: fc4b044d58dcaca5364f0ba669b09030cf3b34dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265236"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a>Método ChangeOwnerAuth de la clase Tpm de Win32 \_

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

*OldOwnerAuth* \[ in, opcional\]
</dt> <dd>

Tipo: **cadena**

Cadena que denomina el valor de autorización del propietario del TPM actual del dispositivo. Use el [**método ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una contraseña a este valor de autorización. No se proporciona el parámetro *OldOwnerAuth* o se proporciona una cadena vacía; este método obtiene el valor del registro si está presente.

</dd> <dt>

*NewOwnerAuth* \[ in, opcional\]
</dt> <dd>

Tipo: **cadena**

Cadena que denomina el nuevo valor de autorización del propietario de TPM. Use el [**método ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una contraseña a este valor de autorización. El *parámetro NewOwnerAuth* no puede estar vacío o **null.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                              | Método realizado correctamente.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>                   | El valor actual de autorización del propietario del TPM es incorrecto.<br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**TPM \_ E \_ DEFENDER \_ LOCK \_ RUNNING**</dt> <dt>2150107139 (0x80280803)</dt> </dl>      | El TPM está en defensa frente a ataques de diccionario y está en un período de tiempo de espera. Para obtener más información, vea el [**método ResetAuthLockOut.**](resetauthlockout-win32-tpm.md)<br/>                                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ AD SCHEMA NOT \_ \_ \_ INSTALLED**</dt> <dt>2150694922 (0x8031000A)</dt> </dl> | No se puede guardar la información de recuperación en la red. El equipo se ha configurado para almacenar información de recuperación en Active Directory Domain Services. Para obtener instrucciones sobre cómo configurar Active Directory, consulte guía de configuración de Cifrado de unidad BitLocker: Copia de seguridad de [BitLocker](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10))y la información de recuperación de TPM Active Directory .<br/> |
| <dl> <dt>**Error de 2147943755**</dt> <dt>conexión (0x8007054B)</dt> </dl>                  | No se puede guardar la información de recuperación en la red. El equipo se ha configurado para almacenar información de recuperación en Active Directory Domain Services. Se requiere una conexión de red para continuar.<br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

El **método ChangeOwnerAuth hace** una copia de seguridad de la nueva autorización del propietario de TPM para Active Directory Domain Services si se han configurado los directiva de grupo adecuados.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                      |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> </dl>

 

 
