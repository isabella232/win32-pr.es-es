---
description: Indica si el volumen se desbloquea automáticamente cuando se monta.
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: Método IsAutoUnlockEnabled de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockEnabled
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a144d54ff4564fa322efadd521e44c2fa9a8173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686643"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a>Método IsAutoUnlockEnabled de la \_ clase EncryptableVolume de Win32

El método **IsAutoUnlockEnabled** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si el volumen se desbloquea automáticamente al montarlo (por ejemplo, cuando los dispositivos de memoria extraíbles están conectados al equipo).

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsAutoUnlockEnabled* \[ enuncia\]
</dt> <dd>

Tipo: **booleano**

Valor booleano que es true si la clave externa usada para desbloquear automáticamente el volumen existe y se ha almacenado en el volumen del sistema operativo que se está ejecutando actualmente; en caso contrario, es false.

</dd> <dt>

*VolumeKeyProtectorID* \[ enuncia\]
</dt> <dd>

Tipo: **String**

Un identificador de cadena único que contiene el identificador de protector de clave de volumen cifrado asociado si *IsAutoUnlockEnabled* es true.

Si *IsAutoUnlockEnabled* es false, *VolumeKeyProtectorID* es una cadena vacía.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                     | Descripción                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                     | Método realizado correctamente.<br/>                                                       |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>    | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ no es el \_ \_ volumen de datos**</dt> <dt>2150694937 (0x80310019)</dt> </dl> | No se puede ejecutar el método para el volumen del sistema operativo que se está ejecutando actualmente.<br/>      |



 

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

 

 
