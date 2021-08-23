---
description: Desmonta el volumen y quita la clave de cifrado del volumen de la memoria del sistema.
ms.assetid: 8d6e42a0-7b43-46d2-aa5e-941567ef2842
title: Método Lock de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Lock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f5053fe027bbae51ce93feb11de5f95bde1d7b17c85a05df1386e5470b1b20fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867665"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a>Método Lock de la clase EncryptableVolume de Win32 \_

El **método Lock** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) desmonta el volumen y quita la clave de cifrado del volumen de la memoria del sistema. El contenido del volumen permanece inaccesible hasta que se desbloquea mediante el método [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o [**el método UnlockWithNumericalPassword.**](unlockwithnumericalpassword-win32-encryptablevolume.md) Este método no se puede ejecutar correctamente para el volumen de sistema operativo que se está ejecutando actualmente.

> [!Note]  
> Si el disco admite el cifrado de hardware, la banda se establece en "bloqueada".

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 Lock(
  [in, optional] boolean ForceDismount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ForceDismount* \[ en, opcional\]
</dt> <dd>

Tipo: **booleano**

Si **es true,** el disco se desmonta a la fuerza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                           | Descripción                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                           | Método realizado correctamente.<br/>                                                                                                                                     |
| <dl> <dt>**E \_ Acceso \_ denegado**</dt> <dt>2147942405 (0x80070005)</dt> </dl>               | Las aplicaciones acceden a este volumen. Si todo el acceso no es exclusivo, especificar el *parámetro ForceDismount* como true permite que el método se ejecute correctamente.<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ENCRYPTED**</dt> <dt>2150694913 (0x80310001)</dt> </dl>          | El volumen está completamente descifrado y no se puede bloquear.<br/>                                                                                                            |
| <dl> <dt>**FVE \_ E \_ PROTECTION \_ DISABLED**</dt> <dt>2150694945 (0x80310021)</dt> </dl>    | La clave de cifrado del volumen está disponible sin cifrar en el disco, lo que impide que el volumen se bloquee.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ RECOVERY KEY REQUIRED \_ \_ 2150694946**</dt> <dt>(0x80310022)</dt> </dl> | El volumen no tiene protectores de clave del tipo "Contraseña numérica" o "Clave externa" que son necesarios para desbloquear el volumen.<br/>                            |



 

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

 

 
