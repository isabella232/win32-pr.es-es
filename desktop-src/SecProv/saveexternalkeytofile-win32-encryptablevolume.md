---
description: Escribe la clave externa asociada al protector de clave de volumen especificado en un archivo del sistema, oculto de solo lectura, en la carpeta especificada.
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: Método SaveExternalKeyToFile de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SaveExternalKeyToFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 879536940ff36a005e1936dffcd7821fff585a65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667894"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a>Método SaveExternalKeyToFile de la \_ clase EncryptableVolume de Win32

El método **SaveExternalKeyToFile** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) escribe la clave externa asociada al protector de clave de volumen especificado en un archivo de solo lectura del sistema, oculto y de solo lectura en la carpeta especificada.

Este método solo se aplica a los protectores de clave del tipo "clave externa" o "TPM y clave de inicio".

## <a name="syntax"></a>Sintaxis


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ de\]
</dt> <dd>

Tipo: **String**

Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*Ruta de acceso* \[ de\]
</dt> <dd>

Tipo: **String**

Una cadena que contiene el volumen o la ubicación de la carpeta donde se va a guardar la clave externa asociada al protector de clave especificado. Esta ruta de acceso no incluye el nombre del archivo, que es interno y puede cambiar de una versión a una versión. Use **GetExternalKeyFileName** para obtener el nombre de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                   | Descripción                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                   | Método realizado correctamente.<br/>                                                                                                             |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl>  | El volumen está bloqueado.<br/>                                                                                                                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "clave externa" o "TPM y clave de inicio".<br/>            |
| <dl> <dt>**Error \_ de Ruta de acceso \_ no \_ encontrada**</dt> <dt>2147942403 (0x80070003)</dt> </dl> | El parámetro *path* no hace referencia a una ubicación válida.<br/> Asegúrese de que el nombre de archivo no se incluye en el parámetro *path* .<br/> |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                      |



 

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

 

 
