---
description: Usa una clave externa proporcionada para acceder al contenido de un volumen de datos.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Método UnlockWithExternalKey de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a61e85608e8ed0f3e5b014d015ce7d59c4f01c8d97ab9092864fe9bb338833ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004223"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithExternalKey de la clase EncryptableVolume de Win32 \_

El **método UnlockWithExternalKey** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa una clave externa proporcionada para acceder al contenido de un volumen de datos.

La clave de cifrado del volumen debe estar protegida con uno o varios protectores de clave del tipo "External Key" mediante el método [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para poder desbloquear el volumen con este método.

> [!Note]  
> Si el disco admite el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado""

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ExternalKey* \[ En\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matriz de bytes que especifica la clave externa de 256 bits utilizada para desbloquear el volumen. Esta clave se puede obtener llamando al [**método GetExternalKeyFromFile.**](getexternalkeyfromfile-win32-encryptablevolume.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.

Si el volumen ya está desbloqueado, este método devuelve 0.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                                                                                       |
| <dl> <dt>**ERROR \_ NO \_ ENCONTRADO**</dt> <dt>No se ha especificado ningún valor (0x)</dt> </dl>          | El volumen no tiene un protector de clave del tipo "External Key".<br/>                                                             |
| <dl> <dt>**ERROR \_ CONTRASEÑA \_ NO VÁLIDA**</dt> No se ha especificado ningún valor <dt>(0x)</dt> </dl>   | Existen uno o varios protectores de clave del tipo "External Key", pero el parámetro *ExternalKey* especificado no puede desbloquear el volumen.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | El *parámetro ExternalKey* no es una matriz de tamaño 4.<br/>                                                                           |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
