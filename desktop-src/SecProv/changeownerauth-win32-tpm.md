---
description: Cambia el valor de autorización de propietario de TPM.
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: Método ChangeOwnerAuth de la clase Win32_Tpm
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154067"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a>Método ChangeOwnerAuth de la \_ clase Win32 TPM

El método **ChangeOwnerAuth** de la clase [**Win32 \_ TPM**](win32-tpm.md) cambia el valor de autorización de propietario de TPM.

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

Tipo: **String**

Cadena que nombra el valor de autorización de propietario del TPM actual del dispositivo. Use el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una contraseña a este valor de autorización. No se proporciona el parámetro *OldOwnerAuth* o se proporciona una cadena vacía, este método obtiene el valor del registro, si está presente.

</dd> <dt>

*NewOwnerAuth* \[ en, opcional\]
</dt> <dd>

Tipo: **String**

Cadena que nombra el nuevo valor de autorización de propietario de TPM. Use el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una contraseña a este valor de autorización. El parámetro *NewOwnerAuth* no puede estar vacío ni ser **nulo.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                              | Método realizado correctamente.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>                   | El valor de autorización de propietario del TPM actual no es correcto.<br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**TPM \_ E \_ defender \_ LOCK \_ Running**</dt> <dt>2150107139 (0x80280803)</dt> </dl>      | El TPM defiende contra los ataques de diccionario y se encuentra en un período de tiempo de espera. Para obtener más información, vea el método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .<br/>                                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ \_No se \_ \_ ha \_ instalado el esquema de ad**</dt> <dt>2150694922 (0x8031000A)</dt> </dl> | No se puede guardar la información de recuperación en la red. El equipo se ha configurado para almacenar información de recuperación en Active Directory Domain Services. Para obtener instrucciones sobre cómo configurar Active Directory, consulte [Guía de configuración de cifrado de unidad BitLocker: copia de seguridad de la información de recuperación de BitLocker y TPM en Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).<br/> |
| <dl> <dt>**Error de conexión**</dt> <dt>2147943755 (0x8007054B)</dt> </dl>                  | No se puede guardar la información de recuperación en la red. El equipo se ha configurado para almacenar información de recuperación en Active Directory Domain Services. Se necesita una conexión de red para continuar.<br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

El método **ChangeOwnerAuth** realiza una copia de seguridad de la nueva autorización de propietario de TPM en Active Directory Domain Services si se ha configurado la configuración de directiva de grupo adecuada.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                      |
| Espacio de nombres<br/>                | \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ TPM. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TPM de Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
