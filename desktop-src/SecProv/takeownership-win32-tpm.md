---
description: Instala un propietario para el TPM.
ms.assetid: 7b4c8785-0925-41a8-a878-7c1f38d31853
title: Método TakeOwnership de la Win32_Tpm clase
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
ms.openlocfilehash: dea6fb69e79988b1a823a12ecae3e37ebd97fc0662c6a2226cd40c9230581cf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739535"
---
# <a name="takeownership-method-of-the-win32_tpm-class"></a>Método TakeOwnership de la clase Tpm \_ win32

El **método TakeOwnership** de la [**clase \_ Tpm de Win32**](win32-tpm.md) instala un propietario para el TPM. El propietario del TPM puede sacar el máximo partido de las funcionalidades de TPM. Una vez establecido un propietario, ningún otro usuario o software puede reclamar la propiedad del TPM.

Los [**métodos IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md)e [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) deben ser true para que **el método TakeOwnership** pueda realizarse correctamente.

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

Tipo: **cadena**

Cadena que identifica al propietario del TPM. Esta cadena debe ser una cadena terminada en NULL codificada en base64 que contenga exactamente 20 bytes de datos binarios. Use el [**método ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una frase de contraseña a este formato esperado. El *parámetro OwnerAuth* se lee del Registro si no se proporciona ninguno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                         | Descripción                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                         | Método realizado correctamente.<br/>                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | El *parámetro OwnerAuth* no es válido.<br/>                                                                                                                                                                 |
| <dl> <dt>**TPM \_ E \_ OWNER \_ SET 2150105108**</dt> <dt>(0x80280014)</dt> </dl>            | Ya existe un propietario en el TPM.<br/>                                                                                                                                                                     |
| <dl> <dt>**TPM \_ E \_ NO \_ ENDORSEMENT 2150105123**</dt> <dt>(0x80280023)</dt> </dl>       | No se puede encontrar ninguna clave de aprobación en el TPM.<br/> Para crear un par de claves de aprobación en el TPM, consulte el [**método CreateEndorsementKeyPair.**](createendorsementkeypair-win32-tpm.md)<br/>             |
| <dl> <dt>**TPM \_ E \_ INSTALL \_ DISABLED 2150105099**</dt> <dt>(0x8028000B)</dt> </dl>     | No se puede instalar un propietario en este TPM.<br/> Para obtener información sobre cómo permitir la instalación de un propietario de dispositivo, [**vea SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).<br/> |
| <dl> <dt>**TPM \_ E \_ DEFENDER \_ LOCK \_ RUNNING**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | El TPM se está defiendo frente a ataques de diccionario y se encuentra en un período de tiempo de espera. Para obtener más información, vea el [**método ResetAuthLockOut.**](resetauthlockout-win32-tpm.md)<br/>                               |



 

## <a name="remarks"></a>Comentarios

Los [**métodos IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md)e [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) deben ser true para **que TakeOwnership** pueda realizarse correctamente.

Debe usar el [**método ConvertToOwnerAuth para**](converttoownerauth-win32-tpm.md) cambiar una frase de contraseña por el valor de entrada usado para el *parámetro OwnerAuth.*

El **método TakeOwnership** hace una copia de seguridad del valor de autorización del propietario Active Directory si se han directiva de grupo configuración adecuada.

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

 

 
