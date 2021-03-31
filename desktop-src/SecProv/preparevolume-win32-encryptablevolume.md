---
description: Crea un volumen de BitLocker con el tipo de sistema de archivos especificado del volumen de detección.
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: Método PrepareVolume de la clase Win32_EncryptableVolume
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154062"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a>Método PrepareVolume de la \_ clase EncryptableVolume de Win32

El método **PrepareVolume** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) crea un volumen de BitLocker con el tipo de sistema de archivos especificado del volumen de detección. Se debe llamar a este método antes de que se pueda proteger el volumen con cualquiera de los métodos **ProtectKeyWith \** _.

## <a name="syntax"></a>Sintaxis

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

_DiscoveryVolumeType * \[ en\]
</dt> <dd>

Tipo: **String**

Cadena que especifica el tipo de volumen de detección.

| Value               | Significado                                                            |
|---------------------|--------------------------------------------------------------------|
| **&lt;ninguna&gt;**    | No hay ningún volumen de detección. Este valor crea un volumen de BitLocker nativo. |
| **&lt;predeterminada&gt;** | Este valor es el comportamiento predeterminado.                                |
| **FAT32**           | Este valor crea un volumen de detección FAT32.                       |

</dd> <dt>

*ForceEncryptionType* \[ de\]
</dt> <dd>

Tipo: **UInt32**

Entero que especifica el tipo de cifrado. Puede ser uno de los valores siguientes.

| Value                                                                                                                                                                                                                                       | Significado                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> No <dt>**especificado**</dt> <dt>0</dt> </dl> | No se ha especificado el tipo de cifrado.<br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <dt>**Software**</dt> <dt>1</dt> </dl>             | Cifrado de software.<br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <dt>**Hardware**</dt> <dt>2</dt> </dl>             | Cifrado de hardware.<br/>                  |

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.

| Código o valor devuelto      | Descripción                     |
|------------------------|---------------------------------|
| **S_OK** <br/> 0 (0X0) | Método realizado correctamente.<br/> |

## <a name="remarks"></a>Observaciones

Si no llama a este método al habilitar un volumen de BitLocker, es lo mismo que llamar a este método con el valor predeterminado en el parámetro *DiscoveryVolumeType* .

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]<br/>                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |

## <a name="see-also"></a>Vea también

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
