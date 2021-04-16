---
description: Restablece el período de tiempo de espera u otro mecanismo que los fabricantes de TPM implementan para protegerse de los ataques de diccionario en los valores de autorización de TPM.
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: Método ResetAuthLockOut de la clase Win32_Tpm
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
ms.openlocfilehash: d28287e410fbaf65ce5b1e617113c35cfece160b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666384"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a>Método ResetAuthLockOut de la \_ clase Win32 TPM

El método **ResetAuthLockOut** de la clase [**Win32 \_ TPM**](win32-tpm.md) restablece el período de tiempo de espera u otro mecanismo que los fabricantes de TPM implementan para protegerse de los ataques de diccionario en los valores de autorización de TPM. En un ataque de diccionario, un atacante intenta adivinar un valor de autorización de TPM correcto al intentar de forma exhaustiva todos los valores posibles.

Use este método si el TPM está bloqueado debido a que hay demasiados intentos incorrectos en especificar la autorización del propietario u otros valores de autorización. Cuando el TPM está bloqueado, algunos o todos los comandos emitidos para el TPM devolverán un error, y se \_ \_ ejecutará el bloqueo de defender E defender \_ \_ (0x80280803).

> [!Note]  
> Este método solo se puede usar una vez cuando el TPM está bloqueado. Si la autorización del propietario proporcionada a este método es incorrecta, el TPM se bloqueará durante todo el período de tiempo de espera y se producirá un error en el restablecimiento del bloqueo.

 

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

Tipo: **String**

Cadena que identifica el propietario del TPM.

Esta cadena debe ser una cadena terminada en NULL con codificación Base64 que contenga exactamente 20 bytes de datos binarios. Use el método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para traducir una frase de contraseña a este formato esperado. Si no se proporciona ninguno, se lee el parámetro *OwnerAuth* en el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM. En la tabla siguiente se enumeran algunos de los valores devueltos comunes.



| Código o valor devuelto                                                                                                                                                            | Descripción                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                            | Método realizado correctamente.<br/>                                                                                                                                                                                                                                     |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl> | El valor de autorización de propietario proporcionado es incorrecto. Se producirá un error en los intentos adicionales al restablecer el bloqueo con este mismo error. Espere hasta que el período de tiempo de espera u otro mecanismo específico del fabricante haya expirado antes de reintentar los comandos de TPM bloqueados.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método llama al \_ comando ResetLockValue de TPM en el TPM. El comportamiento exacto de este método varía entre los fabricantes de TPM. La documentación del fabricante del equipo o del TPM puede proporcionar información adicional sobre la implementación del mecanismo de ataque contra el diccionario.

En general, los fabricantes pueden detectar ataques de diccionario realizando un seguimiento de las autenticaciones con errores. Si el número o la frecuencia de los errores se vuelven lo suficientemente altos, el TPM bloqueará más comandos durante un tiempo determinado. Por lo general, el período de tiempo de espera inicial será breve, para permitir que un usuario legítimo pueda corregir la situación. Si los errores continúan, la duración de cada período de tiempo de espera subsiguiente puede aumentar rápidamente.

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

 

 
