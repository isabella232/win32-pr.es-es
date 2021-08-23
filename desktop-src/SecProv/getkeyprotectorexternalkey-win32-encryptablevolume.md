---
description: Recupera la clave externa para un protector de clave determinado.
ms.assetid: d2b5e7d4-97c1-4d7f-a155-b5cdca2b552e
title: Método GetKeyProtectorExternalKey de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f6db531e28880c6b47cb41d87769917a524965984e2a2fc1099f0d0aa65095f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667895"
---
# <a name="getkeyprotectorexternalkey-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorExternalKey de la clase EncryptableVolume de Win32 \_

El **método GetKeyProtectorExternalKey** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera la clave externa para un protector de clave determinado del tipo adecuado.

El identificador del protector de clave debe hacer referencia a un protector de clave de tipo "Clave externa", "TPM y PIN y clave de inicio" o "TPM y clave de inicio".

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetKeyProtectorExternalKey(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ En\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*ExternalKey* \[ out\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matriz de bytes que especifica la clave externa de 256 bits que se puede usar para desbloquear el volumen correspondiente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                                                                                                                  |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>                                                                                                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | El *parámetro VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "Clave externa", "TPM y PIN y clave de inicio" o "TPM y clave de inicio".<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                           |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
