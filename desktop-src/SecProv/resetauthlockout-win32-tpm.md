---
description: Restablece el período de tiempo de espera u otro mecanismo que los fabricantes de TPM implementan para protegerse frente a ataques de diccionario en valores de autorización de TPM.
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: Método ResetAuthLockOut de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetAuthLockOut
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 779ae7e8578019215e0bab1091512c64d68a84675d702ea7a0d8a5c37e8f081f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906305"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a>Método ResetAuthLockOut de la clase Tpm \_ win32

El **método ResetAuthLockOut** de la clase Tpm de [**Win32 \_**](win32-tpm.md) restablece el período de tiempo de espera u otro mecanismo que los fabricantes de TPM implementan para protegerse frente a ataques de diccionario en valores de autorización de TPM. En un ataque de diccionario, un atacante intenta adivinar un valor de autorización de TPM correcto intentando exhaustivamente todos los valores posibles.

Use este método si el TPM está bloqueado debido a demasiados intentos incorrectos de especificar la autorización del propietario u otros valores de autorización. Cuando el TPM está bloqueado, algunos o todos los comandos emitidos al TPM devolverán un error, TPM \_ E DEFEND LOCK RUNNING \_ \_ \_ (0x80280803).

> [!Note]  
> Este método solo se puede usar exactamente una vez cuando el TPM está bloqueado. Si la autorización de propietario proporcionada a este método es incorrecta, el TPM se bloqueará durante todo el período de tiempo de espera y se producirá un error en los intentos adicionales de restablecer el bloqueo.

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 ResetAuthLockOut(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OwnerAuth* \[ en, opcional\]
</dt> <dd>

Tipo: **cadena**

Cadena que identifica al propietario del TPM.

Esta cadena debe ser una cadena terminada en NULL codificada en base64 que contenga exactamente 20 bytes de datos binarios. Use el [**método ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una frase de contraseña a este formato esperado. El *parámetro OwnerAuth* se lee del Registro si no se proporciona ninguno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM. En la tabla siguiente se enumeran algunos de los valores devueltos comunes.



| Código o valor devuelto                                                                                                                                                            | Descripción                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                            | Método realizado correctamente.<br/>                                                                                                                                                                                                                                     |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl> | El valor de autorización de propietario proporcionado es incorrecto. Los intentos adicionales para restablecer el bloqueo producirán este mismo error. Espere hasta que el período de tiempo de espera u otro mecanismo específico del fabricante haya expirado antes de reintentar los comandos de TPM bloqueados.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método llama al comando \_ ResetLockValue de TPM en el TPM. El comportamiento exacto de este método varía entre los fabricantes de TPM. La documentación del equipo o del fabricante de TPM puede proporcionar información adicional sobre la implementación del mecanismo de ataque anti diccionario.

En general, los fabricantes pueden detectar ataques de diccionario si se realiza un seguimiento de las autenticaciones con errores. Si el número o la frecuencia de los errores son lo suficientemente altos, el TPM bloqueará más comandos durante un tiempo determinado. Por lo general, el período de tiempo de espera inicial será breve, para permitir a un usuario legítimo tener la oportunidad de corregir la situación. Si los errores continúan, la duración de cada período de tiempo de espera posterior puede aumentar rápidamente.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
