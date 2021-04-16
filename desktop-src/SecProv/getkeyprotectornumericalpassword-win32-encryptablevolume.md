---
description: Recupera la contraseña numérica de un protector de clave determinado.
ms.assetid: 5c4663fb-285d-471c-b355-82d553a7e686
title: Método GetKeyProtectorNumericalPassword de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 73a6c774386cd88195074092323969d97f4d7563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686650"
---
# <a name="getkeyprotectornumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorNumericalPassword de la \_ clase EncryptableVolume de Win32

El método **GetKeyProtectorNumericalPassword** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera la contraseña numérica de un protector de clave determinado del tipo adecuado.

El identificador de protector de clave debe hacer referencia a un protector de clave de tipo "contraseña numérica".

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetKeyProtectorNumericalPassword(
  [in]  string VolumeKeyProtectorID,
  [out] string NumericalPassword
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ de\]
</dt> <dd>

Tipo: **String**

Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*NumericalPassword* \[ enuncia\]
</dt> <dd>

Tipo: **String**

Cadena que representa la contraseña que se puede usar para desbloquear el volumen correspondiente.

La contraseña numérica tiene 48 dígitos. Estos dígitos se dividen en 8 grupos de 6 dígitos, con el último dígito de cada grupo que indica un valor de suma de comprobación para el grupo. Suponiendo que un grupo de seis dígitos se etiquete como x1, x2, x3, x4, X5 y x6, la suma de comprobación de dígito x6 se calcula como – x1 + x2 – x3 + x4 – X5 mod 11.

Los grupos de dígitos se separan con un guión. Por lo tanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" es el formato de la contraseña devuelta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                                                               |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>                                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "contraseña numérica".<br/> |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                        |



 

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

 

 
