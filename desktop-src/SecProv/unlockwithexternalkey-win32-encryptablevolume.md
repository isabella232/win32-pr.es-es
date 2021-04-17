---
description: Usa una clave externa proporcionada para tener acceso al contenido de un volumen de datos.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Método UnlockWithExternalKey de la clase Win32_EncryptableVolume
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
ms.openlocfilehash: 4b599f098856937ae5610156cba96a1deea1f64b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668470"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithExternalKey de la \_ clase EncryptableVolume de Win32

El método **UnlockWithExternalKey** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa una clave externa proporcionada para tener acceso al contenido de un volumen de datos.

La clave de cifrado del volumen debe estar protegida con uno o más protectores de clave del tipo "clave externa" mediante el método [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para poder desbloquear el volumen con este método.

> [!Note]  
> Si el disco es compatible con el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado" "

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ExternalKey* \[ de\]
</dt> <dd>

Tipo: **Uint8 \[ \]**

Matriz de bytes que especifica la clave externa de 256 bits usada para desbloquear el volumen. Esta clave se puede obtener llamando al método [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.

Si el volumen ya está desbloqueado, este método devuelve 0.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                                                                                       |
| <dl> <dt>**Error \_ de NO \_ se encontró**</dt> <dt>ningún valor dado (0x)</dt> </dl>          | El volumen no tiene un protector de clave del tipo "external key".<br/>                                                             |
| <dl> <dt>**Error \_ de \_Contraseña no válida**</dt> ; <dt>no se especificó ningún valor (0x)</dt> </dl>   | Uno o varios protectores de clave del tipo "clave externa" existen, pero el parámetro *ExternalKey* especificado no puede desbloquear el volumen.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | El parámetro *ExternalKey* no es una matriz de tamaño 4.<br/>                                                                           |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                |



 

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

 

 
