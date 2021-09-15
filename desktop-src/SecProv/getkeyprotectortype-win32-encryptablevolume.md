---
description: Indica el tipo de un protector de clave determinado.
ms.assetid: 17cdde18-3979-4a19-b36e-aa71994148c9
title: Método GetKeyProtectorType de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorType
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 483394f2e1c80f97442a9e6758f604093d513c3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270756"
---
# <a name="getkeyprotectortype-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorType de la clase EncryptableVolume de Win32 \_

El **método GetKeyProtectorType** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica el tipo de un protector de clave determinado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetKeyProtectorType(
  [in]  string VolumeKeyProtectorID,
  [out] uint32 KeyProtectorType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ En\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*KeyProtectorType* \[ out\]
</dt> <dd>

Tipo: **uint32**

Entero sin signo que especifica el tipo del protector de clave.



| Value                                                                         | Significado                                              |
|-------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Desconocido u otro tipo de protector<br/>           |
| <dl> <dt>1</dt> </dl>  | Módulo de plataforma segura (TPM)<br/>             |
| <dl> <dt>2</dt> </dl>  | Clave externa<br/>                              |
| <dl> <dt>3</dt> </dl>  | Contraseña numérica<br/>                        |
| <dl> <dt>4</dt> </dl>  | TPM y PIN<br/>                               |
| <dl> <dt>5</dt> </dl>  | TPM y clave de inicio<br/>                       |
| <dl> <dt>6</dt> </dl>  | TPM y PIN y clave de inicio<br/>               |
| <dl> <dt>7</dt> </dl>  | Clave pública<br/>                                |
| <dl> <dt>8</dt> </dl>  | Passphrase<br/>                                |
| <dl> <dt>9</dt> </dl>  | Certificado tpm<br/>                           |
| <dl> <dt>10</dt> </dl> | CryptoAPI Next Generation (CNG) Protector<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | El *parámetro VolumeKeyProtectorID* no hace referencia a un *keyProtectorType válido.*<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>  |



 

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
