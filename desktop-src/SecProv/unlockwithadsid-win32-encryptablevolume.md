---
description: Usa la cadena de identificador de seguridad (SID) Active Directory proporcionada para obtener la clave derivada y desbloquear el volumen cifrado.
ms.assetid: 89FBC815-859D-415A-8F26-170FB2DB7387
title: Método UnlockWithAdSid de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: cbd2a327a2ede322c01009fe32aa0492a7e65610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668475"
---
# <a name="unlockwithadsid-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithAdSid de la \_ clase EncryptableVolume de Win32

El método **UnlockWithAdSid** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la cadena de identificador de seguridad (SID) Active Directory proporcionada para obtener la clave derivada y desbloquear el volumen cifrado.

> [!Note]  
> Si el disco es compatible con el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado" "

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 UnlockWithAdSid(
  [in]  string SidString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SidString* \[ de\]
</dt> <dd>

Cadena que contiene el Active Directory SID.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows 8 Enterprise, Windows 8 Pro \[ Desktop\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
