---
description: Restablece el TPM a su estado predeterminado de fábrica.
ms.assetid: 55d6702f-bd57-43e3-b790-617940dd2e01
title: Método Clear de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Clear
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cf75a8af6764e542cecd9bd296c1b1511c4f4513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278232"
---
# <a name="clear-method-of-the-win32_tpm-class"></a>Método Clear de la \_ clase Win32 TPM

El método **Clear** de la clase [**Win32 \_ TPM**](win32-tpm.md) restablece el TPM a su estado predeterminado de fábrica. Un propietario de TPM puede utilizar este método para cancelar la propiedad de TPM e invalidar los materiales criptográficos creados por el propietario anterior. Este método suspende BitLocker si la llamada puede hacer que se requiera la recuperación de BitLocker. BitLocker se reanudará automáticamente una vez que se haya aprovisionado TPM.

> [!Caution]  
> Al borrar el TPM, se perderán todas las claves de TPM creadas y usadas por las aplicaciones. Si estas claves se usaron para cifrar datos, asegúrese de que tiene otra manera de obtener acceso a los datos antes de borrar el TPM.

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 Clear(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OwnerAuth* \[ en, opcional\]
</dt> <dd>

Tipo: **String**

Cadena que identifica el propietario del TPM. Esta cadena debe ser una cadena codificada en Base64 que contenga exactamente 20 bytes de datos binarios. Use el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una frase de contraseña a este formato esperado. Si no se proporciona ninguno, se lee el parámetro *OwnerAuth* en el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                         | Descripción                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                         | Método realizado correctamente.<br/>                                                                                                                                                |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>              | El valor de autorización de propietario proporcionado no puede realizar la solicitud.<br/>                                                                                                        |
| <dl> <dt>**TPM \_ E \_ defender \_ LOCK \_ Running**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | El TPM defiende contra los ataques de diccionario y se encuentra en un período de tiempo de espera. Para obtener más información, vea el método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .<br/> |



 

## <a name="remarks"></a>Observaciones

Ejecutar este método puede ayudar a preparar un equipo equipado con TPM para el reciclaje.

Para borrar el TPM pero ya no tiene la autorización de propietario del TPM, necesita acceso físico al equipo. El método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) incluye funcionalidad que ayuda a borrar el TPM sin la autorización de propietario de TPM.

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

 

 
