---
description: Crea un volumen de BitLocker con el tipo de sistema de archivos especificado del volumen de detección.
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: Método PrepareVolume de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PrepareVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 918e4289f8f2c38af2a4a51bfe92f82a74b30b22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173097"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a>Método PrepareVolume de la clase EncryptableVolume de Win32 \_

El **método PrepareVolume** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) crea un volumen de BitLocker con el tipo de sistema de archivos especificado del volumen de detección. Se debe llamar a este método antes de que el volumen se pueda proteger con cualquiera de los **métodos ProtectKeyWith. \***

## <a name="syntax"></a>Sintaxis

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*DiscoveryVolumeType* \[ En\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica el tipo de volumen de detección.

| Value               | Significado                                                            |
|---------------------|--------------------------------------------------------------------|
| **&lt;Ninguno&gt;**    | Sin volumen de detección. Este valor crea un volumen nativo de BitLocker. |
| **&lt;Predeterminado&gt;** | Este valor es el comportamiento predeterminado.                                |
| **FAT32**           | Este valor crea un volumen de detección FAT32.                       |

</dd> <dt>

*ForceEncryptionType* \[ En\]
</dt> <dd>

Tipo: **uint32**

Entero que especifica el tipo de cifrado. Puede ser uno de los siguientes valores.

| Value                                                                                                                                                                                                                                       | Significado                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <dt>**No especificado**</dt> <dt>0</dt> </dl> | No se especifica el tipo de cifrado.<br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <dt>**Software**</dt> <dt>1</dt> </dl>             | Cifrado de software.<br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <dt>**Hardware**</dt> <dt>2</dt> </dl>             | Cifrado de hardware.<br/>                  |

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.

| Código o valor devuelto      | Descripción                     |
|------------------------|---------------------------------|
| **S_OK** <br/> 0 (0x0) | Método realizado correctamente.<br/> |

## <a name="remarks"></a>Observaciones

Si no llama a este método al habilitar un volumen de BitLocker, es lo mismo que llamar a este método con el valor predeterminado en el parámetro *DiscoveryVolumeType.*

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise, Windows 7 aplicaciones de escritorio Ultimate \[\]<br/>                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |

## <a name="see-also"></a>Vea también

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
