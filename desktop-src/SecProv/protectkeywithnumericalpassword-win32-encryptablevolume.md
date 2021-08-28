---
description: Protege la clave de cifrado del volumen con una contraseña de 48 dígitos con formato especial.
ms.assetid: 23e0b79a-2feb-441a-9785-7ecd3bb4b6c6
title: Método ProtectKeyWithNumericalPassword de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 17a1273b9541a0486180ca6f2cbae622f9a60b849d017711b51b416b14a44ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891491"
---
# <a name="protectkeywithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithNumericalPassword de la clase EncryptableVolume de Win32 \_

El **método ProtectKeyWithNumericalPassword** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) protege la clave de cifrado del volumen con una contraseña de 48 dígitos con formato especial. Esta contraseña numérica se puede usar para recuperarse de los errores de autenticación de otros protectores de clave (por ejemplo, TPM).

Se crea un protector de clave de tipo "Contraseña numérica" para el volumen.

Use el [**método IsNumericalPasswordValid para**](isnumericalpasswordvalid-win32-encryptablevolume.md) validar el formato de la contraseña numérica.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProtectKeyWithNumericalPassword(
  [in, optional] string FriendlyName,
  [in, optional] string NumericalPassword,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FriendlyName* \[ in, opcional\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica un identificador asignado por el usuario para este protector de clave. Si no se especifica este parámetro, se usa un valor en blanco.

</dd> <dt>

*NumericalPassword* \[ in, opcional\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica la contraseña numérica de 48 dígitos con formato especial.

La contraseña numérica debe contener 48 dígitos. Estos dígitos se pueden dividir en 8 grupos de 6 dígitos, y el último dígito de cada grupo indica un valor de suma de comprobación para el grupo. Cada grupo de 6 dígitos debe ser divisible por 11 y debe ser menor que 720896. Suponiendo que un grupo de seis dígitos se etiqueta como x1, x2, x3, x4, x5 y x6, el dígito x6 de suma de comprobación se calcula como –x1+x2–x3+x4–x5 mod 11.

Opcionalmente, los grupos de dígitos se pueden separar mediante un espacio o guion. Por lo tanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" o "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" también pueden contener contraseñas numéricas válidas.

Si no se especifica ninguna contraseña numérica, se genera una aleatoriamente. Use el [**método GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) para obtener la contraseña generada aleatoriamente.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **cadena**

Cadena que es el identificador único asociado al protector creado y que se puede usar para administrar el protector de clave.

Si la unidad admite el cifrado de hardware y BitLocker no ha tomado posesión de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos por banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | El *parámetro NumericalPassword* no tiene un formato válido.<br/> |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>                                           |
| <dl> <dt>**FVE \_ E \_ FORMATO DE CONTRASEÑA \_ \_ NO**</dt> <dt>2150694965 (0x80310035)</dt> </dl> | El *parámetro NumericalPassword* no tiene un formato válido.<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows aplicaciones de escritorio de Vista \[ Ultimate\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
