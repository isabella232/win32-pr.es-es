---
description: Establece la cadena de identificador especificada en los metadatos del volumen.
ms.assetid: 21355669-2052-4e7a-9c9d-aaa67533dd5e
title: Método SetIdentificationField de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 473b10bda95177fa2019a7439b46b475ac3bb8477ef45e19d945e8a7c1bc87a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004273"
---
# <a name="setidentificationfield-method-of-the-win32_encryptablevolume-class"></a>Método SetIdentificationField de la clase EncryptableVolume de Win32 \_

El **método SetIdentificationField** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) establece la cadena de identificador especificada en los metadatos del volumen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetIdentificationField(
  [in, optional] string IdentificationField
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IdentificationField* \[ in, opcional\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica el campo de identificación asignado al volumen. Si la cadena opcional no está presente, se usan los valores del conjunto del Registro. Si la cadena está presente y no está vacía, se usa el valor especificado. El *parámetro IdentificationField* no distingue mayúsculas de minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                                                           |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Esta unidad está bloqueada por Cifrado de unidad BitLocker. Debe desbloquear este volumen desde Panel de control. <br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise, Windows 7 aplicaciones de \[ escritorio Ultimate\]<br/>                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




