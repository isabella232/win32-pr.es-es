---
description: Usa una contraseña numérica proporcionada para tener acceso al contenido de un volumen de datos.
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Método UnlockWithNumericalPassword de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 09676e4a57e03f86b18259a7ffb472a6682eafd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907803"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithNumericalPassword de la \_ clase EncryptableVolume de Win32

El método **UnlockWithNumericalPassword** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa una contraseña numérica proporcionada para tener acceso al contenido de un volumen de datos.

La clave de cifrado del volumen debe estar protegida con uno o varios protectores de clave del tipo "contraseña numérica" (mediante el método [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ) para poder desbloquear el volumen con este método.

> [!Note]  
> Si el disco es compatible con el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado" "

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NumericalPassword* \[ de\]
</dt> <dd>

Tipo: **String**

Cadena que especifica la contraseña numérica.

La contraseña numérica debe contener 48 dígitos. Estos dígitos se pueden dividir en 8 grupos de 6 dígitos, con el último dígito de cada grupo que indica un valor de suma de comprobación para el grupo. Cada grupo de 6 dígitos debe ser divisible entre 11 y debe ser inferior a 65536. Suponiendo que un grupo de seis dígitos se etiquete como x1, x2, x3, x4, X5 y x6, la suma de comprobación de dígito x6 se calcula como – x1 + x2 – x3 + x4 – X5 mod 11.

Los grupos de dígitos se pueden separar opcionalmente con un espacio o un guión. Por lo tanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" o "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" también pueden contener contraseñas numéricas válidas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.

Si el volumen ya está desbloqueado y no se producen otros errores, este método devuelve 0.



| Código o valor devuelto                                                                                                                                                                             | Descripción                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                             | Método realizado correctamente.<br/>                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>            | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                                                                   |
| <dl> <dt>**FVE \_ \_ \_ No \_ se encontró el protector E**</dt> <dt>2150694963 (0x80310033)</dt> </dl>     | El volumen no tiene un protector de clave del tipo "contraseña numérica".<br/> El parámetro *NumericalPassword* tiene un formato válido, pero no se puede usar una contraseña numérica para desbloquear el volumen.<br/>           |
| <dl> <dt>**FVE \_ E \_ error de \_ autenticación**</dt> <dt>2150694951 (0x80310027)</dt> </dl>    | El parámetro *NumericalPassword* no puede desbloquear el volumen.<br/> Uno o varios protectores de clave del tipo "contraseña numérica" existen, pero el parámetro *NumericalPassword* especificado no puede desbloquear el volumen.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ \_ formato de contraseña no válido**</dt> <dt>2150694965 (0x80310035)</dt> </dl> | El parámetro *NumericalPassword* no tiene un formato válido.<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]<br/>                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
