---
description: Usa una contraseña numérica proporcionada para acceder al contenido de un volumen de datos.
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Método UnlockWithNumericalPassword de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: d52cd0dd2c80bf00a55bef0fde40008f7133f28cb3be0a9aa5366076c6502b9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891299"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithNumericalPassword de la clase EncryptableVolume de Win32 \_

El **método UnlockWithNumericalPassword** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa una contraseña numérica proporcionada para acceder al contenido de un volumen de datos.

La clave de cifrado del volumen debe estar protegida con uno o varios protectores de clave del tipo "Contraseña numérica" (mediante el método [**ProtectKeyWithNumericalPassword)**](protectkeywithnumericalpassword-win32-encryptablevolume.md) para poder desbloquear el volumen con este método.

> [!Note]  
> Si el disco admite el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado""

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NumericalPassword* \[ En\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica la contraseña numérica.

La contraseña numérica debe contener 48 dígitos. Estos dígitos se pueden dividir en 8 grupos de 6 dígitos, con el último dígito de cada grupo que indica un valor de suma de comprobación para el grupo. Cada grupo de 6 dígitos debe ser divisible entre 11 y debe ser menor que 65536. Suponiendo que un grupo de seis dígitos se etiqueta como x1, x2, x3, x4, x5 y x6, el dígito x6 de la suma de comprobación se calcula como –x1+x2–x3+x4–x5 mod 11.

Opcionalmente, los grupos de dígitos se pueden separar mediante un espacio o guion. Por lo tanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" o "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" también pueden contener contraseñas numéricas válidas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.

Si el volumen ya está desbloqueado y no se produce ningún otro error, este método devuelve 0.



| Código o valor devuelto                                                                                                                                                                             | Descripción                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                             | Método realizado correctamente.<br/>                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>            | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                                                                   |
| <dl> <dt>**FVE \_ NO \_ SE \_ ENCONTRÓ \_ EL**</dt> <dt>PROTECTOR 2150694963 (0x80310033)</dt> </dl>     | El volumen no tiene un protector de clave del tipo "Contraseña numérica".<br/> El *parámetro NumericalPassword* tiene un formato válido, pero no se puede usar una contraseña numérica para desbloquear el volumen.<br/>           |
| <dl> <dt>**FVE \_ ERROR \_ DE \_ AUTENTICACIÓN**</dt> <dt>2150694951 (0x80310027)</dt> </dl>    | El *parámetro NumericalPassword* no puede desbloquear el volumen.<br/> Existen uno o varios protectores de clave del tipo "Contraseña numérica", pero el parámetro *NumericalPassword* especificado no puede desbloquear el volumen.<br/> |
| <dl> <dt>**FVE \_ E \_ FORMATO DE CONTRASEÑA \_ \_ NO**</dt> <dt>2150694965 (0x80310035)</dt> </dl> | El *parámetro NumericalPassword* no tiene un formato válido.<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
