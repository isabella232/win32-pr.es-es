---
description: Protege la clave de cifrado del volumen con una contraseña de 48 dígitos con formato especial.
ms.assetid: 23e0b79a-2feb-441a-9785-7ecd3bb4b6c6
title: Método ProtectKeyWithNumericalPassword de la clase Win32_EncryptableVolume
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
ms.openlocfilehash: fd17727bc71dbbe517b6424135e1205035027a00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911570"
---
# <a name="protectkeywithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithNumericalPassword de la \_ clase EncryptableVolume de Win32

El método **ProtectKeyWithNumericalPassword** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) protege la clave de cifrado del volumen con una contraseña de 48 dígitos con formato especial. Esta contraseña numérica puede usarse para recuperarse de los errores de autenticación de otros protectores de clave (por ejemplo, TPM).

Se crea un protector de clave de tipo "contraseña numérica" para el volumen.

Use el método [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) para validar el formato de la contraseña numérica.

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

*FriendlyName* \[ en, opcional\]
</dt> <dd>

Tipo: **String**

Cadena que especifica un identificador asignado por el usuario para este protector de clave. Si no se especifica este parámetro, se utiliza un valor en blanco.

</dd> <dt>

*NumericalPassword* \[ en, opcional\]
</dt> <dd>

Tipo: **String**

Una cadena que especifica la contraseña numérica de 48 dígitos con formato especial.

La contraseña numérica debe contener 48 dígitos. Estos dígitos se pueden dividir en 8 grupos de 6 dígitos, con el último dígito de cada grupo que indica un valor de suma de comprobación para el grupo. Cada grupo de 6 dígitos debe ser divisible entre 11 y debe ser inferior a 720896. Suponiendo que un grupo de seis dígitos se etiquete como x1, x2, x3, x4, X5 y x6, la suma de comprobación de dígito x6 se calcula como – x1 + x2 – x3 + x4 – X5 mod 11.

Los grupos de dígitos se pueden separar opcionalmente con un espacio o un guión. Por lo tanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" o "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" también pueden contener contraseñas numéricas válidas.

Si no se especifica ninguna contraseña numérica, se genera una de forma aleatoria. Use el método [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) para obtener la contraseña generada de forma aleatoria.

</dd> <dt>

*VolumeKeyProtectorID* \[ enuncia\]
</dt> <dd>

Tipo: **String**

Una cadena que es el identificador único asociado al protector creado y que se puede usar para administrar el protector de clave.

Si la unidad admite el cifrado de hardware y BitLocker no ha tomado propiedad de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos de cada banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | El parámetro *NumericalPassword* no tiene un formato válido.<br/> |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>                                           |
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

 

 
