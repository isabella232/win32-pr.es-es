---
description: Devuelve el nombre del archivo que contiene la clave externa.
ms.assetid: c02d8dca-f30b-4ab5-a770-1ec6ac0b81c6
title: Método GetExternalKeyFileName de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFileName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bf8de41befa7414c9970ac451d34ee7c5f40dd84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686657"
---
# <a name="getexternalkeyfilename-method-of-the-win32_encryptablevolume-class"></a>Método GetExternalKeyFileName de la \_ clase EncryptableVolume de Win32

El método **GetExternalKeyFileName** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) devuelve el nombre del archivo que contiene la clave externa, si esta clave externa se guarda en una ubicación de archivo mediante el método [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) .

Este método solo se aplica a los protectores de clave del tipo "clave externa", "TPM y PIN y clave de inicio", o "TPM y clave de inicio".

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetExternalKeyFileName(
  [in]  string VolumeKeyProtectorID,
  [out] string FileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ de\]
</dt> <dd>

Tipo: **String**

Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*Nombre de archivo* \[ enuncia\]
</dt> <dd>

Tipo: **String**

Una cadena que especifica el nombre con la extensión, pero sin la ruta de acceso del archivo, del archivo que contiene la clave externa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                                                                                                                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "clave externa", "TPM y PIN y clave de inicio", o "TPM y clave de inicio".<br/> |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                           |



 

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
</dt> <dt>

[**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md)
</dt> </dl>

 

 
