---
description: Cambia una clave externa asociada a un volumen cifrado.
ms.assetid: 14c7e643-f685-40bb-be86-aabc5b883d7e
title: Método ChangeExternalKey de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangeExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7441666ded1acc2234df84fc98ce6d02a117167d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265244"
---
# <a name="changeexternalkey-method-of-the-win32_encryptablevolume-class"></a>Método ChangeExternalKey de la clase EncryptableVolume de Win32 \_

El **método ChangeExternalKey** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) cambia una clave externa asociada a un volumen cifrado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangeExternalKey(
  [in]           string VolumeKeyProtectorID,
  [in, optional] uint8   NewExternalKey[],
  [out]          string NewVolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ En\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> <dt>

 *NewExternalKey* \[ in, opcional\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matriz de bytes que especifica la clave externa de 256 bits usada para desbloquear el volumen.

</dd> <dt>

*NewVolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena único actualizado que se usa para administrar un protector de clave de volumen cifrado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                            | Método realizado correctamente.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                    | El *parámetro NewExternalKey* no es una matriz de tamaño 32.<br/>                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>           | El volumen está bloqueado.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ BOOTABLE \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>          | En este equipo se encuentra un CD/DVD de arranque. Quite el CD/DVD y reinicie el equipo.<br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ NO \_ ENCONTRADO**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | El protector de clave proporcionado no existe en el volumen.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ TIPO DE PROTECTOR \_ \_ NO**</dt> <dt>VÁLIDO 2150694970 (0x8031003A)</dt> </dl> | El *parámetro VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "Contraseña numérica" o "Clave externa". Use el [**método ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey para**](protectkeywithexternalkey-win32-encryptablevolume.md) crear un protector de clave del tipo adecuado.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método se puede usar para cambiar la clave externa de cualquier protector de clave que use una clave externa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise, Windows 7 aplicaciones de \[ escritorio Ultimate\]<br/>                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




