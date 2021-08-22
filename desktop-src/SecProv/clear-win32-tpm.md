---
description: Restablece el TPM a su estado predeterminado de fábrica.
ms.assetid: 55d6702f-bd57-43e3-b790-617940dd2e01
title: Método Clear de la Win32_Tpm clase
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
ms.openlocfilehash: c9c3185fceb315cf9c36caa7de1e450820ad25ce1b31fefc8135c4d57fd76597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892652"
---
# <a name="clear-method-of-the-win32_tpm-class"></a>Método Clear de la clase Tpm de \_ Win32

El **método Clear** de la clase Tpm de [**\_ Win32**](win32-tpm.md) restablece el TPM a su estado predeterminado de fábrica. Un propietario de TPM puede usar este método para cancelar la propiedad del TPM e invalidar los materiales criptográficos creados por el propietario anterior. Este método suspende BitLocker si la llamada a podría provocar que se requiera la recuperación de BitLocker. BitLocker se reanudaría automáticamente una vez que se haya aprovisionado TPM.

> [!Caution]  
> Al borrar el TPM, perderá todas las claves de TPM creadas y usadas por las aplicaciones. Si estas claves se usaron para cifrar los datos, asegúrese de que tiene otra manera de acceder a los datos antes de borrar el TPM.

 

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

Tipo: **cadena**

Cadena que identifica al propietario del TPM. Esta cadena debe ser una cadena codificada en base64 que contenga exactamente 20 bytes de datos binarios. Use el [**método ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una frase de contraseña a este formato esperado. El *parámetro OwnerAuth* se lee del Registro si no se proporciona ninguno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                         | Descripción                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                         | Método realizado correctamente.<br/>                                                                                                                                                |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>              | El valor de autorización de propietario proporcionado no puede realizar la solicitud.<br/>                                                                                                        |
| <dl> <dt>**TPM \_ E \_ DEFENDER \_ LOCK \_ RUNNING**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | El TPM se está defiendo frente a ataques de diccionario y se encuentra en un período de tiempo de espera. Para obtener más información, vea el [**método ResetAuthLockOut.**](resetauthlockout-win32-tpm.md)<br/> |



 

## <a name="remarks"></a>Comentarios

La ejecución de este método puede ayudar a preparar un equipo equipado con TPM para el reciclaje.

Para borrar el TPM, pero ya no tiene la autorización del propietario del TPM, necesita acceso físico al equipo. El [**método SetPhysicalPresenceRequest incluye**](setphysicalpresencerequest-win32-tpm.md) funcionalidad para ayudar a borrar el TPM sin autorización del propietario del TPM.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 
