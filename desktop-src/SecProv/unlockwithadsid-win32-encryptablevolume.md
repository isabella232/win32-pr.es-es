---
description: Usa la cadena Active Directory de seguridad (SID) proporcionada para obtener la clave derivada y desbloquear el volumen cifrado.
ms.assetid: 89FBC815-859D-415A-8F26-170FB2DB7387
title: Método UnlockWithAdSid de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: 14aaa82ff4b17b551ba595d2ea0c33737d651ca0236448d1d089caa82bd5f841
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891390"
---
# <a name="unlockwithadsid-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithAdSid de la clase EncryptableVolume de Win32 \_

El **método UnlockWithAdSid** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la cadena de identificador de seguridad (SID) Active Directory proporcionada para obtener la clave derivada y desbloquear el volumen cifrado.

> [!Note]  
> Si el disco admite el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado""

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 UnlockWithAdSid(
  [in]  string SidString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SidString* \[ En\]
</dt> <dd>

Cadena que contiene el Active Directory SID.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8 Enterprise, Windows 8 Pro solo aplicaciones \[ de escritorio\]<br/>                                    |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
