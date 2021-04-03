---
description: Instala un propietario para el TPM.
ms.assetid: 7b4c8785-0925-41a8-a878-7c1f38d31853
title: Método TakeOwnership de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.TakeOwnership
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: acb0cb03f5e422695623bf6e183d1fd89f63ab60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083298"
---
# <a name="takeownership-method-of-the-win32_tpm-class"></a>Método TakeOwnership de la \_ clase Win32 TPM

El método **TakeOwnerShip** de la clase [**Win32 \_ TPM**](win32-tpm.md) instala un propietario para el TPM. El propietario del TPM puede sacar el máximo partido de las funcionalidades de TPM. Una vez establecido un propietario, ningún otro usuario o software puede reclamar la propiedad del TPM.

Los métodos [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md)y [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) deben ser verdaderos antes de que el método **TakeOwnerShip** pueda realizarse correctamente.

## <a name="syntax"></a>Sintaxis


```mof
uint32 TakeOwnership(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OwnerAuth* \[ en, opcional\]
</dt> <dd>

Tipo: **String**

Cadena que identifica el propietario del TPM. Esta cadena debe ser una cadena terminada en NULL con codificación Base64 que contenga exactamente 20 bytes de datos binarios. Use el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una frase de contraseña a este formato esperado. Si no se proporciona ninguno, se lee el parámetro *OwnerAuth* en el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                         | Descripción                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                         | Método realizado correctamente.<br/>                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | El parámetro *OwnerAuth* no es válido.<br/>                                                                                                                                                                 |
| <dl> <dt>**TPM \_ E \_ propietario \_ set**</dt> <dt>2150105108 (0x80280014)</dt> </dl>            | Ya existe un propietario en el TPM.<br/>                                                                                                                                                                     |
| <dl> <dt>**TPM \_ E \_ sin \_ aprobación**</dt> <dt>2150105123 (0x80280023)</dt> </dl>       | No se puede encontrar ninguna clave de aprobación en el TPM.<br/> Para crear un par de claves de aprobación en el TPM, vea el método [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .<br/>             |
| <dl> <dt>**TPM \_ E \_ instalación \_ deshabilitada**</dt> <dt>2150105099 (0x8028000B)</dt> </dl>     | No se puede instalar un propietario en este TPM.<br/> Para obtener información sobre cómo permitir la instalación de un propietario de dispositivo, vea [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).<br/> |
| <dl> <dt>**TPM \_ E \_ defender \_ LOCK \_ Running**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | El TPM defiende contra los ataques de diccionario y se encuentra en un período de tiempo de espera. Para obtener más información, vea el método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .<br/>                               |



 

## <a name="remarks"></a>Observaciones

Los métodos [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md)y [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) deben ser verdaderos antes de que **TakeOwnerShip** pueda realizarse correctamente.

Debe usar el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para cambiar una frase de contraseña en el valor de entrada que se usa para el parámetro *OwnerAuth* .

El método **TakeOwnerShip** realiza una copia de seguridad del valor de autorización de propietario en Active Directory si se ha configurado la configuración de directiva de grupo adecuada.

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

 

 
