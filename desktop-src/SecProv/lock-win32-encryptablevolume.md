---
description: Desmonta el volumen y quita la clave de cifrado del volumen de la memoria del sistema.
ms.assetid: 8d6e42a0-7b43-46d2-aa5e-941567ef2842
title: Método lock de la clase Win32_EncryptableVolume
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
ms.openlocfilehash: 8fb6cd7b4134f4921cdaf57414843fb6522c5823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907809"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a>Método lock de la \_ clase EncryptableVolume de Win32

El método **Lock** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) desmonta el volumen y quita la clave de cifrado del volumen de la memoria del sistema. El contenido del volumen permanece inaccesible hasta que se desbloquea mediante el método [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o el método [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) . Este método no se puede ejecutar correctamente para el volumen del sistema operativo que se está ejecutando actualmente.

> [!Note]  
> Si el disco es compatible con el cifrado de hardware, la banda se establece en "bloqueada".

 

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

Si es **true** , el disco se desmontará forzosamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                           | Descripción                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                           | Método realizado correctamente.<br/>                                                                                                                                     |
| <dl> <dt>**E \_ ACCESO \_ denegado**</dt> <dt>2147942405 (0x80070005)</dt> </dl>               | Las aplicaciones tienen acceso a este volumen. Si todo el acceso no es exclusivo, si se especifica el parámetro *ForceDismount* como true, se permite que el método se ejecute correctamente.<br/> |
| <dl> <dt>**FVE \_ E \_ no \_ cifrado**</dt> <dt>2150694913 (0x80310001)</dt> </dl>          | El volumen se descifra por completo y no se puede bloquear.<br/>                                                                                                            |
| <dl> <dt>**FVE \_ \_Protección E \_ deshabilitada**</dt> <dt>2150694945 (0x80310021)</dt> </dl>    | La clave de cifrado del volumen está disponible en el disco sin cifrar, lo que impide que se bloquee el volumen.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ clave de recuperación \_ \_ necesaria**</dt> <dt>2150694946 (0x80310022)</dt> </dl> | El volumen no tiene protectores de clave del tipo "contraseña numérica" o "clave externa" que son necesarios para desbloquear el volumen.<br/>                            |



 

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

 

 
