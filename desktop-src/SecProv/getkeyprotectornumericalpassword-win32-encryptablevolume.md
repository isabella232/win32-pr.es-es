---
description: Recupera la contraseña numérica de un protector de clave determinado.
ms.assetid: 5c4663fb-285d-471c-b355-82d553a7e686
title: Método GetKeyProtectorNumericalPassword de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: a97740338b55238a441c2f08dedf4324144625e3bc58a684f36f0ae98886e0b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100645"
---
# <a name="getkeyprotectornumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorNumericalPassword de la clase EncryptableVolume de Win32 \_

El **método GetKeyProtectorNumericalPassword** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera la contraseña numérica de un protector de clave determinado del tipo adecuado.

El identificador del protector de clave debe hacer referencia a un protector de clave de tipo "Contraseña numérica".

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetKeyProtectorNumericalPassword(
  [in]  string VolumeKeyProtectorID,
  [out] string NumericalPassword
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ En\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*NumericalPassword* \[ out\]
</dt> <dd>

Tipo: **cadena**

Cadena que representa la contraseña que se puede usar para desbloquear el volumen correspondiente.

La contraseña numérica es de 48 dígitos. Estos dígitos se dividen en 8 grupos de 6 dígitos, y el último dígito de cada grupo indica un valor de suma de comprobación para el grupo. Suponiendo que un grupo de seis dígitos se etiqueta como x1, x2, x3, x4, x5 y x6, el dígito x6 de suma de comprobación se calcula como –x1+x2–x3+x4–x5 mod 11.

Los grupos de dígitos están separados por un guion. Por lo tanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" es el formato de la contraseña devuelta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                                                               |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>                                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | El *parámetro VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "Contraseña numérica".<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                        |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows aplicaciones de escritorio de Vista \[ Ultimate\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
