---
description: Permite que el propietario del TPM deshabilite o suspenda el TPM.
ms.assetid: d910334d-6da6-423d-ae8d-6e86f300dd52
title: Método Disable de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Disable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: a2bd76795cceaf299843b0b47f6f798d4471c67241f7c3fa206db52060bde745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668045"
---
# <a name="disable-method-of-the-win32_tpm-class"></a>Método Disable de la clase Tpm de \_ Win32

El **método Disable** de la clase Tpm de [**\_ Win32**](win32-tpm.md) permite que el propietario del TPM deshabilite o suspenda el TPM. Este método suspende BitLocker si la llamada a podría provocar que se requiera la recuperación de BitLocker. BitLocker se reanudaría automáticamente una vez que se haya aprovisionado TPM.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Disable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OwnerAuth* \[ in, opcional\]
</dt> <dd>

Tipo: **cadena**

Cadena que identifica al propietario del TPM. Esta cadena debe ser una cadena codificada en base64 que contenga exactamente 20 bytes de datos binarios. Use el [**método ConvertToOwnerAuth para**](converttoownerauth-win32-tpm.md) traducir una frase de contraseña a este formato esperado. El *parámetro OwnerAuth* se lee del Registro si no se proporciona ninguno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                                                         | Descripción                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                         | Método realizado correctamente.<br/>                                                                                                                                                |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>              | El valor de autorización de propietario proporcionado no puede realizar la solicitud.<br/>                                                                                                        |
| <dl> <dt>**TPM \_ E \_ DEFENDER \_ LOCK \_ RUNNING**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | El TPM está en defensa frente a ataques de diccionario y está en un período de tiempo de espera. Para obtener más información, vea el [**método ResetAuthLockOut.**](resetauthlockout-win32-tpm.md)<br/> |



 

## <a name="remarks"></a>Comentarios

Para deshabilitar el TPM sin tener el valor de autorización del propietario del TPM, use el [**método SetPhysicalPresenceRequest.**](setphysicalpresencerequest-win32-tpm.md)

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                      |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
